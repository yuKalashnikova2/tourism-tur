<script setup>
    const props = defineProps({
        subtitle: {
            type: String,
            default: 'Подзаголовок раздела'
        }
    })
</script>
<template>
    <h4 class="subtitle"><strong>{{ subtitle }}</strong></h4>
</template>

<style lang="scss" scoped>
    .subtitle {
        font-size: 4rem;
        line-height: 1;
        font-weight: 400;
        text-align: center;
        color: $black;
    }
</style>