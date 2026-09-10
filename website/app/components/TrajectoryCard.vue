<script setup lang="ts">
  const props = defineProps<{
    title: string
    description: string
    timeline: "present" | "soon" | "far"
    date: string
    place?: string
    popupList: string[]
  }>()
</script>

<template>
  <article>
    <div>
      <p>{{ date }}</p>

      <div>
        <h3>title</h3>
        <p
          v-if="place"
        >
          - {{ place }}
        </p>
      </div>

      <p>{{ description }}</p>

      <div>
        <p
          v-for="popup in popupList"
          :key="popup"
        >
          {{ popup }}
        </p>
      </div>
    </div>
  </article>
</template>