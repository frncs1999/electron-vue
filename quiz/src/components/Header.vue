<template>
  <div>
    <ul class="nav">
        <li class="nav-item">
            <b><a class="nav-link disabled" href="#">Fancy Quiz App</a></b>
        </li>
        <li class="nav-item">
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