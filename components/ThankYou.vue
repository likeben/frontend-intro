<script setup lang="ts">
import { ref } from "vue";
import confetti from "canvas-confetti";

const text = ref("前端技术之旅告一段落");

const onClick = () => {
  text.value = "谢谢大家，撒个花吧";

  const triangle = confetti.shapeFromPath({ path: "M0 10 L5 0 L10 10z" });

  confetti({
    shapes: [triangle],
  });
};
</script>

<template>
  <div class="h-full grid place-items-center">
    <div class="text-center">
      <h1>{{ text }}</h1>
      <button
        class="h-10 px-6 font-semibold rounded-md bg-indigo-600 text-white text-sm"
        v-show="text !== '谢谢大家，撒个花吧'"
        @click="onClick"
      >
        该做点什么呢
      </button>
    </div>
  </div>
</template>
