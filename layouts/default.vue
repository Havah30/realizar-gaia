<template>
    <v-app>
        <v-app-bar color="iniciativa-blue" dense flat fixed app>
            <img src="/iniciativa.png" class="fill-height pa-2" contain />
            <v-spacer />
            <v-btn color="white" plain @click="$vuetify.goTo('#candidatos')"
                >Candidatos</v-btn
            >
        </v-app-bar>
        <v-main>
            <Nuxt />
        </v-main>
        <v-footer class="iniciativa-blue white--text" app>
            <span
                >&copy; {{ new Date().getFullYear() }} Iniciativa Liberal</span
            >
            <v-spacer />
            <v-btn icon href="mailto:gaia@liberal.pt" target="_blank">
                <v-icon color="white" tag="a">mdi-email</v-icon>
            </v-btn>
            <v-btn
                icon
                href="https://www.facebook.com/ILiberalGaia"
                target="_blank"
            >
                <v-icon color="white" tag="a">mdi-facebook</v-icon>
            </v-btn>
            <v-btn icon href="https://twitter.com/GaiaLiberal" target="_blank">
                <v-icon color="white" tag="a">mdi-twitter</v-icon>
            </v-btn>
            <v-btn
                icon
                href="https://www.instagram.com/gaialiberal"
                target="_blank"
            >
                <v-icon color="white" tag="a">mdi-instagram</v-icon>
            </v-btn>
        </v-footer>
    </v-app>
</template>
