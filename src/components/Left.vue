<!--- UserHeader-->
<!--- FriendList-->
<template>
<div id="Left" class="col-sm-4 side-one">
    <userheader></userheader>
    <friend-list></friend-list>
</div>
</template>
<script>
import Userheader from './Userheader'
import FriendList from './FriendList'
export default {
    name:'Left',
    components:{Userheader,FriendList}
    
}
</script>
<style scoped>


div,
span {
  height: 100%;
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
.side-one {
  padding: 0;
  margin: 0;
  height: 100%;
  width: 100%;
  z-index: 1;
  position: relative;
  display: block;
  top: 0;
}



</style>


