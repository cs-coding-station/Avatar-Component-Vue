<template>
  <div class="relative">
    <nuxt-img
      v-if="img"
      :src="img"
      class="h-10 w-10"
      :class="[squareAvatar, borderAvatar]"
    />

    <div
      v-else-if="initials"
      class="h-10 w-10 bg-gray-100 flex justify-center items-center font-medium text-gray-600 text-xl"
      :class="[squareAvatar, borderAvatar]"
    >
      {{ initials }}
    </div>

    <div
      v-else
      class="h-10 w-10 bg-gray-100"
      :class="[squareAvatar, borderAvatar]"
    >
      <Icon name="mdi:account" size="40" color="gray" />
    </div>

    <span
      v-if="dot"
      class="absolute top-0 left-7 rounded-full border-2 border-white h-3.5 w-3.5 bg-red-400"
      :class="`${square ? '-top-2 left-8' : 'top-0 left-7'}`"
    ></span>
  </div>
</template>

<script setup>
const props = defineProps({
  img: {
    type: String,
  },
  square: {
    type: Boolean,
  },
  border: {
    type: Boolean,
  },
  initials: {
    type: String,
  },
  dot: {
    type: Boolean,
  },
});

const squareAvatar = computed(() => {
  if (props.square) return "rounded";
  return "rounded-full";
});

const borderAvatar = computed(() => {
  if (props.border) return "ring-2 ring-blue-500";
});
</script>
