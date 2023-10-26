<template>
    <div class="container-fluid px-0">
        <BannerEspuma />
        <Credibilidade cor="home" />
        <FormulaUnicaEspuma class="pt-5"/>
        <FormaSimplesEspuma class="py-5"/>
        <BeneficiosEspuma class="py-5"/>
        <VitrineEspuma />
        <PassosCuidadoEspuma class="py-5"/>
        <AtivosFormulaEspuma class="py-5"/>
        <ExibcaoKit />
        <FamosasAprovam class="py-5"/>
        <PerguntasFrequentesEspuma class="py-5"/>
        <BotaoCompreAgora  class="mob"/>
    </div>
</template>

<script>
import {mapMutations} from 'vuex'
import VitrineEspuma from '../../components/common/vitrines/vitrine-espuma.vue'
import BannerEspuma from '../../components/gerais/banners/banner-espuma.vue'
import Credibilidade from '../../components/gerais/credibilidade/credibilidade.vue'
import AtivosFormulaEspuma from '../../components/gerais/espuma/ativos-formula-espuma.vue'
import BeneficiosEspuma from '../../components/gerais/espuma/beneficios-espuma.vue'
import FormaSimplesEspuma from '../../components/gerais/espuma/forma-simples-espuma.vue'
import FormulaUnicaEspuma from '../../components/gerais/espuma/formula-unica-espuma.vue'
import PassosCuidadoEspuma from '../../components/gerais/espuma/passos-cuidado-espuma.vue'
import PerguntasFrequentesEspuma from '../../components/gerais/perguntas-frequentes/perguntas-frequentes-espuma.vue'
import ExibcaoKit from '../../components/gerais/serum/exibcao-kit.vue'
import FamosasAprovam from '../../components/gerais/serum/famosas-aprovam.vue'
import BotaoCompreAgora from '../../components/ui/buttons/botao-compre-agora.vue'

export default {
    name: 'EspumaLimpeza',

    components: {
        Credibilidade,
        ExibcaoKit,
        FamosasAprovam,
        FormulaUnicaEspuma,
        AtivosFormulaEspuma,
        FormaSimplesEspuma,
        BeneficiosEspuma,
        PassosCuidadoEspuma,
        VitrineEspuma,
        PerguntasFrequentesEspuma,
        BotaoCompreAgora,
        BannerEspuma,
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
                
                response.data.estrutura.seo.title = "Espuma de Limpeza Facial | Viva Beauty"
                response.data.estrutura.seo.description = "A Espuma de Limpeza Facial Viva Beauty é um produto de limpeza facial que remove as impurezas e a maquiagem, deixando a pele limpa e macia. Confira!"
                this.loading.geral = false;
                this.$aplicaSEO(response.data.estrutura);
                this.changeDadosPageAtual(response.data);
                //comunicacao.$emit('paginaCarregada', response.data);
            }
        });
    }
}

</script>