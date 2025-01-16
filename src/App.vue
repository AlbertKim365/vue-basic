<template>
  <div>
    <ChildComponent
      :sendProps1="title"
      :sendProps2="createAt"
      :sendProps3="obj"
    />
  </div>
</template>

<script>
import ChildComponent from "./components/ChildComponent.vue";

export default {
  components: {
    ChildComponent,
  },
  data() {
    return {
      title: "부모 컨포넌트에서 선언된 데이터 입니다.",
      createAt: 2024,
      obj: {
        id: 2025,
        name: "Kim",
      },
    };
  },
};
</script>

<style lang="scss" scoped></style>
