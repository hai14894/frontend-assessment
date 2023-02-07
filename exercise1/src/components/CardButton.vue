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
    font-size: 14px;
    color: black;
    background-color: white;
    display: inline-block;
    max-width: max-content;
    border-radius: 20px;
    margin-top: 10px; 
    padding: 4px 12px;
    border: 2px solid black;
}
</style>