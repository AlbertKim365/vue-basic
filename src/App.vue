<template>
  <div>
    <!-- <li>{{ sampleArray[0] }}</li>
    <li>{{ sampleArray[1] }}</li>
    <li>{{ sampleArray[2] }}</li>
    <li>{{ sampleArray[3] }}</li> -->

    <li
      v-for="(item, index) in sampleArray"
      :key="item"
      @click="openDialog(index)"
    >
      {{ item }} / {{ index }}
    </li>
    <li v-for="(user, index) in otherArray" :key="user.name">
      {{ user.id }} / {{ user.name }} / {{ index }}
    </li>

    <!-- <li>{{ sampleArray[0] }}</li>
    <li>{{ sampleArray[1] }}</li>
    <li>{{ sampleArray[2] }}</li>
    <li>{{ sampleArray[3] }}</li> -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      sampleArray: ["a", "b", "c", "d"],
      otherArray: [
        { id: 0, name: "John" },
        { id: 1, name: "Kim" },
        { id: 2, name: "Lee" },
        { id: 3, name: "Park" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
