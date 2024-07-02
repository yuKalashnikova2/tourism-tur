<script setup>
const props = defineProps({
    quantity: {
        type: Number,
        default: 1,
    },
    text: {
        type: String,
        default: 'Text here',
    },
})
</script>

<template>
    <div class="advantages__card">
        <div class="advantages__card__quantity">{{ quantity }}</div>
        <div class="advantages__card__text">{{ text }}</div>
    </div>
</template>

<style lang="scss" scoped>
.advantages__card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 16px;
    max-width: 408px;
    &__quantity {
        font-size: 5rem;
        line-height: 1;
        color: $green;
        font-weight: bold;
    }
    &__text {
        font-size: 2.5rem;
        line-height: 1.5;
        font-weight: bold;
        word-break: break-word;
        word-wrap: break-word;
        text-align: center;
    }
}
</style>
