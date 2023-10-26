<template>
  <div>
    <BannerCreme />
    <Credibilidade cor="home" />
    <FormulaCreme class="pt-5"/>
    <BeneficiosCreme class="py-5" />
    <VitrineCreme />
    <PassosCreme class="py-5"/>
    <AtivosCreme class="py-5" />
    <ExibcaoKit />
    <FamosasAprovam class="py-5"/>
    <PerguntasFrequentesCreme class="py-5"/>
    <BotaoCompreAgora class="mob" />
  </div>
</template>

<script>
import {mapMutations} from 'vuex'

import VitrineCreme from '../../components/common/vitrines/vitrine-creme.vue'
import BannerCreme from '../../components/gerais/banners/banner-creme.vue'
import Credibilidade from '../../components/gerais/credibilidade/credibilidade.vue'
import AtivosCreme from '../../components/gerais/creme/ativos-creme.vue'
import BeneficiosCreme from '../../components/gerais/creme/beneficios-creme.vue'
import FormulaCreme from '../../components/gerais/creme/formula-creme.vue'
import PassosCreme from '../../components/gerais/creme/passos-creme.vue'
import PerguntasFrequentesCreme from '../../components/gerais/perguntas-frequentes/perguntas-frequentes-creme.vue'
import ExibcaoKit from '../../components/gerais/serum/exibcao-kit.vue'
import FamosasAprovam from '../../components/gerais/serum/famosas-aprovam.vue'
import BotaoCompreAgora from '../../components/ui/buttons/botao-compre-agora.vue'
export default {
  name: 'Creme',
  components: { BannerCreme, Credibilidade, FormulaCreme, BeneficiosCreme, PassosCreme, AtivosCreme, ExibcaoKit, FamosasAprovam, PerguntasFrequentesCreme, VitrineCreme, BotaoCompreAgora },

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
                    response.data.estrutura.seo.canonical = "https://www.vivabeauty.com.br/products/creme"
                    
                    response.data.estrutura.seo.title = "Creme Hidratante Primer | Viva Beauty"
                    response.data.estrutura.seo.description = "Creme Hidratante Primer"
                    this.loading.geral = false;
                    this.$aplicaSEO(response.data.estrutura);
                    this.changeDadosPageAtual(response.data);
                    //comunicacao.$emit('paginaCarregada', response.data);
                }
            });
        }
}
</script>