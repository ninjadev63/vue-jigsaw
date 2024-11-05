<template>
        <div class="page-container">
          <div class="puzzle-container">    
            <JigsawPuzzle :rows="3" :columns="4" imageUrl="/beach.jpg" />
          </div>
        </div>
</template>

<script setup lang="ts">
</script>

<style>
.page-container {
    width: 100%;
    height: 100%;
    margin: 0;
    padding: 0;
    overflow: auto;
    /* background-color: #f0f0f0; */
    display: flex;
    justify-content: center;
    align-items: center;
}

.puzzle-container {
    width: 100vw;
    height: 100vh;
}
</style>




