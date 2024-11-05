<template>
  <div class="puzzle-container-inner">
    <div id="forPuzzle"></div>
  </div>
</template>



<script setup>
import { onMounted } from 'vue'

const props = defineProps({
  rows: { type: Number, default: 3 },
  columns: { type: Number, default: 4 },
  imageUrl: { type: String, default: "/beach.jpg" }
})

onMounted(async () => {
  const { Puzzle, animate, setPuzzle, events, setImageUrl } = await import('./jigsaw.js')

  const puzzle = new Puzzle({ container: "forPuzzle" })
  setPuzzle(puzzle)

  setImageUrl("/beach.jpg");

  requestAnimationFrame(animate)

  // kludgy way to wait for puzzle to be loaded and ready
  setTimeout(() => {
    events.push({ event: "nbpieces", nbpieces: props.columns * props.rows });
  }, 1000);

})
</script>



<style>
.puzzle-container-inner {
  font-family: Arial, Helvetica, "Liberation Sans", FreeSans, sans-serif;
  margin: 0;
  padding: 0;
  border-width: 0;
  cursor: pointer;
}

#forPuzzle {
  position: absolute;
  width: 95vw;
  height: 95vh;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: #ffffdd;
  overflow: hidden;
}

.polypiece {
  display: block;
  overflow: hidden;
  position: absolute;
}

.moving {
  transition-property: top, left;
  transition-duration: 1s;
  transition-timing-function: linear;
}

.gameCanvas {
  display: none;
  overflow: hidden;
  position: absolute;
}
</style>