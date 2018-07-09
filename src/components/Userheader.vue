<template>
<div id="Userheader">
        <div class="row heading">
            <div class="col-md-3 col-sm-3 col-xs-3 heading-avatar">
              <div class="heading-avatar-icon" > 
                <img src="https://boygeniusreport.files.wordpress.com/2016/05/scared-surprised-cat-face.jpg?quality=98&strip=all&w=782">
              </div>
            </div>
            <div class="col-md-1 col-sm-1 col-xs-1  heading-dot  pull-right">
              <i class="fa fa-ellipsis-v fa-2x  pull-right" aria-hidden="true"></i>
            </div>
            <div class="col-md-2 col-sm-2 col-xs-2 heading-compose  pull-right">
              <i class="fa fa-comments fa-2x  pull-right" aria-hidden="true"></i>
            </div>
          </div>
</div>  
</template>
<script>
export default
{
    name:'userheader',
    userfirstname:'Scarlett',
    userlastname:'Slimm',
   
  created: function() {
  fetch('https://jsonplaceholder.typicode.com/users')
  .then(response => response.json())
  .then(json => console.log(json))
    
    
  }
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
  display: none;
  padding: 0 5px;
  font-size: 12px;
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

