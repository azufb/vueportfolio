<template>
  <div id="app">
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
    <div>
      <Component :is="currentTab"></Component>
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
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

ul {
  display: flex;
  cursor: pointer;
}

ul li {
  list-style: none;
}
</style>
