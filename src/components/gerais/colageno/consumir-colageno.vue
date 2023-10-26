<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>Consumir o Viva Beauty é prático e delicioso</h2>
        </div>
      </div>
      <div class="row mt-5">
        <div class="col-md-6">
          <TabelaColageno />
        </div>
        <div class="col-md-6">

          <ul class="nav nav-tabs">
            <li class="pink-lemonade">
              <a data-toggle="tab" href="#pinkcontent" class="active">Pink Lemonade</a>
            </li>
            <li class="yellow-fruits">
              <a data-toggle="tab" href="#yellowcontent">Yellow Fruits</a>
            </li>
          </ul>

          <div class="tab-content mt-4">
            <div id="pinkcontent" class="tab-pane fade in active show">
              <div class="condensed pink">
                <h3>Pink Lemonade</h3>
                <p><strong>Ingredientes:</strong> Polidextrose, Peptídeos Bioativos de Colágeno Hidrolisado com peso molecular médio de 2kDa (Verisol©), Hialuronato de Sódio obtido pela fermentação de Streptococcus zoopidemicus (Ácido Hialurônico), Ácido Ascórbico (Vitamina C), D-Pantotenato de Cálcio (Ácido Pantotênico), Bisglicinato de Zinco (Zinco), Cloridrato de piridoxina (Vitamina B6), Sulfato de Manganês (Manganês), Acetato de Retinol (Vitamina A), Sulfato Cúprico (Cobre), D-Biotina (Biotina), Cianocobalamina (Vitamina B12), Ácido Ortosilícico estabilizado em cloreto de coline (Silício), Beterraba em pó, Acidulante, Ácido Cítrico, Aromas naturais de limão e framboesa, Edulcorante, glicosídeos de esteviol e Antiumectante Dióxido de Silício.</p>
                <p><strong>NÃO CONTEM GLÚTEM.</strong></p>
                <p><strong>ALÉRGICOS:</strong> PODE CONTER LEITE, PEIXE E SOJA. </p>
                <p>"Por conter ingredientes naturais, este produto pode sofrer pequenas variações sensoriais de cor, sabor e odor conforme safra".</p>
              </div>
              <img src="@/assets/img/colageno/como-consumir/Viva-Beauty-Tabela-Nutricional-Colageno-Pink-Lemoned.png" alt="" class="mt-3">
            </div>
            <div id="yellowcontent" class="tab-pane fade">
              <div class="condensed yellow">
                <h3>Yellow Fruits</h3>
                <p><strong>Ingredientes:</strong> Polidextrose, Peptídeos bioativos de colágeno hidrolisado com peso molecular médio de 2kDa (Verisol®), Hialuronato de sódio obtido pela fermentação de streptococcus zoopidemicus (Ácido hialurônico), Ácido ascórbico (Vitamina C), D-Pantotenato de cálcio (Ácido pantotênico), Bisglicinato de zinco (Zinco), Cloridrato de piridoxina (Vitamina B6), Sulfato de manganês (Manganês), Acetato de retinol (Vitamina A), Sulfato cúprico (Cobre), D-Biotina (biotina), Cianocobalamina (Vitamina B12), Ácido ortosilícico estabilizado em cloreto de colina (Silício), Acidulante ácido cítrico, Aroma natural de Baunilha, Aroma idêntico ao natural de Pêssego, Aroma idêntico ao natural de Manga, Edulcorante glicosídeos de esteviol, e Antiumectante dióxido de silício.</p>
                <p><strong>NÃO CONTEM GLÚTEM.</strong></p>
                <p><strong>ALÉRGICOS:</strong> PODE CONTER LEITE, PEIXE E SOJA. </p>
                <p>"Por conter ingredientes naturais, este produto pode sofrer pequenas variações sensoriais de cor, sabor e odor conforme safra".</p>
              </div>
              <img src="@/assets/img/colageno/como-consumir/Viva-Beauty-Tabela-Nutricional-Colageno-Yellow-Fruits.png" alt="" class="mt-3">
            </div>
          </div>

        </div>
      </div>

      <div class="row passos-consumo mt-5 justify-content-between">
        <div class="col-md-6">
          <img src="@/assets/img/icones/SCOOP.svg" alt="">
          <p>Em um copo ou coqueteleira misturar 10g <strong>( 1 scoop) em 200 ml de água.</strong></p>
        </div>
        <div class="col-md-6">
          <img src="@/assets/img/icones/copo.svg" alt="">
          <p><strong>Misture com o auxílio de uma colher</strong> e pronto, é só tomar sua dose diária de Viva Beauty!</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TabelaColageno from './components/tabela-colageno.vue'
