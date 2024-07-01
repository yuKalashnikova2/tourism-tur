<template>
    <header class="header header_container">
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
        <Button label="Подключиться" />
    </header>
</template>

<style lang="scss">
.header {
    position: fixed;
    z-index: 3;
    display: flex;
    align-items: center;
    background-color: rgba(255, 255, 255, 0.6);
    justify-content: space-between;
    padding: 10px;
    width: 100%;
    border-radius: 50px;
    &_container {
        top: 16px;
   
        // margin: 16px 99px 0 99px;
    }
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
}
</style>
