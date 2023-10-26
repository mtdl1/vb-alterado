<template>
    <section class="produtoSingle">
        <div class="container breadcrumb-single mt-3 mb-3">
            <div class="row">
                <nav aria-label="breadcrumb">
                    <ol class="breadcrumb">
                        <li class="breadcrumb-item"><a href="/">Início</a></li>
                        <li class="breadcrumb-item active pink" id="breadcrumbTitle" aria-current="page">Colágeno Skin Complex Plus</li>
                    </ol>
                </nav>
            </div>
        </div>

        <div class="container">
            <div class="row">
                <div class="col-md-7" id="sliderProductSingle">
                    <div id="custCarousel" class="carousel slide d-flex" align="center">
                        <!-- Thumbnails -->
                        <div class="overflowThumbs">
                            <div class="desk">
                                <ol class="list-group carousel-indicators thumbs d-flex">
                                    <li v-for="(imagem, index) in galeriaImagens" :key="index" :class="['list-inline-item',{active: index==0}]" style="width: 100px;height: 100px!important"> 
                                        <a :id="'carousel-selector-'+ index" class="selected" :data-slide-to="index" data-target="#custCarousel">
                                            <img :src="imagem.arquivos.big" class="img-fluid" alt="" @click="changeSaborOption()">
                                        </a>
                                    </li>
                                </ol>
                            </div>
                            <div class="mob">
                                <ol class="list-groupMob carousel-indicators thumbs d-block">
                                    <li v-for="(imagem, index) in galeriaImagens" :key="index" :class="['list-inline-item',{active: index==0}]" style="width: 100px;height: 100px!important"> 
                                        <a :id="'carousel-selector-'+ index" class="selected" :data-slide-to="index" data-target="#custCarousel">
                                            <img :src="imagem.arquivos.big" class="img-fluid" alt="">
                                        </a>
                                    </li>
                                </ol>
                            </div>
                        </div>

                        <!-- Left and right controls -->
                        <div class="desk">
                            <a class="thumb-controls cima" href="#custCarousel" data-slide="prev"><i class="fa fa-angle-up"></i></a>
                            <a class="thumb-controls baixo" href="#custCarousel" data-slide="next"><i class="fa fa-angle-down"></i></a>
                        </div>
                        <div class="mob">
                            <a class="thumb-controls left cimaMob" href="#custCarousel" data-slide="prev"><i class="fa fa-angle-up"></i></a>
                            <a class="thumb-controls right baixoMob" href="#custCarousel" data-slide="next"><i class="fa fa-angle-down"></i></a>
                        </div>

                        <!-- slides -->
                        <div class="carousel-inner" id="carouselInnerSlider">
                            <div class="imagens-plataforma" v-if="sabores == 0">
                                <div v-for="(imagem, index) in galeriaImagens" :key="index" :class="['carousel-item',{active: index==0}]"> 
                                    <img :src="imagem.arquivos.big" class="img-fluid" alt="">
                                </div>
                            </div>
                            <div class="imagens-sabores">
                                <div class="carousel-item active" v-if="sabores > 0">
                                    <img v-if="sabores == 202" src="@/assets/img/single/Colageno-Skin-Complex-Plus-Pink-Lemonade-Kit-2-Potes.png" class="img-fluid" alt="">
                                    <img v-if="sabores == 219" src="@/assets/img/single/Colageno-Skin-Complex-Plus-Yellow-Fuits-Kit-2-Potes.png" class="img-fluid" alt="">
                                    <img v-if="sabores == 221" src="@/assets/img/single/Colageno-Skin-Complex-Plus-Yellow-Fuits-Pink-Lemonade-Kit-2-Potes.png" class="img-fluid" alt="">
                                 
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-5" id="InfoProduto">
                    <h1 class="titleProduto" id="titleProduct">Colágeno Skin Complex Plus -<br> 2 Potes</h1>
                    <!-- <p class="descricao" id="descricao">
                    </p> -->
                    <p class="checks"> <img src="@/assets/img/single/check.svg" >&nbsp; Tratamento Anti-Idade 7 em 1</p>
                    <p class="checks"> <img src="@/assets/img/single/check.svg" >&nbsp; Até 3x mais Ácido Hialurônico</p>
                    <p class="checks"> <img src="@/assets/img/single/check.svg" >&nbsp; Verisol</p>
                    <p class="checks"> <img src="@/assets/img/single/check.svg" >&nbsp;Silício Orgânico</p>

                    <div class="d-flex align-items-center justify-content-between">
                        <!-- <p class="d-flex align-items-center currentPrice">  -->
                            <!-- <strong class="mr-1">{{ ((precoPor * $store.state.desconto) / 100).toLocaleString('pt-br',{style: 'currency', currency: 'BRL'}) }}</strong>  -->
                        <!-- </p> -->
                    <div class=" d-flex align-items-left old text-left">
                        <p class="priceOld pt-4"> <s>DE: {{ precoDe.toLocaleString('pt-br',{style: 'currency', currency: 'BRL'}) }} </s> </p>
                    </div>
                        <p class="discount"> ECONOMIZE <br> <strong>{{ (precoDe - ((precoPor * $store.state.desconto) / 100)).toLocaleString('pt-br',{style: 'currency', currency: 'BRL'}) }} </strong></p>
                    </div>
                    <div class="d-flex align-items-center mt-3 mb-2">
                        <p class="priceNew">
                             <strong>{{ precoPor.toLocaleString('pt-br',{style: 'currency', currency: 'BRL'}) }}</strong> 
                             <br><span class="emAte"> em até 
                            <strong >{{ $store.state.qtdParcelas }}x de {{ (precoPor/$store.state.qtdParcelas).toLocaleString('pt-br',{style: 'currency', currency: 'BRL'}) }}</strong> sem juros.</span>
                        </p>
                    </div>

                    <div class="form-group select_sabores">
                        <select name="saboresKit2Pt" class="select_option browser-default custom-select" id="saboresKit2Pt" @change="onChange($event)" v-model="sabores">
                            <option class="option" value="0" selected>Escolha o Sabor</option>
                            <option class="option" data-value="" :value="kit.id" v-for="(kit, index) in saboresKit.kit1.todosKits" :key="index">{{ kit.nome }}</option>
                        </select>
                       
                       
                    </div>
                    <div class="btn btn-primary btn-lg green mt-2" @click="addCartBoxCompra()">COMPRE AGORA dwdwd</div>
                    
                    <div class="selos d-flex align-center align-items-center mt-3">
                        <img class="px-3" src="@/assets/img/single/compra-segura.png" alt="Compra segura">
                        <img class="px-3" src="@/assets/img/single/google-safe.png" alt="Compra segura">
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    import $ from "jquery"
    import Comunicacao from "@/comunicacao.js"

    // funcao desktop para avançar e voltar imagens do carousel
    $(function () {
        setTimeout(function() {
            var qtdImages = $('.list-group .list-inline-item').length
            var height = (parseInt($('.carousel .list-group .list-inline-item').outerHeight())) * qtdImages //Calcula altura da coluna de Thumbs
            var numImages = 3 // Quantidade de imagens que vai correr em cada carossel
            var count = Math.floor(height/480) // Quantidade de vezes que pode clicar para avançar
            var marginPadding = 0 // Caso haja margin e padding nos elementos
            var contador = 0 // quantidade de vezes que avançou no carossel (controle de ida e volta)
            var slide = (numImages * marginPadding) + ($('.carousel .list-group .list-inline-item').outerHeight() * numImages) // Tamanho do Slide (quanto de margin pode avançar)

            // Passa o valor da altura da coluna obtida no 'var height'
            $('.carousel .list-group').css('height', height)

            // Avança o Slide para baixo
            $('.baixo').click(function () {
                if(contador < count){
                    contador ++
                    $('.list-group').animate({'margin-top': '-=' + slide + 'px'}, '500')
                }
            });

            // Avança o Slide para cima
            $('.cima').click(function () {
                if(contador >= 1){
                    contador --
                    $('.list-group').animate({'margin-top': '+=' + slide + 'px'}, '500')
                }
            });
        }, 1500);

    })

    // funcao mobile para avancar e voltar imagens do carousel
    $(function () {
        var width = 900 //Calcula largura da linha de Thumbs
        var contador = 0 // quantidade de vezes que avançou no carossel (controle de ida e volta)
        var count = 1  // Quantidade de vezes que pode clicar para avançar
        var slide = 300  // Tamanho do Slide (quanto de margin pode avançar)

        $('.carousel .list-groupMob').css('width', width)

        $('.baixoMob').click(function () {
            if(contador < count){
                contador ++
                $('.list-groupMob').animate({'margin-left': '-=' + slide + 'px'}, '500')
            }
        });

        $('.cimaMob').click(function () {
            if(contador >= 1){
                contador --
                $('.list-groupMob').animate({'margin-left': '+=' + slide + 'px'}, '500')
            }
        });
    })

    export default {
        data() {
            return {
                activeClass: 'active',
                classImage: 'carousel-item',
                nome: '',
                galeriaImagens: [],
                precoDe: '0',
                precoPor: 0,
                urlLista: window.location.pathname,
                idLista: 0,
                 sabores: 0,
                selected: "selected",
                boxCompraCarrinho: {
                    tipo: "lista",
                    itens: [
                        {
                            idProduto: "5",
                            idAtributoSimples: "0",
                            idUnidadeVenda: "0",
                            idArmazem: "0",
                            quantidade: "1",
                            adicional: "",
                            parametros: ""
                        },
                    ]
                },
                saboresKit: {
                    kit1: {
                        precosGerais: {
                            precoDe: 799.98,
                            precoPor: 397.70,
                        },
                        todosKits: {
                            1: {
                                id: '202',
                                nome: '2 Potes - Pink Lemonade',
                            },
                            2: {
                                id: '219',
                                nome: '2 Potes - Yellow Fruits',
                            },
                            3: {
                                id: '221',
                                nome: '1 Pote Pink Lemonade + 1 Pote Yellow Fruits',
                            },

                        },
                    },
                },
            }
            },
            
        
        methods: {
               // obtem o valor do select
            onChange(event) {
                this.sabores = event.target.value
                // this.scrollToDiv()
            },

            changeKit(event) {
                this.kitPotes = event.target.value
                this.changeSaborOption()
                this.scrollToDiv()
            },

            changeSaborOption() {
                this.sabores = 0
                this.kitPotes = 'KIT3POTES'
            },

            // scroll para a div sliderProductSingle
            scrollToDiv() {
                window.scrollTo({
                    top: this.$refs.sliderProductSingle.offsetTop,
                    behavior: 'smooth'
                });
            },

            addCartBoxCompra() {
                //Recupera o id selecionado do produto
                var Produto = this.sabores
                this.boxCompraCarrinho.itens[0].idProduto = Produto

                Comunicacao.$emit('toggleLoader', true)
                let {tipo, itens} = this.boxCompraCarrinho
                let itemAdc       = false
                if (tipo && itens) {
                    //ADICIONA O PRODUTO AO CARRINHO
                    this.$carrinho.add(tipo,itens,(success, response) => {
                        response.data.itens.forEach(prod => {
                            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho.itens[0].idProduto
                        })
                        //PRODUTO ADICIONADO COM SUCESSO
                        if(success){
                            if (Produto == 0) this.$toast.error("Selecione um sabor para adicionar ao carrinho!")
                            else {
                                this.$setDatalayerToAddToCart(
                                    response.data.itens[0].nome,
                                    this.boxCompraCarrinho.itens[0].idProduto,
                                    response.data.itens[0].precos.precoPor,
                                    response.data.itens[0].quantidade
                                )
                                return Comunicacao.$emit('toggleCarrinho', {show: true, data: response.data })
                            }
                        }
                        this.changeDadosPageAtual(response.data)
                        //PROBLEMAS AO ADICIONAR PRODUTO
                        this.$toast.error("Um problema impediu a adição do produto ao carrinho. Tente novamente mais tarde.")
                    })
                    return
                }
            },

            genPath(path, onlyQuery){
                if (onlyQuery) {
                    path = path.replace(/\/.*(\?.*)/g, '$1')
                    return path
                }
                path = path.replace('?', '&')
                return path
            },

            formatMoney(amount, decimalCount = 2, decimal = ",", thousands = ".") {
                try {
                    decimalCount = Math.abs(decimalCount)
                    decimalCount = isNaN(decimalCount) ? 2 : decimalCount

                    const negativeSign = amount < 0 ? "-" : ""

                    let i = parseInt(amount = Math.abs(Number(amount) || 0).toFixed(decimalCount)).toString()
                    let j = (i.length > 3) ? i.length % 3 : 0

                    return negativeSign + (j ? i.substr(0, j) + thousands : '') + i.substr(j).replace(/(\d{3})(?=\d)/g, "$1" + thousands) + (decimalCount ? decimal + Math.abs(amount - i).toFixed(decimalCount).slice(2) : "")
                } catch (e) {
                    //close
                }
            },
        },

        created(){
            this.$requestSend('get', `/v2/front/url/product/detail?url=${this.genPath(this.$route.fullPath)}&offset=0&limit=1`, {}, (success, response) => {
                if (success) {
                    var objetoProduto = JSON.parse(response.request.response)
                    this.nome = objetoProduto.conteudo.nome
                    this.galeriaImagens = objetoProduto.conteudo.midias.imagensFull
                    this.precoDe = objetoProduto.conteudo.precos.de
                    this.precoPor = objetoProduto.conteudo.precos.por
                    document.getElementById("descricao").innerHTML = objetoProduto.conteudo.descricoes.curta
                    this.boxCompraCarrinho.itens[0].idProduto = objetoProduto.conteudo.id

                    //SETA PRODUTO PARA EVENTO DE ADDCART NO GTM
                    let prod = {
                        id: objetoProduto.conteudo.id,
                        nome: objetoProduto.conteudo.nome,
                        marca: {
                            nome: objetoProduto.conteudo.marca.nome,
                        },
                        precos: {
                            por: objetoProduto.conteudo.precos.por,
                        }
                    }
                    this.boxCompraCarrinho.prod = prod

                    this.$aplicaSEO(response.data.estrutura)

                    //VARIÁVEIS PÚBLICAS
                    this.changeDadosPageAtual(response.data)
                }
            });
        },
    }
