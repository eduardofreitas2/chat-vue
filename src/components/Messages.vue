<template>
  <p :class="type">{{ text }}</p>
</template>

<style scoped>
  .received {
    word-break: break-all;
    position: relative;

    border: 2px solid;
    border-radius: 0 8px 8px 8px;
    padding: 0.875rem 1rem;

    margin-right: 30%;
  }

  .received::before {
    content: 'Uko diz:';
    position: absolute;
    top: 0;
    left: 0;
    margin-top: -24px;
  }

  .sent {
    word-break: break-all;
    position: relative;

    border: 2px solid;
    border-radius: 8px 0px 8px 8px;
    padding: 0.875rem 1rem;
    
    margin-left: 30%;
  }

  .sent::before {
    content: 'Você diz:';
    position: absolute;
    top: 0;
    right: 0;
    margin-top: -24px;
  }
</style>

<script setup lang="ts">
  defineProps<{
    type: string
    text: string
  }>()
</script>