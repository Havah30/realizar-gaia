<template>
    <div class="candidates">
        <div
            v-for="candidate in candidates"
            :key="candidate.title"
            class="candidate pa-5"
            :style="candidateStyle(candidate)"
        >
            <div class="label white--text blue darken-4 px-6 py-2">
                <div class="name">{{ candidate.title }}</div>
                <div class="sub-title grey--text text--lighten-1">
                    {{ candidate.subtitle }}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        candidates: {
            type: Array,
            default: () => []
        }
    },
    methods: {
        candidateStyle(candidate) {
            return {
                "background-image": `url(${candidate.photo})`
            }
        }
    }
}
</script>

<style>
.candidates {
    display: flex;
    flex-wrap: wrap;
    text-transform: uppercase;
}

.candidates > .candidate {
    height: 367px;
    width: 367px;
    margin-right: 20px;
    margin-bottom: 20px;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
}

.candidates > .candidate:last-child {
    margin-right: 0;
}

.candidates > .candidate > .label > .name {
    font-size: 24px;
    font-weight: 700;
}

.candidates > .candidate > .label > .sub-title {
    font-size: 16px;
    font-weight: 600;
}
</style>
