<template>
    <div class="container">
        <div class="row justify-content-center" id="perguntas" >
            <div class="accordion w-100" id="faq">
                <div class="card">
                    <div class="card-header" id="faqhead1">
                        <a href="#" class="btn btn-header-link" data-toggle="collapse" data-target="#faq1" aria-expanded="true" aria-controls="faq1">O que é o creme facial Viva Beauty?</a>
                    </div>

                    <div id="faq1" class="collapse show" aria-labelledby="faqhead1" data-parent="#faq">
                        <div class="card-body">
                            <p>O creme facial Viva Beauty limpa profundamente, ilumina e hidrata, além de desacelerar o processo de envelhecimento precoce da pele. Também mantém a elasticidade, diminui a vermelhidão, irritação e inflamação.</p>
                        </div>
                    </div>
                </div>

                <div class="card">
                    <div class="card-header" id="faqhead2">
                        <a href="#" class="btn btn-header-link collapsed" data-toggle="collapse" data-target="#faq2" aria-expanded="true" aria-controls="faq2">Como usar o creme facial Viva Beauty?</a>
                    </div>

                    <div id="faq2" class="collapse" aria-labelledby="faqhead2" data-parent="#faq">
                        <div class="card-body">
                            <p>Com a pele limpa e seca, aplique uma pequena quantidade do produto no rosto e pescoço em movimentos de dentro para fora, até completa absorção.</p>
                        </div>
                    </div>
                </div>

                <div class="card">
                    <div class="card-header" id="faqhead3">
                        <a href="#" class="btn btn-header-link collapsed" data-toggle="collapse" data-target="#faq3" aria-expanded="true" aria-controls="faq3">Posso aplicar o creme facial no pescoço?</a>
                    </div>

                    <div id="faq3" class="collapse" aria-labelledby="faqhead3" data-parent="#faq">
                        <div class="card-body">
                            <p>Sim! Você pode utilizar o creme facial na região do pescoço para potencializar os benefícios do produto.</p>
                        </div>
                    </div>
                </div>

                <div class="card">
                    <div class="card-header" id="faqhead5">
                        <a href="#" class="btn btn-header-link collapsed" data-toggle="collapse" data-target="#faq5" aria-expanded="true" aria-controls="faq5">O creme facial é vegano? Possui parabenos, silicones e petrolatos?</a>
                    </div>

                    <div id="faq5" class="collapse" aria-labelledby="faqhead5" data-parent="#faq">
                        <div class="card-body">
                            <p>Sim! A fórmula é vegana, cruelty free e não possui petrolatos, parabenos, silicones e sulfatos.</p>
                        </div>
                    </div>
                </div>
                
                <div class="card">
                    <div class="card-header" id="faqhead7">
                        <a href="#" class="btn btn-header-link collapsed" data-toggle="collapse" data-target="#faq7" aria-expanded="true" aria-controls="faq7">Em quanto tempo verei resultados?</a>
                    </div>

                    <div id="faq7" class="collapse" aria-labelledby="faqhead7" data-parent="#faq">
                        <div class="card-body">
                            <p>Como as características de cada organismo e pele são individuais, o tempo de aparecimento dos resultados varia de pessoa para pessoa.</p>
                        </div>
                    </div>
                </div>
                
                <div class="card">
                    <div class="card-header" id="faqhead8">
                        <a href="#" class="btn btn-header-link collapsed" data-toggle="collapse" data-target="#faq8" aria-expanded="true" aria-controls="faq8">Em quanto tempo verei resultados?</a>
                    </div>

                    <div id="faq8" class="collapse" aria-labelledby="faqhead8" data-parent="#faq">
                        <div class="card-body">
                            <p>Como as características de cada organismo e pele são individuais, o tempo de aparecimento dos resultados varia de pessoa para pessoa.</p>
                        </div>
                    </div>
                </div>

                <div class="card">
                    <div class="card-header" id="faqhead4">
                        <a href="#" class="btn btn-header-link collapsed" data-toggle="collapse" data-target="#faq4" aria-expanded="true" aria-controls="faq4">Qual prazo de entrega?</a>
                    </div>

                    <div id="faq4" class="collapse" aria-labelledby="faqhead4" data-parent="#faq">
                        <div class="card-body">
                            <p>O Viva Beauty é despachado em média de 24h úteis após aprovação do pagamento.</p>
                            <p><strong>Segue prazo médio para entrega:</strong></p>
                            <ul>
                                <li>Região Sudeste - de 1 a 8 dias úteis</li>
                                <li>Região Sul - de 1 a 9 dias úteis</li>
                                <li>Região Centro-Oeste - de 1 a 10 dias úteis</li>
                                <li>Região Nordeste - de 2 a 14 dias úteis</li>
                                <li>Região Norte - de 3 a 15 dias úteis</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="card">
                    <div class="card-header" id="faqhead6">
                        <a href="#" class="btn btn-header-link collapsed" data-toggle="collapse" data-target="#faq6" aria-expanded="true" aria-controls="faq6">Quando terei direito ao FRETE GRÁTIS anunciado no site?</a>
                    </div>

                    <div id="faq6" class="collapse" aria-labelledby="faqhead6" data-parent="#faq">
                        <div class="card-body">
                            <p>O FRETE GRÁTIS é válido apenas para pedidos acima de R$ 199,00 para os demais, será cobrado o valor fixo de R$ 9,90 para qualquer região do país.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <BotaoCompreAgora class="pt-5 desk"/>

    </div>
