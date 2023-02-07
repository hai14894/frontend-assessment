<template>
    <div v-if="isDesktopSize">
    <div class="tabs">
      <button 
        v-for="(jsonData, index) in jsonData" 
        :key="index" 
        @click="selectedTab = index" 
        :class="{ active: selectedTab === index }">
          {{jsonData.title}}
      </button>
    </div>
    <div class="tab-content">
      <div v-html="jsonData[selectedTab].content"></div>
    </div>
  </div>
  <div v-if="!isDesktopSize">
    <div
      class="accordion"
      v-for="(jsonData, index) in jsonData" 
      :key="index"
      >
      <button 
      @click="toggleAccordion(index)" 
      :class="{ active: activeSection === index }">
        {{ jsonData.title }}
      </button>
      <div v-if="activeSection === index">
        <div v-html="jsonData.content"></div>
      </div>
    </div>
  </div>
</template>

<script>
import data from '../../static/data.json'
    export default {
      data() {
        return {
          selectedTab: 0,
          activeSection: 0,
          jsonData: data
          }
        },
      methods: {
        toggleAccordion(index) {
          this.activeSection = this.activeSection === index ? null : index;
        }
      },
      computed: {
        isDesktopSize() {
          return window.innerWidth > 1000
        }
      },
    }
</script>

<style lang="scss" scoped>
.active {
  background-color: greenyellow;
}
</style>