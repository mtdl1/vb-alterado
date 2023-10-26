<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>Três tipos de ácido hialurônico para uma pele mais <br class="mob"> firme e jovem</h2>
          <p>Conheça os ativos da fórmula do <br class="mob"> sérum Viva Beauty</p>
        </div>
      </div>
      <div class="row justify-content-center descricao mt-3 mb-5">
        <p>O sérum facial Viva Beauty é desenvolvido com três tipos de ácido hialurônico diferentes, que juntos, ajudam a reter a umidade, hidratam <br> profundamente e diminuem visivelmente as rugas e linhas de expressão, deixando a pele com aspecto mais jovem.</p>
      </div>
      <div class="row align-items-center">
        <div class="col-md-4 mob mb-4">
          <img src="@/assets/img/serum/ativos-formula/Viva-Beauty-Serum-Anti-Idade-Landing-Page-Ativos.png" alt="" class="rounded">
        </div>
        <div class="col-md-4">
          <div class="card-ativos">
            <h3>SYN HYCAN</h3>
            <p>Estimula a renovação do ácido hialurônico, melhora a firmeza e elasticidade da pele do rosto, promovendo maciez, suavidade e hidratação.</p>
          </div>
          <div class="card-ativos">
            <h3>ÁCIDO HIALURÔNICO HYA-ACT™ XS</h3>
            <p>Devido à capacidade de manter a umidade da pele, promove hidratação intensa e preenche rugas e linhas finas..</p>
          </div>
        </div>
        <div class="col-md-4 desk">
          <img src="@/assets/img/serum/ativos-formula/Viva-Beauty-Serum-Anti-Idade-Landing-Page-Ativos.png" alt="" class="rounded">
        </div>
        <div class="col-md-4">
          <div class="card-ativos direita">
            <h3>ÁCIDO HIALURÔNICO HYA-ACT™ S</h3>
            <p>Fortalece a barreira natural da pele, retendo a umidade e reduzindo a vermelhidão, além de aumentar a hidratação em até 77%..</p>
          </div>
          <div class="card-ativos direita">
            <h3>ÁCIDO HIALURÔNICO HYA-ACT™ M</h3>
            <p>Proporciona aumento da hidratação em apenas uma hora, formando uma barreira protetora na pele para reter a umidade..</p>
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
  name: 'AtivosFormula',
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

.col-md-4 .card-ativos:first-child{
  margin-bottom: 30px;
}

.card-ativos h3{
  font: normal normal bold 18px/22px Open Sans;
  letter-spacing: -0.72px;
  color: #F38599;
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
  background-color: #F38599;
  margin-left: 10px;
  border-radius: 4px;
}

img{
  max-width: 100%;
}

.card-ativos.direita h3{
  justify-content: start;
}

.card-ativos.direita h3::after{
  display: none;
  border-radius: 4px;
}

.card-ativos.direita h3::before{
  content: "";
  display: inline-block;
  width: 25px;
  height: 15px;
  background-color: #F38599;
  margin-right: 10px;
  border-radius: 4px;
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

@media (max-width: 767px) {
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p{
    font-size: 16px;
  }

  .descricao{
    margin: 15px 0!important;
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
    background-color: #F38599;
    margin-right: 10px;
    border-radius: 4px;
  }
  .card-ativos p{
    text-align: left;
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.64px;
  }
}
</style>