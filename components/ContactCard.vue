<script setup>
const props = defineProps({
    title: {
        type: String,
        default: 'Телефон',
    },
    descry: {
        type: String,
        default: '+7 999 999 56 45',
    },
})
</script>
<template>
    <div class="contact">
        <h6>{{ title }}</h6>
        <span>{{ descry }}</span>
    </div>
</template>

<style lang="scss" scoped>
.contact {
    display: flex;
    flex-direction: column;
    gap: 16px;
    background-color: $white;
    border-radius: 30px;
    padding: 2.25rem;
    & h6 {
        font-size: 2.5rem;
        line-height: 1.5;
        font-weight: bold;
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
    & span {
        font-size: 1.4rem;
        line-height: 1.3;
        @media (min-width: 992px) and (max-width: 1400px) {
            font-size: calc(
                1.14rem + (1.4 - 1.14) * ((100vw - 62rem) / (87 - 62))
            );
            line-height: calc(
                1.4 * (1.14rem + (1.4 - 1.14) * ((100vw - 62rem) / (87 - 62)))
            );
        }
        @media (max-width: 768px) {
            font-size: calc(
                1.14rem + (1.4 - 1.14) * ((100vw - 20rem) / (48 - 20))
            );
            line-height: calc(
                1.4 * (1.14rem + (1.4 - 1.14) * ((100vw - 20rem) / (48 - 20)))
            );
        }
    }
}
</style>
