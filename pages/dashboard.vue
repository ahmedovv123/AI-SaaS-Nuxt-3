<template>
  <div>
    <div class="mb-8 space-y-4">
      <h2 class="text-2xl md:text-4xl font-bold text-center">Explore the power of AI</h2>
      <p class="text-muted-foreground font-light text-sm md:text-lg text-center">Chat with the smartest AI - Explore the power of AI</p>
    </div>
    <div class="px-4 md:px-20 lg:px-32 space-y-4">
      <div
        v-for='tool in tools' :key="tool.link" @click="navigateTo(`${tool.link}`)"
        class="p-4 border-muted border flex items-center justify-between hover:shadow-sm transition cursor-pointer"
      >
        <div class="flex items-center gap-x-4">
          <div :class="`p-2 w-fit rounded-md ${tool.bgColor}`">
            <Icon :name="tool.icon" :class="`h-8 w-8 ${tool.color}`"/>
          </div>
          <div class="font-semibold">
            {{ tool.label }}
          </div>
        </div>
        <Icon name="lucide:arrow-right" class="w-5 h-5"/>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">

</script>

<style scoped>

</style>