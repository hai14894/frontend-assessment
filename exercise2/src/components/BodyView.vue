<template>
  <!--  Desktop/ Tab view -->
    <div v-if="isDesktopSize">
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
      <div v-html="jsonData[selectedTab].content"></div>
  </div>

   <!--  Mobile/ Accordion view-->
  <div v-if="!isDesktopSize">
    <div
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
      <Transition>
        <div v-if="activeSection === index">
          <div v-html="jsonData.content"></div>
        </div>
      </Transition>
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
          jsonData: data,
          screenWidth: 0
          }
        },
      mounted() {
        this.updateScreenWidth()
        window.addEventListener('resize', this.updateScreenWidth)
      },
      beforeUnmount() {
        window.removeEventListener('resize', this.updateScreenWidth)
      },
      methods: {
        toggleAccordion(index) {
          this.activeSection = this.activeSection === index ? null : index;
        },
        updateScreenWidth() {
          this.screenWidth = window.innerWidth
        }
      },
      computed: {
        isDesktopSize() {
          return this.screenWidth > 1000
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
.v-enter-active,
.v-leave-active {
  transition: opacity 0.3s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

</style>