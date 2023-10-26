<template>
    <div class="container-fluid mt-5">
        <carousel :autoplay="true" :nav="false" :dots="false" :loop="true" :responsive="{0:{items:1, dots:true}, 600:{items:4}}">
            <div class="influencer mx-auto" v-for="influencer in influencers" :key="influencer.id">
                <img :src="require(`@/assets/img/influencers/${influencer.imagem}`)" class="img-fluid"  :alt="`Imagem da influenciadora ${influencer.nome}`" :title="`Influenciadora ${influencer.nome}`">
                <h3 class="pt-4 pb-2">{{ influencer.nome }}</h3>
                <p> {{ influencer.social }} </p>
            </div>
        </carousel>
        <div class="row my-5">
            <a href="#KitProduto" class="btn btn-primary mx-auto text-center">Eu quero</a>
        </div>
    </div>
</template>

<script>
    import carousel from 'vue-owl-carousel'

    export default {
        name: 'InfluencersViva',
        components: { 
            carousel 
        },

        data() {
            return {
                influencers: [
                    // {
                    //     id: 1,
                    //     nome: 'Juju Norremose',
                    //     imagem: 'juju-norremose.webp',
                    //     social: '@jujunorremose'
                    // },
                    {
                        id: 1,
                        nome: 'Bella Falconi',
                        imagem: 'bella-falconi.webp',
                        social: '@bellafalconi'
                    },
                    {
                        id: 2,
                        nome: 'Carol Borba',
                        imagem: 'carol-borba.webp',
                        social: '@carolborba1'
                    },
                    {
                        id: 3,
                        nome: 'Izabella Lima',
                        imagem: 'izabella-lima.webp',
                        social: '@izabellabebel'
                    },
                ],
            }
        },
    }
</script>

<style scoped>
    .influencer {
        width: 400px;
    }

    h3 {
        font-size: 19px;
        font-weight: bold;
        font-family: Poppins, sans-serif;
    }

    p {
        font-size: 13px;
        font-family: Poppins, sans-serif;
    }

    .btn {
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

    .btn:hover {
        opacity: .8;
    }
</style>