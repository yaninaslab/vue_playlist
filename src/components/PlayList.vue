<template>
  <div class="song_card">
    <p>{{ id }}</p>
    <h3 ref="song-title">{{ title }}</h3>
    <h5>{{ artist }}</h5>
  </div>
</template>

<script>
export default {
  name: "play-list",
  mounted() {
    this.$root.$on('song_pushed', this.react_to_song_pushed);
    //document.body.style.background = "black";
  },
  methods: {
    react_to_song_pushed(song_title) {
      console.log(song_title);
    },
  },
};
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