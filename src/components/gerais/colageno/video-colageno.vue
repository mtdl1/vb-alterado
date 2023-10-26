<template>
  <div class="bg-alt">
    <div class="container">
      <div class="row">
        <div class="col-md-5">
          <h3>Viva Beauty é o <br> anti-idade das blogueiras!</h3>
          <p><strong>O Skin Complex PLUS é o Tratamento Anti-Idade 7 em 1!</strong> Sua fórmula contém 12 ativos poderosos, entre eles, colágeno Verisol®, ácido hialurônico, silício orgânico, biotina, ácido pantotênico, fibras, vitaminas e minerais essenciais para tratar pele, cabelos, unhas, flacidez, ossos, rugas e celulites!</p>
        </div>
        <div class="col-md-7">
          <iframe class="rounded" width="100%" height="315" src="https://www.youtube.com/embed/fd9hxqNh62s?si=9AIr3cVEgYpdEzrx" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'VideoColageno',
}
</script>

<style scoped>
.bg-alt{
  background-color: #FFFCFD;
}

h3{
  font: normal normal bold 32px/36px Open Sans;
  letter-spacing: 0px;
  color: #333333;
  margin-bottom: 30px;
}

p{
  font: normal normal normal 18px/24px Open Sans;
  letter-spacing: -0.72px;
  color: #333333;
}

p strong{
  font: normal normal bold 18px/24px Open Sans;
  letter-spacing: -0.72px;
  color: #333333;
}

/* responsivo */
@media (max-width: 767px) {
  h3{
    text-align: center;
    font: normal normal bold 24px/26px Open Sans;
    letter-spacing: 0px;
    color: #202020;
  }
  p{
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.64px;
    color: #202020;
    margin-bottom: 30px;
  }
  p strong{
    font: normal normal bold 16px/20px Open Sans;
    letter-spacing: -0.64px;
    color: #202020;
  }
}
</style>