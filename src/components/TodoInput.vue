<template>
    <div>
        <input type="text" v-model="newTodoItem">
        <p @click="addTodo"><i class="fas fa-plus"></i></p>
        <button @click="addTodo">Add</button>
    </div>    
</template>

<script>
export default {
    data() {
        return {
            newTodoItem: ''
        }
    },
    methods: {
        addTodo() {
            if(this.newTodoItem !== "") {
                var value = this.newTodoItem.trim();
                localStorage.setItem(value, value);
                this.clearInput();
            }
        },
        clearInput() {
            this.newTodoItem = '';
        }
    }
}
</script>

<style>

</style>
