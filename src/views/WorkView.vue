
<template>
  <div>
    <div class="title_wrap">
      <div class="title">
        <h2>工作經驗</h2>
      </div>
      <div class="work">
        <div class="work_item" v-for="item in experience">
          <h3>{{item.title}}</h3>
          <h5>{{item.time}}</h5>
          <ul>
            <li>{{item.li1}}</li>
            <li>{{item.li2}}</li>
            <li>{{item.li3}}</li>
            <li>{{item.li4}}</li>
            <li>{{item.li5}}</li>
            <li>{{item.li6}}</li>
          </ul>
        </div>
      </div>
    </div>
      <div class="title">
        <h2>作品</h2>
        <div class="wrap">
          <div class="items" v-for="work in works">
            <img :style="imgStyle(work.img)">
            <div class="text">
              <h2>{{work.name}}</h2>
              <span>專案主要內容：</span>
              <p>-{{work.text1}}</p>
              <p>-{{work.text2}}</p>
              <p>-{{work.text3}}</p>
            </div>
          </div>
        </div>

      </div>
  </div>
</template>

<script>
import img_ax310 from '../assets/ax-310.jpg';
import img_icon_builder from '../assets/icon-builder.jpg';
export default {
  data(){
    return {
      works: [
        {name:'Live Streamer AX310', img:img_ax310, text1:'製作數位/類比時鐘widgets', text2:'製作計時器widgets',text3:'製作鬧鐘widgets'},
        {name:'icon builder(Live Streamer AX310)', img:img_icon_builder, text1:'使用Fabric.js', text2:'功能UI畫面',text3:'實現更改size、color、存檔、對齊線...等功能'}
      ],
      experience: [
        {
          title:'圓剛科技有限公司｜助理⼯程師',
          time:'2020/11-2022/02',
          li1:'使用jenkins做持續整合(CI)',
          li2:'使用jenkins並搭配shell script、puppeteer及python..做自動發行(CD)',
          li3:'使用javascript製作專案(Live Streamer AX310)所需四種widgets',
          li4:'提供sample code給外部開發人員參考',
          li5:'使用fabric js來製作icon-builder網頁，讓使用者可以客製化hotkey的樣式',
          li6:'與後端工程師合作，開發widget store後台管理介面功能'
        },
        {
          title:'國立雲林科技大學｜專任助理',
          time:'2019/06-2020/08',
          li1:'控管國教署、科技部及縣府委託共九項計畫案的經費及核銷',
          li2:'每月統整、計算中心專案、兼任人員薪資、業務獎勵金、加班費',
          li3:'統計各計劃案業務費及人事費的預支款項核結監督',
          li4:'專案人力資源配置與管控',
          li5:'現金出納 財務處理',
          li6:'在控管方面成功在去年教育部委辦計畫共八項中有六項執行率達90%，其中四項更達到95%'
        }
      ]
    }
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

<style scoped>
.title_wrap{
  padding-top: 50px
}

.title > h2{
  background-color: #f8d482;
  color: #344648;
  font-size: 20px;
  text-align: center;
  padding: 10px 0
}
.work{
  background-color: #fff;
  padding: 15px 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center
}

.work > .work_item{
  width: 51%; 
  padding: 15px 0;
}
.work > .work_item > h3{
  text-indent: 2em;
  padding: 5px 0
}
.work > .work_item > h5{
  color: #ccc;
  text-indent: 3em;
}
li{
  margin: 10px 0;
}

/*----作品---　*/
.wrap{
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #fff;
  padding: 20px 0
}
.items{
  width: 25%;
  height: 280px;
  position: relative;
  background-color: #1a467e;
  border-radius: 5px;
  margin-left: 20px;
  overflow: hidden;
}
.wrap > .items:hover .text{
  opacity: 1
} 
.wrap > .items > img{
  display: inline-block;
  width: 100%;
  height: 100%;
  background: center center;
  background-size: 75%;
  background-repeat: no-repeat;
} 
.text{
  position: absolute;
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  padding: 20px;
  background-color: rgba(0,0,0,.6);
  display: flex;
  flex-direction: column;
  justify-content: center;
  line-height: 28px;
  opacity: 0;
  transition: 1s;
}
.text > h2{
  font-size: 25px;
  color: #ff0;
}
.text > span{
  font-size: 18px;
  color: #c2bd60;
  padding: 10px 0;
 
}
.text > p{
  font-size: 14px;
  color: #fff;
  font-weight: 50;
}


@media screen and (max-width: 767px){
  .title_wrap{
    padding-top: 15px;
  }
  .work > .work_item{
    width: 100%; 
    padding: 5px 0;
  }
  .wrap{
    padding: 10px 0 0 0;
    flex-wrap: wrap
  }
  .items{
    width: 100%;
    margin: 0 0 10px 0;
  }
  .text{
    text-align: center
  }
}
@media (min-width: 768px) and (max-width: 979px) {
   .work > .work_item{
    width: 90%; 
  }
  .wrap{
    padding: 10px 0 0 0;
    flex-wrap: wrap
  }
  .items{
    width: 45%;
    margin: 0 0px 10px 0;
  }
  .items:first-child{
    margin-right: 15px;
  }
  .text{
    text-align: center
  }
}
</style>
  