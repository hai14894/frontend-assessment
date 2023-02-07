<template>
    <div>
        <img src="../assets/400x300.png" />
        <div>
            {{ cardText }}
        </div>
       <CardButton 
        msg="READ MORE"/>
    </div>
</template>

<script>
import CardButton from './CardButton.vue';
export default {
  components: { CardButton },
  props: {
    cardText: {
                type: String,
                required: true
            },
  }
    }
</script>

<style lang="scss" scoped>

</style>