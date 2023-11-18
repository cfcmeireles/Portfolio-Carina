<template>
  <div
    class="max-w-xl rounded-2xl max-h-full bg-gray-100 lg:hover:scale-105 lg:hover:duration-500 lg:hover:ease-in-out lg:hover:shadow-md"
  >
    <h2 class="text-xl lg:text-2xl font-bold my-3 py-5 font-rubik">
      <slot name="title"></slot>
    </h2>
    <slot name="image"></slot>
    <p class="text-sm md:text-base lg:text-lg mt-3 mx-5 font-rubik text-black">
      <slot name="description"></slot>
    </p>
    <div class="flex mx-auto mb-5 py-5 items-center justify-center">
      <slot name="skills"></slot>
    </div>
  </div>
</template>
