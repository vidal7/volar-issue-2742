<template>
    <p-component-issue :prop-obligatoire="2"
                       :prop-optionnelle="'abc'"
                       :prop-optionnelle-avec-defaut="true"></p-component-issue>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';
    import PComponentIssue from './p-component-issue.vue';

    export default defineComponent({
        components: { PComponentIssue }
    });
</script>