<template>
  <div id="wrap_skill">
    <h1>Skill</h1>
    <div class="title_boder"></div>
    <div class="skill_wrap">
      <div class="content">
        <h5>hard skills</h5>
        <div v-for="bar in bars" class="row mb-4">
          <div class="col-sm-2 bar_name">{{ bar.variant }}:</div>
          <div class="col-sm-10 pt-1">
            <b-progress height="20px" :value="bar.value" variant="info"  :key="bar.variant"></b-progress>
          </div>
        </div>
      </div>
      <div class="content">
        <h5>soft skills</h5>
        <div v-for="bar in soft_bars" class="row mb-4">
          <div class="col-sm-2 bar_name">{{ bar.variant }}:</div>
          <div class="col-sm-10 pt-1">
            <b-progress height="20px" :value="bar.value" variant="info"  :key="bar.variant"></b-progress>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style>
#wrap_skill .skill_wrap{
  display: flex;
  justify-content: space-between;
  margin-top: 70px;
}
#wrap_skill .content{
  width: 47%;
}
#wrap_skill{
  background-color: #F4F7E9;
}
#wrap_skill h5{
  margin-bottom: 30px;
  padding-left: 20px;
  margin-left: 20px;
  border-left: 5px solid #BBC1BD;
  color: #7B7D7C;
}
#wrap_skill .bar_name{
  text-align:right
}
@media screen and (max-width: 767px){
  #wrap_skill .skill_wrap{
    flex-wrap: wrap
  }
  #wrap_skill .content{
    width: 100%;
    padding-bottom: 30px
  }
  #wrap_skill .bar_name{
    text-align: left
  }
}
@media (min-width: 768px) and (max-width: 979px) {
  #wrap_skill .skill_wrap{
    flex-wrap: wrap
  }
  #wrap_skill .content{
    width: 100%;
    padding-bottom: 30px
  }
}
</style>
<script>
export default {
  data(){
      return {
        bars: [
          { variant: 'HTML', value: 80 },
          { variant: 'JS', value: 65 },
          { variant: 'CSS', value: 75 },
          { variant: 'VUE', value: 45 },
        ],
        soft_bars: [
          { variant: '溝通', value: 85 },
          { variant: '管理', value: 60 },
          { variant: '領導', value: 50 },
        ],
        timer: null
      }
    },
}
</script>