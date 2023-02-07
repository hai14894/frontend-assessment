<template>
    <div v-if="isDesktopSize">
    <div class="tabs">
      <button 
        v-for="(jsonData, index) in jsonData" 
        :key="index" 
        @click="selectedTab = index" 
        :class="[
          'button',
          selectedTab === index ? 'button--active' : '' 
        ]">
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
      :class="[
          'button',
          activeSection === index ? 'button--active' : '' 
        ]">
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
.button {
  padding: 6px 14px;
  font-family: -apple-system, BlinkMacSystemFont, 'Roboto', sans-serif;
  border-radius: 6px;
  color: #948181;
  background: #f7f2f2;
  border: none;
  box-shadow: 0px 0.5px 1px rgba(0, 0, 0, 0.1);

  &--active{
    background-color: greenyellow;
  }
}
</style>