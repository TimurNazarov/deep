<template>
    <div class="wrapper">
      <link href="https://fonts.cdnfonts.com/css/montserrat" rel="stylesheet">
      <textarea @input="updateInput"></textarea>
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
  methods: {
    updateInput(event) {
      this.input = event.target.value;
    }
  },
  computed: {
    computedInput() {/deep/gi
      return this.input.replaceAll(/deep/gi, '♂ deep ♂').replaceAll(/right/gi, '♂ right ♂')
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
