<template>
    <div v-if="posts.length>0">
        <h3>Задачи</h3>
        <PostItem 
        v-for="post in posts"
        :post="post"
        :key="post.id"
        @remove="$emit('remove',post)"
        />
    </div>
    <h2 v-else style="color: green">
        Список пуст
    </h2>

</template>

<script>
import PostItem from './PostItem.vue';

export default{
    props: {
        posts: {
            type: Array,
            required: true
        }
    },
    components: { PostItem }
}
</script>

<style scoped>

</style>