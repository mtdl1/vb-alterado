<template>
    <div class="container-fluid px-0">
        <BannerSerum />
        <Credibilidade cor="home" />
        <FormulaUnica class="pt-5"/>
        <AtivosFormula class="py-5"/>
        <BeneficiosSerum  class="py-5"/>
        <VitrineSerum />
        <PassosCuidado  class="py-5"/>
        <ExibcaoKit />
        <FamosasAprovam class="py-5"/>
        <PerguntasFrequentesSerum class="py-5" />
        <BotaoCompreAgora class="mob"/>
    </div>
</template>

<script>
    import {mapMutations} from 'vuex'
    import VitrineSerum from '../../components/common/vitrines/vitrine-serum.vue'
    import BannerSerum from '../../components/gerais/banners/banner-serum.vue'
    import Credibilidade from '../../components/gerais/credibilidade/credibilidade.vue'
    import PerguntasFrequentesSerum from '../../components/gerais/perguntas-frequentes/perguntas-frequentes-serum.vue'
    import AtivosFormula from '../../components/gerais/serum/ativos-formula.vue'
    import BeneficiosSerum from '../../components/gerais/serum/beneficios-serum.vue'
    import ExibcaoKit from '../../components/gerais/serum/exibcao-kit.vue'
    import FamosasAprovam from '../../components/gerais/serum/famosas-aprovam.vue'
    import FormulaUnica from '../../components/gerais/serum/formula-unica.vue'
    import PassosCuidado from '../../components/gerais/serum/passos-cuidado.vue'
    import BotaoCompreAgora from '../../components/ui/buttons/botao-compre-agora.vue'

    export default {
        name: 'Serum',

        components: {
            BeneficiosSerum,
            Credibilidade,
            FormulaUnica,
            AtivosFormula,
            PassosCuidado,
            ExibcaoKit,
            FamosasAprovam,
                VitrineSerum,
                PerguntasFrequentesSerum,
                BotaoCompreAgora,
                BannerSerum,
        },

        data() {
            return {
                loading: {
                    geral: true,
                    banner: true
                },
            }
        },

        methods: {
            ...mapMutations(['changeDadosPageAtual']),
        },

        created() {
            this.$requestSend('get', '/v2/front/url/home', {}, (success, response) => {
                if (success) {
                    //definindo manualmente os atributos de SEO
                    response.data.estrutura.seo.canonical = "https://www.vivabeauty.com.br/products/serum-anti-idade-multibeneficios-viva-beauty"
                    
                    response.data.estrutura.seo.title = "Sérum Facial Anti-Idade | Viva Beauty"
                    response.data.estrutura.seo.description = "O Sérum Anti-Idade Multibenefícios promove hidratação profunda, reduz poros e linhas de expressão, e uniformiza a pele ✓Até 12x s/ juros ✓Frete Grátis"
                    this.loading.geral = false;
                    this.$aplicaSEO(response.data.estrutura);
                    this.changeDadosPageAtual(response.data);
                    //comunicacao.$emit('paginaCarregada', response.data);
                }
            });
        }
    }

</script>