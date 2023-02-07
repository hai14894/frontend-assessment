<template>
    <div class="d-flex flex-row mt-5">
        <Card 
        cardText="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua."
        />
        <Card 
        cardText="Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."
        />
        <Card 
        cardText="ed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo."
        />
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

</style>