export default {
  name: 'ConsumirColageno',
  components: { TabelaColageno },
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

.nav-tabs{
  border: 0;
}

.nav.nav-tabs li {
    width: 48%;
    text-align: center;
}

.nav.nav-tabs {
    justify-content: space-between;
}

a{
  display: block;
  padding: 15px 0;
}

.pink-lemonade{
  border: 1px solid #F38599;
  border-radius: 4px;
}

.pink-lemonade a.active{
  background-color: #F38599;
  color: #fff;
}

.pink-lemonade a.active {
  color: #fff;
}

.yellow-fruits{
  border: 1px solid #F2C560;
  border-radius: 4px;
}

.yellow-fruits a.active{
  background-color: #F2C560;
}

.pink-lemonade a {
    font: normal normal bold 20px/24px Open Sans;
    letter-spacing: -0.4px;
    color: #F38599;
}

.yellow-fruits a{
  font: normal normal 800 20px/24px Open Sans;
  letter-spacing: -0.4px;
  color: #951837;
}

.condensed {
    border-radius: 4px;
    padding: 20px;
}

.condensed.pink{
  border: 1px solid #F38599;
}

.condensed.yellow{
  border: 1px solid #F2C560;
}

.tab-pane h3 {
    width: fit-content;
    padding: 10px 24px;
    font: normal normal bold 18px/20px Open Sans;
    letter-spacing: 0px;
    border-radius: 4px;
    margin-bottom: 15px;
}

.condensed.pink h3{
  background-color: #F38599;
  color: #fff;
  transition: 0.4s;
}

.condensed.yellow h3{
  background-color: #F2C560;
}

.condensed p{
  font: normal normal normal 14px/18px Open Sans;
  letter-spacing: -0.56px;
  color: #333333;
  margin-bottom: 15px;
}

.condensed strong{
  font: normal normal bold 14px/18px Open Sans;
  letter-spacing: -0.56px;
  color: #333333;
}

img{
  max-width: 100%;
}

.passos-consumo {
    padding: 0 15px;
}

.passos-consumo .col-md-6 {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 50px;
    border: 1px solid #F38599;
    border-radius: 4px;
    max-width: 49%;
}

.passos-consumo .col-md-6 p {
    padding-left: 30px;
    font: normal normal normal 20px/24px Open Sans;
    letter-spacing: -0.8px;
    color: #333333;
}

.passos-consumo .col-md-6 p strong {
    font: normal normal bold 20px/24px Open Sans;
    letter-spacing: -0.8px;
    color: #333333;
}

/* responsivo */
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

@media (max-width: 767px) {
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .tab-pane h3 {
    font: normal normal bold 12px/20px Open Sans;
    letter-spacing: -0.48px;
    padding: 5px 10px;
  }

  .nav-tabs{
    margin-top: 25px;
  }

  .nav-tabs li a{
    font: normal normal bold 12px/7px Open Sans;
    letter-spacing: -0.24px;
  }

  .condensed p{
    font: normal normal normal 12px/16px Open Sans;
    letter-spacing: -0.48px;
  }

  .condensed p strong{
    font: normal normal bold 12px/16px Open Sans;
    letter-spacing: -0.48px;
  }

  .passos-consumo{
    margin-top: 15px!important;
  }

  .passos-consumo .col-md-6 {
    padding: 20px 10px;
    max-width: 100%;
  }

  .passos-consumo .col-md-6:first-child img {
    max-width: 45px;
  }

  .passos-consumo .col-md-6:last-child img {
    max-width: 26px;
  }

  .passos-consumo .col-md-6 p {
    padding-left: 20px;
  }

  .passos-consumo .col-md-6:first-child {
    margin-bottom: 15px;
  }

  .passos-consumo .col-md-6 p {
    font: normal normal normal 12px/16px Open Sans;
    letter-spacing: -0.48px;
  }

  .passos-consumo .col-md-6 p strong {
    font: normal normal bold 12px/16px Open Sans;
    letter-spacing: -0.48px;
  }
  
}

</style>