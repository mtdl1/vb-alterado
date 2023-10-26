<template>
  <div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo text-center">
          <h2>A linha de cuidados definitiva para a sua pele</h2>
          <p>Tudo o que você precisa em 3 produtos com os melhores benefícios</p>
        </div>
      </div>
      <div class="row align-items-center pt-5 informacional">
        <div class="col mob pb-5">
          <img src="@/assets/img/linha-cuidados/Viva-Beauty-Linha-Skin-Care-Produtos.png" alt="">
        </div>
        <div class="col-md-6 d-flex flex-wrap">
          <p class="mb-4">A linha de cuidados Viva Beauty Skin oferece tudo o que a sua pele precisa <strong>com apenas três produtos: espuma de limpeza, sérum e creme hidratante facial</strong>, desenvolvidos com ativos premium para facilitar a sua rotina de cuidados e deixar a sua pele mais jovem, hidratada, e com aparência mais firme.</p>
          <div class="card-beneficios">
            <img src="@/assets/img/linha-cuidados/diminui os poros.svg" alt="">
            <p>Diminui <br> os poros</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/linha-cuidados/reduz a oleosidade.svg" alt="">
            <p>Reduz a <br> oleosidade</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/linha-cuidados/Hidrata profundamente.svg" alt="">
            <p>Hidrata <br> Profundamente</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/linha-cuidados/Acalma.svg" alt="">
            <p>Acalma <br> a pele</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/linha-cuidados/Ação firmadora.svg" alt="">
            <p>Ação <br> firmadora</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/linha-cuidados/Ameniza rugas.svg" alt="">
            <p>Ameniza <br> Rugas</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/linha-cuidados/Aumenta a elasticidade.svg" alt="">
            <p>Aumenta a <br> elasticidade</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/linha-cuidados/Protege  e nutre.svg" alt="">
            <p>Protege <br> e nutre</p>
          </div>
        </div>
        <div class="col-md-6 desk">
          <img src="@/assets/img/linha-cuidados/Viva-Beauty-Linha-Skin-Care-Produtos.png" alt="">
        </div>
      </div>
      <div class="row pt-5 banners-produtos">
        <div class="col-md-4">
          <img src="@/assets/img/linha-cuidados/Viva-Beauty-Home-Skin-Care-serum.png" alt="">
          <a href="/products/serum-facial-anti-idade">
            <p>Saiba mais</p>
          </a>
        </div>
        <div class="col-md-4">
          <img src="@/assets/img/linha-cuidados/Viva-Beauty-Home-Skin-Care.png" alt="">
          <a href="/products/espuma-limpeza">
            <p>Saiba mais</p>
          </a>
        </div>
        <div class="col-md-4">
          <img src="@/assets/img/linha-cuidados/Viva-Beauty-Home-Skin-Care-creme.png" alt="">
          <a href="/products/creme">  
            <p>Saiba mais</p>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'LinhaCuidados',
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

img{
  max-width: 100%;
}

.card-beneficios {
  width: 25%;
  text-align: center;
}

.card-beneficios p{
  text-align: center;
  font: normal normal normal 20px/20px Open Sans;
  letter-spacing: 0px;
  color: #333333;
}

.informacional p{
  font: normal normal normal 18px/24px Open Sans;
  letter-spacing: -0.72px;
  color: #333333;
}

.banners-produtos p{
  font: normal normal bold 24px/24px Helvetica;
  letter-spacing: 0px;
  color: #F38599;
  text-align: center;
  border: 1px solid;
  padding: 25px 0 20px;
  margin-top: -5px;
  border-radius: 0 0 10px 10px;
}

@media (max-width: 767px) {
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p{
    font-size: 16px;
  }

  .banners-produtos .col-md-4{
    margin-bottom: 30px;
  }
  
  .banners-produtos .col-md-4:last-child{
    margin-bottom: 0;
  }

  .banners-produtos p{
    font: normal normal bold 18px/22px Helvetica;
  }

  .informacional p{
    font: normal normal normal 14px/18px Open Sans;
    letter-spacing: -0.72px;
    color: #333333;
  }

}
</style>