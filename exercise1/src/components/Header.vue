<template>
    <div class="header">
        <HeaderMsg
            welcomeText="Hello Developer!"
            headerText="Lorem ipsum dolor sit amet consectetur adipisicing elit."
        />
    </div>
</template>

<script>
import HeaderMsg from "./HeaderMsg.vue"
export default {
    name: 'Header',
    components: {
        HeaderMsg
    }
}
</script>

<style lang="scss" scoped>
.header{
    width: 100%;
    height: 400px;
    background-image: url("../assets/1920x650.png");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    @media (max-width: 1000px) {
        background-image: url("../assets/600x600.png");
    }

}

</style>