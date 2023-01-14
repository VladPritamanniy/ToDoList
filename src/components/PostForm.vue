<template>
    <form @submit.prevent>
        <h4>Создание задачи</h4>
        <MyInput
            v-model:value="post.body"
            type="text" 
            placeholder="Название"
        />
        <MyInput
            v-model:value="post.title"
            type="text" 
            placeholder="Описание"
        />
        <MyButton
            style = "align-self: flex-end; margin-top: 15px"
            @click="createPost"
        >
        Создать
        </MyButton>
    </form>
</template>

<script>
export default{
    data() {
        return {
            post: {
                title: "",
                body: ""
            }
        };
    },
    methods: {
        createPost() {
            this.post.id = Date.now();
            this.$emit("create", this.post);
            this.post = {
                title: "",
                body: ""
            };
        }
    },
}
</script>

<style>
form{
    display: flex;
    flex-direction: column;
}
</style>