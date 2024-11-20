<script setup lang="ts">
const props = defineProps<{
  id: string
  title: string
  description: string
  tag: string
  comments: number
}>()

const emits = defineEmits<{
  "wants-to-comment": [id: string]
}>()
</script>

<template>
  <Card>
    <template #content>
      <div
        class="grid grid-cols-[1fr_max-content] gap-4 items-start md:items-center"
      >
        <div>
          <h3 class="text-base font-semibold">{{ props.title }}</h3>
          <p class="text-sm my-2">{{ props.description }}</p>
          <Badge :value="props.tag" severity="secondary" />
        </div>

        <div>
          <button
            class="flex max-w-max items-center gap-2"
            @click="emits('wants-to-comment', props.id)"
          >
            <i class="pi pi-comment"></i>
            <span class="text-slate-700 font-semibold">{{
              props.comments
            }}</span>
          </button>
        </div>
      </div>
    </template>
  </Card>
</template>
