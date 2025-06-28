<template>
    <v-layout class="overflow-visible" style="height: 56px;">
        <v-bottom-navigation 
            v-model = "value" 
            style   = "position: fixed;"
            v-onchange="redirect_to(value)"
            grow
        >
            <v-btn>
                <v-icon>mdi-home-outline</v-icon>
                Início
            </v-btn>

            <v-btn>
                <v-icon>mdi-account-outline</v-icon>
                Conta
            </v-btn>
            
            <v-btn>
                <v-icon>mdi-cart-outline</v-icon>
                Carrinho
            </v-btn>

            <v-btn>
                <v-icon>mdi-menu</v-icon>
                Menu
            </v-btn>
        </v-bottom-navigation>
    </v-layout>
</template>

<script>
export default {
    name: "AppNavigationBar",
    data() {
        return {
            value: 0,
            routes: [
                "/"
            ]
        }
    },

    methods: {
        redirect_to(router_index) {
            const route_to_go = this.routes[router_index];

            if (route_to_go) {
                this.$router.push(route_to_go);
    
                console.log(`Redirecionando para "${route_to_go}"`);
            }
        }
    }
}
</script>
