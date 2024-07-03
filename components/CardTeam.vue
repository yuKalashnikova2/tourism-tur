<script setup>
const props = defineProps({
    imageName: {
        type: String,
        default: '1.jpg',
    },
    personName: {
        type: String,
        default: 'Name',
    },
    personInfo: {
        type: String,
        default: 'Info',
    },
})

const backgroundStylesTeam = (img) => {
    return {
        'background-image': `url('/team/${img}')`,
        'background-size': 'cover',
    }
}
</script>

<template>
    <div class="card__team">
        <div
            class="card__team__img"
            :style="backgroundStylesTeam(imageName)"
        ></div>
        <h5>{{ personName }}</h5>
        <span>{{ personInfo }}</span>
    </div>
</template>

<style lang="scss" scoped>
.card__team {
    border-radius: 12px;
    width: 100%;
    display: flex;
    flex-direction: column;

    &__img {
        border-radius: 30px;
        overflow: hidden;
        width: 267px;
        height: 400px;

        background-position: center;

        background-repeat: no-repeat;
        margin-bottom: 16px;
        @media (max-width: 768px) {
            width: 100%;
        }
    }
    & h5 {
        font-weight: 400;
        text-align: center;
        font-size: 2.5rem;
        line-height: 1.5;
        margin-bottom: 8px;
        font-weight: bold;
    }
    & span {
        font-size: 1.4rem;
        line-height: 1.3;
        line-height: 1.2;
        color: $black;
        text-align: center;
        font-weight: 400;
    }
}
</style>
