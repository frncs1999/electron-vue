<template>
  <div class="hello">
    <ul class="list-group list-group-flush">
      <li class="list-group-item">Cras justo odio</li>
      <li class="list-group-item">Dapibus ac facilisis in</li>
      <li class="list-group-item">Morbi leo risus</li>
      <li class="list-group-item">Porta ac consectetur ac</li>
      <li class="list-group-item">Vestibulum at eros</li>
    </ul>
  </div>
</template>

<script>
const axios = require('axios');

export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  created() {
    axios.get("https://reddit.com/r/aww.json")
      .then(response => {
        console.log(response.data.data.children)
      })
      .catch(error => {
        console.log(error)
      })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.list-group-flush{border-radius:0}
.list-group-flush>.list-group-item{border-width:0 0 1px}

.list-group-item{position:relative;display:block;padding:.75rem 1.25rem;background-color:#fff;border:1px solid rgba(0,0,0,.125)}
.list-group{display:-ms-flexbox;display:flex;-ms-flex-direction:column;flex-direction:column;padding-left:0;margin-bottom:0;border-radius:.25rem}
</style>
