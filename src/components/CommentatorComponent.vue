<template>
    <div>
        <button @click="comment">
            Comment
        </button>
        <p>
            {{ commentary }}
        </p>
        <p>
            Name: {{ commentator }}
        </p>
    </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
    name: 'CommentatorComponent',
    props:  {
        commentator: {
            type: String,
            required: true
        }
    },
    setup(props) {
        const commentary = ref('');

        const comment = () => {
            commentary.value = "Olá Vue";
        };

        return {
            commentary,
            comment,
            props : props.commentator
        };
    }
});
</script>