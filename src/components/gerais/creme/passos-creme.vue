<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>Três passos para uma pele hidratada e firme</h2>
          <p>Seu skincare rápido e fácil</p>
        </div>
      </div>
      <div class="row mt-5">
        <div class="col-md-4 text-center passo">
          <img src="@/assets/img/icones/PASSO 1-branco.svg" alt="">
          <div class="texto">
            <h3>PASSO 1</h3>
            <p>Com o rosto limpo e seco, aplique uma pequena quantidade do creme facial</p>
          </div>
        </div>
        <div class="col-md-4 text-center passo">
          <img src="@/assets/img/icones/PASSO  2-branco.svg" alt="">
          <div class="texto">
            <h3>PASSO 2</h3>
            <p>Com o rosto limpo e seco, aplique uma pequena quantidade do creme facial</p>
          </div>
        </div>
        <div class="col-md-4 text-center passo">
          <img src="@/assets/img/icones/PASSO 3-branco.svg" alt="">
          <div class="texto">
            <h3>PASSO 3</h3>
            <p>Aplique o protetor solar com FPS indicado para a sua pele.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PassosCreme',
}
</script>

<style scoped>
.bg-alt{
  background-color: #B84955;
}
.titulo h2{
  text-align: center;
  font: normal normal bold 32px/36px Open Sans;
  letter-spacing: -1.28px;
  color: #FFF;
}

.titulo p{
  text-align: center;
  font: normal normal normal 18px/18px Open Sans;
  letter-spacing: 0px;
  color: #FFF;
  margin-top: 10px;
}

.passo h3{
  text-align: center;
  font: normal normal bold 18px/18px Open Sans;
  letter-spacing: 0px;
  color: #FFF;
  margin-top: 15px;
}

.passo p{
  text-align: center;
  font: normal normal normal 16px/24px Open Sans;
  letter-spacing: 0px;
  color: #FFF;
  margin-top: 15px;
  padding: 0 20px;
}

.aviso h3{
  font: normal normal normal 19px/29px Open Sans;
  letter-spacing: 0px;
  display: flex;
  align-items: center;
}

.aviso h3 img{
  margin-right: 10px;
}

.aviso h3 strong{
  font: normal normal bold 19px/29px Open Sans;
  letter-spacing: 0px;
  color: #333333;
  margin-right: 6px;
}

.descricao{
  background-color: #FFF;
  padding: 20px;
  border-radius: 5px;
}

.descricao p{
  text-align: center;
  font: normal normal normal 18px/24px Open Sans;
  letter-spacing: -0.72px;
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

  .passo{
    display: flex;
    align-items: center;
    margin-bottom: 20px;
    padding: 0;
  }

  .passo:last-child{
    margin-bottom: 0;
  }

  .passo img{
    width: 100px;
  }

  .passo .texto h3{
    text-align: left;
    font: normal normal bold 18px/18px Open Sans;
    letter-spacing: 0px;
    padding-left: 20px;
    margin-top: 0;
  }

  .passo .texto p{
    text-align: left;
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.32px;
    padding-right: 0;
    padding-left: 20px;
    margin-top: 5px;
  }

  .aviso h3{
    font: normal normal normal 16px/24px Open Sans;
    letter-spacing: 0px;
  }

  .aviso h3 strong{
    font: normal normal bold 16px/24px Open Sans;
    letter-spacing: 0px;
  }

  .aviso h3 img{
    width: 23px;
  }

  .descricao p{
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.32px;
  }
  
}
</style>