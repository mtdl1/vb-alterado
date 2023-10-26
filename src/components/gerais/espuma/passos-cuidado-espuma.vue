<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>Apenas três passos para <br class="mob"> uma pele limpa e hidratada</h2>
          <p>É simples manter os cuidados diários</p>
        </div>
      </div>
      <div class="row mt-5">
        <div class="col-md-4 text-center passo">
          <img src="@/assets/img/passos-espuma/passo 1.svg" alt="">
          <div class="texto">
            <h3>PASSO 1</h3>
            <p>Lave o rosto, preferencialmente com água morna e seque delicadamente</p>
          </div>
        </div>
        <div class="col-md-4 text-center passo">
          <img src="@/assets/img/passos-espuma/PASSO 2.svg" alt="">
          <div class="texto">
            <h3>PASSO 2</h3>
            <p>Aplique uma pequena quantidade de sérum por toda a região</p>
          </div>
        </div>
        <div class="col-md-4 text-center passo">
          <img src="@/assets/img/passos-espuma/PASSO 3.svg" alt="">
          <div class="texto">
            <h3>PASSO 3</h3>
            <p>Massageie por alguns minutos até completa absorção do produto</p>
          </div>
        </div>
      </div>
      <div class="row mt-5 descricao">
        <p>O sérum facial Viva Beauty é formulado com ativos selecionados que não proporcionam efeitos colaterais ao seu organismo, portanto, não há contraindicações. Em caso de alergias, intolerâncias ou tratamentos dermatológicos, consulte um profissional. Gestantes e lactantes precisam de autorização médica para utilizar o produto.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PassosCuidadoEspuma',
}
</script>

<style scoped>
.bg-alt{
  background-color: #FFF8F5;
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

.passo h3{
  text-align: center;
  font: normal normal bold 18px/18px Open Sans;
  letter-spacing: 0px;
  color: #B84955;
  margin-top: 15px;
}

.passo p{
  text-align: center;
  font: normal normal normal 16px/24px Open Sans;
  letter-spacing: 0px;
  color: #333333;
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
    padding-left: 30px;
    margin-top: 0;
  }
  .passo .texto p{
    text-align: left;
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.32px;
    padding-right: 0;
    padding-left: 30px;
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
  .descricao{
    padding: 20px 10px;
  }
  .descricao p{
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.32px;
  }
}
</style>