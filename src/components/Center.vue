
<template>
    <div id="Center">
      <div class="row app-one">
        <left
        :receivers="receivers"
        />
        <right
         :messages="messages"
         :receiver="receiver"
         :sender="sender"
         :onSend="onSend"/>
      </div>
    </div>
</template>
<script>
import Left from './Left'
import Right from './Right'
export default {
    name:'Center',
    components:{Left,Right},
    props: ['whatsApp'],
    methods:
    {
       
    },
  
   
    data() {
    return {
      messages: [],
      receivers: {},
      receiver: null,
      sender:null,
    };

    }    
}
</script>
<style scoped>
html,
body,
div,
span {
  height: 100%;
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  background: no-repeat fixed center;
  background-size: cover;
}
.app-one {
  background-color: #f7f7f7;
  height: 100%;
  overflow: hidden;
  margin: 0 !important;
  padding: 0 !important;
  box-shadow: 0 1px 1px 0 rgba(0, 0, 0, .06), 0 2px 5px 0 rgba(0, 0, 0, .2);
}
.sideBar-main .row {
  padding: 0 !important;
  margin: 0 !important;
}
</style>

