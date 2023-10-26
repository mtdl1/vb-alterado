<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>Espuma de limpeza facial <br class="mob"> Viva Beauty: <br class="desk"> a fórmula <br class="mob"> mais completa</h2>
          <p>Três passos para uma pele limpa e hidratada</p>
        </div>
      </div>
      <div class="row pt-5">
        <div class="col-md-4 mob mb-4">
          <img src="@/assets/img/espuma/formula-unica/Viva-Beauty-Espuma-Landing-Page-A-formula-ideal.png" alt="">
        </div>
        <div class="col-md-4">
          <div class="card-formula">
            <h3>Limpa Profundamente</h3>
            <p>A combinação de ativos da espuma facial Viva Beauty proporciona uma limpeza profunda e eficiente, <strong>removendo as células mortas, desobstruindo os poros</strong> e deixando a pele preparada para o dia a dia.</p>
          </div>
          <div class="card-formula">
            <h3>Ilumina e hidrata</h3>
            <p>Poo filme biológico que impede a perda de água, a espuma facial mantém a pele hidratada, <strong>proporcionando aumento da elasticidade e firmeza</strong>, além de iluminar e aumentar a umidade da pele.</p>
          </div>
        </div>
        <div class="col-md-4 desk">
          <img src="@/assets/img/espuma/formula-unica/Viva-Beauty-Espuma-Landing-Page-A-formula-ideal.png" alt="">
        </div>
        <div class="col-md-4">
          <div class="card-formula">
            <h3>Desacelera o envelhecimento</h3>
            <p>Por estimular a produção de colágeno e elastina, a espuma facial Viva Beauty atua na prevenção e combate do envelhecimento da pele, <strong>suavizando rugas, linhas finas e cicatrizes</strong>, mantendo o viço e o aspecto jovem.</p>
          </div>
          <div class="card-formula">
            <h3>Calmante e anti-inflamatória</h3>
            <p>Sua ação diminui a vermelhidão e a irritação da pele causadas pelos antioxidantes dos raios de sol e poluição, <strong>além de reduzir a inflamação causada pela oleosidade, acnes e poros dilatados.</strong></p>
          </div>
        </div>
      </div>
      <BotaoCompreAgora class="pb-5" />
    </div>
  </div>
</template>

<script>
import BotaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue'
export default {
  components: { BotaoCompreAgora },
  name: 'FormulaUnicaEspuma',
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

img{
  max-width: 100%;
}

.card-formula{
  background-color: #FFF;
  border-radius: 5px;
  padding: 10px 30px;
  margin-bottom: 30px;
}

.card-formula h3{
  text-align: center;
  font: normal normal bold 18px/22px Open Sans;
  letter-spacing: 0px;
  color: #B84955;
  border-bottom: 1px solid #B84955;
  padding-bottom: 5px;
}

.card-formula p{
  font: normal normal normal 16px/20px Open Sans;
  letter-spacing: -0.64px;
  text-align: center;
  margin-top: 10px;
}

/* reponsivo */
@media (max-width: 767px) {
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p{
    font-size: 16px;
  }
  
  .col-md-4{
    padding: 0;
  }

  .card-formula{
    padding: 10px 15px;
  }

  .card-formula h3{
    font-size: 16px;
  }

  .card-formula p{
    font-size: 14px;
  }
}
</style>