<template>
  <div class="container">
    <div class="row justify-content-center">
      <div class="titulo">
        <h2>Sérum facial Viva Beauty: <br> fórmula única <br class="mob"> para uma pele perfeita.</h2>
        <p>Tudo o que a sua pele precisa está aqui</p>
      </div>
    </div>
    <div class="row pt-5">
      <div class="col-md-4 mob mb-4">
        <img src="@/assets/img/serum/formula-unica/Viva-Beauty-Serum-Anti-Idade-Landing-Page-A-formula-unica.png" alt="">
      </div>
      <div class="col-md-4">
        <div class="card-formula">
          <h3>Melhora a elasticidade da pele</h3>
          <p>Efeito modelador e firmador visível com pele mais umedecida, <strong>melhora a firmeza da pele facial</strong> e aumenta a umidade, maciez e suavidade da pele.</p>
        </div>
        <div class="card-formula">
          <h3>Reduz a aparência das rugas</h3>
          <p>Devido à absorção nas camadas mais profundas da pele, proporciona tratamento de dentro para fora, <strong>diminuindo as linhas finas de expressão e rugas.</strong></p>
        </div>
      </div>
      <div class="col-md-4 desk">
        <img src="@/assets/img/serum/formula-unica/Viva-Beauty-Serum-Anti-Idade-Landing-Page-A-formula-unica.png" alt="">
      </div>
      <div class="col-md-4 last">
        <div class="card-formula">
          <h3>Fortalece a barreira protetora</h3>
          <p>Atua como uma esponja nas camadas superficiais da pele, <strong>formando uma película protetora e fornecendo hidratação imediata</strong>..</p>
        </div>
        <div class="card-formula">
          <h3>Aumenta a hidratação e umidade</h3>
          <p><strong>Forma uma barreira de proteção natural na pele e acalma a vermelhidão</strong>. Estudos comprovam que, combinado ao HYA-ACT ™ M há um aumento de até 77% na hidratação da pele..</p>
        </div>
      </div>
    </div>

    <BotaoCompreAgora class="pb-5 desk" />

  </div>
</template>

<script>
import BotaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue'
export default {
  components: { BotaoCompreAgora },
  name: 'FormulaUnica',
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
  background-color: #FAFAFA;
  border-radius: 5px;
  padding: 10px 30px;
  margin-bottom: 30px;
}

.card-formula h3{
  text-align: center;
  font: normal normal bold 18px/22px Open Sans;
  letter-spacing: 0px;
  color: #F38599;
  border-bottom: 1px solid #F38599;
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
    margin-bottom: 15px;
  }

  .card-formula h3{
    font-size: 16px;
  }

  .card-formula p{
    font-size: 14px;
  }
}
</style>