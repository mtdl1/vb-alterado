<template>
  <div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo pb-5">
          <h2>Conheça nossos produtos</h2>
        </div>
      </div>
      <div class="row">
        <div class="col-6 col-md-3 produto text-center">
          <a href="/products/colageno"><img src="@/assets/img/produtos/exibe-todos/Viva-Beauty-Home-Produto-Colageno.png" alt=""></a>
          <a href="/products/colageno">
            <p>Colágeno <br class="mob"> Skin Complex</p>
          </a>
        </div>
        <div class="col-6 col-md-3 produto text-center">
          <a href="/products/serum-facial-anti-idade">
            <img src="@/assets/img/produtos/exibe-todos/Viva-Beauty-Home-Produto-Serum-Facial-Anti-Idade.png" alt="">
          </a>
          <a href="/products/serum-facial-anti-idade">
            <p>Sérum Facial <br class="mob"> Anti-Idade</p>
          </a>
        </div>
        <div class="col-6 col-md-3 produto text-center">
          <a href="/products/espuma-limpeza">
            <img src="@/assets/img/produtos/exibe-todos/Viva-Beauty-Home-Produto-Espuma.png" alt="">
          </a>
          <a href="/products/espuma-limpeza">
            <p>Espuma de <br class="mob"> Limpeza Facial</p>
          </a>
        </div>
        <div class="col-6 col-md-3 produto text-center">
          <a href="/products/creme">
            <img src="@/assets/img/produtos/exibe-todos/Viva-Beauty-Home-Produto-Creme-Hidratante-Primer.png" alt="">
          </a>
          <a href="/products/creme">
            <p>Creme <br class="mob"> Hidratante Primer</p>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'VitrineProdutosHome',
}
</script>

<style scoped>
.titulo h2{
  text-align: center;
  font: normal normal bold 32px/36px Open Sans;
  letter-spacing: -1.28px;
  color: #333333;
}

img{
  max-width: 100%;
}

.produto p{
  text-align: center;
  font: normal normal 600 18px/22px Open Sans;
  letter-spacing: -0.18px;
  color: #333333;
  margin-top: 10px;
}

@media (max-width: 767px) {
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .produto{
    margin-bottom: 30px;
  }

  .produto p{
    font: normal normal 600 16px/18px Open Sans;
  letter-spacing: -0.16px;
  color: #333333;
  }

}
</style>