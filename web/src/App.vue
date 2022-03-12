 
 
 
 <template>


  <div>
    <h1 class="h1" >{{ titulo }}</h1>
    <!-- <ul class="list-group"> -->
      <div class="row">
      <div class="col" v-for="foto of fotos">
        
        <div class="card imgs" style="width: 18rem;">
  <img :src="foto.url" class="card-img-top" :alt="foto.titulo" >
  <div class="card-body">
    <h5 class="card-title">{{foto.titulo}}</h5>
    <!-- <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
    <a href="#" class="btn btn-primary">Go somewhere</a> -->
  </div>
</div>

      </div>

      </div>
    <!-- </ul> -->
  </div>
</template>

<script>
export default {
  data()  {
    return {
      titulo: "Alurapic",
      fotos: [],
    };
  },

  created() {
    this.$http.get('http://localhost:3000/v1/fotos')
        .then( res => res.json())
        .then(img => this.fotos = img, err => console.log(err));
  }
  
};
</script>

<style>
.corpo {
  font-family: Helvetica, sans-serif;
  width: 96%;
}
.centralizado {
  list-style: none;
}
.imgs{
  width: 320px;
  margin: 15px
}
</style>
