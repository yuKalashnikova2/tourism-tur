<script setup>
const props = defineProps({
    imageName: {
        type: String,
        default: '1.jpeg',
    },
    subtitle: {
        type: String,
        default: 'Подзаголовок раздела',
    },
    date: {
        type: String,
        default: '12.12.2024',
    },
    text: {
        type: String,
        default: 'Text here',
    },
})
const backgroundStyles = (img) => {
    return {
        'background-image': `url('/last_news/${img}')`,
        'background-size': 'cover',
    }
}
</script>
<template>
    <div class="last__news">
        <div class="last__news__img" :style="backgroundStyles(imageName)"></div>
        <h5 class="last__news__subtitle">{{ subtitle }}</h5>
        <span class="last__news__text">{{ date }}</span>
        <span class="last__news__text">{{ text }}</span>

        <Button label="Узнать" />
    </div>
</template>

<style lang="scss" scoped>
.last__news {
    max-width: 267px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    @media(max-width: 992px) {
        max-width: 100%;
    }
    &__img {
        border-radius: 30px;
        overflow: hidden;
        width: 267px;
        height: 400px;
        background-position: center;
        background-repeat: no-repeat;
        @media(max-width: 992px) {
        width: 100%;
    }
    }
    &__subtitle {
        font-size: 2.5rem;
        line-height: 1.5;
        margin-bottom: 8px;
    }
    &__text {
        text-align: left;
        font-size: 1.4rem;
        line-height: 1.3;
        margin-bottom: 16px;
    }
}
</style>
