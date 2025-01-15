<template>
  <div>{{ count }}</div>
  <h1>Vue.js 라이프사이클 테스트</h1>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  beforeCreate() {
    console.log(`lifeCycle is beforeCreate`, this.count);
  },
  created() {
    console.log(`olifeCycle is created`, this.count);
    this.test();
  },
  // beforeMount() {
  //   console.log(`lifeCycle is beforeMount`, document.querySelector("h1"));
  // },
  // Mounted() {
  //   console.log(`olifeCycle is Mounted`, document.querySelector("h1"));
  // },
  methods: {
    test() {
      console.log(`함수 호출!!!`);
    },
  },
};
</script>

<style lang="scss" scoped></style>
