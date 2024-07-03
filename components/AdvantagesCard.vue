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
    @media (max-width: 768px) {
        max-width: 100%;
    }
    &__quantity {
        font-size: 5rem;
        line-height: 1;
        color: $green;
        font-weight: bold;
        @media (max-width: 768px) {
            max-width: 100%;
            font-size: calc(2.4rem + (5 - 2.4) * ((100vw - 20rem) / (48 - 20)));
            line-height: calc(
                1.1 * (2.4rem + (5 - 2.4) * ((100vw - 20rem) / (48 - 20)))
            );
        }
    }

    &__text {
        font-size: 2.5rem;
        line-height: 1.5;
        font-weight: bold;
        word-break: break-word;
        word-wrap: break-word;
        text-align: center;
        @media (min-width: 992px) and (max-width: 1400px) {
            font-size: calc(
                1.525rem + (2.5 - 1.525) * ((100vw - 62rem) / (87 - 62))
            );
            line-height: calc(
                1.4 * (1.525rem + (2.5 - 1.525) * ((100vw - 62rem) / (87 - 62)))
            );
        }
        @media (max-width: 768px) {
            font-size: calc(
                1.525rem + (2.5 - 1.525) * ((100vw - 20rem) / (48 - 20))
            );
            line-height: calc(
                1.4 * (1.525rem + (2.5 - 1.525) * ((100vw - 20rem) / (48 - 20)))
            );
        }
    }
}
</style>
