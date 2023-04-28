<template>
    <a href="https://github.com/vuejs/language-tools/issues/2742">Issue 2742</a>
</template>

<script lang="ts">
    import { defineComponent, PropType } from 'vue';

    export default defineComponent({
        name: 'PComponentIssue',

        props: {
            propOptional: {
                type: undefined as unknown as PropType<string>
            },
            propOptionalWithDefault: {
                default: true,
                type: undefined as unknown as PropType<boolean>
            },
            propMandatory: {
                required: true,
                type: undefined as unknown as PropType<number>
            }
        },

        emits: {
            'event-without-payload': (): void => { },
            'event-with-payload': (a: number, b: boolean) => { }
        },

        created(): void {
            this.$emit('event-without-payload');
            this.$emit('event-with-payload', 1, true);
        },
    });
</script>