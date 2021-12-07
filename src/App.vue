<template>
  <div id="app">
    <page-body></page-body>

    <div class="song_grid">
    <song-list v-for="song in songs"
    :key="song['id']"
    :title="song['title']"
    :artist="song['artist']"
    >
    </song-list>
  
    </div>

    <play-list></play-list>
  </div>
</template>

<script>
import PageBody from './components/PageBody.vue'
import SongList from './components/SongList.vue'
import PlayList from './components/PlayList.vue'

export default {
  name: 'App',
  components: {
    PageBody,
    SongList,
    PlayList,
  },

data() {
  return {
    songs: [
      {
      id: 1,
      title: "My Way",
      artist: "Cassette",
      },
      {
      id: 2,
      title: "Love",
      artist: "Lena",
      },
      {
      id: 3,
      title: "In Your Eyes",
      artist: "The Weeknd",
      },
      {
      id: 4,
      title: "Save Your Tears",
      artist: "The Weeknd",
      },
      {
      id: 5,
      title: "The Business",
      artist: "Tiesto",
      },
      {
      id: 6,
      title: "Out of Time",
      artist: "Why So Sad",
      },
      {
      id: 7,
      title: "So Long",
      artist: "MALFA",
      },
    ],
  };
},
};
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.song_grid {
  display: grid;
  margin-left: 15%;
  
}
</style>