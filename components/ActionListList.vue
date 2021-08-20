<template>
    <div class="action-list-list">
        <ActionList
            v-for="item in items"
            :key="`${item.first}${item.second}`"
            v-bind="item"
        />
    </div>
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
.action-list-list > .action-list {
    margin-bottom: 16px;
}

.action-list-list > .action-list:last-child {
    margin-bottom: 0;
}
</style>
