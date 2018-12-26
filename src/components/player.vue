<template>
    <div id="player">
         <audio id="audio" ref="audio" controls></audio>
         <div id="upload" @dragover.prevent="allowdrop" @drop.prevent="getMusicFile">
         </div>
        <h1>test</h1>
    </div>
</template>

<script>

export default {
    name: 'player',

    data(){
        
        return{
             music:[],
        }
    },
    
    watch:{
        music: function(music) { 
                this.$refs.audio.src = URL.createObjectURL(music);
                this.$refs.audio.src = URL.createObjectURL(music[0]);
                this.$refs.audio.play();
                console.log("put");
                return
            
        },
    },
   

    methods:{

        getMusicFile(e){    
            const audioFiles = e.dataTransfer.files; 
            //this.music = e.dataTransfer.files;
            //const data = e.originalEvent=.dataTransfer; 
            //const music = audioFiles.files[0];
            //const audioPlayer = document.getElementById('audio');
            //const music = e.dataTransfer.files[0];
            //audioFile = music.file[0];
            let audioPlayer = document.getElementById('audio');
            audioPlayer.src = URL.createObjectURL(audioFiles);
           // this.$refs.audio.src = URL.createObjectURL(music);
            //let audioFile = document.getElementById('upload').file[0];
            //let audioFile = document.getElementById('upload').getAsFiles();
            //let audioFile = e.target.files || e.dataTransfer.files;
            //let audioFile = e.dataTransfer.file[0];
            //audioPlayer.src = URL.createObjectURL(audioFile);
            
           // console.log(music);
            

             /*for (let i = 0; i < audioFiles.length; i++) {
                let file = audioFiles[i];
                
        
            }
            console.log(file);*/
            
      
      
            //audioFile.src = "/static/audios/RRRepeat!!!(320kbps-48kHz).mp3";

            
        },

        
        

        allowdrop(e){
        },


    },
}   
</script>



<style>
    #upload{
        background:#ffff;
        width:100vw;
        height:100vh;
    }
</style>


