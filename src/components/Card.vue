<template>
<div class = "card_container">
   <div class="card">
  <img src="https://www.w3schools.com/howto/img_avatar.png" alt="Avatar" style="width:100%">
  <div class="container">
    <h4><b>{{name}}</b></h4>
    <p>{{mail}}</p>
    <p>{{phone}}</p>
  </div>
</div>
</div>

     
</template>

<script>

export default {
  name: 'HelloWorld',
  props: ['users','name', 'mail', 'phone']
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.card_container{
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  
}

.card {
  /* Add shadows to create the "card" effect */
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 45%;
}

/* On mouse-over, add a deeper shadow */
.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}

/* Add some padding inside the card container */
.container {
  padding: 2px 16px;
}
.card {
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  border-radius: 5px; /* 5px rounded corners */
}

/* Add rounded corners to the top left and the top right corner of the image */
img {
  border-radius: 5px 5px 0 0;
  width: 10%;
}
</style>
