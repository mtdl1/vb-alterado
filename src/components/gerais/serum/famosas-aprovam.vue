<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="titulo">
        <h2>As peles mais famosas provam <br class="mob"> e aprovam Viva Beauty</h2>
        <p>Viva Beauty: o melhor colágeno para sua pele</p>
      </div>
    </div>
    <div class="row mt-5 justify-content-between px-3">
      <div class="col-md-6 d-flex align-items-center p-0 famosas">
        <img src="@/assets/img/famosas-aprovam/foto.png" alt="">
        <div class="texto px-3">
          <h3>Bella Falconi</h3>
          <p>Uso e amo o colágeno Viva Beauty há tantos e tantos anos, porque a fórmula dele é impecável. É o único sete em um do mercado com 12 ativos.</p>
        </div>
      </div>
      <div class="col-md-6 d-flex align-items-center p-0 famosas">
        <img src="@/assets/img/famosas-aprovam/foto-1.png" alt="">
        <div class="texto px-3">
          <h3>Lau Caroline</h3>
          <p>É um colágeno completo, muito bom por sinal, super fluido, fácil de dissolver, além de proporcionar vários beneficios.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FamosasAprovam',
}
</script>

<style scoped>
img{
  max-width: 100%;
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

.col-md-6{
  flex: 0 0 48%;
  max-width: 48%;
}

.famosas{
  box-shadow: 0px 3px 6px #00000029;
  border-radius: 5px;
}

.famosas h3{
  font: normal normal bold 18px/20px Open Sans;
  letter-spacing: -0.72px;
  color: #333333;
}

.famosas h3::before{
  content: '"';
  margin-right: 1px;
  font: normal normal bold 25px/20px Nunito;
  letter-spacing: -1px;
  color: #FB6F92;
}

.famosas p{
  font: normal normal normal 14px/18px Open Sans;
  letter-spacing: -0.56px;
  color: #333333;
  margin-top: 10px;
}


@media (max-width: 767px) {
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p{
    font-size: 16px;
  }
  .col-md-6{
    flex: 0 0 70%;
    max-width: 100%;
    margin: 0 auto 20px;
  }

  .famosas{
    flex-wrap: wrap;
  }

  .famosas img{
    margin:  0 auto;
  }
  .texto{
    padding-top: 20px;
    padding-bottom: 20px;
  }
}
</style>