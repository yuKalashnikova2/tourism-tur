<script setup>
const props = defineProps({
    avatar: {
        type: String,
        default: 'photo-1.jpg',
    },
    name: {
        type: String,
        default: 'Эйюп Ахмет Уйгун',
    },
})
</script>

<template>
    <div class="consult" id="team">
        <div>
            <p class="consult__title">Лучший консультант в оздоровительном</p>
            <p class="consult__title">туризме!</p>
        </div>

        <div class="consult__image">
            <img :src="'/team/' + avatar" alt="" />
        </div>
        <span class="consult__name">{{ name }}</span>
    </div>
</template>

<style lang="scss" scoped>
.consult {
    display: flex;
    flex-direction: column;
    gap: 16px;
    align-items: center;
    justify-content: center;
    &__title {
        font-size: 2.5rem;
        line-height: 1.5;
        word-break: break-word;
        word-wrap: break-word;
        font-weight: 400;
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
    &__image {
        width: 120px;
        height: 120px;
        border-radius: 50%;
        overflow: hidden;
        @media (min-width: 1500px) {
            width: 180px;
            height: 180px;
        }
        & img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
    }
    &__name {
        font-size: 1.4rem;
        line-height: 1.3;
        font-weight: bold;
        @media (min-width: 1500px) {
            font-size: 2rem;
        }
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
