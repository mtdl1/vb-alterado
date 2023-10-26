<template>
  <div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>A fórmula ideal e descomplicada para tratar a pele do rosto</h2>
          <p>Sete ativos potentes para os cuidados diários</p>
        </div>
      </div>
      <div class="row pt-5">
        <div class="col-md-4 mob mb-4">
          <img src="@/assets/img/creme/formula/Viva-Beauty-Creme-Hidratante-Landing-Page-A-formula-ideal.png" alt="">
        </div>
        <div class="col-md-4">
          <div class="card-formula">
            <h3>Hidratação profunda</h3>
            <p>A combinação poderosa de agentes hidratantes promove a nutrição e restauração da umidade natural da pele com toque aveludado e sedoso.</p>
          </div>
          <div class="card-formula">
            <h3>Reduz linhas de expressão</h3>
            <p>Devido à ação antienvelhecimento, atua na renovação celular, promove a redução de rugas, diminuindo a aspereza e melhora a elasticidade da pele.</p>
          </div>
        </div>
        <div class="col-md-4 desk">
          <img src="@/assets/img/creme/formula/Viva-Beauty-Creme-Hidratante-Landing-Page-A-formula-ideal.png" alt="">
        </div>
        <div class="col-md-4 direita">
          <div class="card-formula">
            <h3>Ação firmadora</h3>
            <p>Os ativos possuem efeito tensor, deixando a pele visivelmente mais firme e resistente, preservando o contorno e evitando o surgimento de rugas.</p>
          </div>
          <div class="card-formula">
            <h3>Antioxidante e anti-inflamatório</h3>
            <p>Reduz as inflamações, diminuindo a vermelhidão e a irritação, além de proteger contra os efeitos dos radicais livres que causam o envelhecimento da pele.</p>
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
  name: 'FormulaCreme',
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

.card-formula{
  border-radius: 5px;
  margin-bottom: 30px;
}

.card-formula h3{
  font: normal normal bold 18px/22px Open Sans;
  letter-spacing: 0px;
  color: #B84955;
  border-bottom: 1px solid #B84955;
  padding-bottom: 5px;
}

.card-formula p{
  font: normal normal normal 16px/20px Open Sans;
  letter-spacing: -0.64px;
  margin-top: 10px;
}

.direita .card-formula h3{
  text-align: right;
}

.direita .card-formula p{
  text-align: right;
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

  .card-formula h3{
    font-size: 16px;
    text-align: center!important;
  }

  .card-formula p{
    font-size: 14px;
    text-align: center!important;
  }
}
</style>