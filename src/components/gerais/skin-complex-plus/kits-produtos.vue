<template>
    <div class="container-fluid bg-light" id="KitProduto">
        <div class="container py-4">
        <p class=" tratamento text-center"><strong>Tratamento Anti-Idade 7 em 1<br class="mob"> Skin Complex Plus</strong> com Colágeno <br class="desk">Verisol® + Ácido Hialurônico + Silício Orgânico</p>
            <div class="row align-items-center">
                <div class="col-md-7 text-center">

                   <div v-show="kit == 201">
                    <img src="@/assets/img/skin-complex-plus/Colageno-Skin-Complex-Plus-Pink-Lemonade-Kit-1-Pote.png" alt="Pote de Skin Complex Plus com rótulo rosa e ao lado um pote de colágeno de uma marca concorrente" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" class="img-fluid" width="525" v-show="sabores == 201 || sabores == 0">
                    <img src="@/assets/img/skin-complex-plus/Colageno-Skin-Complex-Plus-Yellow-Fuits-Kit-1-Pote.png" alt="Pote de Skin Complex Plus com rótulo rosa e ao lado um pote de colágeno de uma marca concorrente" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" class="img-fluid" width="525" v-show="sabores == 218">

                    </div> 
                    <div v-show="kit == 202">
                    <img src="@/assets/img/skin-complex-plus/Viva-Beauty-SkinPlus-2-Potes.png" alt=" Dois potes de Skin Complex Plus com rótulo na cor rosa" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" class="img-fluid" width="525" v-show="sabores2 == 202 ">

                    <img src="@/assets/img/skin-complex-plus/Viva-Beauty-SkinPlus-yellow-2-Potes.png" alt=" Dois potes de Skin Complex Plus com rótulo na cor rosa" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" class="img-fluid" width="525" v-show="sabores2 == 219">

                    <img src="@/assets/img/skin-complex-plus/Colageno-Skin-Complex-Plus-Yellow-Fuits-Pink-Lemonade-Kit-2-Potes.png" alt=" Dois potes de Skin Complex Plus com rótulo na cor rosa" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" class="img-fluid" width="525" v-show="sabores2 == 221 || sabores2 == 0">
                    </div>

                    <div v-show="kit == 203">
                    <img src="@/assets/img/skin-complex-plus/Colageno-Skin-Complex-Plus-Pink-Lemonade-Kit-4-Potes-Brinde.png" alt=" Potes de Skin Complex Plus com rótulo na cor rosa" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" class="img-fluid" width="525" v-show="sabores3 == 203 || sabores3 == 0">
                    <img src="@/assets/img/skin-complex-plus/Colageno-Skin-Complex-Plus-Yellow-Fuits-Kit-4-Potes-Brinde.png" alt=" Potes de Skin Complex Plus com rótulo na cor rosa" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" class="img-fluid" width="525" v-show="sabores3 == 220">
                    <img src="@/assets/img/skin-complex-plus/Colageno-Skin-Complex-Plus-Yellow-Fuits-Pink-Lemonade-Kit-4-Potes-Brinde.png" alt=" Potes de Skin Complex Plus com rótulo na cor rosa" title="Tratamento anti-idade Skin Complex Plus, muito mais que um simples colágeno! Resultados visíveis já no primeiro mês de uso" class="img-fluid" width="525" v-show="sabores3 == 222">
                    </div>
                </div>
                
                <div class="col-md-5 py-4">
                    <label for="kit1" :class="['d-flex align-items-center mt-3 position-relative bg-white', {altcolor: kit == 201, active: kit == 201}]">
                        <div class="circ-select">
                            <input type="radio" id="kit1" name="kit" v-model="kit" value="201" class="d-flex align-items-center "  @change="onChangeKit($event)">
                        </div>
                        <div class="info-kit ml-2">
                            <h2 class="name-kit pb-2">1 UNIDADE (1 MÊS)</h2>
                            <div class="featured position-absolute">
                                <div class="off mt-4"><strong>{{ (Math.floor(100 - (saboresKit.kit1.precosGerais.precoPor*$store.state.desconto)/saboresKit.kit1.precosGerais.precoDe)) }}% OFF</strong></div>
                            </div>
                            <div class="precoDe">DE {{ saboresKit.kit1.precosGerais.precoDe.toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}</div>
                            <!-- <div class="precoPor-vista pb-1">{{ (Math.ceil(parseFloat(saboresKit.kit1.precosGerais.precoPor) * $store.state.desconto) / 100).toLocaleString('pt-br',{style: 'currency', currency: 'BRL'}) }}</div> -->
                            <div class="precoParcela"> <strong class="preco">{{ saboresKit.kit1.precosGerais.precoPor.toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}</strong> <br> <span class="parcela">
                            em até <strong >{{ $store.state.qtdParcelas }}x</strong> de <strong>{{ (saboresKit.kit1.precosGerais.precoPor/$store.state.qtdParcelas).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}</strong> sem juros </span></div>
                            <div class="form-group select_sabores">
                            <select name="saboresKit" class="select_option browser-default custom-select" id="saboresKit1" @change="onChange($event)" v-model="sabores">
                                    <option class="option" value="0" selected>Escolha o sabor</option>
                                    <option class="option" :value="kit1.id" v-for="(kit1, index) in saboresKit.kit1.todosKits" :key="index">{{ kit1.nome }}</option>
                            </select>
                        </div>

                    </div>
                        
                    </label>
                    <label for="kit2" :class="['d-flex align-items-center mt-3 position-relative bg-white', {altcolor: kit == 202, active: kit == 202}]">
                        <div class="circ-select">
                            <input type="radio" id="kit2" name="kit" v-model="kit" value="202" @change="onChangeKit($event)">
                        </div>
                        <div class="info-kit ml-2">
                            <h2 class="name-kit pb-2">2 UNIDADES (2 MESES)</h2>
                           <div class="featured position-absolute">
                                <div class="off mt-4"><strong>{{ (Math.floor(100 - (saboresKit.kit2.precosGerais.precoPor*$store.state.desconto)/saboresKit.kit2.precosGerais.precoDe)) }}% OFF</strong></div>
                            </div>
                            <div class="precoDe">DE {{ saboresKit.kit2.precosGerais.precoDe.toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}</div>
                            <!-- <div class="precoPor-vista pb-1">{{ (Math.ceil(parseFloat(saboresKit.kit1.precosGerais.precoPor) * $store.state.desconto) / 100).toLocaleString('pt-br',{style: 'currency', currency: 'BRL'}) }}</div> -->
                            <div class="precoParcela"> <strong class="preco">{{ saboresKit.kit2.precosGerais.precoPor.toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}</strong> <br> <span class="parcela">
                            em até <strong >{{ $store.state.qtdParcelas }}x</strong> de <strong>{{ (saboresKit.kit2.precosGerais.precoPor/$store.state.qtdParcelas).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}</strong> sem juros </span></div>
                             <div class="form-group select_sabores">
                            <select name="saboresKit" class="select_option browser-default custom-select" id="saboresKit2" @change="onChange($event)" v-model="sabores2">
                                    <option class="option" value="0" selected>Escolha o sabor </option>
                                    <option class="option"  :value="kit2.id" v-for="(kit2, index) in saboresKit.kit2.todosKits" :key="index">{{ kit2.nome }}</option>
                            </select>
                        </div>
                        </div>
                    </label>
                   <label for="kit3" :class="['d-flex align-items-center mt-3 position-relative bg-white', {altcolor: kit == 203, active: kit == 203}]">
                        <div class="circ-select">
                            <input type="radio" id="kit3" name="kit" v-model="kit" value="203" @change="onChangeKit($event)">
                        </div>
                        <div class="info-kit ml-2">
                            <h2 class="name-kit pb-2">4 UNIDADES + BRINDE (5 MESES)</h2>
                            <div class="featured position-absolute">
                                <div class="off mt-4"><strong>{{ (Math.floor(100 - (saboresKit.kit3.precosGerais.precoPor*$store.state.desconto)/saboresKit.kit3.precosGerais.precoDe)) }}% OFF</strong></div>
                            </div>
                            <div class="precoDe">DE {{ saboresKit.kit3.precosGerais.precoDe.toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}</div>
                            <!-- <div class="precoPor-vista pb-1">{{ (Math.ceil(parseFloat(saboresKit.kit3.precosGerais.precoPor) * $store.state.desconto) / 100).toLocaleString('pt-br',{style: 'currency', currency: 'BRL'}) }}</div> -->
                            <div class="precoParcela"> <strong class="preco">{{ saboresKit.kit3.precosGerais.precoPor.toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}</strong> <br> <span class="parcela">
                            em até <strong >{{ $store.state.qtdParcelas }}x</strong> de <strong>{{ (saboresKit.kit3.precosGerais.precoPor/$store.state.qtdParcelas).toLocaleString('pt-BR', { style: 'currency', currency: 'BRL' }) }}</strong> sem juros </span></div>
                             <div class="form-group select_sabores">
                                <select name="saboresKit" class="select_option browser-default custom-select" id="saboresKit3" @change="onChange($event)" v-model="sabores3">
                                        <option class="option" value="0">Escolha o sabor</option>
                                        <option class="option" :value="kit3.id" v-for="(kit3, index) in saboresKit.kit3.todosKits" :key="index">{{ kit3.nome }}</option>
                                </select>
                        </div>
                        </div>
                    </label>
                    <button class="btn btn-primary mt-3" @click="addCartBoxCompra()">COMPRE AGORA</button>
                </div>
            </div>
        </div>
<!-- teste depploy -->
    </div>
</template>

<script>
    import Comunicacao from '@/comunicacao.js'

    export default {
        name: 'ProdutosSkinComplex',
        data() {
            return {
                kit: '202',
                sabores: 0,
                sabores2: 221,
                sabores3: 0,
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
                            precoDe: 399.99,
                            precoPor: 227.70,
                        },
                        todosKits: {
                            1: {
                                id: '201',
                                nome: '1 Pote - Pink Lemonade',
                            },
                            2: {
                                id: '218',
                                nome: '1 Pote - Yellow Fruits',
                            },
                        },
                    },
                    kit2: {
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
                    kit3: {
                        precosGerais: {
                            precoDe: 1599.96,
                            precoPor: 697.70,
                        },
                        todosKits: {
                            1: {
                                id: '203',
                                nome: '4 Potes + Brinde - Pink Lemonade',
                            },
                            2: {
                                id: '220',
                                nome: '4 Potes + Brinde - Yellow Fruits',
                            },
                            3: {
                                id: '222',
                                nome: '2 Potes Yellow Fruits + 2 Potes Pink Lemonade + Brinde',
                            },
                        },
                    },
                },
            }
        },

        methods: {
            // obtem valor do radio button
            onChangeKit(event) {
                this.kit = event.target.value
                if(event.target.id == 'kit1'){
                    this.sabores = "201"
                    this.sabores2 = "0"
                    this.sabores3 = "0"
                }else if(event.target.id == "kit2") {
                    this.sabores2 = "221" 
                    this.sabores = "0"
                    this.sabores3 = "0"
                } else if(event.target.id == "kit3") { 
                    this.sabores3 = "222"
                    this.sabores = "0"
                    this.sabores2 = "0"
                }

            },
            // select sabor do kit
            onChange(event) {
                if(event.target.id == 'saboresKit2'){
                    this.sabores = "0"
                    this.sabores3 = "0"
                    document.getElementById('kit2').classList.add('active')
                    this.kit = "202"; 
                    if(document.getElementById('kit1').className == 'active') {
                        document.getElementById('kit1').classList.remove('active');
                    } else if(document.getElementById('kit3').className == 'active') {
                        document.getElementById('kit3').classList.remove('active');
                    }
                }
                else if(event.target.id == 'saboresKit1'){
                    this.sabores2 = "0"
                    this.sabores3 = "0"
                    document.getElementById('kit1').classList.add('active')
                    this.kit = "201";
                    if(document.getElementById('kit2').className == 'active') {
                        document.getElementById('kit2').classList.remove('active');
                    } else if(document.getElementById('kit3').className == 'active') {
                        document.getElementById('kit3').classList.remove('active');
                    }
                }
                else if(event.target.id == 'saboresKit3'){
                    this.sabores = "0"
                    this.sabores2 = "0"
                    document.getElementById('kit3').classList.add('active')
                    this.kit = "203";
                    if(document.getElementById('kit2').className == 'active') {
                        document.getElementById('kit2').classList.remove('active');
                    } else if(document.getElementById('kit1').className == 'active') {
                        document.getElementById('kit1').classList.remove('active');
                    }
                }
            },

            addCartBoxCompra() {
                //Recupera o id selecionado do produto
                let Produto;
                this.sabores != 0 ? Produto = this.sabores : 0;
                this.sabores2 != 0 ? Produto = this.sabores2 : 0;
                this.sabores3 != 0 ? Produto = this.sabores3 : 0;

                this.boxCompraCarrinho.itens[0].idProduto = Produto
                Comunicacao.$emit('toggleLoader', true)
                let {tipo, itens} = this.boxCompraCarrinho
                let itemAdc       = false
                if (tipo && itens) {
                    //ADICIONA O PRODUTO AO CARRINHO
                    this.$carrinho.add(tipo,itens,(success, response) => {
                        response.data.itens.forEach(prod => {
                            itemAdc = itemAdc ? itemAdc : prod.hash.idProduto == this.boxCompraCarrinho.itens[0].idProduto;                     
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
        },
    }
</script>

<style scoped>
    .bg-light {
        background-color: #F5F5F5!important;
    }

    .bg-light p {
        color: rgb(0, 0, 0);
    }

    p {
        font-size: 22px;
        font-family: Poppins, sans-serif;
        color: #000;
        font-weight: 400;
    }

    label {
        cursor: pointer;
        outline: 1px solid #c1c1c1;
        padding: 8px 20px;
        width: 350px;
        /* height: 124px; */
        font-size: 14px;
        font-family: Poppins, sans-serif;
        border-radius: 8px;
    }

    label .name-kit {
        font: normal normal normal 15px/17px Helvetica;
        letter-spacing: 0px;
        color: #333333;
    }

    label .precoDe {
        text-decoration: line-through;
        font: normal normal normal 12px/11px Helvetica;
        letter-spacing: -0.48px;
        color: #666666;
        padding-bottom: 3px;
    }

    label .precoPor-vista {
        font: normal normal bold 32px/35px Helvetica;
        letter-spacing: -1.28px;
        color: #333333;
    }

    label .precoParcela {
        font: normal normal 300 11px/13px Helvetica;
        letter-spacing: -0.44px;
        color: #333333;
    }

    label .precoParcela .preco {
        font: normal normal bold 32px/32px Helvetica;
        letter-spacing: -0.44px;
        color: #333333;
    }

    .parcela{
       font: normal normal normal 13px/15px Helvetica; 
       padding-top: 5px;
    }

   
    .featured {
        top: 5px;
        right: 0;
    }

    .flag {
        width: 95px;
        height: 24px;
        background: #3D0916 0% 0% no-repeat padding-box;
        font: normal normal bold 12px/15px Helvetica;
        letter-spacing: 0px;
        color: #FFFFFF;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    
    .off {
        width: 61px;
        height: 22px;
        background: #951837 0% 0% no-repeat padding-box;
        font: normal normal bold 12px/15px Helvetica;
        letter-spacing: 0px;
        color: #FFFFFF;
        display: flex;
        justify-content: center;
        align-items: center;
        margin-left: auto;
    }

    .active {
        outline: 1px solid #951837;
    }

    .btn {
        width: 350px;
        background: #12AC53 !important;
        border: 1px solid #12AC53;
        padding: 10px !important;
        border-radius: 4px !important;
        color: white !important;
        transition: 0.5s;
    }

    .btn:hover {
        opacity: .65;
        transition: 0.5s;
    }

    input[type="radio"] {
        -webkit-appearance: none;
        -moz-appearance: none;
        appearance: none;
        background-color: #ff428a00;
        margin: 0;
        color: rgb(83, 76, 76);
        width: 30px!important;
        height: 30px!important;
        border-radius: 50%;
        padding-right: 20px;
        transition: 0.5s;
    }

    input[type="radio"]:checked {
        background-color: #951837;
        border: 5px solid #e6d2c9!important;
        transition: 0.5s;
    }

    .circ-select {
        border-radius: 50%;
        border: 1px solid #951837;
        display: flex;
        margin: 0 10px;
    }

    .altcolor{
        background-color: #FAEBD7 !important;
    }

    .altcolor input[type="radio"]:checked {
        border: 5px solid #FAEBD7!important;
    }

    .form-group {
        padding-top: 10px;
    }

  
    @media(max-width: 768px) {
        .bg-light {
        background-color: #F5F5F5!important;
    }


        span{
            display: block;
            margin-left: 0!important;
            width: fit-content;
        }

        label {
            width: auto;
            padding: 8px 20px 8px 0;
        }

        .info-kit.ml-2 {
            margin-left: 0!important;
        }

        .btn {
            width: 100%;
        }

        h1.w-75 {
            width: 100% !important;
        }

        p.w-75 {
            width: 100% !important;
        }

        label .name-kit {
            font: normal normal normal 14px/16px Helvetica;
        }

        .flag {
            width: 90px;
            font: normal normal bold 11px/15px Helvetica;
        }

        .tratamento {
            text-align: left !important;
            margin: auto;
            font-size: 20px
        }

        input[type="radio"] {
            width: 25px !important;
            height: 25px !important;
            padding-right: 0 !important;
        }
    }
</style>