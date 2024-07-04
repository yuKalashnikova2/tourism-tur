import { SocialCard } from '#build/components';
<template>
    <div class="footer">
        <ul class="footer__menu">
            <li><NuxtLink to="#main">Главная</NuxtLink></li>
            <li><NuxtLink to="#price">Услуги</NuxtLink></li>
            <li><NuxtLink to="#contacts">Контакты</NuxtLink></li>
            <li><NuxtLink to="#team">О нас</NuxtLink></li>
        </ul>
        <div class="footer__social">
            <SocialCard iconImage="soc-b-1.svg" link="https://instagram.com/zdorovekrasotaiturizm" />
            <SocialCard iconImage="soc-b-5.svg" link="https://vk.com/zdorovekrasotaiturizm" />
            <SocialCard iconImage="soc-b-6.svg" link="https://t.me/zdorovekrasotaiturizm" />
        </div>
        <div class="footer__copyright">
            <span>© 2024 Оздоровительный Туризм</span>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 32px;
    background-color: $black;
    color: $white;
    &__menu {
        display: flex;
        gap: 30px;
        list-style: none;
        padding: 0;
        margin: 0;
        @media (max-width: 768px) {
            flex-wrap: wrap;
        }
        & li {
            font-size: 2.5rem;
            @media (min-width: 992px) and (max-width: 1400px) {
                font-size: calc(
                    1.525rem + (2.5 - 1.525) * ((100vw - 62rem) / (87 - 62))
                );
                line-height: calc(
                    1.4 *
                        (
                            1.525rem + (2.5 - 1.525) *
                                ((100vw - 62rem) / (87 - 62))
                        )
                );
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
        }
    }
    & a {
        color: $white-secondary;
        line-height: 1;
        word-break: break-word;
        word-wrap: break-word;
        font-weight: 400;
        transition: text-decoration 0.3s linear;
        &:hover {
            text-decoration: underline;
        }
    }
    &__copyright {
        font-size: 1.4rem;
        line-height: 1.3;
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
    &__social {
        display: flex;
        text-align: center;
        gap: 16px;
        flex-wrap: wrap;
    }
}
</style>
