<template>
  <div
    class="max-w-xl rounded-2xl max-h-full bg-gray-100 transition-transform duration-300 transition-margin duration-300 transform scale-100 lg: hover:scale-110 transition-transform duration-500 ease-in-out shadow-md"
  >
    <h2 class="text-2xl font-bold my-3 py-5 font-rubik">
      <slot name="title"></slot>
    </h2>
    <slot name="image"></slot>
    <p class="mt-3 mx-5 font-rubik text-black">
      <slot name="description"></slot>
    </p>
    <div class="flex mx-auto mb-5 py-5 items-center justify-center">
      <slot name="skills"></slot>
    </div>
  </div>
</template>