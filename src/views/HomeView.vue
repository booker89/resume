<template>
  <div class="title_wrap">
    <div class="title">
      <h2>個人資料</h2>
    </div>
    <div class="info-wrap">
      <div class="personal_img">
        <img src ="../assets/me.jpg"/> 
      </div>
      <div class="info_content">
        <div class="content" v-for="info in Infos">
          <div class="img" :style="imgStyle(info.img)"/>
          <div>{{info.name}}</div>
        </div>
      </div>
    </div>
    <div class="title">
      <h2>關於我</h2>
      <div class="about_content" v-for="item in about">
        <h3>{{item.name}}</h3>
        <p>{{item.content}}</p>
      </div>
    </div>
    <div class="title">
      <h2>技能</h2>
      <div class="graph">
        <div class="left">
          <div>HTML</div>
          <div class="graph_out"></div>
          <div class="graph_in html"></div>
          <div>CSS</div>
          <div class="graph_out"></div>
          <div class="graph_in css"></div>
        </div>
        <div class="right">
          <div>JavaScript</div>
          <div class="graph_out"></div>
          <div class="graph_in javascript"></div>
          <div>Vue</div>
          <div class="graph_out"></div>
          <div class="graph_in vue"></div>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
import Infos from '@/Infos';
export default {
  data(){
    return {
      about: [
        {
          name:'【出生背景】', 
          content:'生長在純樸的家庭，家中排行老二，因為負責任的態度深獲姊妹們的信賴，每當他們有困難時，我總用最客觀的角度幫助他們分析、解決問題。'
        },
        {
          name:'【求學過程】', 
          content:'畢業於國立虎尾科技大學休閒遊憩系，喜歡嘗試、挑戰新的事物，在學期間修過許多外系的課程，在大四時選修了網頁前端課程，在實作的過程中雖然會遇到問題，但透過網路搜尋或是跟夥伴討論讓我去思考錯誤的原因，真正從錯誤中學習。現在我不怕遇到程式錯誤，反而更享受debug的過程，因為每一次都可以學到一些新的觀念，讓自己養成長久學習的良好習慣。'
        },
        {
          name:'【自學過程】', 
          content:'為了能更熟悉怎麼使用JavaScript，所以我利用網路上一位國外工程師Wesbos提供的30個簡單的JS作品，並利用三十天的時間每天實作一個作品並把過程、遇到的問題寫成部落格，讓我在忘記時幫助自己喚醒記憶。由於一些技術對我來說是陌生的，在學完這30天後讓我比較知道一些js的事件、canvas用法及Array的各種操作等，但我知道技術是不斷日益更新，所以在學習上一旦停滯不前就有可能被淘汰，而我也樂於發展自己在前端工程上的技能，讓自己不斷地精進。'
        },
        {
          name:'【工作經歷】', 
          content:'曾任職於圓剛科技股份有限公司，擔任研發助理工程師，撰寫測試步驟(shell script...)，協助專案透過jenkins做持續整合及自動發行，提升後續開發時間，並在其中學到了用Puppeteer抓取網頁資料及使用少量的python操作excel檔案的讀寫；在專案期間(Live Streamer AX310)使用canvas套件-fabric js來製作icon-builder網頁，讓使用者可以客製化hotkey的樣式，並透過javascript協助開發四種widget(數位時鐘、類比時鐘、計時器、鬧鐘)，過程中要跟同仁串接各種事件的api，學到資料互相傳遞及分工合作的重要性，另外也協助撰寫提供給外部開發者的sample code。盡全力達成公司的營運目標、提昇公司績效、創造優良的公司形象。'
        },
        {
          name:'【未來規劃】', 
          content:'給自己的工作期許，希望在未來的路途上，可以不斷的突破成長，充分發揮專長，學習更多新的技術，精益求精成為一名傑出的軟體工程師。'
        }
      ],
    }
  },
  computed:{
    Infos(){
      return Infos;
    }
  },
  methods:{
    imgStyle(img){
      return {
        backgroundImage: `url('${img}')`,
      };
    },
  },
};
</script>

<style scoped>
.title_wrap{
  padding-top: 50px;
}

.title > h2{
  background-color: #f8d482;
  color: #344648;
  font-size: 20px;
  text-align: center;
  padding: 10px 0;
 
}
.info-wrap{
  width: 100%;
  display: flex;
  justify-content: right;
  align-items: center;
  background-color: #fff;
  padding: 20px 0
}
.info-wrap > .personal_img{
  width: 10%;
}
.info-wrap > .personal_img > img{
  display: block;
  width: 100%;
  border-radius: 50%
}
.info-wrap > .info_content{
  width: 50%;
  margin-left: 25px
}
.info-wrap > .info_content > .content{
  display: flex;
  color: #000;
  margin-bottom: 10px
}
.img{
  display: inline-block;
  width: 30px;
  height: 30px;
  background: center center;
  background-size: 75%;
  background-repeat: no-repeat;
  margin-right: 20px;
}

.about_content{
  color: #000;
  padding: 0 20px 25px 20px;
  background-color: #fff;

}
.about_content > h3{
  padding: 15px 0 5px 0;
}
.about_content > p{
  text-indent: 2em;
  letter-spacing: 1.5px;
  line-height: 24px
}

/*skill*/
.graph{
  background-color: #fff;
  display: flex;
  justify-content: center;
  padding: 20px 0;
}
.graph > .left{
  width: 25%;
  margin-right: 20px
}
.graph > .right{
  width: 25%;
}

.graph_out{
  max-width: 350px;
  height: 16px;
  padding: 2px;
  border: 2px solid #2c4f54;
}
.graph_in{
  position: relative;
  background-color: #007bbb;
  height: 16px;
  top: -19px;
  left: 3px;
}
.html{
  max-width: 290px;
}
.css{
  max-width: 270px;
}
.javascript{
  max-width: 250px;
}
.vue{
  max-width: 150px;
}

@media screen and (max-width: 767px){
  .title_wrap{
    padding-top: 15px;
  }
  .info-wrap{
    justify-content: center;
    flex-wrap: wrap;
  }
  .info-wrap > .personal_img{
    width: 40%;
  }
  .info-wrap > .info_content{
    width: 100%;
    margin: 15px 0 0 0;
    padding: 0 10px 0 90px
  }
  .about_content > h3{
    text-align: center;
  }
  .graph{
    flex-wrap: wrap;
  }
  .graph > .left, 
  .graph > .right{
    width: 100%;
    padding: 0 15px 0 15px;
  }
  .graph > .left{
    margin-right: 0px
  }
  
}
@media (min-width: 768px) and (max-width: 979px) {
  .graph{
    flex-wrap: wrap;
  }
  .graph > .left{
    width: 51%;
    margin-right: 0px
  }
  .graph > .right{
    width: 51%;
  }
}

</style>
