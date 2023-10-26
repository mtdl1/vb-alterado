<template>
    <main>
        <BannerHome />
        <Credibilidade cor="home" />
        <ExibeProdutos class="py-5" />
        <VitrineHome />
        <MelhorTratamento class="py-5"/>
        <LinhaCuidados class="py-5" />
        <VideoColageno class="py-5" />
        <ExibcaoKit />
        <FamosasAprovam class="py-5"/>
        <PerguntasFrequentesColageno class="pb-5"/>
    </main>
</template>

<script>
import { mapState, mapGetters, mapMutations } from "vuex";
import VitrineHome from "../components/common/vitrines/vitrine-home.vue";
import BannerHome from "../components/gerais/banners/bannerHome.vue";
import VideoColageno from '../components/gerais/colageno/video-colageno.vue';
import Credibilidade from "../components/gerais/credibilidade/credibilidade.vue";
import ExibeProdutos from "../components/gerais/exibe-produtos/exibe-produtos.vue";
import LinhaCuidados from "../components/gerais/linha-cuidados/linha-cuidados.vue";
import MelhorTratamento from "../components/gerais/melhor-tratamento/melhor-tratamento.vue";
import PerguntasFrequentesColageno from '../components/gerais/perguntas-frequentes/perguntas-frequentes-colageno.vue';
import ExibcaoKit from '../components/gerais/serum/exibcao-kit.vue';
import FamosasAprovam from '../components/gerais/serum/famosas-aprovam.vue';

    export default {
    data() {
        return {
        loading: {
            geral: true,
            banner: true,
        },
        };
    },

    components: {
        BannerHome,
        Credibilidade,
        ExibeProdutos,
        VitrineHome,
        MelhorTratamento,
        LinhaCuidados,
        VideoColageno,
        ExibcaoKit,
        FamosasAprovam,
        PerguntasFrequentesColageno,
    },

    methods: {
        ...mapMutations(["changeDadosPageAtual"]),
    },

    computed: {
        ...mapState({
        screenWidth: (state) => state.screenWidth,
        faq: (state) => state.duvidas.faq,
        }),
        ...mapGetters(["tipoImg"]),
    },

    created() {
        this.$requestSend("get", "/v2/front/url/home", {}, (success, response) => {
        if (success) {
            //definindo manualmente os atributos de SEO
            response.data.estrutura.seo.canonical =
            "https://www.vivabeauty.com.br/";
            response.data.estrutura.seo.title =
            "VIVA BEAUTY | O colágeno Verisol® 7 em 1 mais completo!";
            response.data.estrutura.seo.description =
            "Sua pele perfeita com Colágeno Verisol da Viva Beauty! Ativos de primeira linha, nutrição avançada e 100% natural ✓Até 8x s/ juros";
            this.loading.geral = false;
            this.$aplicaSEO(response.data.estrutura);
            this.changeDadosPageAtual(response.data);
        }
        });
    },

    metaInfo: {
        meta: [
        {
            property: "og:title",
            content: "VIVA BEAUTY | O colágeno Verisol® 7 em 1 mais completo!",
        },
        {
            property: "og:description",
            content:
            "Sua pele perfeita com Colágeno Verisol da Viva Beauty! Ativos de primeira linha, nutrição avançada e 100% natural ✓Até 8x s/ juros",
        },
        { property: "og:site_name", content: "Viva Beauty" },
        { property: "og:type", content: "Website" },
        { property: "og:url", content: "https://www.vivabeauty.com.br" },
        {
            property: "og:image",
            content:
            "https://www.vivabeauty.com.br/upload/editor/Viva-Beauty-Skin-Complex-Plus-2-potes.jpg",
        },
        {
            property: "og:image:alt",
            content: " Dois potes de Skin Complex Plus com rótulo na cor rosa",
        },
        {
            property: "twitter:title",
            content: " VIVA BEAUTY | O colágeno Verisol® 7 em 1 mais completo!",
        },
        {
            property: "twitter:description",
            content:
            "Sua pele perfeita com Colágeno Verisol da Viva Beauty! Ativos de primeira linha, nutrição avançada e 100% natural ✓Até 8x s/ juros ",
        },
        {
            property: "twitter:card:",
            content: "twitter:card: summary_large_image",
        },
        {
            property: "twitter:image",
            content:
            "https://www.vivabeauty.com.br/upload/editor/Viva-Beauty-Skin-Complex-Plus-2-potes.jpg",
        },
        {
            property: "twitter:image:alt:",
            content: " Dois potes de Skin Complex Plus com rótulo na cor rosa",
        },
        ],
    },
};
</script>