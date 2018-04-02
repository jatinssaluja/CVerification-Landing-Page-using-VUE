<template>
  <div class="Modal">
       <slot></slot>
      </div>
</template>

<script>
export default {
  name: 'Modal',
  data () {
    return {};
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.Modal {
position: fixed;
 z-index: 500;
 background-color: white;
 width: 50%;
 /*border: 1px solid #ccc;*/
 border: none transparent;
 border-radius: 5px;
 box-shadow: 1px 1px 1px black;
 padding: 16px;
 left: 15%;
 top: 15%;
 box-sizing: border-box;
 transition: all 0.3s ease-out;
 animation: animatezoom 0.6s;
}



@keyframes animatezoom {
    from {transform: scale(0)}
    to {transform: scale(1)}
}





@media (min-width: 600px) {
    .Modal {
        width: 500px;
        left: calc(50% - 250px);
    }
}



</style>
