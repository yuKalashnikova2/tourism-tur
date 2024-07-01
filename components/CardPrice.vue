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
            <span>
                <strong>${{ price }}</strong
                >/операция</span
            >
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
    &-title {
        background-color: $green;
        color: $white;
        display: flex;
        flex-direction: column;

        & h5 {
            font-size: 2.5rem;
            line-height: 1.5;
            & strong {
                font-weight: bold;
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
    padding: 36px;
}
</style>
