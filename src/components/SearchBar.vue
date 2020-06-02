<template>
  <div class="search-bar">
    <input @keypress.enter="onInput" placeholder="아르를 검색해라..">
  </div>
</template>

<script>
export default {
  name: 'SearchBar',
  methods: {
    onInput(event) {
      // emit 1. 위로 커스텀 이벤트를 쏜다.
      this.$emit('input-change', event.target.value)
    }
  },
}
</script>

<style scoped>
/*
  scoped 옵션은 해당 컴포넌트에만 영향을 준다.
  하지만 클래스 지정은 해야 한다. (성능이슈)
 */
div.search-bar {
  text-align: center;
  margin: 20px;
}

div.search-bar > input {
  width: 75%;
}
</style>



<style lang="stylus">
</style>
