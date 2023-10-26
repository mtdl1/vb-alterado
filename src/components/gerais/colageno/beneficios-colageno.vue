<template>
  <div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo text-center">
          <h2>Tratamento Anti-Idade <br class="mob"> 7 em 1 Skin Complex Plus <br class="mob"> com <br class="desk"> Colágeno Verisol ® <br class="mob"> + Ácido Hialurônico <br class="mob"> + Silício Orgânico (Nutricolin®)</h2>
        </div>
      </div>
      <div class="row align-items-center pt-5">
        <div class="col-md-6">
          <img src="@/assets/img/colageno/beneficios/Viva-Beauty-Colageno-Tratamento-Anti-Idade.png" alt="">
        </div>
        <div class="col-md-6 d-flex flex-wrap">
          <div class="card-beneficios">
            <img src="@/assets/img/colageno/beneficios/ICONE PELE.svg" alt="">
            <p>Pele</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/colageno/beneficios/CABELO.svg" alt="">
            <p>Cabelos</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/colageno/beneficios/celulite.svg" alt="">
            <p>Celulites</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/colageno/beneficios/Grupo 806.svg" alt="">
            <p>Flacidez</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/colageno/beneficios/unhas.svg" alt="">
            <p>Unhas</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/colageno/beneficios/OSSOS.svg" alt="">
            <p>Ossos</p>
          </div>
          <div class="card-beneficios">
            <img src="@/assets/img/colageno/beneficios/rugas.svg" alt="">
            <p>Rugas</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BeneficiosColageno',
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
}

.card-beneficios p{
  text-align: center;
  font: normal normal normal 20px/20px Open Sans;
  letter-spacing: 0px;
  color: #333333;
}

@media (max-width: 767px) {
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p{
    font-size: 16px;
  }
}
</style>