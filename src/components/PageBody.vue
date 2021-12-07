<template>
    <div>
<h1>Welcome to My Playlist!</h1>
<div class="lists">
<h2>Song Collection</h2>
<h2>My Playlist</h2>
</div>
    </div>
</template>

<script>

    export default {
        name: "page-body"
    }
</script>

<style scoped>
.lists {
    display: grid;
    grid-auto-flow: column;
    place-items: center;
}
div {
    margin-bottom: 30px;
}
h1, h2 {
    color: whitesmoke;
}
</style>