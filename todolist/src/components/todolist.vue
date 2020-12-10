<template>
    <ul>
        <li v-for="(todo, index) in todos" v-on:click="deleteTodo(index)" v-bind:key="index">{{ todo }}</li>
    </ul>
</template>

<script>
export default {
    props: ['todos'],
    methods: {
        deleteTodo(index){
            this.$emit('delete-todo', index);
        }
    }
}
</script>

<style>
    li {
        background-color: rgb(255, 92, 92);
        color: white;
        text-align: center;
        margin: 5px;
        padding: 20px;
        font-size: 25px;
        flex-flow: 'roboto';
        border: black solid 1px;
        border-radius: 12px;
        list-style-type: none;
        cursor: pointer;
    }
    ul {
        margin-left: -40px;
        /* padding-top: 20px; */
    }
</style>