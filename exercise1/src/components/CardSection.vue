<template>
    <div class="card-wrapper">
        <div class="d-flex flex-row justify-content-center card-container">
        <Card 
        cardText="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
        />
        <Card 
        cardText="Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
        />
        <Card 
        cardText="Dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure  omnis usantium doloremquaperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo."
        />
    </div>
    </div>
    
</template>

<script>
import Card from './Card.vue';
    export default {
        name: 'CardSection',
    components: {
        Card
    }
    }
</script>

<style lang="scss" scoped>
.card-container{
    margin:0;
}
.card-wrapper{
    margin-top:10px;
}
</style>