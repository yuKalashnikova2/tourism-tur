<script setup>
const props = defineProps({
    image: {
        type: String,
        default: 'part-1.jpeg',
    },
})
</script>

<template>
    <div class="card__partners">
        <img :src="`/partners/${image}`" alt="" />
    </div>
</template>

<style lang="scss" scoped>
.card__partners {
    border-radius: 30px;
    overflow: hidden;
    max-width: 187px;
    height: auto;

    & img {
        width: 100%;
        height: 100%;
        filter: grayscale(100%);
    }
}
</style>
