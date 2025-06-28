<template>
    <v-container class="enviar-para-container" fluid>
        <v-row align="center" no-gutters>
            <v-col cols="auto">
                <v-icon color="white" size="22" class="mr-2">mdi-map-marker-outline</v-icon>
                <span class="enviar-para-label">Enviar para</span>
            </v-col>
            <v-col cols="auto">
                <v-select
                    v-model="selectedState"
                    :items="states"
                    item-title="state"
                    item-value="abbr"
                    hide-details
                    return-object
                    single-line
                    dense
                    class="enviar-para-select"
                    placeholder="Selecione"
                    style="min-width: 120px"
                />
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    name: "HomeEnviarPara",
    data() {
        return {
            selectedState: null,
            states: [
                { state: 'Acre', abbr: 'AC' },
                { state: 'Alagoas', abbr: 'AL' },
                { state: 'Amapá', abbr: 'AP' },
                { state: 'Amazonas', abbr: 'AM' },
                { state: 'Bahia', abbr: 'BA' },
                { state: 'Ceará', abbr: 'CE' },
                { state: 'Distrito Federal', abbr: 'DF' },
                { state: 'Espírito Santo', abbr: 'ES' },
                { state: 'Goiás', abbr: 'GO' },
                { state: 'Maranhão', abbr: 'MA' },
                { state: 'Mato Grosso', abbr: 'MT' },
                { state: 'Mato Grosso do Sul', abbr: 'MS' },
                { state: 'Minas Gerais', abbr: 'MG' },
                { state: 'Pará', abbr: 'PA' },
                { state: 'Paraíba', abbr: 'PB' },
                { state: 'Paraná', abbr: 'PR' },
                { state: 'Pernambuco', abbr: 'PE' },
                { state: 'Piauí', abbr: 'PI' },
                { state: 'Rio de Janeiro', abbr: 'RJ' },
                { state: 'Rio Grande do Norte', abbr: 'RN' },
                { state: 'Rio Grande do Sul', abbr: 'RS' },
                { state: 'Rondônia', abbr: 'RO' },
                { state: 'Roraima', abbr: 'RR' },
                { state: 'Santa Catarina', abbr: 'SC' },
                { state: 'São Paulo', abbr: 'SP' },
                { state: 'Sergipe', abbr: 'SE' },
                { state: 'Tocantins', abbr: 'TO' },
            ],
        };
    },
};
</script>

<style scoped>
.enviar-para-container {
    background: #232f3e;
    color: white;
    padding: 0 16px;
    min-height: 48px;
    display: flex;
    align-items: center;
}
.enviar-para-label {
    font-weight: 500;
    font-size: 15px;
    margin-right: 8px;
}
.enviar-para-select .v-input__control {
    background: transparent;
    color: white;
}
.enviar-para-select .v-field__input {
    color: white;
}
</style>