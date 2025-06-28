<template>
    <v-sheet class="mx-auto">
        <v-slide-group :show-arrows="false">
            <v-slide-group-item
                v-for="(category, i) in categories"
                :key="i"
                v-slot="{ isSelected, toggle }"
            >
                <v-btn
                    :color="isSelected ? 'primary' : undefined"
                    class="ma-0"
                    rounded="0"
                    elevation="0"
                    @click="toggle"
                    style="width: 80px; height: 80px;"
                >
                    <v-row>
                        <v-col style="display: flex; align-items: center; justify-content: center; flex-direction: column;">
                            <v-img
                                :lazy-src="category.img"
                                :src="category.img"
                                height="40"
                                width="40"
                                class="mb-2"
                                cover
                                rounded
                            />
                            
                            <span class="text-caption">
                                {{ category.label }}
                            </span>
                        </v-col>
                    </v-row>
                </v-btn>
            </v-slide-group-item>
        </v-slide-group>
    </v-sheet>
</template>

<script setup>
const categories = [
    { img: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg', label: 'Sunshine' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', label: 'Road' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', label: 'House' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg', label: 'Sunshine' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', label: 'Road' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', label: 'House' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg', label: 'Sunshine' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/road.jpg', label: 'Road' },
    { img: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', label: 'House' },
    // Adicione mais categorias conforme necessário
]
</script>