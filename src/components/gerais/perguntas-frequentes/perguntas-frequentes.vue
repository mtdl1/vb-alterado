<template>
    <div class="container">
        <div class="row justify-content-center" id="perguntas" >
            <div class="accordion w-100" id="faq">
                <div class="card">
                    <div class="card-header" id="faqhead1">
                        <a href="#" class="btn btn-header-link" data-toggle="collapse" data-target="#faq1" aria-expanded="true" aria-controls="faq1">Tem alguma contraindicação ou efeito colateral?</a>
                    </div>

                    <div id="faq1" class="collapse show" aria-labelledby="faqhead1" data-parent="#faq">
                        <div class="card-body">
                            <p>O Viva Beauty é totalmente natural, sem açúcar e ainda não engorda! NÃO é recomendado para gestantes, lactantes e crianças!</p>
                        </div>
                    </div>
                </div>

                <div class="card">
                    <div class="card-header" id="faqhead2">
                        <a href="#" class="btn btn-header-link collapsed" data-toggle="collapse" data-target="#faq2" aria-expanded="true" aria-controls="faq2">Em quanto tempo os resultados são visíveis?</a>
                    </div>

                    <div id="faq2" class="collapse" aria-labelledby="faqhead2" data-parent="#faq">
                        <div class="card-body">
                            <p>Os resultados são visíveis a partir de 8 semanas de uso do Viva Beauty, mas começam a ser notados a partir de 4 semanas. Disponibilizamos estudos do Verisol que comprovam os resultados (no rodapé do site)!</p>
                        </div>
                    </div>
                </div>

                <div class="card">
                    <div class="card-header" id="faqhead3">
                        <a href="#" class="btn btn-header-link collapsed" data-toggle="collapse" data-target="#faq3" aria-expanded="true" aria-controls="faq3">Os ingredientes são naturais?</a>
                    </div>

                    <div id="faq3" class="collapse" aria-labelledby="faqhead3" data-parent="#faq">
                        <div class="card-body">
                            <p>Sim, como diferencial priorizamos sempre a qualidade e principalmente pensamos na sua saúde em longo prazo. Por isso não utilizamos corantes artificiais, malto e nem conservantes!</p>
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
                    <div class="card-header" id="faqhead5">
                        <a href="#" class="btn btn-header-link collapsed" data-toggle="collapse" data-target="#faq5" aria-expanded="true" aria-controls="faq5">Como devo consumir?</a>
                    </div>

                    <div id="faq5" class="collapse" aria-labelledby="faqhead5" data-parent="#faq">
                        <div class="card-body">
                            <p>Em um copo ou coqueteleira misturar 10g (1 scoop) em 200 ml de água com auxílio de uma colher.</p>
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

        <BotaoCompreAgora class="pt-5"/>

    </div>
</template>

<script>
import BotaoCompreAgora from '../../ui/buttons/botao-compre-agora.vue';
    export default {
        components: { BotaoCompreAgora },
            name: 'PerguntasFrequentes',

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
        .w-75 {
            width: 100% !important;
        }
    }
</style>