<template>
   <div class="buttons-demo">
    <dx-check-box v-model="button1" text="Click to change buttons"/>
    <div>
      <dx-button template="button1Template" v-if="button1">
        <template #button1Template="{}">Button 1</template>
      </dx-button>
      <dx-button template="button2Template" v-else>
        <template #button2Template="{}">Button 2</template>
      </dx-button>
    </div>
  </div>
</template>

<script>
import ExampleBlock from "./example-block";

import { DxButton, DxCheckBox } from "../../src";

export default {
  components: {
    DxCheckBox,
    DxButton
  },
  data: function() {
      return {
       button1: true
      }
  }
};
</script>