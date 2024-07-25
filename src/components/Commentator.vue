<template>
    <div>
        <button @click="comment">
            Comment
        </button>
        <p>
            {{ commentary }}
        </p>
    </div>
</template>

<script lang="ts">

import { defineComponent, ref } from 'vue';

export default defineComponent({
    name: 'CommentatorComponent',
    setup() {
        const commentary = ref('');

        const comment = () => {
            commentary.value = "Olá Vue";
        };

        return {
            commentary,
            comment
        };
    }
});
</script>