<template>
  <div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>A melhor e mais completa fórmula do mercado</h2>
          <p>Com ingredientes de alta tecnologia, o colágeno Skin Complex Plus Viva Beauty <strong>possui fórmula completa e exclusiva, acelerando os <br> resultados em até 6x!</strong> Além disso, é totalmente natural, sem corantes artificiais, sem açúcares e sem gorduras, tudo o que você precisa em <br> um único produto <strong>para tratar pele, unhas, cabelos, rugas, flacidez, celulites e ossos!</strong></p>
        </div>
      </div>

      <div class="row align-items-center mt-5">
        <div class="col-md-4 mob mb-4">
          <img src="@/assets/img/colageno/formula/viva-beauty-colageno.png" alt="">
        </div>
        <div class="col-md-4">
          <div class="card-ativos">
            <h3>COLÁGENO VERISOL®</h3>
            <p>Único com aprovação da ANVISA para tratamento da pele, <strong>possui peptídeos bioativos de rápida absorção que potencializam os resultados</strong>, reconstruindo a estrutura celular, estimulando a metabolização do colágeno e promovendo melhoria na firmeza, elasticidade e redução das rugas e linhas de expressão.</p>
          </div>
          <div class="card-ativos">
            <h3>SILÍCIO ORGÂNICO (NUTRICOLIN®)</h3>
            <p>Com eficácia reconhecida pela ANVISA, é conhecido como “proteína da beleza” por atuar na síntese de colágeno, elastina e queratina, <strong>responsáveis pela saúde e beleza da pele, cabelos e unhas,</strong> favorecendo a firmeza, resistência, brilho e fortalecimento. Também atua na formação dos ossos e dos tecidos conjuntivos.</p>
          </div>
        </div>
        <div class="col-md-4 desk">
          <img src="@/assets/img/colageno/formula/viva-beauty-colageno.png" alt="">
        </div>
        <div class="col-md-4">
          <div class="card-ativos direita">
            <h3>ÁCIDO HIALURÔNICO</h3>
            <p>Atua na hidratação e renovação da pele, agindo de dentro para fora ao preencher os espaços vazios e reter a água nas células das camadas mais profundas, <strong>auxiliando na redução das linhas de expressão e rugas, além de promover mais elasticidade e resistência</strong>, promovendo um aspecto mais liso e jovem.</p>
          </div>
          <div class="card-ativos direita">
            <h3>ÁCIDO PANTOTÊNICO</h3>
            <p>Possui propriedades antioxidantes, cicatrizantes, anti-inflamatórias e alto poder hidratante, atrai e retém a umidade na pele, <strong>além de auxiliar na prevenção e suavização dos sinais de envelhecimento precoce, como rugas e linhas finas.</strong> Também contribui com a saúde e beleza dos cabelos e unhas.</p>
          </div>
        </div>
      </div>

      <div class="row justify-content-between mt-5">
        <ul>
          <li>Zero Glúten</li>
          <li>Zero Açúcares</li>
          <li>Zero Malto</li>
          <li>Fonte de Fibras</li>
          <li>Fonte de Biotina</li>
          <li>Vitaminas e Minerais</li>
          <li>Baixas calorias</li>
          <li>Zero Gordura</li>
        </ul>
      </div>

      <BotaoCompreAgora class="pt-5 desk" />

    </div>
  </div>
</template>

<script>
import BotaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue'
export default {
  components: { BotaoCompreAgora },
  name: 'FormulaColageno',
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

ul{
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
  list-style: none;
}

li{
  background-color: #F38599;
  padding: 10px 20px;
  font: normal normal bold 14px/18px Open Sans;
  letter-spacing: 0px;
  color: #FFFFFF;
  border-radius: 3px;
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

  .card-ativos h3{
    text-align: center;
    font: normal normal bold 18px/18px Open Sans;
    justify-content: center;
  }
  .card-ativos h3::after{
    display: none;
  }
  /* .card-ativos h3::before{
    content: "";
    display: inline-block;
    width: 25px;
    height: 15px;
    background-color: #F38599;
    margin-right: 10px;
  } */

  .card-ativos.direita h3::before{
    display: none;
  }

  .card-ativos.direita h3{
    justify-content: center;
  }

  .card-ativos p{
    text-align: center;
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.64px;
  }

  ul{
    justify-content: center;
    gap: 5px;
  }

  ul li{
    font: normal normal bold 11px/10px Open Sans;
    letter-spacing: 0px;
    color: #FFFFFF;
  }
}
</style>