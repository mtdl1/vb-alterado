<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>Quatro ativos, uma solução para a sua pele</h2>
          <p>Os melhores ingredientes do mercado</p>
        </div>
      </div>
      <div class="row align-items-center mt-4">
        <div class="col-md-4 mob">
          <img class="rounded" src="@/assets/img/espuma/formula-unica/Viva-Beauty-Espuma-Landing-Page-ativos.png" alt="">
        </div>
        <div class="col-md-4">
          <div class="card-ativos">
            <h3>PLANTCOL</h3>
            <p>Colágeno vegetal rico em aminoácidos e proteínas que protege a pele da desidratação, aumenta a elasticidade e renova a vitalidade da pele com efeito tensor.</p>
          </div>
          <div class="card-ativos">
            <h3>ALGISIUM C (SILÍCIO)</h3>
            <p>Combate o envelhecimento, a perda de elasticidade, estimula a síntese de colágeno e elastina, possui ação anti-inflamatória, anti-radicais livres, hidrata e amacia.</p>
          </div>
        </div>
        <div class="col-md-4 desk text-center">
          <img class="rounded" src="@/assets/img/espuma/formula-unica/Viva-Beauty-Espuma-Landing-Page-ativos.png" alt="">
        </div>
        <div class="col-md-4">
          <div class="card-ativos direita">
            <h3>EXTRATO DE HAMAMÉLIS</h3>
            <p>Antioxidante, limpa e esfolia a pele sem ressecar, controla a oleosidade, minimiza poros e uniformiza a textura da pele, além de suavizar cicatrizes de acne e linhas finas.</p>
          </div>
          <div class="card-ativos direita">
            <h3>EXTRATO DE CENTELHA ASIÁTICA (CICA):</h3>
            <p>Estimula a produção de colágeno, auxilia no processo de cicatrização, diminui a vermelhidão, hidrata e diminui a perda de água, além de ser anti-inflamatório e antienvelhecimento.</p>
          </div>
        </div>
      </div>

      <BotaoCompreAgora class="pt-5 desk" />
    </div>
  </div>
</template>

<script>
import BotaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue'
export default {
  components: { BotaoCompreAgora },
  name: 'AtivosFormulaEspuma',
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

.descricao p{
  font: normal normal normal 16px/20px Open Sans;
  letter-spacing: -0.64px;
  color: #333333;
  text-align: center;
}

.card-ativos{
  margin-bottom: 30px;
}

.card-ativos:last-child{
  margin-bottom: 0;
}

.card-ativos h3{
  font: normal normal bold 18px/22px Open Sans;
  letter-spacing: -0.72px;
  color: #B84955;
  display: flex;
  align-items: center;
  justify-content: flex-end;
  margin-top: 15px;
}

.card-ativos h3::after{
  content: "";
  display: inline-block;
  width: 25px;
  height: 15px;
  background-color: #B84955;
  margin-left: 10px;
}

.card-ativos.direita h3{
  justify-content: start;
}

.card-ativos.direita h3::after{
  display: none;
}

.card-ativos.direita h3::before{
  content: "";
  display: inline-block;
  width: 25px;
  height: 15px;
  background-color: #B84955;
  margin-right: 10px;
}

.card-ativos p{
  text-align: right;
  font: normal normal normal 16px/20px Open Sans;
  letter-spacing: -0.64px;
  color: #333333;
  margin-top: 10px;
}

.card-ativos.direita p{
  text-align: left;
}

img	{
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
  .descricao p{
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.64px;
    text-align: left;
  }
  .col-md-4{
    padding: 0;
  }
  .card-ativos h3{
    text-align: left;
    font: normal normal bold 18px/18px Open Sans;
    justify-content: flex-start;
  }
  .card-ativos h3::after{
    display: none;
  }
  .card-ativos h3::before{
    content: "";
    display: inline-block;
    width: 25px;
    height: 15px;
    background-color: #B84955;
    margin-right: 10px;
  }
  .card-ativos p{
    text-align: left;
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.64px;
  }
}
</style>