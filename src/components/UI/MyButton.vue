<template>
    <button class="btn">
        <slot></slot>
    </button>
</template>

<script>
export default{
    name: 'MyButton'
}
</script>

<style scoped>
.btn{
    padding: 10px 15px;
    background: none;
    color: teal;
    border: 1px solid teal;
}
.btn:hover{
    background-color:rgb(182, 227, 196) ;
}
</style>