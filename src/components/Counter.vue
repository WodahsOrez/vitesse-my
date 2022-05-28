<script setup lang="ts">
const props = defineProps<{
  initial: number
}>()

const { count, inc, dec } = useCounter(props.initial)
</script>

<template>
  <div>
    {{ count }}
    <ElButton class="inc" @click="inc()">
      +
    </ElButton>
    <button class="dec" @click="dec()">
      -
    </button>
  </div>
</template>
