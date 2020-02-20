<template>
  <div class="container">
    <h4>Quote</h4>
    <textarea v-model="quote"></textarea>
    <button @click="onclick" :disabled="disable || !quote">Add Quote</button>
  </div>
</template>

<script>
export default {
  props: ['addQuote', 'disable'],
  data () {
    return {
      quote: ''
    }
  },
  methods: {
    onclick () {
      this.addQuote(this.quote)
      this.quote = ''
    }
  }
}
</script>

<style scoped>
.container {
  width: calc(100% - 800px);
  margin: 0 auto;
}
h4 {
  margin-bottom: 10px;
}
textarea {
  display: block;
  width: 100%;
  height: 100px;
  margin-bottom: 20px;
  padding: 5px;
  box-sizing: border-box;
}
textarea:focus {
  outline: none;
}
button {
  width: 100px;
  height: 30px;
  background-color: #a6a6fc;
  border: 0;
  color: #fff;
  text-align: center;
  border-radius: 4px;
  font-size: 14px;
  cursor: pointer;
}
button:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}
</style>
