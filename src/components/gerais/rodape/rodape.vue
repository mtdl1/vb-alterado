<template>
    <div>
        <div class="container py-5">
            <div class="row infos pb-5">
                <div class="col-md-3">
                    <h4>Sobre Viva Beauty</h4>
                    <a href="https://www.vivabeauty.com.br/pages/quem-somos">
                        <p>Quem Somos</p>
                    </a>
                    <a href="https://blog.vivabeauty.com.br">
                        <p>Blog Viva Beauty.</p>
                    </a>
                    <a href="https://trabalheconosco.vagas.com.br/vitabe">
                        <p>Trabalhe Conosco</p>
                    </a>
                </div>
                <div class="col-md-3">
                    <h4>Links Úteis</h4>
                    <a href="https://www.vivabeauty.com.br/checkout/acesso">
                        <p>Rastreio</p>
                    </a>
                    <a href="https://www.vivabeauty.com.br/checkout/acesso">
                        <p>Meus Pedidos</p>
                    </a>
                    <a href="https://www.vivabeauty.com.br/pages/politica-de-privacidade">
                        <p>Política de Privacidade</p>
                    </a>
                    <a href="https://www.vivabeauty.com.br/pages/termos-e-condicoes">
                        <p>Termos e Condições</p>
                    </a>
                </div>
                <div class="col-md-3">
                    <h4>Atendimento ao cliente</h4>
                    <p>Segunda a sexta-feira das 8h às 18h.</p>
                    <p>(11) 4616-6343</p>
                    <p>Televendas: 0800 878 7023</p>
                    <a href="https://wa.me/5555114395632">
                        <p class="wp-rodape">Whats App</p>
                    </a>
                </div>
                <div class="col-md-3 text-center desk">
                    <img src="@/assets/img/icones/Não testamos em  animais.png" alt="">
                </div>
            </div>
            <div class="row mt-5 infos dois pb-4">
                <div class="col-md-4">
                    <h4>Meios de pagamento</h4>
                    <img src="@/assets/img/icones/bandeiras-cartoes.png" alt="">
                </div>
                <div class="col-md-4">
                    <h4>Siga nossas redes</h4>
                    <div class="row justify-content-between w-50">
                        <a href="https://facebook.com/vivabeautybrasil/"><img src="@/assets/img/icones/Facebook-Logo.svg" alt=""></a>
                        <a href="https://www.instagram.com/vivabeautybr/"><img src="@/assets/img/icones/Instagram-Logo.svg" alt=""></a>
                        <a href="https://www.tiktok.com/@vivabeautybr/"><img src="@/assets/img/icones/Tiktok-Logo.svg" alt=""></a>
                        <a href="https://www.youtube.com/@vivabeautybr"><img src="@/assets/img/icones/Youtube-Logo.svg" alt=""></a>
                    </div>
                </div>
                <div class="col-md-4">
                    <h4>Certificado e Segurança</h4>
                    <img src="@/assets/img/icones/SELOS.png" alt="">
                </div>
            </div>
        </div>
        <div class="faixa-final py-5">
            <div class="container">
                <div class="row justify-content-center mb-4">
                        <img src="@/assets/img/logo/logo viva.png" alt="">
                </div>
                <div class="row justify-content-center">
                    <p>Copyright © Vita Cosmeticos LTDA. Todos os direitos reservados.</p>
                    <p>Av. Onze de Agosto, 1451 - sala 707. Jardim Ribeiro, Valinhos/SP. CEP: 13270-190 | Brasil.</p>
                    <p>CNPJ: 39.256.537/0004-03</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Rodape',
}
</script>

<style scoped>
.infos{
    border-bottom: 1px solid #CCCCCC;
}

.infos:last-child{
    border-bottom: 0;
}

.infos h4{
    font: normal normal 800 18px/18px Open Sans;
    letter-spacing: -0.18px;
    color: #333333;
    margin-bottom: 20px;
}

.infos a{
    margin-bottom: 20px;
    display: block;
}

.infos a:last-child{
    margin-bottom: 0;
}

.infos p{
    font: normal normal normal 16px/18px Open Sans;
    letter-spacing: -0.16px;
    color: #333333;
    margin-bottom: 20px;
}

.infos p:last-child{
    margin-bottom: 0;
}

.infos.dois {
    justify-content: center;
}

.infos.dois .col-md-4 {
    text-align: center;
}

.infos.dois .col-md-4 {
    text-align: center;
}

.wp-rodape{
    background-color: #18A851;
    font-size: 16px!important;
    font-weight: bold!important;
    letter-spacing: -0.16px;
    color: #FFFFFF!important;
    width: fit-content;
    padding: 7px 50px;
    border-radius: 4px;
}

img{
    max-width: 100%;
}

.faixa-final{
    background-color: #F38599;
}

.faixa-final p{
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.16px;
    color: #FFFFFF;
    width: 100%;
    text-align: center;
}

/* responsivo */
@media (max-width: 500px){
    .infos{
        text-align: center;
    }

    .infos h4{
        text-align: center;
        margin-top: 25px;
    }

    .infos p{
        text-align: center;
    }

    .infos p:last-child{
        text-align: center;
    }

    .wp-rodape{
        margin: 0 auto;
    }

    .row.w-50{
        width: 100%!important;
    }

    .faixa-final p{
        text-align: center;
        font: normal normal normal 12px/16px Open Sans;
        letter-spacing: -0.12px;
    }
}
</style>