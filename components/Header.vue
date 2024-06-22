<template>
  <div class="blue-dim header">
    <h1 class="title">The Game Of Life</h1>
    <h1 class="title version">v0.1</h1>
  </div>
</template>

<script lang="ts" setup>

</script>

<style>
.header {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: end;
  background-color: var(--bg);
  padding: 20px;
}
h1.title {
  color: var(--fg);
}
.version {
  align-self: flex-end;
}
</style>