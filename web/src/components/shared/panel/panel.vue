<template>
  <div class="card imgs" style="width: 18rem">
    <img :src="img" class="card-img-top" :alt="title" />
    <div class="card-body">
      <h5 class="card-title">{{ title }}</h5>
      <!-- <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a> -->
    </div>
  </div>
</template>

<script>
export default {
 props: ['title', 'img']
};
</script>

<style>

.imgs {
  /* width: 320px;*/
  margin: 15px;
}
</style>
