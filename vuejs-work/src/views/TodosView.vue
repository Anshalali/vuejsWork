<script setup></script>

<template>
  <main>
    <h1>Create Todo</h1>
    <TodoCreator />
  </main>
</template>

<style lang="scss" scoped>
main {
  display: flex;
  flex-direction: column;
  max-width: 500px;
  width: 100%;
  margin: 0 auto;
  padding: 40px 16px;
  border: 1px solid red;
  h1 {
    margin-bottom: 16px;
    text-align: center;
    border: 1px dotted green;
  }
}
</style>
