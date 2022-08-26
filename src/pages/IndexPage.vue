<template>
  <q-page class="bg">
    <div class="row bg-primary">
      <div class="col">
        <div class="prac ">
          <div
            class="text-h4 text-bold text-black q-mt-xl q-pb-lg q-pl-lg"
            style="margin-left:auto; margin-right: auto; display: block;"
          >
            Learn How to make this beautiful ui by AS (ANURAG SINGH)
          </div>
          <div class="text-h5 text-bold text-blue q-pb-sm q-pl-lg q-pr-lg">
            Join the AS academy today for free for these amazing contents
          </div>
          <q-input
            color="lime-11"
            bg-color="green"
            filled
            placeholder="Your Email"
            class="q-pl-lg q-pr-lg q-pb-lg"
            style="font-family:'Courier New', Courier, monospace;"
          >
            <template v-slot:prepend>
              <q-icon name="email" />
            </template>
            <template v-slot:append>
              <q-btn label="Start Learning" color="purple"></q-btn>
            </template>
          </q-input>
        </div>
      </div>
      <div class="col gt-sm">
        <q-img src="https://images.cdn4.stockunlimited.net/preview1300/academy-logo-design_1968150.jpg" style="height: 28%; width: 30%; margin-top:8%; margin-left: auto; margin-right:auto; display: block;"
        />
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
});
</script>
<style scoped>

/* .emge {
  background-image: url(https://images.pexels.com/photos/301926/pexels-photo-301926.jpeg?cs=srgb&dl=pexels-pixabay-301926.jpg&fm=jpg);
} */

.prac{
  text-align: center;
  max-width: 650px;
  margin-left: auto;
  margin-right: auto;
}


</style>
