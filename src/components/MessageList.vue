<template>
   <ul class="messages">
       <div class="row message-body">
        <Message /> 
       </div>
  </ul>
</template>
<script>
import Message from './Message';

export default {
    name:'MessageList',
    props:['messages'],
    components:
    {
        Message,
    },
}
</script>
<style scoped>
ul{
    padding: 10px;
}
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

</style>
