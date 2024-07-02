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

    <section class="section_one container">
        <Subtitle subtitle="Планы Лечения" />
        <CardPriceWrapper />
    </section>
    <section class="section_two container">
        <Subtitle subtitle="Последние новости" />
        <CardLastNewsWrapper />
    </section>
    <section class="section_three container">
        <Subtitle subtitle="Медицинский туризм: Россия - Турция" />
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
            <Button label="Узнать больше" />
        </div>
    </section>
    <section class="section_five container">
        <Subtitle subtitle="Наша команда" />
        <CardTeamWrapper />
    </section>
    <section>
        <marquee
            scrollamount="12"
            loop="-1"
            scrolldelay="1"
            class="scrolling-text"
            >Бесплатная консультация * Бронирование и проживание * Отпуск и
            анализы * Операция и процедуры * Сопровождение и гарантия * Фото до
            и после *
        </marquee>
    </section>

    <section class="section_seven container">
        <Subtitle subtitle="Наши партнеры" />
        <CardPartnersWrapper />
    </section>

    <section class="section_eight">
        <div class="section_eight__banner"></div>
    </section>
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
    <section class="section_eleven container container-100">
        <AdvantagesWrapper />
    </section>
    <section class="section_twelve container">
        <Subtitle subtitle="Ответы на вопросы" />
        <div class="container-100">
            <QuestionsWrapper />
        </div>
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
            & span {
                font-size: 1.4rem;
                line-height: 1.3;
                display: inline-block;
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
            font-size: calc(
                1.14rem + (1.4 - 1.14) * ((100vw - 62rem) / (87 - 62))
            );
            line-height: calc(
                1.4 * (1.14rem + (1.4 - 1.14) * ((100vw - 62rem) / (87 - 62)))
            );
        }
    }
    &_twelve {
        background-color: $background-green;
    }
}
.mb-48 {
    margin-bottom: 3rem !important;
}
.container-100 {
    margin-right: 100px;
    margin-left: 100px;
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
}
</style>
