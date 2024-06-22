<template>
  <div>
    <Header />
  </div>
  <div class="container">
    <div class="rightpanel">
    <div class="panel controls">
      <Button @click="play()"><Icon name="mdi:play" color="var(--fg)" size="50px"/></Button>
      <Button @click="pause()"><Icon name="mdi:pause" color="var(--fg)" size="50px"/></Button>
      <Button @click="reset()"><Icon name="ic:baseline-settings-backup-restore" color="var(--fg)" size="50px"/></Button>
    </div>
    <div class="panel controls">
      <Button @click="play()"><Icon name="ic:baseline-edit" color="var(--fg)" size="50px"/></Button>
      <Button @click="pause()"><Icon name="mingcute:random-fill" color="var(--fg)" size="50px"/></Button>
    </div>
    </div>
    <div class="panel game">
      <canvas ref="canvas" class="gridCanvas" width="100%" height="100%"/>
    </div>
  </div>
</template>

<script lang="js">
import '~/assets/css/colors.css'
import '~/assets/css/reset.css'

let canvas = this.$refs.canvas as HTMLCanvasElement
const ctx = canvas.getContext("2d");

function draw() {
        const canvas = document.getElementById("canvas");
        if (canvas.getContext) {
          const ctx = canvas.getContext("2d");

          ctx.fillStyle = "rgb(200 0 0)";
          ctx.fillRect(10, 10, 50, 50);

          ctx.fillStyle = "rgb(0 0 200 / 50%)";
          ctx.fillRect(30, 30, 50, 50);
        }
}

draw()

function play() {
  console.log("Play")
}
function pause() {
  console.log("Pause")
}
function reset() {
  console.log("Reset")
}

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
  height: fit-content;
  justify-content: center;
  margin-bottom: 30px;
}
.game {
  width: 100%;
}
.container {
  margin-top: 50px;
  margin-left: 70px;
  margin-right: 70px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.gridCanvas {
  position: relative !important;
  border-radius: 5px;
  box-shadow: 0 2px 3px rgba(0, 0, 0, 0.2);
  width: 100%;
  aspect-ratio: 1/1;
}
.rightpanel {
  display: flex;
  flex-direction: column;
  justify-content: start;
}

</style>