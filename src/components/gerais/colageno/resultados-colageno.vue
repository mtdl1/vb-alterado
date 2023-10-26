<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>O Skin Complex PLUS é um Tratamento Anti-Idade 7 em 1!</h2>
        </div>
      </div>
      <div class="row mt-3">
        <div class="col-md-3 " id="sabor">
          <p><span>96%</span> <br> Aprovaram o <br> sabor!</p>
        </div>
        <div class="col-md-3 " id="eficacia">
          <p><span>89%</span> <br> Aprovaram a <br> eficácia!</p>
        </div>
        <div class="col-md-3 " id="resultados">
          <p><span>93%</span> <br> Notaram <br> resultados</p>
        </div>
        <div class="col-md-3 " id="pele">
          <p><span>81%</span> <br> Sentiram a <br> pele + firme </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ResultadosColageno',
}
</script>

<style scoped>
.bg-alt{
  background-color: #F38599;
}

.titulo h2{
  text-align: center;
  font: normal normal bold 32px/36px Open Sans;
  letter-spacing: -1.28px;
  color: #FFFFFF;
}

.col-md-3{
  min-height: 270px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  text-align: center;
}
.col-md-3 p{
  font: normal normal normal 20px/22px Open Sans;
  letter-spacing: -0.8px;
  color: #FFFFFF;
}

.col-md-3 p span{
  font: normal normal bold 50px/54px Open Sans;
  letter-spacing: -2px;
  color: #FFFFFF;
}

#sabor{
  background-image: url(../../../assets/img/colageno/resultados/LINHA.png);
}

#eficacia, #resultados, #pele{
  background-image: url(../../../assets/img/colageno/resultados/LINHA2.png);
}

@media (max-width: 767px) {
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .row{
    justify-content: center;
  }

  .col-md-3{
    min-height: 200px;
    background-size: contain;
    width: 45%;
  }

  .col-md-3 p{
    font: normal normal normal 16px/18px Open Sans;
    letter-spacing: -0.64px;
  }

  .col-md-3 p span{
    font: normal normal bold 30px/32px Open Sans;
    letter-spacing: -1.2px;
  }
}
</style>