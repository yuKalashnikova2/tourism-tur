<template>
    <header class="header">
        <div class="header__logo">
            <div class="header__image">
                <img src="/logo.jpeg" alt="logo" />
            </div>
            <h2>Оздоровительный туризм в Турцию</h2>
        </div>

        <ul class="header__menu">
            <li class="header__menu-item">Услуги</li>
            <li class="header__menu-item">Фотографии</li>
            <li class="header__menu-item">О нас</li>
            <li class="header__menu-item">Контакты</li>
        </ul>

        <button class="header__btn">Подключиться</button>
    </header>
</template>

<style lang="scss">
.header {
    position: fixed;
    display: flex;
    align-items: center;
    background-color: rgba(255, 255, 255, 0.6);
    justify-content: space-between;
    padding: 10px;
    width: 100%;
    border-radius: 50px;
    & h2 {
        font-size: 20px;
    }
    &__logo {
        display: flex;
        align-items: center;
        gap: 16px;
    }
    &__image {
        width: 103px;
        height: 68px;
        border-radius: 50px;
        overflow: hidden;
        & img {
            width: 100%;
        }
    }
    &__menu {
        display: flex;
        &-item {
            font-size: 1rem;
            font-weight: 400;
            padding: 16px;
            &:hover {
                background-color: #f8f9fa;
                border-radius: 15px;
                cursor: pointer;
            }
        }
    }
    &__btn {
        background-color: $green;
        border-radius: 50px;
        font-weight: 600;
        margin: 0.6rem 0.6rem;
        padding: 20px;
        white-space: normal;
        transition: all 0.2s ease-in-out;
        display: inline-flex;
        align-items: center;
        justify-content: center;
        word-break: break-word;
        color: $white;
        font-size: 16px;
        display: flex;
        align-items: center;
        justify-content: center;
        &:hover {
            opacity: .6;
            cursor: pointer;
        }
    }
}
</style>
