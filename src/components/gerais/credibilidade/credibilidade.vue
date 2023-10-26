<template>
 <div class="containerCredibilidade">
    <div class="container">
        <div class="row justify-content-center">
            <div class="col-6 col-md-3">
                <div class="row justify-content-center align-items-center">
                    <div class="col-3 col-md-3 text-center px-0">
                        <div :class="['img-selo parcelamento', {home: cor == 'home'}] " alt="Imagem de parcelamento em até 8x sem juros" title="Parcelamento em até 8x sem juros"></div>
                    </div>
                    <div class="col-9 col-md-9 pl-1">
                        <p>PARCELAMENTO EM <br> <strong>ATÉ {{ $store.state.qtdParcelas }}X SEM JUROS</strong></p>
                    </div>
                </div>
            </div>
            <div class="col-6 col-md-3">
                <div class="row justify-content-center align-items-center">
                    <div class="col-3 col-md-3 text-center px-0">
                        <div :class="['img-selo pagamento', {home: cor == 'home'}]" alt="Imagem de pagamento no PIX com +10% de desconto" title="Pagamento no PIX com +10% de desconto"></div>
                    </div>
                    <div class="col-9 col-md-9 pl-1">
                        <p>PAGAMENTO NO PIX <br> <strong>+ {{ $store.state.descontoPix }}% DE DESCONTO</strong></p>
                    </div>
                </div>
            </div>
            <div class="col-6 col-md-3">
                <div class="row justify-content-center align-items-center">
                    <div class="col-3 col-md-3 text-center px-0">
                        <div :class="['img-selo envio', {home: cor == 'home'}]" alt="Imagem de envio em até 24h para São Paulo" title="Envio em até 24h para São Paulo"></div>
                    </div>
                    <div class="col-9 col-md-9 pl-1">
                        <p><strong>ENVIO IMEDIATO</strong> <br> PARA TODO BRASIL</p>
                    </div>
                </div>
            </div>
            <div class="col-6 col-md-3">
                <div class="row justify-content-center align-items-center">
                    <div class="col-3 col-md-3 text-center px-0">
                        <div :class="['img-selo frete', {home: cor == 'home'}]" alt="Imagem de frete grátis para todo o Brasil" title="Frete grátis para todo o Brasil"></div>
                    </div>
                    <div class="col-9 col-md-9 pl-1">
                        <p><strong>FRETE GRÁTIS</strong> <br> ACIMA DE R$ {{ $store.state.freteGratis }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
 </div>
</template>

<script>
    export default {
        name: 'Credibilidade',
        props: ['cor']
    }
</script>

<style scoped>

    .containerCredibilidade {
        background-color: #FAFAFA;
    }

    .container {
        padding: 31px 0 23px;
    }

    p {
        font: normal normal normal 14px/18px Open Sans;
        letter-spacing: -0.56px;
        color: #000000;
    }

    p strong {
        font: normal normal bold 14px/18px Open Sans;
        letter-spacing: -0.56px;
        color: #000000;
    }

    .img-selo {
        width: 58px;
        height: 58px;
    }

    .home {
        background-color: #f38599;
    }

    .parcelamento {
        mask: url("../../../assets/img/credibilidade/ICONE-8x.png") no-repeat center / contain;
        -webkit-mask: url("../../../assets/img/credibilidade/ICONE-8x.png") no-repeat center / contain;
    }

    .pagamento {
        mask: url("../../../assets/img/credibilidade/ICONE-PIX.png") no-repeat center / contain;
        -webkit-mask: url("../../../assets/img/credibilidade/ICONE-PIX.png") no-repeat center / contain;
    }

    .envio {
        mask: url("../../../assets/img/credibilidade/ICONE-ENVIO.png") no-repeat center / contain;
        -webkit-mask: url("../../../assets/img/credibilidade/ICONE-ENVIO.png") no-repeat center / contain;
    }

    .frete {
        mask: url("../../../assets/img/credibilidade/ICONE-FRETE.png") no-repeat center / contain;
        -webkit-mask: url("../../../assets/img/credibilidade/ICONE-FRETE.png") no-repeat center / contain;
    }

    @media(max-width: 768px) {
        p {
            font: normal normal normal 12px/14px Open Sans;
            letter-spacing: -0.48px;
        }

        p strong {
            font: normal normal bold 12px/14px Open Sans;
            letter-spacing: -0.48px;
        }

        .col-6.col-md-3, .col-9.col-md-9 {
            padding-right: 0 !important;
        }

        .col-6.col-md-3 {
            margin-bottom: 10px;
        }

        .img-selo {
            width: 40px;
            height: 40px;
        }
    }
</style>