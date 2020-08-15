<template>
    <div id="myworks">
        <ul>
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
            <Component :is="currentTab"></Component>
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