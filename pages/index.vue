<template>
  <div class="p-10">
    <h1 class="font-bold text-2xl mb-10">CRM system by Sokolov</h1>
    <div>
      <UiCard class="mb-3" draggable="true">
        <UiCardHeader role="button">name card</UiCardHeader>
        <UiCardContent>Компания</UiCardContent>
        <UiCardFooter>Date</UiCardFooter>
      </UiCard>
    </div>
  </div>
</template>

<script setup>
  useSeoMeta(
      {
        title: 'Home | CRM System',
      }
  )

</script>

<style lang="scss" scoped>

</style>