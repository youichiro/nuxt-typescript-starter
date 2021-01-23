<template>
<div>
  <h1>This is Test</h1>
  <TestComponent :user="testUser" />
</div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import TestComponent from "~/components/TestComponent.vue";

@Component({
  components: {
    TestComponent,
  },
})
export default class IndexPage extends Vue {
  myname = {
      firstName: "aki",
      lastName: "kato"
    }
  get testUser(){
    return this.myname
  }
}
</script>
