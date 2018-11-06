<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h3>{{ user.name }}</h3>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import { User } from '../models/user';

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
  @Prop() private user!: User;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
