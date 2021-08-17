<template>
    <v-app>
        <v-app-bar color="iniciativa-blue" dense flat fixed app>
            <img src="/iniciativa.png" class="fill-height pa-2" contain />
            <v-spacer />
            <v-btn color="white" plain>Candidatos</v-btn>
        </v-app-bar>
        <v-main>
            <v-container>
                <Nuxt />
            </v-container>
        </v-main>
        <v-footer class="iniciativa-blue white--text" app>
            <span
                >&copy; {{ new Date().getFullYear() }} Iniciativa Liberal</span
            >
        </v-footer>
    </v-app>
</template>

<script>
export default {
    data() {
        return {
            items: [
                {
                    icon: "mdi-apps",
                    title: "Welcome",
                    to: "/"
                },
                {
                    icon: "mdi-chart-bubble",
                    title: "Inspire",
                    to: "/inspire"
                }
            ]
        }
    }
}
</script>
