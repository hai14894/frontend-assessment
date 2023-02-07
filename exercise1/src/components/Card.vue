<template>
    <div class="container-md d-flex flex-column container mb-3 ml-3 mr-3">
        <img src="../assets/400x300.png" class="card__img"/>
        <div class="card__text">
            {{ cardText }}
        </div>
        <div class="d-flex justify-content-center">
            <CardButton 
                msg="READ MORE"
                class="card__button"
                />
        </div>
       
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
.card__text{
    height: 100%;
}
.card__img{
    margin-top: 10px;
    margin-bottom: 10px;
    border-radius: 10px;
}
.card__button{
    margin-bottom: 10px;
}
</style>