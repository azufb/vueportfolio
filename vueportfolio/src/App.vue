<template>
  <div id='app'>
    <div class='mainTitle'>
      <h1>I am Azusa...</h1>
      <ul class='mainTab'>
        <li
        :class="{ active: currentTab === 'HomeTab' }"
        @click="currentTab = 'HomeTab'"
        >Home</li>
        <li
        :class="{ active: currentTab === 'ProfileTab' }"
        @click="currentTab = 'ProfileTab'"
        >Profile</li>
        <li
        :class="{ active: currentTab === 'MyWorksTab' }"
        @click="currentTab = 'MyWorksTab'"
        >My Works</li>
      </ul>
    </div>
    <div>
      <transition mode='out-in'>
      <component :is="currentTab"></component>
      </transition>
    </div>
  </div>
</template>

<script>
import HomeTab from './components/HomeTab.vue';
import ProfileTab from './components/ProfileTab.vue';
import MyWorksTab from './components/MyWorksTab';

export default {
  name: 'app',
  // 表示するタブの初期値
  data() {
    return {
      currentTab: 'HomeTab',
    };
  },
  components: {
    HomeTab,
    ProfileTab,
    MyWorksTab
  }
}
</script>

<style>
/* ページ遷移アニメーション */
.v-enter {
  transform: translate(-100px, 0);
  opacity: 0;
}

.v-enter-to {
  opacity: 1;
}

.v-enter-active {
  transition: all 1s 0s ease;
}

.v-leave {
  transform: translate(0,0);
  opacity: 1;
}

.v-leave-to {
  transform: translate(100px, 0);
  opacity: 0;
}

.v-leave-active {
  transition: all .5s 0s ease;
}

/* 全体 */
body {
  margin: 0px;
  background-color: #c8c9c9;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: black;
  margin-top: 0px;
}

/* トップのサイトタイトルとトップのナビゲーション */
.mainTitle {
  margin-top: 0px;
  margin-bottom: 0px;
  padding-left: 35px;
  display: flex;
  background-color: #e6e6e6;
}

h1 {
  margin-top: 7px;
  margin-bottom: 0px;
  font-size: 60px;
  font-family: 'Oswald', sans-serif;
}

/* ナビゲーション・タブの設定 */
.mainTab {
  display: flex;
  cursor: pointer;
  margin-top: 55px;
  margin-bottom: 0px;
  margin-left: 150px;
  padding-left: 0px;
  height: 30px;
  font-size: 20px;
}

.mainTab li {
  list-style: none;
  margin-right: 45px;
  font-family: 'Oswald', sans-serif;
}

.mainTab .active {
  border-bottom: 2px solid #d85782;
}

.profs {
  display: flex;
  cursor: pointer;
  padding-left: 0px;
}

.profs li {
  list-style: none;
  margin-right: 15px;
}

.profs .active {
  border-bottom: 2px solid #d85782;
}

.mWorks {
  display: flex;
  cursor: pointer;
}

.mWorks li {
  list-style: none;
  margin-right: 15px;
}

.mWorks .active {
  border-bottom: 2px solid #d85782;
}

.details {
  display: flex;
  cursor: pointer;
  padding-left: 0px;
}

.details li {
  list-style: none;
  margin-top: 15px;
  margin-right: 15px;
}

.details .active {
  border-bottom: 2px solid #d85782;
  padding-left: 15px;
  padding-right: 15px;
  font-size: 24px;
}

/* 各ページの見出し */
h2 {
  border-bottom: 4px solid #d85782;
}

/* 資格のページと成果物一覧ページの一覧表 */
table {
  margin-top: 50px;
  border-collapse: collapse;
  cursor: pointer;
}

th {
  border-bottom: 2px solid #d85782;
}

td {
  width: 230px;
  text-align: center;
  border-bottom: 1px solid black;
  cursor: pointer;
}

/* Homeのページ (imgは元々幅650pxだった)*/
#aisatu {
  margin-left: 45px;
  margin-right: 45px;
}

