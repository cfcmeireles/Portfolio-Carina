<template>
  <label :for="label"> {{ label }}</label>
  <input
    v-if="type === 'text' || type === 'email'"
    :type="type"
    :id="id"
    :placeholder="placeholder"
    class="w-full p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
  />
  <textarea
    v-else-if="type === 'textarea'"
    class="w-full h-40 p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
    :type="type"
    :id="id"
    :placeholder="placeholder"
  ></textarea>
  <input
    v-else
    class="py-3 px-5 rounded cursor-pointer text-white bg-green-300 hover:bg-green-500"
    :type="type"
  />
</template>


<script>
export default {
  props: {
    label: {
      type: String,
    },
    type: {
      type: String,
      required: true,
    },
    id: {
      type: String,
    },
    placeholder: {
      type: String,
    },
  },
};
</script>
