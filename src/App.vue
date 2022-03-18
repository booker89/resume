<template>
  <div class="menu">
    <router-link to="/">基本介紹</router-link>
    <router-link to="/work">工作經驗</router-link>
    <div class="cover"></div>
    <div class="content">
      <router-view></router-view>
    </div>
    <Footer></Footer>
  </div>
</template>

<script>
import Footer from '@/components/Footer.vue'
  export default {
    components: {
      Footer
    }
  }
</script>

<style>
html, body, .app{
  padding: 0;
  margin: 0;
  font-family: Arial;
  color: #444;
}
body{
  background-color: #1a467e
}
div, span,h1, h2, h3, h4, h5, h6, p{
	margin: 0;
	padding: 0;
}
</style>

<style scoped>
a{
  display: inline-block;
  font-size: 14px;
  color: white;
  text-decoration: none;
  padding: 15px 25px;
  color: #f8d482;
}
a:hover{
  background-color: #f8d48220;
}
.cover{
  width: 100%;
  height: 450px;
  background: url('./assets/images.jpg');
  background-position: 30% 80%;
  background-size: cover;
}
.content{
  width: 100%;
  padding: 0 150px 50px;
  box-sizing: border-box;
}
</style>