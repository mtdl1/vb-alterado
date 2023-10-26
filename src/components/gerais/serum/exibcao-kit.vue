<template>
  <div class="bg-alt position-relative">
    <div class="row justify-content-center">
      <div class="titulo pt-5">
        <h2>Encontre em um só lugar tudo o que a sua pele, unhas e <br class="mob"> cabelos precisam</h2>
        <p>Não perca a oportunidade de ter o <br class="mob"> kit completo Viva Beauty</p>
      </div>
    </div>
    <div id="pin-1" class="descricao-produto position-absolute">
      <div class="box">
        <div class="texto">
          <h3>Espuma Facial</h3>
          <p>Limpa profundamente, ilumina e hidrata, desacelerando o processo de envelhecimento, mantendo a elasticidade da pele, além de diminuir a vermelhidão e inflamação.</p>
        </div>
      </div>
    </div>
    <div id="pin-2" class="descricao-produto pin-2 position-absolute">
      <div class="box">
        <div class="texto">
          <h3>Sérum Facial</h3>
          <p>Melhora a firmeza da pele significativamente, além de ajudar a reter a umidade, fornecendo hidratação e diminuindo visivelmente as rugas e linhas de expressão.</p>
        </div>
      </div>
    </div>
    <div id="pin-3" class="descricao-produto position-absolute">
      <div class="box">
        <div class="texto">
          <h3>Creme Facial</h3>
          <p>Possui ação anti-inflamatória, antioxidante, reduz a aparência dos poros progressivamente e potencializa os efeitos da hidratação.</p>
        </div>
      </div>
    </div>
    <div id="pin-4" class="descricao-produto pin-4 position-absolute">
      <div class="box">
        <div class="texto">
          <h3>Colágeno Skin Complex</h3>
          <p>Proporciona redução significativa da profundidade das rugas após 4 semanas de uso, e principalmente retarda os sinais do envelhecimento da pele agindo de dentro para fora.</p>
        </div>
      </div>
    </div>
    <BotaoCompreAgora  class="position-absolute btn desk"/>
  </div>
</template>

<script>
import BotaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue'
export default {
  components: { BotaoCompreAgora },
  name: 'ExibicaoKit',
}
</script>

<style scoped>
.bg-alt{
  height: 100%;
  background-color: white;
  background-image: url('../../../assets/img/exibicao-kit/foto.png');
  background-repeat: no-repeat;
  background-size: 100% 100%; 
  height: 80vh;
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

.descricao-produto{
  width: 8%;
  height: 8%;
  background-image: url(../../../assets/img/icones/+.png);
  background-position: top center;
  background-repeat: no-repeat;
  background-size: contain;
}

.descricao-produto:hover > .box {
  display: block;
}

.box {
  position: absolute;
  top: 240%;
  transform:translateY(-50%);
  left:-30%;
  display: none;
  width: 250px;
  z-index: 999999;
}

.texto {
    background-color: #fff;
    margin-top: 40px;
    padding: 20px;
    border-radius: 10px;
}

.box h3{
  text-align: center;
  font: normal normal bold 16px/18px Open Sans;
  letter-spacing: -0.64px;
  color: #F38599;
}

.box p{
  text-align: center;
  font: normal normal normal 14px/18px Open Sans;
  letter-spacing: -0.56px;
  color: #333333;
  margin-top: 10px;
}

#pin-1{
  top: 28%;
  left: 23%;
}

#pin-2{
  top: 28%;
  left: 38%;
}

#pin-3{
  top: 59%;
  left: 30%;
}

#pin-4{
  top: 68%;
  left: 63%;
}

.btn{
  bottom: 50px;
  left: 50%;
  transform: translateX(-50%);
  z-index: 999;
}

/* responsivo */
@media (max-width: 767px) {
  .bg-alt{
    background-image: url('../../../assets/img/exibicao-kit/Viva-Beauty-Home-Sessão-Interativa-mobile.jpg');
    background-size: cover; 
    height: 120vh;
  }
  .titulo{
    padding: 0 15px;
  }
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p{
    font-size: 16px;
  }
  #pin-1{
      top: 45%;
      left: 30%;
  }
  #pin-2{
      top: 35%;
      left: 32%;
  }
  #pin-3{
    top: 40%;
    left: 56%;
  }
  #pin-4{
      top: 60%;
      left: 55%;
  }
  .box{
    top: 190%;
    left: -320%;
    z-index: 999;
  }
  .pin-2 .box{
    left: -20%;
  }
  .pin-4 .box{
    left: -620%;
  }
  
}
</style>