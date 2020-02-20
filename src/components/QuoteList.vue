<template>
  <ul>
    <li v-for="(quote, index) in quotes" :key="index" @click="deleteQuote(index)">
      {{quote}}
    </li>
  </ul>
</template>

<script>
export default {
  props: ['quotes', 'deleteQuote']
}
</script>

<style scoped>
ul {
  list-style-type: none;
  display: flex;
  flex-wrap: wrap;
  padding: 0;
}
ul > li {
  min-width: 200px;
  padding: 5px;
  border: 1px solid;
  border-radius: 5px;
  margin: 10px;
  cursor: pointer;
}
ul > li:hover {
  box-shadow: 0px 1px 0px 0px;
}
</style>
