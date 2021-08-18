<template>
    <div class="action-list">
        <p class="header ma-0">
            <span v-if="first" class="first">{{ first }}</span>
            <span v-if="second" class="second">{{ second }}</span>
        </p>
        <ul class="lines pa-0">
            <li v-for="line in lines" :key="line" class="line">✓ {{ line }}</li>
        </ul>
    </div>
</template>

<script>
export default {
    props: {
        first: {
            type: String,
            default: null
        },
        second: {
            type: String,
            default: null
        },
        lines: {
            type: Array,
            default: () => []
        }
    }
}
</script>

<style>
.action-list > .header {
    font-size: 40px;
    font-weight: bold;
    text-transform: uppercase;
}

.action-list > .header > .first {
    background: #ba007c;
    color: #ff0;
    padding: 1px;
    line-height: 1.2em;
}

.action-list > .header > .second {
    color: #000085;
}

.action-list > .lines {
    font-size: 30px;
    font-weight: bold;
    line-height: 1.2em;
    color: #00adef;
    list-style: none;
}
</style>
