<template>
  <div id="app">
    <!--audio controls preload="auto" autoplay>
      <source id="audio" ref='audio' src="" type="audio/mpeg">
    </audio> -->
    <!--playList />
    <h1>我是個音樂播放器</h1>
    <audio src="" id="audio"  ></audio>
    
    <button v-for="(item , btn) in btns" :key="btn" @click="btnInput(item)">{{item}}</button>
    <p>上傳你的音樂</p>
    <input id="upload" type="file" accept="audio/*" @change="musicPath" multiple /></br>
    <button type="button" @click="musicPath2">按我改變src</button-->
    <player />
  </div>
</template>

<script>
import playList from './components/playList.vue'
import player from './components/player.vue'

export default {
  name: 'App',
  components:{
    playList,
    player
  },
  data(){
    return{
      btns:['play' , 'stop' ],

    
    };
    
    
  },

  /*methods:{
     musicPath(){
      let audioPlayer = document.getElementById('audio');
      let audioFile = document.getElementById('upload').files[0];
      audioPlayer.src = URL.createObjectURL(audioFile);
      
      
      console.log('playing');
      
      
      //audioFile.src = "/static/audios/RRRepeat!!!(320kbps-48kHz).mp3";


      
      
    },

    btnInput(label){
      let audioPlayer = document.getElementById('audio');
      if(label === "play"){
        audioPlayer.play();
      }else if(label === "stop"){
        audioPlayer.pause();
      }

    },

    musicPath2(){

      let audioFile = document.getElementById('audio');
      audioFile.src = "http://www.noiseaddicts.com/samples_1w72b820/3720.mp3";

      //this.$refs.audio.src = "/static/audios/RRRepeat!!!(320kbps-48kHz).mp3"

    }

    

    
  },*/
  
  
  



        
    

}
</script>



    

<style>
body{
  margin:0px;
  padding:0px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
