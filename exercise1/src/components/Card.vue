<template>
    <div class="card__container mb-3">
        <img src="../assets/400x300.png" class="card__img m-3"/>
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
.card__container{
    display:flex;
    flex-direction: column;
    width: 20rem;
    border-radius: 10px;
    border: 2px solid rgb(157, 154, 154);
    margin-left: 10px;
    margin-right:10px;
}
.card__text{
    height: 100%;
}
.card__img{
    border-radius: 10px;
    
}
.card__button{
    margin-bottom: 10px;
}
</style>