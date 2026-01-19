<template>
  <div class="apple">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'banana',
      message: 'I like bananas AND strawberries'
    }
  }
};
</script>

<style>
  .apple {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: lightpink;   
    color: peachpuff;              
  }
</style>
