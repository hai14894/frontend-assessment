<template>
    <div>
    <div 
      v-if="isDesktopSize"
      class="tabs">
      <button 
        v-for="(jsonData, index) in jsonData" 
        :key="index" @click="selectedTab = index" 
        :class="{ active: selectedTab === index }">
          {{jsonData.title}}
      </button>
    </div>
    <div class="tab-content">
      <div v-html="jsonData[selectedTab].content"></div>
    </div>
  </div>
</template>

<script>
import data from '../../static/data.json'
    export default {
      data() {
        return {
          isDesktopSize: window.innerWidth > 1000,
          selectedTab: 0,
          jsonData: data
    }
  }
    }
</script>

<style lang="scss" scoped>

</style>