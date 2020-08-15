<template>
  <div id="app">
    <div class="mainTitle">
      <h1>I am Azusa...</h1>
      <ul>
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
      <component :is="currentTab"></component>
    </div>
  </div>
</template>

<script>
import HomeTab from './components/HomeTab.vue';
import ProfileTab from './components/ProfileTab.vue';
import MyWorksTab from './components/MyWorksTab.vue';

export default {
  name: 'App',
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
body {
  margin: 0px;
  background-color: #c8c9c9;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: black;
  margin-top: 0px;
}

.mainTitle {
  margin-top: 0px;
  display: flex;
  background-color: #e6e6e6;
}

h1 {
  margin-top: 0px;
  font-family: 'Oswald', sans-serif;
}

ul {
  display: flex;
  cursor: pointer;
}

ul li {
  list-style: none;
  font-family: 'Oswald', sans-serif;
}

h2 {
    border-bottom: 3px solid #d85782;
}
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
</style>
