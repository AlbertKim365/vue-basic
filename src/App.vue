<template>
  <button @click="changeMessage">{{ message }}</button>
  {{ watchMessage }}
</template>

<script>
export default {
  data() {
    return {
      message: "안녕하세요! Vue.js Watch 기능 테스트 오리지널 문구",
    };
  },
  watch: {
    message() {
      this.watchMessage = "Watch 동작";
    },
  },
  methods: {
    changeMessage() {
      console.log(`함수 호출`);
      this.message = "변경된 message 데이터 입니다.";
    },
  },
};
</script>

<style lang="scss" scoped></style>
