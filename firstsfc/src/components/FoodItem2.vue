<template>
  <div class="pears">
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'pears',
      message: 'I like chico'
    }
  }
};
</script>

<style>
  .pears {
    border: dashed black 1px;
    display: inline-block;
    margin: 10px;
    padding: 10px;
    background-color: #d6fffd;   
    color: #7cc1bd;              
  }
</style>

