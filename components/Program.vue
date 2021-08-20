<template>
    <v-expansion-panels class="program">
        <v-expansion-panel v-for="item in items" :key="item.header">
            <v-expansion-panel-header
                class="program-header iniciativa-blue--text"
            >
                {{ item.header }}
                <template #actions>
                    <v-icon color="iniciativa-blue"> $expand </v-icon>
                </template>
            </v-expansion-panel-header>
            <v-expansion-panel-content>
                <ul class="program-list grey--text text--darken-1">
                    <li v-for="line in item.content" :key="line">{{ line }}</li>
                </ul>
            </v-expansion-panel-content>
        </v-expansion-panel>
    </v-expansion-panels>
</template>

<script>
export default {
    props: {
        items: {
            type: Array,
            default: () => []
        }
    }
}
</script>

<style>
.program .program-header {
    font-weight: 700;
    font-size: 26px;
}

.program .program-list {
    font-size: 18px;
}
</style>
