<template>
  <div flex="~" justify-between>
    <div v-if="lName">
      <Link :to="lTo">{{ lName }}</Link>
    </div>
    <div v-if="centerText">
      {{ centerText }}
    </div>
    <div v-if="rName">
      <Link :to="rTo">{{ rName }}</Link>
    </div>
  </div>
</template>

<script lang="ts" setup>
const props = defineProps({
  lName: {
    default: ''
  },
  rName: {
    default: ''
  },
  lTo: {
    default: 1
  },
  rTo: {
    default: 1
  },
  centerText: {
    default: ''
  }
})
</script>

<style scoped>
</style>