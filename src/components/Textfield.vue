<script setup>
const props = defineProps({
  value: {
    required: true,
  },
  className: {},
});
const emit = defineEmits(["update:value"]);

const handleChange = (e) => {
  emit("update:value", e.target.value);
  console.log(props.value);
};
</script>
<template>
  <div>
    <input
      :value="props.value"
      type="text"
      id="first_name"
      @change="handleChange"
      :class="[
        'bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500',
        props.className,
      ]"
      placeholder="search"
      required />
  </div>
</template>
