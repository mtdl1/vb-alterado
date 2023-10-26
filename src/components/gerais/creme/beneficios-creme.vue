<template>
    <div class="bg-alt">
        <div class="container">
            <div class="row justify-content-center">
                <div class="titulo">
                    <h2>7 ativos reunidos para <br class="mob"> uma pele de porcelana</h2>
                    <p>A tecnologia cosmética em seu favor</p>
                </div>
            </div>
            <div class="row my-5">
                <div class="col-md-4 desk">
                    <img src="@/assets/img/creme/ativos/Viva-Beauty-Creme-Hidratante-Landing-Page-7-Ativos.png" alt="">
                </div>
                <div class="col-md-8 info-ativos">
                    <p>Desenvolvido com Miniporyl, ativo altamente eficiente na diminuição dos poros, o creme facial Viva Beauty também possui Hydrovance, LDP White, D-Pantenol, óleo de coco e esqualano, combinação ideal para potencializar os efeitos da hidratação,além da ação antioxidante e anti-inflamatória. E o queridinho Rice Silk, forma uma camada de proteção instantânea sobre a pele, o resultado? Uma pele de porcelana sem sair de casa.</p>
                </div>

                <div class="col mob mt-5">
                    <img src="@/assets/img/creme/ativos/Viva-Beauty-Creme-Hidratante-Landing-Page-7-Ativos.png" alt="">
                </div>

            </div>
            <div class="row">
                <div class="col-4 col-md-2">
                    <img src="@/assets/img/beneficios-espuma/formula-vegana.svg" alt="" class="img-fluid">
                    <p>Fórmula vegana</p>
                </div>
                <div class="col-4 col-md-2">
                    <img src="@/assets/img/beneficios-espuma/Cruelty free.svg" alt="" class="img-fluid">
                    <p>Cruelty free</p>
                </div>
                <div class="col-4 col-md-2">
                    <img src="@/assets/img/beneficios-espuma/Sem parabenos.svg" alt="" class="img-fluid">
                    <p>Sem parabenos</p>
                </div>
                <div class="col-4 col-md-2">
                    <img src="@/assets/img/beneficios-espuma/SEM SULFATOS.svg" alt="" class="img-fluid">
                    <p>Sem sulfatos</p>
                </div>
                <div class="col-4 col-md-2">
                    <img src="@/assets/img/beneficios-espuma/SEM SILICONE.svg" alt="" class="img-fluid">
                    <p>Sem silicone</p>
                </div>
                <div class="col-4 col-md-2">
                    <img src="@/assets/img/beneficios-espuma/SEM PETROLATOS.svg" alt="" class="img-fluid">
                    <p>Sem petrolatos</p>
                </div>
            </div>
            <botao-compre-agora class="pt-5 desk" />
        </div>
    </div>
</template>

<script>
import botaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue'
    export default {
        components: { botaoCompreAgora },
        name: 'BeneficiosCreme',
    }
</script>

<style scoped>
.bg-alt {
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

img{
    max-width: 100%;
}

.col-md-2 {
    text-align: center;
}

p{
    text-align: center;
    font: normal normal bold 18px/22px Open Sans;
    letter-spacing: 0px;
    color: #B84955;
    margin-top: 13px;
}

.info-ativos p{
    font: normal normal normal 16px/24px Open Sans;
    letter-spacing: 0px;
    color: #545454;
    text-align: left;
    margin-top: 0;
}

@media(max-width: 768px) {

    .titulo h2{
        font: normal normal bold 24px/26px Open Sans;
        letter-spacing: -0.96px;
    }

    .titulo p{
        font-size: 16px;
    }

    .col-4{
        margin-bottom: 20px;
    }

    .col-4:nth-child(n+3):nth-child(-n+6){
        margin-bottom: 0;
    }

    p{
        font: normal normal bold 18px/18px Open Sans;
        letter-spacing: 0px;
    }
}
</style>