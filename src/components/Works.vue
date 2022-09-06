<template>
  <div id="wrap_works">
  <h1>Works</h1>
  <div class="title_boder"></div>
    <div class="blog-card" v-for="work in works">
      <div class="meta">
        <div class="photo" :style="worksImg(work.img)"/>
      </div>
      <div class="description">
        <h1>{{work.title}}</h1>
        <p>{{work.li1}}</p>
        <p>{{work.li2}}</p>
        <p>{{work.li3}}</p>
        <p>{{work.li4}}</p>
        <p>{{work.li5}}</p>
        <p>{{work.li6}}</p>
      </div>
    </div>
  </div>
</template>
<style>
#wrap_works{
  background-color: #F4F7E9;
}

.blog-card {
  display: flex;
  margin: 70px auto;
  box-shadow: 0 3px 7px -1px rgba(0, 0, 0, .1);
  margin-bottom: 1.6%;
  background: #fff;
  line-height: 1.4;
  border-radius: 5px;
  overflow: hidden;
  z-index: 0;
}
.blog-card:nth-child(odd){
  flex-direction: row-reverse;
  justify-content: space-between
}
.blog-card:hover .photo {
  transform: scale(1.3) rotate(3deg);
}
.blog-card .meta {
  position: relative;
  z-index: 0;
  height: 350px;
  width: 40%;
}
.blog-card .photo {
  background-position: center;
  background-size: 100%;
  width: 100%; 
  height: 350px;
  transition: transform 0.2s;
  display: inline-block;
  background-repeat: no-repeat;
}

.description {
  padding: 1rem;
  background: #fff;
  position: relative;
  z-index: 1;
  width: 55%;
  
}
#wrap_works .description h1 {
  color: #7B7D7C;
  line-height: 1;
  margin: 0;
  font-size: 30px;
  font-weight: 500;
}

.description p {
  position: relative;
  margin: 1rem 0 0;
  text-indent: -0.7rem;
}
@media screen and (max-width: 767px){
  .blog-card{
    flex-wrap: wrap;
    align-items: center;

  }
  .blog-card .meta {
    width: 100%;
    height: 200px
  }
  .blog-card .photo {
    height: 200px
  }
  .description{
    width: 100%
  }
  .description h1{
    font-size: 24px;
  }
}
@media (min-width: 768px) and (max-width: 979px) {
  .blog-card{
    flex-wrap: wrap

  }
  .blog-card .meta {
    width: 100%
  }
  .description{
    width: 100%
  }
  
}

</style>
<script>
import works from '@/works';
export default {
computed:{
  works(){
    return works;
  }
},
methods:{
  worksImg(img){
    return {
      backgroundImage: `url('${img}')`,
    };
  },
},

}

</script>