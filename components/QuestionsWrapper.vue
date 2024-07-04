<script setup>
import { ref } from 'vue'
const questions = ref([
    {
        id: 1,
        title: 'Этапы организации',
        info: 'Доверьте свое здоровье профессионалам - наши клиники проведут процедуры и лечение на высочайшем уровне',
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
        title: 'Процедуры и Лечение',
        info: 'Доверьте свое здоровье профессионалам – наши клиники проведут операцию и процедуры на высочайшем уровне.',
    },
    {
        id: 5,
        title: 'Сопровождение и гарантия',
        info: 'Доверьте свое здоровье профессионалам - наши клиники проведут процедуры и лечение на высочайшем уровне.',
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
