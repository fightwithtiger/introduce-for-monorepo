<template>
  <div flex="~" justify-between>
    <div>
      <Link :to="lTo">{{ lName }}</Link>
    </div>
    <div v-if="centerText">
      {{ centerText }}
    </div>
    <div>
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

// console.log(props.left)


</script>

<style scoped>
</style>