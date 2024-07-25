<template>
    <div>
        <button @click="comment">
            Comment
        </button>
        <p>
            Name: {{ commentator }}
        </p>

        <p> 
            {{ NameAndComment }} 
        </p>
        <!-- <p>
            {{ commentary }}
        </p> -->
    </div>
</template>

<script lang="ts">
import { computed, defineComponent, ref } from 'vue';

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

        const NameAndComment = computed(() => {
            return (commentary.value != null) && (commentary.value != '') ?  `${props.commentator} - ${commentary.value}` : 'Waiting Comment'
        });

        return {
            commentary,
            comment,
            props : props.commentator,
            NameAndComment
        };
    }
    
});
</script>