<template>
  <p>Reaction time: {{score}} ms</p>
  <p class="speed">{{speed}}</p>
</template>

<script>
export default {
props: ['score'],
data() {
  return {
    speed: null
  }
},
mounted() {
  if(this.score < 350){
    this.speed = "Very fast"
  }
  else if (this.score < 500){
    this.speed = "Relatively fast"
  }
  else {
    this.speed ="Not so fast"
  }
}
}
</script>

<style>
.speed{
  font-size: 1.4rem;
  color: #0faf82;
  font-weight: bold;
}
</style>