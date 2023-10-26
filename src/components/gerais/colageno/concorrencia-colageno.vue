
<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo col">
          <h2>Viva Beauty x Concorrência</h2>
        </div>
      </div>
      <div class="row mt-5 align-items-center">
        <div class="col-12 mob mb-5">
          <img src="@/assets/img/colageno/concorrencia/Viva-Beauty-concorrencia.png" alt="">
        </div>
        <div class="col-6 col-md-3">
          <ul>
            <li>Colágeno Verisol® <img src="@/assets/img/icones/CHECK 6.svg" alt=""></li>
            <li>Ácido Hiaulônico <img src="@/assets/img/icones/CHECK 6.svg" alt=""></li>
            <li>Silício Orgânico (Nutricolin®) <img src="@/assets/img/icones/CHECK 6.svg" alt=""></li>
            <li>Vitaminas<img src="@/assets/img/icones/CHECK 6.svg" alt=""></li>
            <li>Minerais <img src="@/assets/img/icones/CHECK 6.svg" alt=""></li>
            <li>Rico em Biotina <img src="@/assets/img/icones/CHECK 6.svg" alt=""></li>
            <li>Ácido Pantotênico <img src="@/assets/img/icones/CHECK 6.svg" alt=""></li>
            <li>Fonte de Fibras <img src="@/assets/img/icones/CHECK 6.svg" alt=""></li>
          </ul>
        </div>
        <div class="col-md-6 desk">
          <img src="@/assets/img/colageno/concorrencia/Viva-Beauty-concorrencia.png" alt="">
        </div>
        <div class="col-6 col-md-3 direita">
          <ul>
            <li> <img src="@/assets/img/icones/CHECK 6 desativado.png" alt=""> Colágeno Hidrolisado </li>
            <li> <img src="@/assets/img/icones/CHECK 6 desativado.png" alt=""> Sem Ácido Hiaulônico </li>
            <li> <img src="@/assets/img/icones/CHECK 6 desativado.png" alt=""> Sem vitaminas </li>
            <li> <img src="@/assets/img/icones/CHECK 6 desativado.png" alt=""> Poucos minerais </li>
          </ul>
        </div>
      </div>
      <div class="row justify-content-center mt-5 desk">
        <botaoCompreAgora />
      </div>
    </div>
  </div>
</template>

<script>
import botaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue'
export default {
  components: { botaoCompreAgora },
  name: 'ConcorrenciaColageno',
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

ul li{
  text-align: right;
  margin-bottom: 15px;
}

ul li:last-child{
  margin-bottom: 0;
}

ul li img{
  margin-left: 10px;
}

.direita ul li{
  text-align: left;
}

img{
  max-width: 100%;
}

@media (max-width: 991px){
  .titulo h2{
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p{
    font-size: 16px;
  }
  
  ul li{
    display: flex;
    align-items: center;
    justify-content: flex-end;
    font: normal normal normal 14px/14px Open Sans;
    letter-spacing: -0.28px;
    color: #333333;
  }
  
  .direita ul li{
    justify-content: flex-start;
  }

  .direita ul li img{
    margin-left: 0;
    margin-right: 10px;
  }

  .row.mt-5.align-items-center{
    align-items: flex-start!important;
  }
}
</style>