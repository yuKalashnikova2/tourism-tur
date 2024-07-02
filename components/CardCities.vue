<script setup>
const props = defineProps({
    cityName: {
        type: String,
        default: 'Город',
    },
    image: {
        type: String,
        default: 'city-1.jpeg',
    },
    info: {
        type: String,
        default: 'Информация о городе',
    },
})
</script>
<template>
    <div class="card__cities">
        <div class="card__cities__img">
            <img :src="'/cities/' + image" alt="" />
        </div>
        <div class="card__cities__info">
            <h5>{{ cityName }}</h5>
            <span>{{ info }}</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.card__cities {
    border-radius: 2rem !important;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: $white;
    padding: 36px;
    &__img {
        border-radius: 50px;
        overflow: hidden;
        width: 80px;
        height: 80px;
        margin-bottom: 1rem !important;
        & img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    &__info {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        color: $black;
        & h5 {
            font-size: 2.5rem;
            line-height: 1.5;

            font-weight: bold;
            display: block;
            text-align: center;
        }
        & span {
            text-align: center;
            font-size: 1.4rem;
            line-height: 1.3;
            word-break: break-word;
            word-wrap: break-word;
            font-weight: 400;
        }
    }
}
</style>
