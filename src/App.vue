<template>
    <div class="wrapper">
      <link href="https://fonts.cdnfonts.com/css/montserrat" rel="stylesheet">
      <textarea  v-model="input"></textarea>
      <div class="copy">{{ computedInput }}</div>
    </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      input: ''
    }
  },
  computed: {
    computedInput() {
      return this.input.replaceAll(/deep/gi, '♂♂♂ deep ♂♂♂')
    }
  }
}
</script>

<style>
  .wrapper {
    padding-top: 300px;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    font-family: 'Montserrat';
  }
  .copy {
    background: rgba(0,0,0,.1);
    width: 500px;
    max-width: 100%;
    min-height: 200px;
    margin-top: 20px;
    padding: 10px;
  }
  textarea {
    padding: 10px;
    width: 500px;
    max-width: 100%;
    resize: none;
  }
</style>
