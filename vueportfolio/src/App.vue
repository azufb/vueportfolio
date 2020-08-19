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
import MyWorksTab from './components/MyWorksTab.vue';

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
  font-size: 50px;
  font-family: 'Oswald', sans-serif;
}

.mainTab {
  margin-top: 30px;
  margin-bottom: 0px;
  padding-left: 150px;
  height: 30px;
}

/* ナビゲーション・タブの設定 */
.mainTab {
  display: flex;
  cursor: pointer;
}

.mainTab li {
  list-style: none;
  margin-right: 15px;
  font-family: 'Oswald', sans-serif;
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

.mWorks {
  display: flex;
  cursor: pointer;
}

.mWorks li {
  list-style: none;
  margin-right: 15px;
}

.details {
  display: flex;
  cursor: pointer;
  padding-left: 0px;
}

.details li {
  list-style: none;
  margin-right: 15px;
}

/* 各ページの見出し */
h2 {
    border-bottom: 3px solid #d85782;
}

/* 資格のページと成果物一覧ページの一覧表 */
table {
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

/* Homeのページ */
#aisatu {
  margin-left: 45px;
  margin-right: 45px;
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
  margin-left: 80px;
}

.twitterIcon {
  padding-left: 20px;
}

.facebookIcon {
  padding-left: 5px;
}

.githubIcon {
  padding-left: 5px;
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

footer {
  margin-top: auto;
  font-family: 'Oswald', sans-serif;
  background-color: #e6e6e6;
}

footer p {
  margin-top: 0px;
  margin-bottom: 0px;
}

</style>
