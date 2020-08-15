<template>
    <div id="detail">
        <h2>詳細</h2>
        <ul>
            <li
            :class="{ active: currentTab === 'MemoAppTab' }"
            @click="currentTab = 'MemoAppTab'"
            >メモアプリ</li>
            <li
            :class="{ active: currentTab === 'TaskKanriTab' }"
            @click="currentTab = 'TaskKanriTab'"
            >タスク管理アプリ</li>
            <li
            :class="{ active: currentTab === 'HomerunTab' }"
            @click="currentTab = 'HomerunTab'"
            >ほめるん</li>
            <li
            :class="{ active: currentTab === 'VueToDoAppTab' }"
            @click="currentTab = 'VueToDoAppTab'"
            >ToDoアプリ</li>
        </ul>
        <div>
            <Component :is="currentTab"></Component>
        </div>
    </div>
</template>

<script>
import MemoAppTab from './MemoAppTab.vue';
import TaskKanriTab from './TaskKanriTab.vue';
import HomerunTab from './HomerunTab.vue';
import VueToDoAppTab from './VueToDoAppTab.vue';

export default {
    name: 'detail',
    data() {
    return {
      currentTab: 'MemoAppTab',
    };
  },
  components: {
    MemoAppTab,
    TaskKanriTab,
    HomerunTab,
    VueToDoAppTab
  }
}
</script>