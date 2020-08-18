<template>
    <div id='myworks'>
        <ul class='mWorks'>
            <li
            :class="{ active: currentTab === 'ListTab' }"
            @click="currentTab = 'ListTab'"
            >一覧</li>
            <li
            :class="{ active: currentTab === 'DetailTab' }"
            @click="currentTab = 'DetailTab'"
            >詳細</li>
        </ul>
        <div>
            <component :is="currentTab"></component>
        </div>
    </div>
</template>

<script>
import ListTab from './ListTab.vue';
import DetailTab from './DetailTab.vue';

export default {
    name: 'myworks',
    data() {
    return {
      currentTab: 'ListTab',
    };
  },
  components: {
    ListTab,
    DetailTab
  }
    
}
</script>