<script setup>
import { defineEmits, ref, reactive } from 'vue';

const emit = defineEmits(["createTodo"]);

const todo = ref('testing');

const todoState = reactive({
    todo: "",
});

const createTodo = () => {
    emit("createTodo", todo.value);
};

</script>

<template>
    <div class="input-wrap">
        <input type="text" v-model="todoState.todo" />
        <button @click="createTodo()">Create</button>
    </div>
    <p>{{ todoState.todo }}</p>
</template>

<style lang="scss" scoped>
.input-wrap {
    display: flex;
    transition: 250ms ease;
    border: 2px solid #41b080;

    &:focus-within {
        box-shadow: 0 -4px 6px -1px rgb(0 0 0 / 0.1),
            0 -2px 4px -2px rgb(0 0 0 / 0.1);
    }

    input {
        width: 100%;
        padding: 8px 6px;
        border: none;
        &:focus {
            outline: none;
        }
    }

    button {
        padding: 8px 16px;
        border: none;
    }
}
</style>