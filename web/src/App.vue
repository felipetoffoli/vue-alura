 
 
 
 <template>


  <div>
    <h1 class="h1" >{{ titulo }}</h1>
      <div class="row">
      <div class="col" v-for="foto of fotos">
        
      <panel :img="foto.url" :tile="foto.title"></panel>
  </div>
</div>

      </div>

      </div>
    <!-- </ul> -->
  </div>
</template>

<script>
import Panel from './components/shared/Panel/Panel.vue'
export default {
  components: { 
    Panel
  },

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
  /* width: 320px;*/
  margin: 15px
}
</style>
