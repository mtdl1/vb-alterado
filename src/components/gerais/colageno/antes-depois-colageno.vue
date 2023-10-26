<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo text-center">
          <h2>Muito mais que um <br class="mob"> simples colágeno!</h2>
          <p>Resultados visíveis já no primeiro mês de uso!</p>
        </div>
      </div>
      <div class="row justify-content-between mt-5">
        <div class="col-md-4">
          <img class="rounded" src="@/assets/img/colageno/antes-depois/Viva-Beauty-Antes-Depois-01.png" alt="">
        </div>
        <div class="col-md-4 desk">
          <img class="rounded" src="@/assets/img/colageno/antes-depois/Viva-Beauty-Antes-Depois-02.png" alt="">
        </div>
        <div class="col-md-4 desk">
          <img class="rounded" src="@/assets/img/colageno/antes-depois/Viva-Beauty-Antes-Depois-03.png" alt="">
        </div>
      </div>
      <div class="row mt-5 justify-content-center texto-formula">
        <div class="col">
          <p>Nossa fórmula é super completa <br class="mob"> e exclusiva, <strong>acelerando os resultados em até 6x</strong> em relação a maioria dos colágenos do mercado!</p>
        </div>
      </div>
      <div class="row justify-content-center">
        <botaoCompreAgora class="mt-5 desk" />
      </div>
    </div>
  </div>
</template>

<script>
import botaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue'
export default {
  components: { botaoCompreAgora },
  name: 'AntesDepoisColageno',
}
</script>

<style scoped>
.bg-alt{
  background-color: #FAFAFA;
}
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

@media (max-width: 767px) {
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p{
    font-size: 16px;
  }

  .texto-formula p{
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.64px;
    color: #202020;
    text-align: center;
  }

  .texto-formula p strong{
    font-weight: normal;
  }
}
</style>