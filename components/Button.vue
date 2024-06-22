<template>
  <div class="Button">
    <slot></slot>
  </div>
</template>

<script lang="ts" setup>

</script>

<style>
.Button {
  background-color: var(--blue);
  color: var(--fg);
  border: none;
  border-radius: 10px;
  padding: 10px;

  margin: 5px;
  cursor: pointer;
  display: flex;
  justify-content: center;
}
</style>