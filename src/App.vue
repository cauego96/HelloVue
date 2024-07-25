<template>
  <div>
    <CommentatorComponent commentator="Caue Oliveira" />
  </div>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';
  import CommentatorComponent from './components/CommentatorComponent.vue';

  export default defineComponent({
    name: 'ParentComponent',
    components: {
        CommentatorComponent
    }
  });
</script>