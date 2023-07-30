<script setup>
  import { ref } from 'vue'
  import { useElementVisibility  } from '@vueuse/core'
  import HelloWorld from './components/HelloWorld.vue'

  const templateRef = ref(null)
  const isElementVisible = useElementVisibility(templateRef)
</script>

<template>
  <HelloWorld :msg="'this tracking-widest'"/>
  <main
    ref="templateRef"
    class="p-3 bg-yellow-200" >
    Tailwind CSS: this text should have background color of
    <code>bg-yellow-200</code>
  </main>

  <div class="h-[110vh]"></div>

  <section class="fixed bottom-0 right-0">useElementVisibility check (scroll to see): {{ isElementVisible }}</section>

</template>
