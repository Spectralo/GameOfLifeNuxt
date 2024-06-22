<template>
  <div>
    <Header />
  </div>
  <div class="container">
    <div class="panel controls">
      <Button @click="play()"><Icon name="mdi:play" color="var(--fg)" size="50px"/></Button>
      <Button @click="pause()"><Icon name="mdi:pause" color="var(--fg)" size="50px"/></Button>
      <Button @click="reset()"><Icon name="ic:baseline-settings-backup-restore" color="var(--fg)" size="50px"/></Button>
    </div>
    <div class="panel game">
      <h1>Generation: 0</h1>
    </div>
  </div>
</template>

<script lang="ts" setup>
import '~/assets/css/colors.css'
import '~/assets/css/reset.css'


</script>

<style>
body {
  background-color: var(--bg3);
  font-family: Rubik;
}
.panel {
  background-color: var(--blue-dim);
  border-radius: 10px;
  margin-left: 10px;
  margin-right: 10px;
}
.controls {
  width: fit-content;
  display: flex;
  flex-direction: column;
  height: 100%;
  justify-content: center;
}
.game {
  width: 100%;
}
.container {
  margin-top: 50px;
  margin-left: 50px;
  margin-right: 50px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}


</style>