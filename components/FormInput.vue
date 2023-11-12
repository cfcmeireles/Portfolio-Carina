<template>
  <label :for="label"> {{ label }}</label>
  <input
    v-if="type !== 'textarea'"
    :type="type"
    :id="id"
    :placeholder="placeholder"
    class="w-full p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
  />
  <textarea
    v-else
    class="w-full h-40 p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
    :type="type"
    :id="id"
    :placeholder="placeholder"
  ></textarea>
</template>


<script>
export default {
  props: {
    label: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      required: true,
    },
    id: {
      type: String,
      required: true,
    },
    placeholder: {
      type: String,
      required: true,
    },
  },
};
</script>
