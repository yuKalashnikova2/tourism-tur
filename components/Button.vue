<script setup>
const props = defineProps({
    label: {
    type: String,
    default: 'Button',
  },
  backgroundColor: {
    type: Boolean,
    default: false
  }
})
</script>
<template>
     <button class="btn" :class="[backgroundColor ? 'btn_transparent' : '']">{{ label }}</button>
</template>

<style lang="scss" scoped>
      .btn {
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
        &_transparent {
            background-color: transparent;
            border:2px solid $white;
        }
        &:hover {
            opacity: .6;
            cursor: pointer;
        }
    }
</style>