<template lang="html">
  <div class="not-found">
    <h1>
      404
    </h1>
    <h2>Página não encontrada</h2>
    <p>a página que você está procurando não<br class="mob"> pode ser encontrada </p>
    <button class="mt-4"><a href="/">  
      IR PARA HOME
    </a>
    </button>

    <span class="my-4">Confira a linha completa:</span>

    <img  src="@/assets/img/banners/404.png" class="img-fluid mx-auto"/>
    
  </div>

</template>

<script>
import { mapMutations } from 'vuex';

export default {
  methods: {
    ...mapMutations(['changeDadosPageAtual']),
  },

  created(){
    //RESPONSE FIXO DE 404
    var response = {
      estrutura: {
        nivel: "404",
        seo: {
          title: "Página não encontrada",
          description: "",
          keywords: "",
          canonical: "",
          indexar: false
        }
      }
    }

    //CARREGA O SEO
    this.$aplicaSEO(response.estrutura);

    //CARREGA AS VARIÁVEIS PÚBLICAS
     this.changeDadosPageAtual(response.data);
  }
}

</script>

<style lang="css" scoped>
div{
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px 0;
  flex-direction: column;
}

h1{
font: normal normal bold 90px helvetica;
color: #951837;
}

h2{
font: normal normal 700 60px helvetica;
color: #333333;
}

p{
font: normal normal normal 30px helvetica;
color: #333333;
}

button {
  width: 300px;
  height: 65px;
  background: #00B451;
  border-radius: 5px;
  border: none;
}
a{
  
font: normal normal normal 25px Open sans;
color: #ffffff;

}
.not-found{
  min-height: calc(100vh - 60vh);

} 

span {
  font: normal normal bold 30px Open sans;
  color: #333333;
}

@media (max-width: 768px) {
  h1 {
   font-size: 60px; 
  }
  h2 {
   font-size: 30px; 
  }

  p {
    font-size: 17px;
    text-align: center;
    margin: 12px;
  }

  span {
    font-size: 20px;
   
  }

  button {
    width: 165px;
    height: 44px;
  }

  a{
  font: normal normal normal 15px Open sans;
  color: #ffffff;

}

img {
  position: relative;
  margin: auto;
  max-width: 92%;
}
}

</style>
