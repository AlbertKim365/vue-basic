<template>
  <div>{{ props.sendProps1 }}</div>
  <div>{{ props.sendProps2 }}</div>
  <div>{{ props.sendProps3.id }}</div>
  <div>{{ props.sendProps3.name }}</div>
</template>

<script setup lang="ts">
interface Obj {
  id: number;
  name: string;
}

interface Props {
  sendProps1: String;
  sendProps2: Number;
  sendProps3: Obj;
}
const props = defineProps<Props>();
</script>

<style lang="scss" scoped></style>
