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
        padding: 20px;
        transition: all 0.2s ease-in-out;
        display: flex;
        align-items: center;
        justify-content: center;
        color: $white;
        font-size: 1.4rem;
        display: flex;
        align-items: center;
        justify-content: center;
        @media(min-width: 1500px) {
          font-size: 2rem;
        }
        @media(max-width: 768px) {
          padding: 12px;
        }
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