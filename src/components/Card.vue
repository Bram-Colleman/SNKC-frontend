<script setup>
defineProps(['image', 'name', 'role', 'belt', 'cert']);

</script>

<template>
  <div class="cardContainer">
    <img class="pic" :src="image" alt="">
    <span class="role">{{ role }}</span>
    <span class="name">{{ name }}</span>
    <span class="belt">{{ belt }}</span>
    <span class="cert">{{ cert }}</span>
    
  </div>

</template>

<style scoped>
.cardContainer {
    display: flex;
    flex-direction: column;
  margin: 2rem 0;
  word-break: break-all;
  overflow-wrap: break-word;  
  hyphens: auto;  
  max-width: 333px;
  padding-bottom: 1rem;
  flex-grow: 0;

  border-top-left-radius: .75rem;
  border-top-right-radius: .75rem;
  text-align: center;

  -webkit-box-shadow: 0px 8px 14px 0px rgba(0,0,0,0.29);
-moz-box-shadow: 0px 8px 14px 0px rgba(0,0,0,0.29);
box-shadow: 0px 8px 14px 0px rgba(0,0,0,0.29);
}

.pic {
    width: 333px;
    border-top-left-radius: .75rem;
  border-top-right-radius: .75rem;
  margin-bottom: .5rem;
}
.role {
    color: #de251d;
    font-weight: lighter;
}
.name {
    font-size: 1.5rem;
}
.belt, .cert {
    font-weight: lighter;
}





@media only screen and (max-width: 600px)  {
.activityContainer {
  margin: 2rem 0;
}
}
</style>
  
