<template>
<div id="Keyboard">
   <div class="row reply">
          <div class="col-sm-1 col-xs-1 reply-emojis">
          <i class="fa fa-smile-o fa-2x"></i>
          </div>
          <div class="col-sm-10 col-xs-10 reply-main">
            <input class="form-control" rows="1" id="message"
                          placeholder="Bir mesaj girin"
                          v-model="message"
                           @keydown.enter="onKeyDown"
           />
          </div>
          <div class="col-sm-1 col-xs-1 reply-recording">
            <i class="fa fa-microphone fa-2x" aria-hidden="true"></i>
          </div>
        </div>
        
</div>
</template>
<script>
export default {
    name: 'KeyBoard',   
    methods: {
      onKeyDown() {
        if (this.message) {
          this.onSend(this.message);
          this.message = '';
           
        }
      },
      onSend(text)
      {
        this.message=text;
        this.messageId=Math.floor((Math.random()*10000));
        console.log(this.message);
        console.log(this.messageId);
        this.messages.push({"id":this.messageId,"message":this.message});
        console.log(this.messages);
      }
    },
    data() {
      return {
        message: '',
        messageId:0,
        messages:[],
        
      };
    },
  };
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
.row
{
  
    padding: 0 !important;
    margin: 0 !important;

}

.reply {
    height: 70px;
  }
  .reply-emojis {
    padding: 5px 0 !important;
  }
  .reply-emojis i {
    padding: 5px 2px !important;
    font-size: 1.8em !important;
  }
  .reply-main {
    padding: 2px 8px !important;
  }
  .reply-main input {
    padding: 8px !important;
    font-size: 18px;
  }
  .reply-recording {
    padding: 5px 0 !important;
  }
  .reply-recording i {
    padding: 5px 0 !important;
    font-size: 1.8em !important;
    z-index: 2px;
  }
  .reply-send {
    padding: 5px 0 !important;
  }
  .reply-send i {
    padding: 5px 2px 5px 0 !important;
    font-size: 1.8em !important;
    z-index: 2px;
  }

</style>
