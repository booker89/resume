<template>
  <div class="title_wrap">
    <div id="home" class="info-wrap">
      <div class="personal_img">
        <img src ="../assets/me.jpg"/> 
      </div>
      <div class="info_content">
        <div class="content">
          <h3>王卉旻 Mandy</h3>
          </br>
          <p>有管理政府單位各式專案的經驗，也曾擔任過前端工程師，所以更能夠從不同角度出發思考需求，以及會思考如何加速數據變現的腳步</p>
          </br>
          <p>個性開朗，心思細膩成熟，勇於面對新的挑戰，樂於接觸學習新的事物，會盡力完成被賦予的責任。</p>
          </br>
          <button class="morebtn" v-on:click="scrollToElement({behavior: 'smooth'},'#wrap_info')">了解更多</button>
        </div>
      </div>
    </div>
    <Info></Info>
    <Skill></Skill>
    <Experience></Experience>
    <Works></Works>
    <Hobbies></Hobbies>
    <Footer></Footer>
  </div>
  
</template>

<script>
import Infos from '@/Infos';
import Footer from '@/components/Footer.vue';
import Hobbies from '@/components/Hobbies.vue';
import Experience from '@/components/Experience.vue';
import Works from '@/components/Works.vue';
import Skill from '@/components/Skill.vue';
import Info from '@/components/Info.vue';
export default {
  components: {
      Footer,
      Hobbies,
      Experience,
      Works,
      Skill,
      Info
  },
  data(){
    return {}
  },
  methods: {
    scrollToElement(options,name) {
      const el = this.$el.querySelector(name);
      console.log('el',el)
      if (el) {
        el.scrollIntoView(options);
      }
    },
  }

};
</script>

<style>
#wrap_info,#wrap_experience,#wrap_hobbies,#wrap_skill,#wrap_works{
	width: 100%;
  padding: 100px 150px;
	margin: auto;
}
#wrap_experience:after{
  content: '';
  display: block;
  width: 100%;
  height: 0px;
  clear: both;
}
#wrap_info h1,
#wrap_experience h1,
#wrap_hobbies h1,
#wrap_skill h1,
#wrap_works h1{
  color: #F7E5A1
}
#wrap_info .title_boder,
#wrap_experience .title_boder,
#wrap_hobbies .title_boder,
#wrap_skill .title_boder,
#wrap_works .title_boder{
  width: 100px;
  border-bottom: 5px solid #F7E5A1;
}


.title_wrap{
  width: 100%;
  margin: auto;
  position: relative;
  z-index: 2;
  background-color: #FFFCF4;
  padding: 0;

}
.info-wrap{
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #F4F7E9;
  padding: 70px 0;
}
.personal_img{
  width: 330px;
  height: 325px
}
.personal_img > img{
  display: block;
  height: 100%;
  border-radius: 50%;

}
.info-wrap > .info_content{
  width: 25%;

}

.personal_img .img{
  display: inline-block;
  width: 30px;
  height: 30px;
  background: center center;
  background-size: 75%;
  background-repeat: no-repeat;
  margin-right: 20px;
}

.morebtn{
  background-color: #999a99;
  color: #000;
  border: none;
  color: #fff;
  padding: 7px 15px;
  border-radius: 5px
}
.morebtn:hover{
  background-color: #7B7D7C;
}
.morebtn:focus{
  outline: none;
}



@media screen and (max-width: 767px){

  .info-wrap{
    flex-wrap: wrap
  }
  .info-wrap > .info_content{
    width: 100%;
    padding: 20px
  }
  .personal_img{
    width: 230px;
    height: 225px;
    display: flex;
    justify-content: center
  }
  #home h3{
    text-align: center
  }
  #home .content{
    position: relative;
  }
  #home .morebtn{
    position: absolute;
    bottom: -10%;
    left: 50%;
    transform: translate(-50%,10%);
  }
   #wrap_info,#wrap_experience,#wrap_hobbies,#wrap_skill,#wrap_works{
    padding: 30px;
  }
  
}
@media (min-width: 768px) and (max-width: 979px) {
  .info-wrap > .info_content{
    width: 50%;
  }
  #wrap_info,#wrap_experience,#wrap_hobbies,#wrap_skill,#wrap_works{
    padding: 30px;
  }
}

</style>
