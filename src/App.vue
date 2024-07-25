<template>
  <Commentator/>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import Commentator from './components/Commentator.vue';

@Options({
  components: {
    Commentator,
  },
})
export default class App extends Vue {}
</script>