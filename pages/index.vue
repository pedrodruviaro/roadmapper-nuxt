<script setup lang="ts"></script>

<template>
  <article
    class="grid gap-4 md:grid-cols-[1fr_2fr] lg:gap-6 xl:grid-cols-[1fr_2.5fr]"
  >
    <aside class="space-y-4 lg:space-y-6">
      <Card class="bg-gradient-to-r from-pink-500 to-cyan-500 text-white">
        <template #content>
          <div class="md:pt-10">
            <h1 class="font-bold mb-1 text-xl">Roadmapper</h1>
            <p>Feedback Board</p>
          </div>
        </template>
      </Card>

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

      <Card>
        <template #content>
          <div>
            <h2 class="font-black lg:text-lg">Roadmap</h2>
            <ul class="grid gap-1 mt-3">
              <li class="flex items-center justify-between">
                <div class="flex-1 flex items-center gap-2">
                  <span class="block w-2 h-2 rounded-full bg-pink-400"></span>
                  <p>Planned</p>
                </div>
                <span class="block font-semibold text-slate-700">3</span>
              </li>

              <li class="flex items-center justify-between">
                <div class="flex-1 flex items-center gap-2">
                  <span class="block w-2 h-2 rounded-full bg-yellow-400"></span>
                  <p>In-Progress</p>
                </div>
                <span class="block font-semibold text-slate-700">6</span>
              </li>

              <li class="flex items-center justify-between">
                <div class="flex-1 flex items-center gap-2">
                  <span class="block w-2 h-2 rounded-full bg-cyan-400"></span>
                  <p>Live</p>
                </div>
                <span class="block font-semibold text-slate-700">1</span>
              </li>
            </ul>
          </div>
        </template>
      </Card>
    </aside>

    <section class="space-y-4 lg:space-y-6">
      <Card class="bg-slate-700 text-white">
        <template #content>
          <div class="flex flex-wrap gap-4 justify-between">
            <div class="flex items-center gap-2">
              <i class="pi pi-tags text-lg lg:text-xl"></i>
              <h2 class="font-bold text-lg lg:text-xl">6 Suggestions</h2>
            </div>

            <Button label="Add Feedback" size="small" icon="pi pi-plus" />
          </div>
        </template>
      </Card>

      <div class="space-y-4">
        <Card v-for="i in 6">
          <template #content>list item</template>
        </Card>
      </div>
    </section>
  </article>
</template>
