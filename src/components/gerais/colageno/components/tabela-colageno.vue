<template>
    <div>
        <div class="row">
            <div>
                <table class="table ">
                    <thead>
                        <tr>
                            <th scope="col" colspan="3" class="border-bottotm-0 text-center pt-2 pb-0 titulo"><strong>Informação nutricional</strong></th>
                        </tr>
                        <tr>
                            <th scope="col" colspan="3" class="border-top-0 border-bottom-0 text-center pt-0 pb-2 subtitulo">Porção 10g (1 Scoop)</th>
                        </tr>
                        <tr>
                            <th scope="col" colspan="2" class="porcao"><strong>Quantidade por porção</strong></th>
                            <th scope="col" class="text-center">%VD(*)</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="(dado, index) in dataTable" :key="index">
                            <th scope="row">{{ dado.col1 }}</th>
                            <td class="text-center" width="30%">{{ dado.col2 }}</td>
                            <td class="text-center" width="20%">{{ dado.col3 }}</td>
                        </tr>
                    </tbody>
                    <tfoot>
                        <tr>
                            <th scope="col" colspan="3" class="text-left py-1">"Não contém quantidades significativas de gorduras totais, gorduras saturadas, gorduras trans."</th>
                        </tr>
                    </tfoot>
                </table>
                <p class="adicional-tabela">(*)Valores diários de referência com base em uma dieta de 2000 kcal ou 8400kj. Seus valores diários podem ser maiores ou menores dependendo de suas necessidades energéticas. (**)Valores diários não estabelecidos.</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:'TabelaColageno',

    data() {
        return {
            dataTable: [
                {
                    col1: 'Valor Energético',
                    col2: '33 Kcal = 139 kJ',
                    col3: '2%',
                },
                {
                    col1: 'Carboidratos',
                    col2: '6,5 g',
                    col3: '2%',
                },
                {
                    col1: 'Proteínas',
                    col2: '2,3 g',
                    col3: '2%',
                },
                {
                    col1: 'Fibra Alimentar',
                    col2: '6,47 g',
                    col3: '26%',
                },
                {
                    col1: 'Sódio',
                    col2: '5 mg',
                    col3: '0%',
                },
                {
                    col1: 'Verisol©',
                    col2: '2,5 g',
                    col3: '**',
                },
                {
                    col1: 'Silício Orgânico (Nutracolin©)',
                    col2: '100 μg',
                    col3: '**',
                },
                {
                    col1: 'Ácido Hialurônico',
                    col2: '50 mg',
                    col3: '**',
                },
                {
                    col1: 'Vitamina C',
                    col2: '45 mg',
                    col3: '100%',
                },
                {
                    col1: 'Ácido Pantotênico',
                    col2: '4 mg',
                    col3: '80%',
                },
                {
                    col1: 'Zinco',
                    col2: '1,7 mg',
                    col3: '24%',
                },
                {
                    col1: 'Vitamina B6',
                    col2: '1 mg',
                    col3: '77%',
                },
                {
                    col1: 'Manganês',
                    col2: '0,5 mg',
                    col3: '21%',
                },
                {
                    col1: 'Vitamina A',
                    col2: '480 μg',
                    col3: '80%',
                },
                {
                    col1: 'Cobre',
                    col2: '216 μg',
                    col3: '24%',
                },
                {
                    col1: 'Biotina',
                    col2: '24 μg',
                    col3: '80%',
                },
                {
                    col1: 'Vitamina B12',
                    col2: '0,56 μg',
                    col3: '23%',
                },
            ],
        };
    },
}
</script>

<style scoped>
p {
    font: normal normal normal 14px/18px Open Sans;
    letter-spacing: -0.28px;
    color: #000;
    padding-top: 10px;
    margin-bottom: -10px;
    padding-bottom: 5px;
}

.row div{
    border-radius: 10px;
}

table{
    border-collapse: separate;
    border: 1px solid #000;
    border-radius: 10px!important;
}

th, td {
    color: #000;
    padding: 3px 20px;
    font: normal normal normal 16px/20px Open Sans;
    letter-spacing: -0.32px;
}

th strong {
    font: normal normal 800 20px/26px Open Sans;
    letter-spacing: -0.4px;
    color: #000;
}

thead th{
    border: 0;
    border-radius: 10px;
}

.titulo strong{
    font: normal normal bold 20px/20px Open Sans;
    letter-spacing: -0.8px;
    color: #333333;
}

.subtitulo{
    font: normal normal normal 16px/16px Open Sans;
    letter-spacing: -0.64px;
    color: #333333;
}

.porcao strong{
    font: normal normal bold 18px/18px Open Sans;
    letter-spacing: -0.36px;
    color: #333333;
}

.adicional-tabela{
    font: normal normal normal 14px/18px Open Sans;
    letter-spacing: -0.56px;
    color: #333333;
}

@media(max-width: 768px) {
    .row.align-items-center.py-3 {
        padding-top: 5px !important;
    }

    p {
        font: normal normal normal 12px/15px Open Sans;
        padding-top: 10px;
    }

    th, td {
        font: normal normal normal 12.5px/15px Open Sans;
    }

    th strong {
        font: normal normal 800 15px/18px Open Sans;
    }
}

@media(max-width: 362px){
    th, td {
        font: normal normal normal 11px/15px Open Sans;
    } 
}
</style>