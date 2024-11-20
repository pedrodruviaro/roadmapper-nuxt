<script setup lang="ts"></script>

<template>
  <Card>
    <template #content>
      <div class="flex flex-wrap gap-3">
        <Button
          size="small"
          label="State"
          severity="secondary"
          v-for="i in 6"
        />
      </div>
    </template>
  </Card>
</template>
