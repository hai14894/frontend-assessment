<template>
    <div class="container-md d-flex flex-column justify-content-center container">
        <img src="../assets/400x300.png" class="img"/>
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
.container{
    width: 20rem;
    border-radius: 10px;
    border: 2px solid rgb(157, 154, 154);
}
.img{
}
</style>