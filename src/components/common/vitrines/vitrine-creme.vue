<template>
  <div class="container py-5" id="produtos">
    <div class="row justify-content-center pb-5">
      <div class="titulo">
        <h2>O creme facial mais eficaz para a sua pele está aqui</h2>
        <p>Escolha o kit que melhor te atende</p>
      </div>
    </div>
    <div class="row">
      <div class="col-md-6">
        <CardProduto :produto="products.creme[0]"/>
      </div>
      <div class="col-md-6">
        <CardProduto :produto="products.colageno[3]" :header="'bgPink'"/>
      </div>
    </div>
  </div>
</template>

<script>
import products from '@/data/produtos.js';
import CardProduto from '../../ui/card-produto.vue';
export default {
  components: { CardProduto },
  name: 'VitrineCreme',
  data() {
    return {
      products: products[0]
    }
  },
}
</script>

<style scoped>
.titulo h2{
  text-align: center;
  font: normal normal bold 32px/36px Open Sans;
  letter-spacing: -1.28px;
  color: #333333;
}

.titulo p{
  text-align: center;
  font: normal normal normal 18px/18px Open Sans;
  letter-spacing: 0px;
  color: #333333;
  margin-top: 10px;
}

/* responsivo */
@media (max-width: 767px) {

  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p{
    font-size: 16px;
  }

  .col-md-6 {
    margin-bottom: 20px;
  }
  .col-md-6:last-child {
    margin-bottom: 0;
  }
}
</style>