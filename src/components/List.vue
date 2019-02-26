<template>
    <div class="list">
        <div class="item" v-for="(item, index) in items" :key="index">
            <slot v-bind="item" />
        </div>
    </div>
</template>

<script>
export default {
    name: 'List',
    props: {
        items: {
            type: Array,
        }
    }
}
</script>
