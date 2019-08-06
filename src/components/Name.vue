<template>
  <div class="name">
    <span class="first">{{first}}</span>
    <div class="box">
      <div v-for="(letter, index) in middle" :key="index" class="letter">{{letter}}</div>
      <span>{{last}}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "name",
  props: ["first", "middle", "last"]
};
</script>
