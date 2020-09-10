<template>
  <div>
    <ul class="nav">
        <li class="nav-item">
            <h1><b><a class="nav-link disabled">Fancy Quiz App</a></b></h1>
        </li><li class="nav-item">
            <a class="nav-link disabled">Counter: {{ numCorrect }}/{{ numTotal }}</a>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: [
    'numCorrect',
    'numTotal'
  ]
}
</script>

<style scoped>
ul {
    display: block; 
    text-align:center;
}
</style>