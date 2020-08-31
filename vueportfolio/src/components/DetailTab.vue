<template>
    <div id='detail'>
        <h2>詳細</h2>
        <p>
          今まで制作した成果物の中から、いくつかピックアップしてご紹介!!<br>
          Go to Appボタンを押すとアプリを実際に使用してみることが可能です!
        </p>
        <ul class='details'>
            <li
            :class="{ active: currentTab === 'EquipmentManagerTab' }"
            @click="currentTab = 'EquipmentManagerTab'"
            >Equipment Manager</li>
            <li
            :class="{ active: currentTab === 'ToDoManagerTab' }"
            @click="currentTab = 'ToDoManagerTab'"
            >ToDo Manager</li>
            <li
            :class="{ active: currentTab === 'MemoAppTab' }"
            @click="currentTab = 'MemoAppTab'"
            >タグメモ！</li>
            <li
            :class="{ active: currentTab === 'TaskKanriTab' }"
            @click="currentTab = 'TaskKanriTab'"
            >タスク管理アプリ</li>
            <li
            :class="{ active: currentTab === 'HomerunTab' }"
            @click="currentTab = 'HomerunTab'"
            >ほめるん</li>
        </ul>
        <div>
            <component :is="currentTab"></component>
        </div>
    </div>
</template>

<script>
import EquipmentManagerTab from './worksdetail/EquipmentManagerTab';
import ToDoManagerTab from './worksdetail/ToDoManagerTab';
import MemoAppTab from './worksdetail/MemoAppTab.vue';
import TaskKanriTab from './worksdetail/TaskKanriTab.vue';
import HomerunTab from './worksdetail/HomerunTab.vue';
// import VueToDoAppTab from './worksdetail/VueToDoAppTab.vue';

export default {
    name: 'detail',
    data() {
    return {
      currentTab: 'EquipmentManagerTab',
    };
  },
  components: {
    EquipmentManagerTab,
    ToDoManagerTab,
    MemoAppTab,
    TaskKanriTab,
    HomerunTab,
    // VueToDoAppTab
  }
}
</script>