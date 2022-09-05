<template>
  <div class="menu">
    <div class="bartop">
      <b-navbar class="bar_wrap" toggleable="lg"  fixed="top">
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav >
            <b-navbar-brand href="#" class="pic">
              <img class="logo" src="./assets/icon-10.png">
            </b-navbar-brand>
            <button v-on:click="scrollToElement({behavior: 'smooth'},'#home')">Home</button>
            <button v-on:click="scrollToElement({behavior: 'smooth'},'#wrap_info')">About me</button>
            <button v-on:click="scrollToElement({behavior: 'smooth'},'#wrap_skill')">Skill</button>
            <button v-on:click="scrollToElement({behavior: 'smooth'},'#wrap_experience')">Experience</button>
            <button v-on:click="scrollToElement({behavior: 'smooth'},'#wrap_works')">Works</button>
            <button v-on:click="scrollToElement({behavior: 'smooth'},'#wrap_hobbies')">Interest</button>
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    </div>
    <div class="cover"></div>
    <div class="content">
      <router-view></router-view>
    </div>
    
  </div>
  
</template>

<script>

import Footer from '@/components/Footer.vue'
export default {
  components: {
    Footer
  },
  data (){
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

}
</script>

<style>
html, body, .app{
  padding: 0;
  margin: 0;
  font-family: '微軟正黑體';
  width: 100%;
  overflow-x: hidden
}

div, span,h1, h2, h3, h4, h5, h6, p{
	margin: 0;
	padding: 0;
}
</style>

<style scoped>
.menu{
  background-color: #F8F9FA;
}
.bar_wrap{
  background-color: #FAEFC9;
  padding: 0
}

.pic{
  width: 50px;
  height: 65px;
  margin-left: 30px;
  margin-right: 15px;
  border-radius: 20%;
  padding: 10px 0;
}
.logo{
  width: 100%;
}
#nav-collapse button{
  border: none;
  font-size: 18px;
  font-weight: 600;
  color: #7B7D7C;
  position: relative;
  margin-right: 30px;
  background-color: #FAEFC9
}
#nav-collapse button:hover{
  color: #000
}
  
#nav-collapse button:after{
  content: '';
  position: absolute;
  border-bottom: 2px solid #000;
  bottom: 15px;
  left: 50%;
  right: 50%;
  transition: .3s;
}
  
#nav-collapse button:hover:after{
  left: 0%;
  right: 0%;
}

#nav-collapse button:focus{
  outline: none;
}

.cover{
  max-width: 100%;
  height: 450px;
  background: url('./assets/images.jpg');
  background-position: 30% 80%;
  background-size: cover;
}
.content{
  width: 100%;
  box-sizing: border-box;
  position: relative
}
.content::after{
  content: '';
  width: 200px;
  height: 200px;
  background-color: #F4F7E9;
  position: absolute;
  border-radius: 50%;
  top: 0;
  left: 50%;
  transform: translateY(-90px);
  box-shadow: 130px -20px 0 10px #F4F7E9,
  245px -10px 0 -10px #F4F7E9,
  400px -25px 0 10px #F4F7E9,
  550px -10px 0 -20px #F4F7E9,
  650px 10px 0 -20px #F4F7E9,
  800px -15px 0 10px #F4F7E9,
  -130px -35px 0 10px #F4F7E9,
  -260px 10px 0 -10px #F4F7E9,
  -400px -30px 0 20px #F4F7E9,
  -550px -20px 0 -20px #F4F7E9,
  -650px 10px 0 -20px #F4F7E9,
  -750px -30px 0 -20px #F4F7E9,
  -850px -10px 0 -20px #F4F7E9,
  -980px 0px 0 -20px #F4F7E9,
  100px -50px 0 20px rgba(0,0,0,.3),
  245px -60px 0 -10px rgba(0,0,0,.3),
  400px -60px 0 10px rgba(0,0,0,.3),
  550px -35px 0 -20px rgba(0,0,0,.3),
  650px -10px 0 -20px rgba(0,0,0,.3),
  -110px -60px 0 30px rgba(0,0,0,.3),
  -240px -20px 0 -10px rgba(0,0,0,.3),
  -390px -70px 0 15px rgba(0,0,0,.3),
  -570px -40px 0 20px rgba(0,0,0,.3),
  -750px -50px 0 -20px rgba(0,0,0,.3),
  -850px -30px 0 -20px rgba(0,0,0,.3)
}
  
.content::before{
  content: '';
  width: 100%;
  height: 200px;
  position: absolute;
  background-color: #F8F9FA;
  top: 0;
  left: 0;
  z-index: 1;
}

@media screen and (max-width: 767px){
  .pic{
    display: none
  }
  #nav-collapse button{
    margin-right: 0px;
    margin-bottom: 10px
  }
  #nav-collapse button:after{
    bottom: 0px;
  }
}
@media (min-width: 768px) and (max-width: 979px) {
  .pic{
    display: none
  }
  #nav-collapse button{
    margin-right: 0px;
    margin-bottom: 15px
  }
  #nav-collapse button:after{
    bottom: 0px;
  }

}
</style>