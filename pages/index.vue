<template>
    <div class="index">
        <v-container>
            <div class="banner mt-4 mb-16 mx-auto">
                <v-img src="/banner.jpg" max-width="100%" contain />
            </div>
            <ActionList
                first="realizar"
                second="gaia"
                :lines="actionListLines"
            />
        </v-container>
        <div
            id="candidatos"
            class="candidatos iniciativa-blue white--text my-16"
        >
            <v-container>
                <h1 class="my-4">Os nossos candidatos</h1>
                <Candidates :candidates="candidates" />
            </v-container>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        actionListLines: {
            type: Array,
            default: () => ["Fazer isto", "E aquilo"]
        },
        candidates: {
            type: Array,
            default: () => [
                {
                    title: "Orlando Monteiro da Silva",
                    subtitle: "Câmara Municipal de Gaia",
                    photo: "https://picsum.photos/600"
                },
                {
                    title: "Rui Leite de Castro",
                    subtitle: "Assembleia Municipal de Gaia",
                    photo: "https://picsum.photos/600"
                },
                {
                    title: "Miguel Monteiro dos Santos",
                    subtitle: "Junta de Freguesia de Vilar de Andorinho",
                    photo: "https://picsum.photos/600"
                },
                {
                    title: "Pedro Matos",
                    subtitle:
                        "Junta de Freguesia de Mafamude e Vilar do Paraíso",
                    photo: "https://picsum.photos/600"
                }
            ]
        }
    }
}
</script>

<style>
.index > .banner {
    max-width: 800px;
}
</style>
