<script setup>
const props = defineProps({
    packageName: {
        type: String,
        default: 'Стандарт',
    },
    price: {
        type: Number,
        default: 999,
    },
    text: {
        type: String,
        default: 'Text here',
    },
})
</script>

<template>
    <div class="card__price">
        <div class="card__price-title padding_36">
            <h5>
                <strong>{{ packageName }}</strong>
            </h5>
            <!-- <span>
                <strong>${{ price }}</strong
                >/операция</span
            > -->
        </div>
        <div class="card__price__text padding_36">
            <p>{{ text }}</p>
        </div>
        <div class="padding_36">
            <Button label="Выбрать" class="btn_width" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
.card__price {
    border-radius: 30px;
    background-color: $white;
    overflow: hidden;
    max-width: 339px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    @media (min-width: 1500px) {
        max-width: 100%;
    }
    @media (max-width: 1200px) {
        max-width: 100%;
    }
    &-title {
        background-color: $green;
        color: $white;
        display: flex;
        flex-direction: column;
        @media (min-width: 1500px) {
        height: 155px;
    }
        & h5 {
            font-size: 1.8rem;
            line-height: 1.5;
            @media (min-width: 1500px) {
                font-size: 2.5rem;
            }
            @media (max-width: 768px) {
                font-size: calc(
                    1.525rem + (2.5 - 1.525) * ((100vw - 20rem) / (48 - 20))
                );
                line-height: calc(
                    1.4 *
                        (
                            1.525rem + (2.5 - 1.525) *
                                ((100vw - 20rem) / (48 - 20))
                        )
                );
            }

            & strong {
                font-weight: bold;
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
                    1.4 *
                        (1.14rem + (1.4 - 1.14) * ((100vw - 62rem) / (87 - 62)))
                );
            }
            @media (max-width: 768px) {
                font-size: calc(
                    1.14rem + (1.4 - 1.14) * ((100vw - 20rem) / (48 - 20))
                );
                line-height: calc(
                    1.4 *
                        (1.14rem + (1.4 - 1.14) * ((100vw - 20rem) / (48 - 20)))
                );
            }
        }
    }
    &__text {
        text-align: left;
        font-size: 1.4rem;
        line-height: 1.3;
        margin-top: 16px;
        flex-grow: 1;
    }
}
.btn_width {
    width: 100%;
    margin-top: auto;
}
.padding_36 {
    padding: 24px;
}
</style>
