<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row justify-content-center">
        <div class="titulo">
          <h2>A melhor e mais completa fórmula de colágeno do mercado</h2>
          <p>O melhor tratamento para a sua pele</p>
        </div>
      </div>
      <div class="row lista-beneficios mt-5 align-items-center">
        <div class="col-md-6 text-center desk">
          <img
            class="rounded"
            src="@/assets/img/melhor-tratamento/Viva-Beauty-Home-Colageno-Pink-Lemoned.png"
            alt=""
          />
        </div>
        <div class="col-md-6 informacional">
          <p>
            Com ingredientes de alta tecnologia, o colágeno Skin Complex Plus
            Viva Beauty possui fórmula completa e exclusiva, acelerando os
            resultados em até 6x e mais:
          </p>
          <img
            src="@/assets/img/melhor-tratamento/Viva-Beauty-Home-Colageno-Pink-Lemoned.png"
            alt=""
            class="mob py-3 rounded"
          />
          <ul class="mt-3">
            <li>Reduz rugas e linhas de expressão</li>
            <li>Aumenta a elasticidade da pele</li>
            <li>Fortalece unhas e cabelos</li>
            <li>Potencializa a produção de ácido hialurônico</li>
            <li>Contribui com a saúde dos ossos</li>
            <li>Ameniza as ondulações das celulites</li>
            <li>Mantém a pele nutrida e hidratada</li>
            <li>Participa da formação de tecidos conjuntivos</li>
          </ul>
          <p class="mt-3">
            Além desses benefícios, é totalmente natural, sem corantes
            artificiais, sem açúcares e sem gorduras, tudo o que você precisa em
            um único produto para tratar pele, unhas, cabelos, rugas, flacidez,
            celulites e ossos!
          </p>
          <p class="mt-3"><strong>Sabores deliciosos:</strong> </p>
          <p class="sabores mt-4"> <span class="sab-pink">Pink Lemonade</span> <span class="yellow">Yellow Fruits</span> </p>
        </div>
      </div>
      <div class="row mt-5">
        <a href="/products/colageno" class="btn-cta-colageno">
          <p>Saiba Mais</p>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  name: "MelhorTratamento",
};
</script>

<style scoped>
.bg-alt{
  background-color: #FAFAFA;
}
img {
  max-width: 100%;
}
.titulo h2 {
  text-align: center;
  font: normal normal bold 32px/36px Open Sans;
  letter-spacing: -1.28px;
  color: #333333;
}

.titulo p {
  text-align: center;
  font: normal normal normal 18px/18px Open Sans;
  letter-spacing: 0px;
  color: #333333;
  margin-top: 10px;
}

.informacional p {
  font: normal normal normal 18px/24px Open Sans;
  letter-spacing: 0px;
  color: #333333;
}

.lista-beneficios ul {
  columns: 2;
}

.lista-beneficios ul li {
  list-style: disc;
  list-style: outside;
  margin-left: 20px;
  font: normal normal normal 18px/24px Open Sans;
  letter-spacing: -0.72px;
  color: #333333;
}

.lista-beneficios ul li::marker {
  color: #f38599;
}

.sabores span{
  font: normal normal bold 18px/24px Open Sans;
  letter-spacing: 0px;
  border-radius: 4px;
  /* display: block;
  width: fit-content; */
  padding: 10px 20px;
}

.sab-pink {
  background-color: #f38599;
  color: #fff;
}

.yellow {
  background-color: #F5D068;
  color: #951837;
}

.btn-cta-colageno {
    display: block;
    margin: 0 auto;
}

.btn-cta-colageno p {
    font: normal normal bold 24px/28px Helvetica;
    letter-spacing: 0px;
    color: #F38599;
    padding: 20px 120px;
    border: 1px solid;
    border-radius: 4px;
    border-color: #F38599;
    transition: 0.5s;
}

.btn-cta-colageno:hover {
    text-decoration: none;
}

.btn-cta-colageno:hover p {
    color: #fff;
    background-color: #F38599;
    transition: 0.5s;
}

/* reponsivo */
@media (max-width: 767px) {
  .titulo h2 {
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: -0.96px;
  }

  .titulo p {
    font-size: 16px;
  }

  .col-md-6 {
    padding: 0;
  }

  .informacional p {
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.64px;
  }

  .lista-beneficios ul {
    padding: 0 15px;
  }

  .lista-beneficios ul li {
    font: normal normal normal 16px/16px Open Sans;
    letter-spacing: -0.64px;
    margin-bottom: 10px;
    list-style-position: outside;
  }

  img {
    max-width: 100%;
  
  }
  .sabores span{
    font: normal normal bold 16px/20px Open Sans;
  }

  .btn-cta-colageno {
    width: 100%;
    text-align: center;
  }

  .btn-cta-colageno p{
    font: normal normal bold 20px/24px Helvetica;
  }

}
</style>