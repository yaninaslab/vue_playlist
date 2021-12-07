<template>
    
<div class="song_card">
        <p>{{ id }}</p>
        <h3>{{ title }}</h3>
        <h5>{{ artist }}</h5>
    </div>
</template>

<script>
    export default {
        name: "play-list"
    }
</script>

<style scoped>
.song_card {
    display: grid;
    width: 300px;
    height: 200px;
    margin: 10px;
    border-radius: 5px;
    box-shadow: 3px 3px 6px gray;
    background-color: whitesmoke;
}
</style>