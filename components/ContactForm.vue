<template>
  <form class="max-w-screen-sm md:max-w-screen-md lg:max-w-full" @submit.prevent="handleSubmit">
    <label class="text-white" for="name">Name</label>
    <input
      type="text"
      id="name"
      name="First Name"
      placeholder="Your name"
      v-model="nameInput"
      class="w-full p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
      required
    />
    <label class="text-white" for="email">Email</label>
    <input
      type="email"
      name="email"
      id="email"
      placeholder="Your email"
      v-model="emailInput"
      class="w-full p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
      required
    />
    <label class="text-white" for="message">Message</label>
    <textarea
      class="w-full h-40 p-3 border-2 border-gray-400 rounded box-border mt-1.5 mb-4 resize-y"
      type="textarea"
      name="message"
      id="message"
      v-model="messageInput"
      placeholder="Write here"
      required
    ></textarea>
    <input
      class="py-3 px-5 rounded cursor-pointer text-white bg-green-300 hover:bg-green-500"
      type="submit"
      placeholder="Submit"
    />
    <div class="text-white inline ml-5" v-if="messageSent">Message sent ✅</div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      messageSent: false,
    };
  },
  methods: {
    async handleSubmit() {
      if (
        this.nameInput &&
        /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(this.emailInput) &&
        this.messageInput
      ) {
        try {
          const response = await fetch("https://api.web3forms.com/submit", {
            method: "POST",
            headers: {
              "Content-Type": "application/json",
            },
            body: JSON.stringify({
              access_key: "6e598c04-34c4-4c0a-9678-ace03cf38c95",
              botcheck: "",
              redirect: "https://portfolio-carina-meireles.netlify.app/contact",
              name: this.nameInput,
              email: this.emailInput,
              message: this.messageInput,
            }),
          });
          if (response.ok) {
            this.messageSent = true;
            this.nameInput = "";
            this.emailInput = "";
            this.messageInput = "";
          } else {
            console.error("Form submission failed:", response.statusText);
          }
        } catch (error) {
          console.error("An error occurred during form submission:", error);
        }
      }
    },
  },
};
</script>
