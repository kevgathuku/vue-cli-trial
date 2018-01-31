<template>
  <div class="about">
    <BulmaTabs>
      <tab-panel name="Pictures" :selected="true">
        <p>Here's some pictures for you</p>
      </tab-panel>
      <tab-panel name="Music">
        <p>Here's some music for you</p>
      </tab-panel>
      <tab-panel name="Videos">
        <p>Here's some videos for you</p>
      </tab-panel>
      <tab-panel name="Documents">
        <p>Here's some documents for you</p>
      </tab-panel>
    </BulmaTabs>
  </div>
</template>

<script>
import BulmaTabs from "@/components/BulmaTabs.vue";
import TabPanel from "@/components/TabPanel.vue";

export default {
  components: {
    "tab-panel": TabPanel,
    BulmaTabs
  }
}
</script>
