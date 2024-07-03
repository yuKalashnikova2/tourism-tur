<script setup>
import { ref } from 'vue'

const list = ref(['Услуги', 'Фотографии', 'О нас', 'Контакты'])

const isVisible = ref(false)
</script>

<template>
    <header class="header header_container">
        <div class="header__logo">
            <div class="header__image">
                <img src="/logo.jpeg" alt="logo" />
            </div>
            <h2>Оздоровительный туризм в Турцию</h2>
        </div>
        <div class="burger__wrapper">
            <header class="burger__header">
                <div
                    class="burger__button"
                    :class="{ open: isVisible }"
                    @click="isVisible = !isVisible"
                >
                    <span></span>
                    <span></span>
                    <span></span>
                </div>
            </header>
        </div>

        <ul class="header__menu">
            <li class="header__menu-item">
                <NuxtLink to="#contacts">Услуги</NuxtLink>
            </li>
            <li class="header__menu-item">
                <NuxtLink to="#contacts">Фотографии</NuxtLink>
            </li>
            <li class="header__menu-item">
                <NuxtLink to="#contacts">О нас</NuxtLink>
            </li>
            <li class="header__menu-item">
                <NuxtLink to="#contacts">Контакты</NuxtLink>
            </li>
        </ul>
        <div class="d-none">
            <Button label="Подключиться" />
        </div>
        <Transition>
            <nav class="burger__nav" v-if="isVisible">
                <ul class="burger__list">
                    <li class="burger__item" v-for="lis in list">
                        <NuxtLink to="#contacts">{{ lis }}</NuxtLink>
                    </li>
                </ul>
            </nav>
        </Transition>
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
    border-radius: 50px;

    &_container {
        top: 16px;
        width: 100%;
    }
    & h2 {
        font-size: 1.2rem;
        @media (min-width: 992px) and (max-width: 1400px) {
            font-size: calc(
                1.07rem + (1.2 - 1.07) * ((100vw - 62rem) / (87 - 62))
            );
        }
        @media (max-width: 768px) {
            font-size: calc(
                1.07rem + (1.2 - 1.07) * ((100vw - 20rem) / (48 - 20))
            );
        }
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
        @media (max-width: 768px) {
            width: 60px;
            height: 40px;
        }
        & img {
            width: 100%;
        }
    }
    &__menu {
        display: flex;
        @media (max-width: 992px) {
            display: none;
        }
        &-item {
            font-size: 1.2rem;
            line-height: 1.5;
            font-weight: 400;
            padding: 16px;
            & a {
                color: $text-black;
            }
            &:hover {
                background-color: #f8f9fa;
                border-radius: 15px;
                cursor: pointer;
            }
        }
    }
}
.d-none {
    display: block;
    @media (max-width: 992px) {
        display: none;
    }
}

.burger {
    &__wrapper {
        overflow-y: hidden;
        border-radius: 8px;
        display: none;
        @media (max-width: 992px) {
            display: block;
        }
    }
    &__header {
        padding: 23px 34px;
        z-index: 10;
        overflow-y: hidden;
        position: relative;
    }
    &__nav {
        background-color: rgba(255, 255, 255, 0.6);
        position: absolute;
        top: 6rem;
        left: 1rem;
        right: 1rem;
        width: 98%;
        display: flex;
        justify-content: center;
        padding: 20px;
        height: auto;
        border-radius: 30px;
        z-index: 5;
        @media (min-width: 993px) {
            display: none;
        }
    }
    &__list {
        display: flex;
        list-style: none;
        flex-direction: column;
        width: 100%;
    }
    &__item {
        cursor: pointer;
        font-size: 1.2rem;
        line-height: 1.5;
        font-weight: 400;
        padding: 16px;
        & a {
            color: $text-black;
        }
        &:hover {
            background-color: #f8f9fa;
            border-radius: 15px;
            cursor: pointer;
        }
    }
    &__button {
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        z-index: 5;
        align-items: center;
        border: none;
        outline: none;
        width: 30px;
        height: 20px;
        cursor: pointer;
        span {
            display: block;
            position: absolute;
            background-color: $text-black;
            width: 30px;
            height: 2px;
            left: 5px;
            &:nth-child(1) {
                transform: translateY(10px);
                transition: background cubic-bezier(0.075, 0.82, 0.165, 1),
                    opacity 0.3s, transform 0.4s;
            }

            &:nth-child(3) {
                transform: translateY(-10px);
                transition: background cubic-bezier(0.075, 0.82, 0.165, 1),
                    opacity 0.3s, transform 0.4s;
            }
        }
    }
}
.open {
    & span {
        &:nth-child(1) {
            transform: translateY(0) rotate(45deg);
        }
        &:nth-child(2) {
            opacity: 0;
        }
        &:nth-child(3) {
            transform: translateY(0) rotate(-45deg);
        }
    }
}
.v-enter-active,
.v-leave-active {
    transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
    opacity: 0;
}
</style>