.homeDisp {
  display: flex;
}

.profpic1 {
  margin-left: 90px;
}

.text2 {
  display: none;
}

.profpic2 {
  display: none;
}

/* Profileページ */
#prof {
  margin-left: 45px;
  margin-right: 45px;
}

.profileDetail {
  display: flex;
}

.keireki {
  margin-left: 65px;
}

.twitterIcon {
  margin-left: 40px;
}

.facebookIcon {
  margin-left: 5px;
}

.githubIcon {
  margin-left: 5px;
}

.twitterIcon:link, .twitterIcon:visited,
.twitterIcon:hover, .twitterIcon:active {
  color: #1DA1F2;
  cursor: pointer;
}

.facebookIcon:link, .facebookIcon:visited,
.facebookIcon:hover, .facebookIcon:active {
  color: #3b5998;
  cursor: pointer;
}

.githubIcon:link, .githubIcon:visited,
.githubIcon:hover, .githubIcon:active {
  color: #333;
  cursor: pointer;
}

/* 成果物一覧ページ */
.list {
  margin-left: 45px;
  margin-right: 45px;
}

/* 成果物詳細ページ */
#detail {
  margin-left: 45px;
  margin-right: 45px;
}

.detail {
  display: flex;
}

h3 {
  margin-top: 0px;
}

.btn {
  background-color: black;
  font-family: 'Oswald', sans-serif;
  height: 30px;
  font-size: 17px;
  margin-left: 15px;
}

.btn:hover {
  background-color: #d85782;
}

.goToApp:link, .goToApp:visited,
.goToApp:hover, .goToApp:active {
  color: white;
  text-decoration: none;
}

.githubIcon2 {
  margin-left: 10px;
}

.githubIcon2:link, .githubIcon2:visited,
.githubIcon2:hover, .githubIcon2:active {
  color: #333;
  cursor: pointer;
}


footer {
  margin-top: auto;
  font-family: 'Oswald', sans-serif;
  background-color: #e6e6e6;
}

footer p {
  margin-top: 0px;
  margin-bottom: 0px;
}

@media(max-width: 767px) {
  table {
    margin-top: 20px;
  }

  th {
    font-size: 12px;
  }

  td {
    width: 230px;
    text-align: center;
    border-bottom: 1px solid black;
    font-size: 10px;
  }

  .genre {
    display: none;
  }

  .mainTitle {
    width: auto;
  }

  h1 {
    margin-top: 15px;
    margin-bottom: 0px;
    font-size: 40px;
    font-family: 'Oswald', sans-serif;
  }

  .mainTab {
    display: block;
    margin-top: 0px;
    margin-left: 10px;
    font-size: 17px;
  }

  .mainTab li {
    width: 70px;
    text-align: center;
  }

  #aisatu {
    margin-left: 10px;
    margin-right: 10px;
  }

  #prof {
    margin-left: 10px;
    margin-right: 10px;
  }

  .profileDetail {
    display: block;
    margin-left: 10px;
    margin-right: 10px;
  }

  .keireki {
    margin-left: 0px;
    margin-right: 0px;
  }

  .list {
    margin-left: 10px;
    margin-right: 0px;
    padding-left: 10px;
    padding-right: 10px;
    width: auto;
  }

  .latest {
    font-size: 10.5px;
  }

  .display {
    font-size: 8px;
  }

  #detail {
    margin-left: 10px;
    margin-right: 10px;
  }

  .details {
    display: inline;
  }

  .details li {
    margin-top: 15px;
  }

  .details .active {
    border-left: none;
    border-right: none;
    border-top: none;
    border-bottom: 2px solid #d85782;
    text-align: center;
    font-size: 15px;
  }

  .detail {
    margin-top: 10px;
    display: block;

  }

  .text1 {
    display: none;
  }

  .text2 {
    display: inline;
    font-size: 11px;
  }

  .profpic1 {
    display: none;
  }

  .profpic2 {
    display: inline;
  }
}

</style>