</script>

<style scoped>
.label-title {
        font: normal normal bold 20px/30px Open Sans;
        letter-spacing: -0.8px;
        color: #333333;
    }

   .select_sabores{ 
        position: relative;
        user-select: none;
        border: 1px solid #707070;
        border-radius: 8px;
        margin:5px auto 15px;
        appearance: none;
        -webkit-appearance: none;
        -moz-appearance: none;
        font-family: 'Helvetica', sans-serif;
        font-size: 15px;
        width: 100%;
        height: 50px;
        text-align: center;
        line-height: 2.5;
    }

    .select_sabores select {
        width: 100%;
        height: 100%;
        border: none;
        border-radius: 8px;
        padding: 10px;
        /* background: #fff; */
    }


    .breadcrumb-single .breadcrumb {
        background-color: unset;
        font-size: 20px;
    }

    .pink {
        color: #000000;
    }

    span.carousel-control-prev-icon, span.carousel-control-next-icon {
        transform: rotate(90deg);
    }

    .thumb-controls i {
        color: #555555;
        font-size: 20px;
    }

    .cima {
        position: absolute;
        top: 0;
        width: 105px;
        left: 0;
        z-index: 99;
    }

    .baixo {
        position: absolute;
        bottom: 37px;
        width: 105px;
        left: 0;
        z-index: 99;
    }

    .list-group.carousel-indicators.thumbs {
        height: 1100px;
        overflow: hidden;
        align-self: flex-start;
    }

    #custCarousel .carousel-indicators li img {
        display: block;
    }

    .carousel-inner{width: 560px}

    .carousel-inner img{width:100%;height:auto}

    #custCarousel .carousel-indicators{
        width: 150px;
        position:relative;
        margin:0;
        flex-direction:column;
        right:unset;
        bottom:unset;
        left:unset;
        padding:unset;
        z-index: 8;
    }

    /* Slider Produtos */

    .titleProduto {
        padding: 0 0 25px;
        font: normal normal bold 28px/30px Open Sans;
        letter-spacing: 0px;
        color: #1A1A1A;
    }

    p.descricao {
        font-size: 15px;
        padding: 0 0 18px;
        line-height: 1;
        color: #3c3c3c;
        font-family: "Roboto Regular", sans-serif;
    }

    .priceOld s {
        font: normal normal normal 16px/16px Helvetica-Normal;
        letter-spacing: 0px;
        color: #666666;
    }

     .priceNew, .discount {
        margin: -10px 0 0 0;
    }
    
    .emAte {
        font: normal normal normal 16px/18px Helvetica;
        letter-spacing: -0.32px;
        color: #666666;
    
    }

    .discount {
        background: #FFFF00;
        padding: 5px 10px;
        box-sizing: border-box;
        font: normal normal normal 14px/16px Helvetica-Normal;
        letter-spacing: 0px;
        color: #1A1A1A;
    }

    .discount strong {
        font-size: 20px;
        font-weight: 900;
        color: #1A1A1A;
    }

    .txtPrice {
        font-size: 18px;
        color: #000;
        font-weight: bold;
        font-family: "Roboto Regular", sans-serif;
    }

    .green {
        background: #18A851;
        border-color: #18A851;
        width: 100%;
        padding: 20px;
        font-weight: bold;
        font-size: 20px;
    }

    .green:active, .green:hover {
        opacity: .8;
        border-color: #18A851 !important;
    }

    .priceNew {
        font: normal normal bold 45px/28px Helvetica;
        letter-spacing: 0px;
        color: #1A1A1A;
    }

    .off-percent {
        font: normal normal normal 16px/16px Helvetica-Normal;
        letter-spacing: -0.64px;
        color: #18A851;
    }

    /* Slider Column */

    div#custCarousel {
        height: 560px;
    }

    .carousel-item {
        height: 560px;
    }

    div#carouselInnerSlider {
        align-self: flex-start;
    }

    .overflowThumbs {
        height: 490px;
        overflow: hidden;
        margin-top: 20px;
    }

    .carousel-indicators li {
        opacity: 1 !important;
    }

    .checks {
        padding-top: 7px;
        color: #4B4B4B;
    }

    @media (max-width: 767px) {
        .breadcrumb-single .breadcrumb {
            background-color: unset;
            font-size: 13px;
        }

        .pink {
            color: #333;
            font-weight: bold;
        }

        .overflowThumbs {
            height: 120px;
            overflow: hidden;
            margin-top: 20px;
            text-align: left;
        }

        .thumb-controls {
            background: #00000044;
        }

        .thumb-controls:hover {
            background: #0000007e;
        }

        .thumb-controls i {
            color: #fff;
            font-size: 25px;
        }

        .left {
            position: absolute;
            bottom: 0 !important;
            top: unset;
            width: 25px;
            height: 118px;
            left: 0px;
            z-index: 8;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .left i {
            transform: rotate(-90deg);
        }

        .right {
            position: absolute;
            bottom: 0 !important;
            width: 25px;
            height: 118px;
            right: 0px;
            left: unset;
            z-index: 8;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .right i {
            transform: rotate(270deg);
        }

        .list-group.carousel-indicators.thumbs {
            /* height: 1100px; */
            overflow: hidden;
            align-self: flex-start;
        }

        .list-groupMob.carousel-indicators.thumbs {
            overflow: hidden;
            align-self: flex-start;
            width: 90px;
            justify-content: flex-start;
            width: 90px;
            justify-content: flex-start;
        }

        .carousel-item {
            height: auto;
        }

        /* Slider Produtos */

        .titleProduto {
            padding: 0 0 25px;
            font: normal normal bold 28px/30px Open Sans;
            letter-spacing: 0px;
            color: #1A1A1A;
        }

        p.descricao {
            font-size: 15px;
            padding: 0 0 18px;
            line-height: 1;
            color: #3c3c3c;
            font-family: "Roboto Regular", sans-serif;
        }

        .priceOld,
        .priceNew {
            margin: 0 10px 0 0;
        }
        
        .priceNew strong {
            color: #000;
        }
        
        .emAte {
        font: normal normal normal 16px/18px Helvetica;
        letter-spacing: -0.32px;
        color: #666666;
    
    }

        .discount {
            background: #fff154;
            font: normal normal normal 14px/16px Helvetica-Normal;
            color: #000;
            font-weight: 900;
            padding: 5px 60px 5px 5px;
            box-sizing: border-box;
            position: relative;
            /* right: -60px; */
            width: 100px;
            border-radius: 5px;
            text-align: right;
            line-height: 1;
        }

        .txtPrice {
            font-size: 18px;
            color: #000;
            font-weight: bold;
            font-family: "Roboto Regular", sans-serif;
        }

        .green {
            background: #18A851;
            border-color: #18A851;
            width: 100%;
            padding: 20px;
            font-weight: bold;
            font-size: 20px;
        }

        .green:active,
        .green:hover {
            opacity: .8;
            border-color: #18A851 !important;
        }

        .currentPrice {
            font-weight: 900;
            font-size: 30px !important;
            margin: -10px 0 0 !important;
            position: relative;
        }

        .currentPrice strong {
            font: normal normal bold 32px/38px Helvetica;
            padding-bottom: 5px;
            padding-top: 10px;
        }

        .off-percent {
            font: normal normal normal 13px/14px Helvetica-Normal;
            position: absolute;
            right: -45%;
        }

        /* Slider Column */

        div#custCarousel {
            flex-direction: column-reverse;
            overflow: hidden;
            height: auto;
            margin-bottom: 20px;
        }

        div#carouselInnerSlider {
            align-self: flex-start;
        }

        .list-groupMob #custCarousel .carousel-indicators {
            flex-direction: row;
            height: 120px !important;
            order: 2;
            width: 900px;
            justify-content: flex-start;
        }

        .carousel-inner img {
            width: 100%;
            height: auto
        }

        #custCarousel .carousel-indicators li img {
            width: 100px;
            height: 100px;
        }

        .carousel-inner {
            width: 100% !important;
        }

        .carousel-item img {
            width: 100% !important;
        }

        .titleProduto {
            font-size: 20px;
        }

        .descricao {
            display: none;
        }

        .discount {
            font-size: 11px !important;
            padding: 5px !important;
        }

        .subTitle {
            font-size: 18px;
        }

        li.list-inline-item {
            width: unset !important;
        }

        img.thumbnailsprod {
            width: 120px !important;
        }

        @media(max-width: 360px) {
            .currentPrice strong {
                font: normal normal bold 28px/32px Helvetica;
            }

            .discount {
                font: normal normal normal 10px/12px Helvetica-Normal;
                width: 85px;
            }

            .discount strong {
                font-size: 16px !important;
            }

            .off-percent {
                right: -50%;
            }

            .priceNew {
                font: normal normal normal 12px/14px Helvetica;
            }
        }
    }

</style>
