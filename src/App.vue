<template>
  <h1>{{ text }}</h1>
  <h1>changeText 함수 호출 값 : {{ changeText() }}</h1>
  <h1>changeText 함수 호출 값 : {{ changeText() }}</h1>
  <h1>changeText 함수 호출 값 : {{ changeText() }}</h1>

  <h2>{{ computedText }}</h2>
  <h2>{{ computedText }}</h2>
  <h2>{{ computedText }}</h2>
</template>

<script>
export default {
  data() {
    return {
      text: "Computed 테스트 데이터 문구 입니다.",
    };
  },
  computed: {
    computedText() {
      console.log(`computed 기능을 생성 하였습니다.`, this.text);
      return this.text.split("").reverse().join("");
    },
  },
  methods: {
    changeText() {
      console.log(`함수 호출`, this.text);

      return this.text.split("").reverse().join("");
    },
  },
};
</script>

<style lang="scss" scoped></style>
