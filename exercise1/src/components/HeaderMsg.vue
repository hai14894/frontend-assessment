<template>
    <div>
        <div class="message message--bold">{{ welcomeText }}</div>
        <div class="message">{{ headerText }}</div>
    </div>
</template>

<script>
    export default {
        props: {
            welcomeText: {
                type: String,
                required: true
            },
            headerText: {
                type: String,
                required: true
            },
        }
    }
</script>

<style lang="scss" scoped>
.message {
    color: white;
    &--bold {
        font-weight: bold;
        font-size: 3rem;
    }
}
</style>