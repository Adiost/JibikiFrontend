<template>
    <md-button class="md-icon-button md-dense" to="" @click="exportCard">
        <md-icon>
            backup
        </md-icon>
    </md-button>
</template>

<script>
    export default {
        name: "ExportAnki",

        props: {
            data: {
                type: Object
            },
            type: {
                type: Number
            }
        },

        methods: {
            exportCard() {
                this.$store.dispatch('generateCard', {type: this.type, data: this.data});
            }
        },
    }
</script>

<style scoped lang="scss">
    div {
        max-width: 40px;
        display: inline-flex;
        float: right;
    }

    button {
        margin: 0;
    }
</style>
