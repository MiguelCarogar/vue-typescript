<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld :user="user" msg="Welcome to Your Vue.js + TypeScript App"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import { User } from '../models/user';

@Component({
  components: {
    HelloWorld,
  },
})
export default class Home extends Vue {
  private user: User;

  constructor() {
    super();
    this.user = {
      id: 1,
      name: 'Peter',
    };
  }
}
</script>
