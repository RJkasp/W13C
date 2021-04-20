<template>
  <div>
      <!-- event listner -->
    <song-list @whenClicked="pushSongListener"></song-list>
    <!-- loop listens for when button is clicked and stores the data inside a h3tag and p tag -->
    <article v-for="song in playList" :key="song">
    <h3>{{ song.title }}</h3>
    <p>{{ song.artist }}</p>
    </article>
  </div>
</template>

<script>
//injecting songlist into playlist
import SongList from "./SongList.vue"
export default {
  name: "play-list",
  components:{
    SongList,
  },
  data(){
      return{
          playList:[

          ]
      }
  },
  //function function to push data into event listener above in template
     methods:{
        pushSongListener: function(data){
            this.playList.push(data);
        }
    }, 
 
};
</script>

<style scoped>
</style>