<template>
  <div>
    <a href="#produtos">
      <p class="btn-compre-agora">Compre Agora</p>
    </a>
  </div>
</template>

<script>
export default {
  name: 'BotaoCompreAgora',
}
</script>

<style scoped>
.btn-compre-agora {
  background-color: #18A851;
  color: #fff;
  padding: 15px 80px;
  border-radius: 5px;
  font: normal normal bold 24px/24px Helvetica;
  letter-spacing: -0.24px;
  cursor: pointer;
  width: fit-content;
  margin: 0 auto;
  transition: 0.5s;
}
.btn-compre-agora:hover {
  opacity: 0.8;
  transition: 0.5s;
}

/* em celular é um botao fixo na parte debaixo */
@media (max-width: 767px) {
  .btn-compre-agora {
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    margin: 0 auto;
    width: 100%;
    text-align: center;
    padding: 15px 0;
    border-radius: 0;
    z-index: 999;
  }
}
</style>