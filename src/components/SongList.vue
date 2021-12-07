<template>

    <div class="song_card">
        <p>{{ id }}</p>
        <h3 ref="song-title">{{ title }}</h3>
        <h5>{{ artist }}</h5>
        <div class="select_song">
        <button @click="push_song">>></button></div>
    </div>
    

</template>

<script>
    export default {
        name: "song-list",
        mounted() {
        document.body.style.background = "black";
  },
  methods: {
      push_song() {
          var song_title = this.$refs['song-title'].value;
          this.$emit('song_pushed', song_title);
      }
  },
  props: {
      id: String,
      title: String,
      artist: String,
  },

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
.select_song {
    margin-left: 250px;
    width: 50px;
}
button {
    width: 40px;
    height: 20px;
}
</style>