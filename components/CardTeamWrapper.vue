<template>
    <div class="team" >
        <CardTeam imageName="photo-1.jpg" personName="Эйюп" 
        personInfo="Консультант по оздоровительному туризму" />
        <CardTeam imageName="photo-2.jpeg" personName="Айлин" 
        personInfo="Координатор по клиникам" />
        <CardTeam imageName="photo-3.jpeg" personName="Озан" 
        personInfo="Эксперт по процедурам" />
        <CardTeam imageName="photo-4.jpeg" personName="Джанан" 
        personInfo="Менеджер по лечению" />
    </div>
</template>

<style lang="scss" scoped>
    .team {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        gap: 32px;
        align-items: stretch;
        margin-top: 3rem !important;
        @media(max-width: 992px) {
            grid-template-columns: repeat(2, 1fr);
            gap: 0.5rem;    
        }
        @media(max-width: 768px) {
            grid-template-columns: repeat(1, 1fr);
            gap: 1rem;
        }
    }
</style>