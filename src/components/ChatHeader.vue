<template>
    <div id="ChatHeader">
        <div class="row heading">
          <div class="col-sm-2 col-md-1 col-xs-3 heading-avatar">
            <div class="heading-avatar-icon">
              <img src="https://boygeniusreport.files.wordpress.com/2016/05/scared-surprised-cat-face.jpg?quality=98&strip=all&w=782">
            </div>
          </div>
          <div class="col-sm-8 col-xs-7 heading-name">
            <a class="heading-name-meta">Carbon
            </a>
            <span class="heading-online">Online</span>
          </div>
          <div class="col-sm-1 col-xs-1  heading-dot pull-right">
            <i class="fa fa-ellipsis-v fa-2x  pull-right" aria-hidden="true"></i>
          </div>
        </div>
    </div>    
</template>
<script>
export default {
    name:'ChatHeader'
    
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

.heading {
  padding: 10px 16px 10px 15px;
  margin: 0 !important;
  height: 60px;
  width: 100%;
  background-color: #eee;
  z-index: 1000;
}

.heading-avatar {
  padding: 0 !important;
  cursor: pointer;

}

.heading-avatar-icon img {
  border-radius: 50%;
  height: 40px;
  width: 40px;
}

.heading-name {
  padding: 0 !important;
  cursor: pointer;
}

.heading-name-meta {
  font-weight: 700;
  font-size: 100%;
  padding: 5px;
  padding-bottom: 0;
  text-align: left;
  text-overflow: ellipsis;
  white-space: nowrap;
  color: #000;
  display: block;
}
.heading-online {
 
  padding: 0 5px;
  font-size: 15px;
  color: #93918f;
}
.heading-compose {
  padding: 0;
}

.heading-compose i {
  text-align: center;
  padding: 5px;
  color: #93918f;
  cursor: pointer;
}

.heading-dot {
  padding: 0;
  margin-left: 10px;
}

.heading-dot i {
  text-align: right;
  padding: 5px;
  color: #93918f;
  cursor: pointer;
}


</style>


