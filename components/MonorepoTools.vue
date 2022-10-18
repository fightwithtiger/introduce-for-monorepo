<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  count: {
    default: 0,
  },
})

interface Tool {
  name: string
  url: string
}

const tools = [
  {
    name: 'Bazel',
    url: 'https://github.com/bazelbuild/bazel?utm_source=monorepo.tools',
  },
  {
    name: 'Gradle',
    url: 'https://github.com/gradle/gradle?utm_source=monorepo.tools',
  },
  {
    name: 'Lage',
    url: 'https://github.com/microsoft/lage?utm_source=monorepo.tools',
  },
  {
    name: 'Lerna',
    url: 'https://github.com/lerna/lerna',
  },
  {
    name: 'pnpm',
    url: 'https://github.com/pnpm/pnpm',
  },
  {
    name: 'Nx',
    url: 'https://github.com/nrwl/nx',
  },
  {
    name: 'Pants',
    url: 'https://github.com/pantsbuild/pants',
  },
  {
    name: 'Rush',
    url: 'https://github.com/microsoft/rushstack',
  },
  {
    name: 'Turborepo',
    url: 'https://github.com/vercel/turborepo',
  },
]

const handleClick = (tool: Tool) => {
  window.open(tool.url)
}

</script>

<template>
  <div flex="~ wrap gap6" w="140" m-x="auto" >
    <div 
      decoration-none
      border="1px solid gray-300 opacity-50"
      p-x="3"
      p-y="4"
      font="mono"
      hover:bg="amber-400"
      w="40"
      rounded
      text-center
      bg="gray-200 opacity-50"
      v-for="tool of tools"
      :key="tool.name"
      :href="tool.url"
      @click="handleClick(tool)"
    >
      {{ tool.name }}
    </div>
  </div>
</template>
