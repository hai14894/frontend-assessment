<template>
    <button class="button">
        {{ msg }}
    </button>
</template>

<script>
    export default {
        props: {
            msg: {
                type: String,
                required: true
            }
        }
    }
</script>

<style lang="scss" scoped>
.button{
    font-weight: bold;
    
}
</style>