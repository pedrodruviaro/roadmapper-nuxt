<script setup lang="ts"></script>

<template>
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
</template>
