<template>
    <div class="main">
        <div class="image-container">
            <img src="/banner.jpeg" alt="Фоновая картинка" />
            <div class="text-overlay">
                <div>
                    <h1 class="main__title">Турция Здоровье</h1>
                    <p>
                        Отправьтесь в удивительное путешествие от оздоровления в
                        России до красоты в Турции с Эйюпом Ахметом Уйгуном!
                    </p>

                    <Button
                        label="Узнать больше"
                        backgroundColor
                        class="button_width"
                    />
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.main {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    &__title {
        color: $yellow;
        font-size: 4rem;
    }
}

.image-container {
    position: relative;
    width: 100%;
    //   height: 100vh;
    overflow: hidden;
}

.image-container img {
    width: 100%;
    height: auto;
    object-fit: cover;
}

.text-overlay {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    text-align: center;
    color: $white;
    z-index: 1;
    padding: 20px;
    background-color: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;

    & div {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 32px;
        & p {
            font-size: 1.4rem;
            line-height: 1.3;
        }
    }
}
.button_width {
    max-width: 232px;
}
</style>
