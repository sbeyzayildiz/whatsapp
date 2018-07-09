<template>
    <div id="ChatBall">
        <div class="row message">            
            <MessageList :messages="messages"/> 
            </div>
            <keyboard :onSend="onSend"/>
          </div>           
</template>
<script>
import MessageList from './MessageList'
import Keyboard from './Keyboard'

export default {
    name:'ChatBall',
    props: ['messages','onSend',],
    components:{MessageList,Keyboard}
     
    
}
</script>
<style scoped>
@media screen and (max-width: 700px)
{
div,
span {
  height: 100%;
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.row
{
  
    padding: 0 !important;
    margin: 0 !important;

}


.message {
  padding: 0 !important;
  margin: 0 !important;
  background-size: cover;
  overflow-y: auto;
  border: 1px solid #f7f7f7;
  height: calc(100% - 140px);
}

}

</style>
