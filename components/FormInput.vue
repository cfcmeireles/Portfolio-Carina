<template>
  <form action="https://api.web3forms.com/submit" method="POST">
    <input
      type="hidden"
      name="access_key"
      value="6e598c04-34c4-4c0a-9678-ace03cf38c95"
    />
    <input
      type="checkbox"
      name="botcheck"
      class="hidden"
      style="display: none"
    />
    <input
      type="hidden"
      name="redirect"
      value="https://portfolio-carina-meireles.netlify.app/submit"
    />
    <label class="text-white" for="name">Name</label>
    <input
      type="text"
      id="name"
      name="First Name"
      placeholder="Your name"
      class="w-full p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
      required
    />
    <label class="text-white" for="email">Email</label>
    <input
      type="email"
      name="email"
      id="email"
      placeholder="Your email"
      class="w-full p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
      required
    />
    <label class="text-white" for="subject">Subject</label>
    <textarea
      class="w-full h-40 p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
      type="textarea"
      name="message"
      id="subject"
      placeholder="Write here"
      required
    ></textarea>
    <input
      class="py-3 px-5 rounded cursor-pointer text-white bg-green-300 hover:bg-green-500"
      type="submit"
      placeholder="Submit"
    />
  </form>
</template>



