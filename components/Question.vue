<script setup>
import { ref, computed } from 'vue'

const props = defineProps({
    title: {
        type: String,
        default: 'Тема вопроса',
    },
    info: {
        type: String,
        default: 'Текст вопроса',
    },
})

const expanded = ref(false)
const contentStyle = computed(() => {
    return { 'max-height': expanded.value ? '100px' : 0 }
})

const infoStyle = computed(() => {
    return { opacity: expanded.value ? 1 : 0 }
})
</script>
<template>
    <article class="question">
        <header>
            <h4 @click="expanded = !expanded" class="question-title">
                {{ title }}
            </h4>
            <div
                class="question__arrow"
                :class="{ 'question__arrow--open': expanded }"
                @click="expanded = !expanded"
            >
                <img src="/downarrow.svg" alt="" />
            </div>
        </header>
        <div :style="contentStyle" class="content">
            <p :style="infoStyle" class="info">{{ info }}</p>
        </div>
    </article>
</template>

<style scoped lang="scss">
.question {
    background-color: $white;
    padding: 2.25rem;
    border-radius: 2rem !important;
}

.question p {
    margin-bottom: 0;
    margin-top: 0.5rem;
}
.question header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.question-title {
    cursor: pointer;
    color: $black;
    display: flex;
    flex-direction: column;
    gap: 1rem;

    font-weight: 500;
    font-size: calc(1.525rem + (2.5 - 1.525) * ((100vw - 62rem) / (87 - 62)));
    line-height: calc(
        1.4 * (1.525rem + (2.5 - 1.525) * ((100vw - 62rem) / (87 - 62)))
    );
}

.content {
    max-height: 0;
    transition: max-height 0.2s ease-out;
}
.info {
    z-index: -1;
    opacity: 0;
    transition: opacity 0.2s ease-out;
    font-size: calc(1.14rem + (1.4 - 1.14) * ((100vw - 62rem) / (87 - 62)));
    line-height: calc(
        1.4 * (1.14rem + (1.4 - 1.14) * ((100vw - 62rem) / (87 - 62)))
    );
}
.question__arrow {
    width: 27px;
    height: 20px;
    cursor: pointer;
    transition: transform 0.3s;
    & img {
        width: 100%;
        height: 100%;
    }
    &--open {
        transform: rotate(180deg);
        transition: transform 0.3s;
    }
}
</style>
