 <template>
  <div>
    <h1>{{ titulo }}</h1>
    <ul>
      <li v-for="foto of fotos">
        <img :src="foto.url" :alt="foto.titulo" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      titulo: "Alurapic",
      fotos: [
        {
          url: "https://i.pinimg.com/236x/48/cb/98/48cb987275f8e7e16ed281c35c28a98f.jpg",
          titulo: "cachorro",
        },
        {
          url: "https://i.pinimg.com/236x/48/cb/98/48cb987275f8e7e16ed281c35c28a98f.jpg",
          titulo: "cachorro",
        },
        {
          url: "https://i.pinimg.com/236x/48/cb/98/48cb987275f8e7e16ed281c35c28a98f.jpg",
          titulo: "cachorro",
        },
      ],
    };
  },
};
</script>

<style>
</style>
