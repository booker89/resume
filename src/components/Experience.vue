<template>
  <div id="wrap_experience">
    <h1>Experience</h1>
    <div class="title_boder"></div>
    <section class="timeline">
    <div class="column">
      <div class="row">
        <div class="text">
          <h3>雍盛科技 ┃ 前端網頁設計工程師</h3>
          <p>- 使用vue製作環保署網站的圖資申請、圖資審查功能、頁面。</p>
          <p>- 運用vue及資料庫的建立製作宜蘭縣下水道營運管理系統的派工管理模組。</p>
          <p>- 透過公司套件XGIS及資料庫的建立開發測速照相APP後台及APP部份的畫面、功能製作。</p>
          <p>- 透過公司套件XGIS及資料庫的建立製作地磅站後台。</p>
        </div>
        <div class="icon">
          <div><i><font-awesome-icon icon="fa-solid fa-star"/></i></div>
        </div>
        <div class="time">
          <time>2022.04-2022.08</time>
        </div>
      </div>
      <div class="row">
        <div class="text">
          <h3>圓剛科技 ┃ 助理⼯程師</h3>
          <p>- 使用jenkins替公司專案做持續整合(CI)，並搭配shell script、puppeteer及python..做自動發行(CD)。</p>
          <p>- 運用javascript製作專案(Live Streamer AX310)所需四種widgets。</p>
          <p>- 提供專案Live Streamer AX310的sample code(js)給外部開發人員參考。</p>
          <p>- 透過fabric.js來製作icon-builder網頁，讓使用者可以客製化Live Streamer AX310的hotkey及background樣式。</p>
          <p>- 與團隊合作，開發widget store後台管理介面功能。</p>
        </div>
        <div class="icon">
          <div><i><font-awesome-icon icon="fa-solid fa-star" /></i></div>
        </div>
        <div class="time">
          <time>2020.11-2022.02</time>
        </div>
      </div>
      <div class="row">
        <div class="text">
          <h3>雲林科技大學 ┃ 專案助理</h3>
          <p>- 控管國教署、科技部及縣府委託共九項計畫案的經費及核銷，在控管方面成功在2019年教育部委辦計畫共八項中有六項執行率達90%，其中四項更達到95%，盡全力達成公司的營運目標、提昇公司績效、創造優良的公司形象。</p>
          <p>- 每月統整、計算中心專案、兼任人員薪資、業務獎勵金、加班費。</p>
          <p>- 統計各計劃案業務費及人事費的預支款項核結監督。</p>
          <p>- 專案人力資源配置與管控。</p>
          <p>- 現金出納 財務處理。</p>
        </div>
        <div class="icon">
          <div><i><font-awesome-icon icon="fa-solid fa-star" /></i></div>
        </div>
        <div class="time">
          <time>2019.06-2020.08</time>
        </div>
      </div>
      <div class="row">
        <div class="text">
          <h3>沐綿產後護理之家 ┃ 櫃台招待</h3>
          <p>- 關心月子媽媽們的身體、精神狀況並解決媽媽們的問題。</p>
          <p>- 負責接待並過濾訪客，提供解說和諮詢的服務。</p>
          <p>- 處理緊急突發事件。</p>
          <p>- 文件的輸入、建檔與彙整。</p>
          <p>- 客訴案件處理，協助完成需求及解決問題。</p>
        </div>
        <div class="icon">
          <div><i><font-awesome-icon icon="fa-solid fa-star" /></i></div>
        </div>
        <div class="time">
          <time>2017.03-2019.05</time>
        </div>
      </div>
      <div class="row">
        <div class="text">
          <h3>大墩陽光-兒童冬令營 ┃ 營隊老師</h3>
          <p>- 擔任老師以簡單有趣、情境圖畫的方式教導小朋友們知識。</p>
          <p>- 帶領孩童透過戶外的遊戲競賽了解團隊合作的重要性。</p>
          <p>- 與孩童建立良好關係、維持秩序、配課的流暢度、與家長的應對。</p>
          <p>- 處理突發狀況，並解決問題。</p>
        </div>
        <div class="icon">
          <div><i><font-awesome-icon icon="fa-solid fa-star" /></i></div>
        </div>
        <div class="time">
          <time>2017.01-2017.02</time>
        </div>
      </div>
    </div>
  </section>
  </div>
