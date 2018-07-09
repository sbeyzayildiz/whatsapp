<template>
<div id="Message">
  <!--koşul-->
  <div v-if="receiver">
            <div class="col-sm-12 message-main-receiver">
              <div class="receiver">
                <div class="message-text">
                 Mesaj içeriği
                </div>
                <span class="message-time pull-right">
                  <!--{{time}}-->15.08
                </span>
              </div>
            </div> 
  </div>
  <div v-if="!receiver">
             <div class="col-sm-12 message-main-sender">
              <div class="sender">
                <div class="message-text">
                  Thanks n I know its awesome...!
                </div>
                <span class="message-time pull-right">
                  Sun
                </span>
              </div>
            </div> 
  </div>
</div>

    
</template>
<script>
import leftPad from 'left-pad';
import Keyboard from './Keyboard';

export default {
    name:'Message',
    props: [
      'message',
     
    ],
    methods: {
      time() {
                const time = new Date(this.message.timestamp);
                 return `${time.getHours()}:${leftPad(time.getMinutes(), 2, '0')}`;
      },
      
    },
    data() {
     receiver:true
    }
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
.row
{
   padding: 0 !important;
    margin: 0 !important;
}
.message-body {
  margin: 0 !important;
  padding: 0 !important;
  width: auto;
  height: auto;
}

.message-main-receiver {
  /*padding: 10px 20px;*/
  max-width: 60%;
}

.receiver {
  width: auto !important;
  padding: 4px 10px 7px !important;
  border-radius: 10px 10px 10px 0;
  background: #ffffff;
  font-size: 12px;
  text-shadow: 0 1px 1px rgba(0, 0, 0, .2);
  word-wrap: break-word;
  display: inline-block;
}

.message-text {
  margin: 0 !important;
  padding: 5px !important;
  word-wrap:break-word;
  font-weight: 200;
  font-size: 14px;
  padding-bottom: 0 !important;
}
.message span {
    font-weight: bold;
  }

.message small {
    font-size: 10px;
    color: #999;
    font-weight: normal;
 }
 .message-time {
  margin: 0 !important;
  margin-left: 50px !important;
  font-size: 12px;
  text-align: right;
  color: #9a9a9a;

}
 li
 {
   list-style-type: none;
 }
 .message-main-sender {
  padding: 3px 20px !important;
  margin-left: 40% !important;
  max-width: 60%;
}
.sender {
  float: right;
  width: auto !important;
  background: #dcf8c6;
  border-radius: 10px 10px 0 10px;
  padding: 4px 10px 7px !important;
  font-size: 12px;
  text-shadow: 0 1px 1px rgba(0, 0, 0, .2);
  display: inline-block;
  word-wrap: break-word;
}

</style>
