<script setup lang="ts"></script>

<template>
  <article
    class="grid gap-4 md:grid-cols-[1fr_2fr] lg:gap-6 xl:grid-cols-[1fr_2.5fr]"
  >
    <aside class="space-y-4 lg:space-y-6">
      <DashboardAsideBox />
      <DashboardAsideFilters />
      <DashboardAsideRoadmap />
    </aside>

    <section class="space-y-4 lg:space-y-6">
      <DashboardHeader />

      <div class="space-y-4">
        <RoadmapCard
          v-for="i in 6"
          :key="i"
          id="1"
          title="New Feature"
          description="Hello feature!"
          tag="Feature"
          :comments="4"
          @wants-to-comment="(id: string) => console.log('* -> wants to comment!', id)"
        />
      </div>
    </section>
  </article>
</template>
