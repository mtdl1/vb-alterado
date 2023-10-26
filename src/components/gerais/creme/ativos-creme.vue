<template>
  <div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>A combinação de sete <br class="mob"> ativos que <br class="desk"> a sua pele precisa <br class="mob"> em um só produto</h2>
          <p>Resultados surpreendentes</p>
        </div>
      </div>
      <div class="row mt-5">
        <ul>
          <li>
            <h3>RICE SILK:</h3>
            <p>Absorve a oleosidade em excesso, é benéfico para peles acneicas e oleosas, deixando a textura aveludada e uniforme com acabamento mate.</p>
          </li>
          <li>
            <h3>MINIPORYL</h3>
            <p>Com ação adstringente, diminui a aparência dos poros, aumenta a luminosidade e reduz a quantidade de sebo em excesso.</p>
          </li>
          <li> 
            <h3>D - PANTENOL</h3>
            <p>Devido à capacidade de reter a umidade, hidrata a pele e auxilia na prevenção do envelhecimento precoce, renovação da pele e cicatrização.</p>
          </li>
          <li>
            <h3>HYDROVANCE</h3>
            <p>Hidratante intenso com toque seco, nutre, revitaliza e deixa a pele com aspecto aveludado.</p>
          </li>
          <li>
            <h3>LDP WHITE:</h3>
            <p>Preenchimento funcional, com efeito antienvelhecimento, que auxilia na redução de pequenas rugas, diminuindo imperfeições com toque seco</p>
          </li>
          <li>
            <h3>ESQUALANO</h3>
            <p>Possui ação hidratante e antienvelhecimento, promove a renovação celular, aumento da elasticidade e a redução de rugas.</p>
          </li>
          <li>
            <h3>ÓLEO DE COCO</h3>
            <p>Com propriedades antimicrobianas, inibe o crescimento de fungos e bactérias, reduz inflamações, hidrata, cicatriza, lubrifica e reduz rachaduras e ressecados.</p>
          </li>
          <li>
            <h3></h3>
            <p></p>
          </li>
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
  name: 'AtivosCreme',
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
  font: normal normal normal 18px/22px Open Sans;
  letter-spacing: 0px;
  color: #333333;
  margin-top: 10px;
}

ul{
  columns: 2;
}

ul li{
  margin-bottom: 30px;
}

ul li h3{
  font: normal normal bold 18px/22px Open Sans;
  letter-spacing: -0.72px;
  color: #B84955;
}

ul li h3::before{
  content: "";
  display: inline-block;
  width: 25px;
  height: 15px;
  background-color: #B84955;
  margin-right: 10px;
  border-radius: 4px;
}

ul li:last-child h3::before{
  display: none;
}

ul li p{
  font: normal normal normal 16px/20px Open Sans;
  letter-spacing: -0.32px;
  color: #545454;
}

/* responsivo */
@media (max-width: 767px) {
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p{
    font-size: 16px;
  }
  
  ul{
    columns: 1;
  }

  ul li:nth-child(7n), ul li:nth-child(8n){
    margin-bottom: 0px;
  }
}
</style>