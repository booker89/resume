<template>
  <div id="wrap_info">
    <h1>About me</h1>
    <div class="title_boder"></div>
    <div class="wrap">
      <div class="info_wrap">
        <h5>Profile</h5>
        <div class="info_content" v-for="info in info_profile">
          <div class="img" :style="imgStyle(info.img)"/>
          <div>{{info.name}}</div>
        </div>
      </div>
      <div class="info_wrap">
        <h5>Contact</h5>
        <div class="info_content" v-for="info in info_contact">
          <div class="img" :style="imgStyle(info.img)"/>
          <div>{{info.name}}</div>
        </div>
      </div>
      <div class="info_wrap">
        <h5>Interest</h5>
        <div class="info_content" v-for="info in info_interest">
          <div class="img_wrap">
            <div class="img" :style="imgStyle(info.img)"/>
          </div>
          <div>{{info.name}}</div>
        </div>
      </div>
      <div class="info_wrap">
        <h5>Link</h5>
        <div class="info_content" v-for="info in info_link">
          <div class="img" :style="imgStyle(info.img)"/>
          <a :href="info.link"  target="_blank">{{info.name}}</a>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
#wrap_info .wrap{
  margin-top: 70px;
  display: flex;
  justify-content: space-between;
}
.info_wrap{
  width: 50%;
  padding-left: 10px;
}
#wrap_info h5{
  margin-bottom: 30px;
  padding-left: 20px;
  border-left: 5px solid #BBC1BD;
  color: #7B7D7C
}
#wrap_info a{
  text-decoration: none;
  color: #000;
  position: relative;
}
#wrap_info a:hover{
  text-decoration: none;
  color: #7B7D7C
}
#wrap_info a:after{
  content: '';
  position: absolute;
  border-bottom: 2px solid #7B7D7C;
  bottom: 0px;
  left: 50%;
  right: 50%;
  transition: .3s;
}
  
#wrap_info a:hover:after{
  left: 0%;
  right: 0%;
}
.info_wrap > .info_content{
  display: flex;
  color: #000;
  margin-bottom: 20px;
}

.info_wrap .img{
  display: inline-block;
  width: 30px;
  height: 30px;
  background: center center;
  background-size: 75%;
  background-repeat: no-repeat;
  margin-right: 20px;
  transition: .3s;
}
.info_wrap .img:hover{
  transform: scale(1.4)
}

@media screen and (max-width: 767px){
  #wrap_info .wrap{
    flex-wrap: wrap
  }
  .info_wrap{
    width: 100%;
    padding-bottom: 30px
  }
  .info_content{
    padding-left: 25px
  }
}

</style>


<script>
import Infos from '@/Infos';
export default {
  computed:{

    info_profile: function() {
      return Infos.filter(function(item) {
        return item.count <= 4;
      });
    },
    info_contact: function() {
      return Infos.filter(function(item) {
        return item.count <= 6 && item.count > 4;
      });
    },
    info_interest: function() {
      return Infos.filter(function(item) {
        return item.count <= 8 && item.count > 6;
      });
    },
    info_link: function() {
      return Infos.filter(function(item) {
        return item.count <= 11 && item.count > 8;
      });
    },
  },
  methods:{
    imgStyle(img){
      return {
        backgroundImage: `url('${img}')`,
      };
    },
  },
}
</script>