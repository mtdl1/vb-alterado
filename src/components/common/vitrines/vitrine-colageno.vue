<template>
  <div class="container py-5" id="produtos">
    <div class="row pb-5">
      <div class="titulo">
        <h2>Tratamento Anti-Idade 7 em 1 Skin Complex Plus com Colágeno Verisol ® + Ácido Hialurônico + Silício Orgânico (Nutricolin®)</h2>
      </div>
    </div>
    <div class="row">
      <div class="col-md-6">
        <CardProduto :produto="products.colageno[0]"/>
      </div>
      <div class="col-md-6">
        <CardProduto :produto="products.colageno[1]" :header="'bgPink'"/>
      </div>
      <div class="col-md-6 mt-md-5">
        <CardProduto :produto="products.colageno[2]"/>
      </div>
      <div class="col-md-6 mt-md-5">
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
  name: 'VitrineColageno',
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
  color: #333;
}

/* responsivo */
@media (max-width: 767px) {

  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .col-md-6 {
    margin-bottom: 20px;
  }

  .col-md-6:last-child {
    margin-bottom: 0;
  }

}
</style>