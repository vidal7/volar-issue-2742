<template>
    <p-component-issue :prop-mandatory="2"
                       :prop-optional="'abc'"
                       :prop-optional-with-default="true"
                       @event-without-payload="handleEventWithoutPayload"
                       @event-with-payload="handleEventWithPayload"></p-component-issue>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';
    import PComponentIssue from './p-component-issue.vue';

    export default defineComponent({
        components: { PComponentIssue },

        methods: {
            handleEventWithoutPayload(): void {
                console.log('handleEventWithoutPayload');
            },

            handleEventWithPayload(): void {
                console.log('handleEventWithPayload');
            }
        }
    });
</script>