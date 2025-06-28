<template>
    <v-container
        style="background-color: #232f3e;"
    >
        <v-row justify="center">
            <v-col>
                <v-text-field
                    v-model="search"
                    label="Pesquise na Amazon.com.br"
                    prepend-inner-icon="mdi-magnify"
                    outlined
                    clearable
                    hide-details="auto"
                    @keyup.enter="onSearch"
                    :append-outer-icon="search ? 'mdi-arrow-right' : ''"
                    @click:append-outer="onSearch"
                    style=" background-color: white; border-radius: 10px;"
                />
            </v-col>
        </v-row>
    </v-container>
</template>

<script setup>
import { ref } from 'vue'

const search = ref('')

function onSearch() {
    if (search.value.trim()) {
        // Adicione aqui a lógica de pesquisa, por exemplo:
        // this.$emit('search', search.value)
        alert(`Pesquisando por: ${search.value}`)
    }
}
</script>