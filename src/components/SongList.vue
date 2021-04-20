<template>
  <div id="songs">
      <!-- Loop -->
    <article @whenClicked="pushSong" v-for="song in SongList" :key="song.id">
      <h3>{{ song.title }}</h3>
      <p>{{ song.artist }}</p>
      <!-- //eventListener -->
      <button @click="pushSong(song.title, song.artist)">
        Add To Playlist
      </button>
    </article>
  </div>
</template>

<script>

export default {
  name: "song-list",
  data() {
    return {
      SongList: [
        {
          id: 1,
          title: "Mount Everest",
          artist: "Labrinth",
        },
        { id: 2, title: "Mount Everest 2", artist: "Labrinth" },
        { id: 3, title: "Mount Everest 3", artist: "Labrinth" },
        { id: 4, title: "Mount Everest 4", artist: "Labrinth" },
        { id: 5, title: "Mount Everest 5", artist: "Labrinth" },
      ],
    }
  },
  //function that choses song when clicked and sends title and artist.
   methods: {
    pushSong: function (title, artist) {
      this.$emit("whenClicked", {
        title: title,
        artist: artist,
      });
    }
  }
}
</script>

<style scoped>
</style>