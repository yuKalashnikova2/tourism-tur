
<template>
    <div class="main" id="main">
        <div class="image-container">
            <img src="/banner.jpeg" alt="Фоновая картинка" />
            <div class="text-overlay">
                <div>
                    <h1 class="main__title">Процедуры лечения в Турции</h1>
                    <p class="main__description">
                        Отправьтесь в удивительное путешествие от оздоровления в
                        России до красоты в Турции с Эйюпом Ахметом Уйгуном!
                    </p>
                    <div class="m-10">
                        <NuxtLink to="#contacts">
                            <Button label="Узнать больше" backgroundColor />
                        </NuxtLink>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <section class="section_one container">
        <Subtitle subtitle="Планы Лечения" />
        <CardPriceWrapper />
    </section>
    <section class="section_two container">
        <Subtitle subtitle="Фотографии" />
        <CardLastNewsWrapper />
    </section>
    <section class="section_three container">
        <Subtitle subtitle="Оздоровительный туризм: Россия - Турция" />
        <VideoComponent class="container-100" />
    </section>
    <section class="section_four container">
        <div class="section_four_styles container-100">
            <Subtitle subtitle="Откройте новый мир здоровья!" />
            <span
                >Путешествие в Турцию для операций и процедур станет вашим
                лучшим решением. Доверьте свое здоровье профессионалам и
                наслаждайтесь результатом!</span
            >
            <div class="flex">
                <NuxtLink class="w-100" to="#contacts">
                    <Button class="w-100" label="Узнать больше" />
                </NuxtLink>
            </div>
        </div>
    </section>
    <!-- <section class="section_five container">
        <Subtitle subtitle="Наша команда" />
        <CardTeamWrapper />
    </section> -->
    <section>
        <marquee
            scrollamount="12"
            loop="-1"
            scrolldelay="1"
            class="scrolling-text"
            >Бесплатная консультация * Бронирование и проживание * Отпуск и
            анализы * Операция и процедуры * Сопровождение и гарантия *
        </marquee>
    </section>

    <!-- <section class="section_seven container">
        <Subtitle subtitle="Наши партнеры" />
        <CardPartnersWrapper />
    </section> -->

    <!-- <section class="section_eight">
        <div class="section_eight__banner"></div>
    </section> -->
    <section class="section_nine container">
        <BestConsult name="Эйюп Ахмет Уйгун" avatar="photo-1.jpg" />
    </section>
    <section class="section_ten container">
        <div class="container-100 width-800">
            <Subtitle subtitle="Идеальные курортные города" />
            <h5 class="section_ten__cities__title">
                Отправляйтесь в Турцию для незабываемого отдыха и лечения
            </h5>
        </div>
        <CardCitiesWrapper />
    </section>
    <!-- <section class="section_eleven container container-100">
        <AdvantagesWrapper />
    </section> -->
    <section class="section_twelve container">
        <Subtitle subtitle="Этапы организации" />
        <div class="container-100">
            <QuestionsWrapper />
        </div>
    </section>
    <section class="section_thirteen container">
        <Subtitle subtitle="Подписывайтесь на нас" />
        <SocialWrapper />
    </section>
    <section class="section_fourteen container">
        <Subtitle subtitle="Наши контакты" />
        <ContactsWrapper />
    </section>
    <section class="section_fifteen container">
        <Footer />
    </section>
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
        line-height: 1;
        @media (min-width: 1401px) {
            font-size: 7rem;
        }
        @media (max-width: 768px) {
            font-size: calc(2.4rem + (5 - 2.4) * ((100vw - 20rem) / (48 - 20)));
            line-height: calc(
                1.1 * (2.4rem + (5 - 2.4) * ((100vw - 20rem) / (48 - 20)))
            );
        }
    }
    &__description {
        font-size: 1.4rem;
        line-height: 1.3;
        @media (min-width: 1401px) {
            font-size: 3rem;
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
    @media(max-width:768px) {
        height: 500px;
    }
}
.container {
    padding-top: 5rem;
    padding-bottom: 4rem;
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
    @media (max-width: 768px) {
        padding-top: 2rem;
        padding-bottom: 2rem;
    }

    & div {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 32px;
        @media (max-width: 768px) {
            gap: 4px;
        }
    }
}
.button_width {
    max-width: 232px;
}

.section {
    &_one {
        background-color: $background-green;
    }
    &_four {
        background-color: $background-green;
        text-align: center;
        &_styles {
            background-color: $yellow;
            border-radius: 30px;
            padding: 64px;
            display: flex;
            flex-direction: column;
            gap: 40px;
            margin-left: 16px;
            margin-right: 16px;
            @media (min-width: 1500px) {
                padding: 88px;
            }
            & span {
                font-size: 1.4rem;
                line-height: 1.3;
                display: inline-block;
            }
            & a {
                width: 100%;
                display: block;
                @media (min-width: 1500px) {
                    width: 140%;
                }
            }
        }
    }
    &_eight {
        &__banner {
            background-image: url('/banner-2.jpeg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            width: 100%;
            height: 1000px;
        }
    }
    &_ten {
        background-color: $background-green;
        &__cities__title {
            margin-top: 2rem !important;
            text-align: center;
            word-break: break-word;
            word-wrap: break-word;
            font-weight: 400;
            font-size: 1.4rem;
            line-height: 1.3;
            @media (min-width: 1500px) {
                font-size: 1.7rem;
            }
            @media (min-width: 992px) and (max-width: 1400px) {
                font-size: calc(
                    1.14rem + (1.4 - 1.14) * ((100vw - 62rem) / (87 - 62))
                );
                line-height: calc(
                    1.4 *
                        (1.14rem + (1.4 - 1.14) * ((100vw - 62rem) / (87 - 62)))
                );
            }
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

    &_twelve {
        background-color: $background-green;
    }
    &_thirteen {
        background-color: $white;
    }
    &_fourteen {
        background-color: $background-green;
    }
    &_fifteen {
        background-color: $black;
    }
}
.mb-48 {
    margin-bottom: 3rem !important;
}
.container-100 {
    margin-right: 100px;
    margin-left: 100px;
    @media (max-width: 768px) {
        margin-right: 8px;
        margin-left: 8px;
    }
}
.scrolling-text {
    font-size: calc(2.4rem + (5 - 2.4) * ((100vw - 62rem) / (87 - 62)));
    line-height: 1.3;
    text-align: center;
    white-space: nowrap;
    font-weight: bold;
}
.width-800 {
    max-width: 800px;
    margin: 0 auto;
    @media (min-width: 1500px) {
        max-width: 100%;
    }
}

.w-150 {
    width: 150px;
}
.m-10 {
    margin: 10px;
}
.flex {
    margin: 0 auto;
}
</style>
