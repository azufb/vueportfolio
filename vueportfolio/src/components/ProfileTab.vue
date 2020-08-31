<template>
    <div id='prof'>
        <ul class='profs'>
            <li
            :class="{ active: currentTab === 'DataTab' }"
            @click="currentTab = 'DataTab'"
            >自己紹介</li>
            <li
            :class="{ active: currentTab === 'CertificatesTab' }"
            @click="currentTab = 'CertificatesTab'"
            >資格・スキル</li>
        </ul>
        <div>
            <component :is="currentTab"></component>
        </div>
    </div>
</template>

<script>
import DataTab from './DataTab.vue';
import CertificatesTab from './Certificates.vue';

export default {
    name: 'prof',
    // 表示するタブの初期値
    data() {
    return {
      currentTab: 'DataTab',
    };
  },
  components: {
    DataTab,
    CertificatesTab
  }
}
</script>

<style>
.currentTab {
  border-bottom: 1px solid #d85782;
}
</style>