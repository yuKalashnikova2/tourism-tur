<script setup>
const props = defineProps({
    subtitle: {
        type: String,
        default: 'Подзаголовок раздела',
    },
})
</script>
<template>
    <h4 class="subtitle">
        <strong>{{ subtitle }}</strong>
    </h4>
</template>

<style lang="scss" scoped>
.subtitle {
    font-size: 4rem;
    line-height: 1;
    font-weight: 400;
    text-align: center;
    color: $black;
    @media (max-width: 768px) {
        font-size: calc(2.05rem + (4 - 2.05) * ((100vw - 20rem) / (48 - 20)));
        line-height: calc(
            1.3 * (2.05rem + (4 - 2.05) * ((100vw - 20rem) / (48 - 20)))
        );
    }
}
</style>
