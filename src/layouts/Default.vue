<template>
  <div id="app">

    <header class="header">
      <div class="header__left"/>
      <div class="header__right right">        
        <ToggleTheme />
      </div>
    </header>

    <main class="main">
      <slot/>
    </main>
    
  </div>
</template>

<script>
import ToggleTheme from '~/components/ToggleTheme.vue'

export default {
  props: {
    showLogo: { default: true }
  },
  components: {
    ToggleTheme
  }
}
</script>

<style lang="scss">
.header {
  margin-top: -30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  top:0;
  z-index: 10;

  &__left,
  &__right {
    float: right;
    display: flex;
    align-items: center;
  }

  .right {
    position: relative;
    top: 45px;
    right: 15px;
  }

  @media screen and (min-width: 1300px) {
    //Make header sticky for large screens
    position: sticky;
    width: 100%;

    .right{
      top: 15px;
    }
  }
}
</style>