</template>
<style>

.timeline > h3 {
  text-align: center;
  text-transform: capitalize;
  font-size: 2rem;
  font-weight: bold;
  padding: 1rem;
}

.timeline > .column {
  display: flex;
  flex-direction: column;
  position: relative;
  margin-top: 70px;
}

.timeline > .column::before {
  content: "";
  display: block;
  position: absolute;
  left: 50%;
  transform: translatex(-50%);
  border: 1px solid rgba(49, 49, 49, 0.5);
  height: calc(100% / 5 * 5);
  z-index: -1;
}

.timeline > .column > .row {
  display: flex;
}

/* row text */
.timeline > .column > .row > .text {
  flex: 1 1 calc(50% - 50px);
  position: relative;
  box-shadow: 0 1rem 3rem rgba(0, 0, 0, 0.175);
}
.timeline > .column > .row h3 {
  color: #fff; 
  background-color: #A29C97;
  padding: 1rem;
  border-top-left-radius: 5px;
  border-top-right-radius: 5px;
}

.timeline > .column > .row p {
  padding: 5px 15px;
  margin: 0;
  color: #000;
  border-bottom-left-radius: 5px;
  border-bottom-right-radius: 5px;
  text-indent: -0.7rem;
}

/* row icon */
.timeline > .column > .row > .icon {
  flex: 1 1 100px;
}

.timeline > .column > .row > .icon > div {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin: auto;
  background: #fff;
  box-shadow: 0 1rem 3rem rgb(0 0 0 / 18%);
  position: relative;
  
}

.timeline > .column > .row > div i {
  display: block;
  font-size: 1.5rem;
  color: #FCEBB6;
  text-align: center;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

/* row time */
.timeline > .column > .row > .time {
  flex: 1 1 calc(50% - 50px);
  padding-top: 1rem;
  
}

.timeline > .column > .row:nth-child(even) {
  flex-direction: row-reverse;
    
}

.timeline > .column > .row:nth-child(even) > div:last-child {
  text-align: end;

}

.timeline > .column > .row:nth-child(even) h3::before {
  content: "";
  position: absolute;
  left: -20px;
  border: 10px solid rgba(0, 0, 0, 0);
  border-right-color: #A29C97;
  
}
.timeline > .column > .row:nth-child(odd) h3::after {
  content: "";
  position: absolute;
  right: -20px;
  border: 10px solid rgba(0, 0, 0, 0);
  border-left-color: #A29C97;
}


/* mobile version */
@media screen and (max-width: 768px) {
  .timeline > .column {
    display: flex;
  }
  .timeline > .column > .row:nth-child(odd) {
    display: flex;
    flex-wrap: wrap;
    flex-direction: column-reverse;
    margin-bottom: 30px;
  }
  .timeline > .column > .row:nth-child(even) {
    display: flex;
    flex-wrap: wrap;
    flex-direction: column-reverse;
    margin-bottom: 30px;
  }
  .timeline > .column > .row:nth-child(even) > .time:last-child {
    text-align: start;
  }
  .timeline > .column > .row > .icon {
    display: none
  }
  .timeline > .column > .row > .time {
    width: 100%;
    flex: none
  }
  .timeline > .column > .row > .text {
    width: 100%
  }
  .timeline > .column::before {
    display: none;
  }
  .timeline > .column > .row:nth-child(even) h3::before {
    display: none;
  }
  .timeline > .column > .row:nth-child(odd) h3::after {
    display: none;
  }

}
</style>
