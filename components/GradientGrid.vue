<template>
  <section>
    <div class="grid max-w-screen-xl grid-cols-1 gap-8 px-4 mx-auto sm:px-6 lg:px-8 sm:grid-cols-2 lg:grid-cols-3">
      <gradient-card
        v-for="gradient of gradients"
        :key="gradient.id"
        :name="gradient.name"
        :colors="gradient.colors"
        :direction="gradient.direction"
        :version="gradient.version"
        :controls="directions"
        :overlap="overlap"
        v-on="$listeners"
      />
    </div>
  </section>
</template>

<script>
export default {
  props: {
    gradients: {
      type: Array,
      required: true
    },
    directions: {
      type: Boolean,
      default: true
    },
    overlap: {
      type: Boolean,
      default: true
    }
  }
}
</script>
