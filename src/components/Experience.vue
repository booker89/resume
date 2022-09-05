<template>
  <div id="wrap_experience">
    <h1>Experience</h1>
    <div class="title_boder"></div>
    <ul class="timeline">
      <li>
        <a href="javascript:void(0)">
          <h3>雍盛科技 ┃ 前端網頁設計工程師</h3>
          <span>2022.04-2022.08</span>
          <p>- 環保署網站製作</p>
          <p>- 宜蘭縣下水道營運管理系統</p>
          <p>- 測速照相後台</p>
          <p>- 地磅後台</p>
        </a>
        
      </li>
      <li>
        <a href="javascript:void(0)">
          <h3>圓剛科技 ┃ 助理⼯程師</h3>
          <span>2020.11-2022.02</span>
          <p>- 使用jenkins做持續整合(CI)，並搭配shell script、puppeteer及python..做自動發行(CD)</p>
          <p>- 使用javascript製作專案(Live Streamer AX310)所需四種widgets</p>
          <p>- 使用fabric js來製作icon-builder網頁，讓使用者可以客製化hotkey的樣式</p>
          <p>- 與後端工程師合作，開發widget store後台管理介面功能</p>
        </a>
      </li>
      <li>
        <a href="javascript:void(0)">
          <h3>雲林科技大學 ┃ 專案助理</h3>
          <span>2019.06-2020.08</span>
          <p>- 控管國教署、科技部及縣府委託共九項計畫案的經費及核銷，在控管方面成功在去年教育部委辦計畫共八項中有六項執行率達90%，其中四項更達到95%，盡全力達成公司的營運目標、提昇公司績效、創造優良的公司形象</p>
          <p>- 統計各計劃案業務費及人事費的預支款項核結監督。</p>
          <p>- 專案人力資源配置與管控。</p>
        </a>
      </li>
      <li>
        <a href="javascript:void(0)">
          <h3>沐綿產後護理之家 ┃ 櫃台招待</h3>
          <span>2017.03-2019.05</span>
          <p>- 關心月子媽媽們的身體、精神狀況並解決媽媽們的問題。</p>
          <p>- 負責接待並過濾訪客，提供解說和諮詢的服務。</p>
          <p>- 處理緊急突發事件。</p>
          <p>- 文件的輸入、建檔與彙整。</p>
          <p>- 客訴案件處理，協助完成需求及解決問題。</p>
        </a>
      </li>
      <li>
        <a href="javascript:void(0)">
          <h3>大墩陽光-兒童冬令營 ┃ 營隊老師</h3>
          <span>2017.01-2017.02</span>
          <p>- 擔任老師以簡單有趣、情境圖畫的方式教導小朋友們知識</p>
          <p>- 帶領孩童透過戶外的遊戲競賽了解團隊合作的重要性</p>
          <p>- 與孩童建立良好關係、維持秩序、配課的流暢度、與家長的應對</p>
          <p>- 處理突發狀況，並解決問題</p>
        </a>
      </li>
    </ul>
  </div>
</template>
<style>

#wrap_experience a{
  text-decoration: none;
  color: #000;
}
#wrap_experience span{
  display: inline-block;
  padding: 10px 0;
  color: #929593
}
.timeline{
  padding: 70px 0 200px;
}
.timeline li{
  list-style-type: none;
  width: 50%;
  box-sizing: border-box;
  padding: 40px 0;
  position: relative;
}
.timeline li:nth-child(odd){
  float: left;
  padding-right: 120px;
}
.timeline li:nth-child(even){
  float: right;
  padding-left: 120px;
  transform: translateY(50%);
}
.timeline li:nth-child(odd)::after{
  content: '';
  position: absolute;
  z-index: -1;
  width: 1px;
  top: 0;
  height: 100%;
  background-color: #ccc;
  right: 0;
}
.timeline li:last-child::after{
  height: 50%;
  border: 1px solid #ccc
}

.timeline li:before{
  content: '';
  position: absolute;
  top: 0;
  bottom: 0;
  margin: auto;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background-color: #aaa;
  z-index: 2;
}
.timeline li:nth-child(odd)::before{
  right: -10px;
}
.timeline li:nth-child(even)::before{
  left: -10px;
}
.timeline a{
  display: block;
  text-decoration: none;
  background-color: #fff;
  border: 1px solid #aaa;
  box-sizing: border-box;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 3px 3px 5px #888; 
}
.timeline a:hover{
  background-color: #D5D6CF
}
.timeline a:hover h3{
  color: #000;

}
.timeline h3{
  color: #7B7D7C;
  font-weight: 500;
  margin-bottom: 1em;
  margin: 0

}
.timeline p{
  color: #000;
  font-weight: 200;
  line-height: 1.5;
  margin: 0
}

.timeline h3::after{
  content: '';
  position: absolute;
  height: 1px;
  width: 120px;
  background-color: #BBC1BD;
  top: 0;
  bottom: 0;
  margin: auto;
}
.timeline li:nth-child(odd) h3::after{
  right: 0;
}
.timeline li:nth-child(even) h3::after{
  left: 0;
}
@media screen and (max-width: 767px){
  .timeline{
    padding: 30px 0px;
  }
  .timeline li:nth-child(odd){
    padding-right: 0px;
  }

  .timeline li{
    width: 100%;
    padding: 10px 0;
  }
  .timeline li:nth-child(odd){
    float: none;
    padding-right: 0px;
    margin-bottom: 20px
  }
  .timeline li:nth-child(even){
    float: none;
    padding-left: 0px;
    margin-bottom: 20px;
    transform: translateY(0%);
  }

  .timeline h3::after{
    display: none
  }
  .timeline li:before{
    display: none
  }
  .timeline li:nth-child(odd)::after{
    display: none
  }
}
@media (min-width: 768px) and (max-width: 979px) {
  .timeline li:nth-child(odd){
 
    padding-right: 30px;
  }
  .timeline li:nth-child(even){
    padding-left: 30px;
  }
  .timeline h3::after{
    width: 30px;
  }
}
</style>
