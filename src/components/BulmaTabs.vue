<template>
    <div class="container">
        <div class="tabs is-centered">
            <ul>
                <li v-for="tab in tabs" :key="tab.name" :class="{'is-active': tab.isActive}">
                    <a :href="tab.href" @click="selectTab(tab)">
                        {{tab.name}}
                    </a>
                </li>
            </ul>
        </div>
        <div class="tabs-details">
            <slot></slot>
        </div>
    </div>
</template>

<script>
import TabPanel from "@/components/TabPanel.vue";

export default {
  name: "BulmaTabs",
  components: {
    "tab-panel": TabPanel
  },

  data() {
    return {
      tabs: []
    };
  },

  created() {
    this.tabs = this.$children;
  },

  methods: {
    selectTab(selectedTab) {
        this.tabs.forEach(tab => {
            tab.isActive = (tab.name == selectedTab.name);
        })
    }

  }
};
</script>
