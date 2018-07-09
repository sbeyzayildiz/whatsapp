<template>
   <div id="Right" class="col-sm-8 conversation">
       <chat-header :receiver="receiver"></chat-header>
       <chat-ball :messages="messages"></chat-ball>
   </div>
</template>
<script>
import ChatHeader from './ChatHeader'
import ChatBall from './ChatBall'
export default {
    name:'Right',
    components: {ChatHeader,ChatBall},
     
    props:[
        
        'messages',
        'receiver',
    ],
    
}
</script>
<style scoped>
div,
span {
  height: 100%;
  width: 100%;
 
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
 .conversation {
    padding: 0 !important;
    margin: 0 !important;
    height: 100%;
    /*width: 100%;*/
    border-left: 1px solid rgba(0, 0, 0, .08);
    /*overflow-y: auto;*/
  }

</style>