</template>

<script>
import BotaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue';
    export default {
        components: { BotaoCompreAgora },
            name: 'PerguntasFrequentesCreme',

        data() {
            return {
                data: {
                    "@context": "https://schema.org",
                    "@type": "FAQPage",
                    mainEntity: [],
                }
            }
        },

        mounted() {
        const elemento = document.querySelectorAll('#perguntas');
        elemento[0].children[0].children.forEach(item => {
            let title = item.children[0].innerText;
            let text = item.children[1].innerText;

            this.data.mainEntity.push({
            "@type": "Question",
            name: title,
            acceptedAnswer: {
                "@type": "Answer",
                text: text,
            }
            });
        });

            let script = document.createElement("script");
            script.type = "application/ld+json";
            script.innerHTML = JSON.stringify(this.data);
            document.getElementsByTagName("head")[0].appendChild(script);
    }
}


</script>

<style scoped>
    .btn-act {
        width: 180px;
        cursor: pointer;
        padding: 10px 20px;
        margin: 30px auto;
        text-align: center;
        color: #ffffff;
        background: #12AC53;
        border: none;
        font-size: 18px;
    }

    .btn-act:hover {
        opacity: .8;
    }

    .accordion#faq .card {
        margin-bottom: 10px;
        border: 0;
    }

    .accordion#faq .card .card-header {
        border: 0;
        padding: 0;
        margin-bottom: 0;
        border-radius: 0!important;
    }

    .accordion#faq .card .card-header .btn-header-link {
        width: 100%;
        text-align: left;
        padding: 15px;
        box-shadow: none;
        font: normal normal bold 20px/20px Open Sans;
        letter-spacing: 0px;
        color: #333333;
        background: #fff;
        border-bottom: 1px solid #aaa;
        border-radius: 0;
    }

    .card-body p{
        font: normal normal normal 18px/24px Open Sans;
        letter-spacing: 0px;
        color: #333333;
    }

    .accordion#faq .card .card-header .btn-header-link:after {
        content: "\f068";
        font: normal normal normal 16px/1 FontAwesome;
        float: right;
        padding-top: 10px;
    }

    .accordion#faq .card .card-header .btn-header-link.collapsed {
        color: #444;
        background: #fff !important;
    }

    .accordion#faq .card .card-header .btn-header-link.collapsed:after {
        content: "\f067";
    }

    .accordion#faq .card .collapsing {
        line-height: 32px;
    }

    .accordion#faq .card .collapse {
        border: 0;
    }

    .accordion#faq .card .collapse.show {
        line-height: 30px;
        color: #222;
    }

    @media(max-width: 768px) {

        .container.py-5{
            padding-bottom: 0px!important;
        }
        .w-75 {
            width: 100% !important;
        }

        .accordion#faq .card .card-header .btn-header-link{
            font-size: 16px;
        }
        .accordion#faq .card .card-header .btn-header-link:after {
            padding-top: 2px;
        }
        .card-body p{
            font-size: 14px;
            line-height: 18px;
        }
    }
</style>