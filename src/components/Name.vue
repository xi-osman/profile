<template>
  <div class="name">
    <span class="first">{{first}}</span>
    <div class="box">
      <span v-for="(letter, index) in middle" :key="index" class="letter">{{letter}}</span>
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
