<template>
  <div class="props-accordion">
    <slot />
  </div>
</template>

<script setup>
import { defineProps, computed } from 'vue'

// name: 'AreaProps',
defineProps({
  accordion: { type: Object, required: true },
})
</script>

<style scoped lang="scss">
.props-accordion {
  overflow: scroll;
  display: flex;
  flex-direction: column;
  > * {
    flex: 1;
  }
}

* {
  scrollbar-width: thin;
  scrollbar-color: #491988 #300748;
}
::-webkit-scrollbar {
  width: 5px;
}
::-webkit-scrollbar:horizontal {
  height: 5px;
}
::-webkit-scrollbar-track {
  background: #300748;
  border-radius: 10px;
}
::-webkit-scrollbar-thumb {
  background: #491988;
  border-radius: 10px;
}
::-webkit-scrollbar-thumb:hover {
  background: #5c26a2;
}
</style>
