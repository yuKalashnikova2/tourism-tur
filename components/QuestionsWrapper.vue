<script setup>
import { ref } from 'vue'
const questions = ref([
    {
        id: 1,
        title: 'Бесплатная консультация',
        info: 'Получите бесплатную консультацию от эксперта по оздоровительному туризму прямо сейчас!',
    },
    {
        id: 2,
        title: 'Бронирование авиабилетов',
        info: 'Доверьте нам заботу о вашем комфорте – мы забронируем для вас авиабилеты и проживание в Турции.',
    },
    {
        id: 3,
        title: 'Отпуск и анализы',
        info: 'Наши клиники расположены в курортных городах, где вы сможете насладиться отдыхом и пройти все необходимые анализы.',
    },
    {
        id: 4,
        title: 'Операция и процедуры',
        info: 'Доверьте свое здоровье профессионалам – наши клиники проведут операцию и процедуры на высочайшем уровне.',
    },
    {
        id: 5,
        title: 'Сопровождение и гарантия',
        info: 'Мы будем рядом с вами на каждом этапе – от прибытия в Турцию до полного восстановления после операции.',
    },
])
</script>
<template>
    <section class="question__wrapper">
        <Question
            v-for="question in questions"
            :key="question.id"
            :title="question.title"
            :info="question.info"
        />
    </section>
</template>

<style scoped lang="scss">
.question__wrapper {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin-top: 3rem !important;
}
</style>
