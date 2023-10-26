<template>
  <div>
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>A forma mais simples de <br class="mob"> ter uma pele limpa e hidratada</h2>
          <p>Os melhores ativos em uma <br class="mob"> fórmula poderosa</p>
        </div>
      </div>
      <div class="row lista-beneficios mt-5 align-items-center">
        <div class="col-md-6 informacional">
          <p>Desenvolvida com silício, Plantcol e Extratos de Hamamélis e Centelha Asiática, a espuma de limpeza facial Viva Beauty trata a sua pele de fora para dentro, ao limpar profundamente, iluminar e hidratar, além de desacelerar o processo de envelhecimento, diminuir a vermelhidão e inflamação, mantendo a elasticidade da pele.</p>
          <img src="@/assets/img/espuma/formula-unica/Viva-Beauty-Espuma-Landing-Page-beneficios.jpg" alt="" class="mob py-3 rounded">
          <ul class="mt-3">
            <li>Limpa profundamente</li>
            <li>Acalma e desinflama</li>
            <li>Não resseca a pele</li>
            <li>Hidrata e ilumina</li>
            <li>Diminui vermelhidão e inflamação</li>
            <li>Aumenta a elasticidade</li>
            <li>Desacelera o envelhecimento</li>
            <li>Ajuda a prevenir acnes</li>
            <li>Desobstrui os poros</li>
            <li>Controla a oleosidade</li>
          </ul>
          <p class="mt-3">A espuma de limpeza facial Viva Beauty possui fórmula vegana, sem silicones, sulfatos, petrolatos e parabenos, garantindo cuidados delicados e eficientes.</p>
        </div>
        <div class="col-md-6 text-center desk">
          <img class="rounded" src="@/assets/img/espuma/formula-unica/Viva-Beauty-Espuma-Landing-Page-beneficios.jpg" alt="">
        </div>
      </div>
        <BotaoCompreAgora class="pt-5 desk"/>
    </div>
  </div>
</template>

<script>
import BotaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue'
export default {
  components: { BotaoCompreAgora },
  name: 'FormaSimplesEspuma',
}
</script>

<style scoped>

img{
  max-width: 100%;
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

.informacional p{
  font: normal normal normal 18px/24px Open Sans;
  letter-spacing: 0px;
  color: #333333;
}

.lista-beneficios ul{
  columns: 2;
}

.lista-beneficios ul li{
  list-style: disc;
  list-style: outside;
  margin-left: 20px;
  font: normal normal normal 18px/24px Open Sans;
  letter-spacing: -0.72px;
  color: #333333;
}

.lista-beneficios ul li::marker{
  color: #B84955;
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

  .col-md-6{
    padding: 0;
  }

  .informacional p{
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.64px;
  }

  .lista-beneficios ul {
    padding: 0 15px;
  }
  
  .lista-beneficios ul li{
    font: normal normal normal 16px/16px Open Sans;
    letter-spacing: -0.64px;
    margin-bottom: 10px;
    list-style-position: outside;
  }

  img{
    max-width: 100%;
  }
}
</style>