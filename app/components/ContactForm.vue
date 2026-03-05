<template>
  <form
    name="contact-form"
    method="POST"
    data-netlify="true"
    data-netlify-honeypot="bot-field"
    class="space-y-4"
    @submit.prevent="onSubmit"
  >
    <input
      type="hidden"
      name="form-name"
      value="contact-form"
    >
    <p hidden>
      <label>Don't fill this out: <input name="bot-field"></label>
    </p>
    <div class="flex flex-col gap-1">
      <label
        for="email"
        class="text-sm font-medium"
      >Email</label>
      <input
        id="email"
        v-model="state.email"
        type="email"
        name="email"
        required
        class="w-xs rounded-md border border-gray-300 bg-white px-3 py-2 text-sm shadow-sm transition-colors focus:border-primary-500 focus:outline-none focus:ring-1 focus:ring-primary-500 dark:border-gray-600 dark:bg-gray-800 dark:text-white"
      >
    </div>
    <div class="flex flex-col gap-1">
      <label
        for="name"
        class="text-sm font-medium"
      >Name</label>
      <input
        id="name"
        v-model="state.name"
        type="text"
        name="name"
        required
        class="w-xs rounded-md border border-gray-300 bg-white px-3 py-2 text-sm shadow-sm transition-colors focus:border-primary-500 focus:outline-none focus:ring-1 focus:ring-primary-500 dark:border-gray-600 dark:bg-gray-800 dark:text-white"
      >
    </div>
    <div class="flex flex-col gap-1">
      <label
        for="message"
        class="text-sm font-medium"
      >Message</label>
      <textarea
        id="message"
        v-model="state.message"
        name="message"
        required
        rows="4"
        class="w-xs rounded-md border border-gray-300 bg-white px-3 py-2 text-sm shadow-sm transition-colors focus:border-primary-500 focus:outline-none focus:ring-1 focus:ring-primary-500 dark:border-gray-600 dark:bg-gray-800 dark:text-white"
      />
    </div>
    <button
      type="submit"
      class="rounded-md bg-primary-500 px-4 py-2 text-sm font-medium text-white shadow-sm transition-colors hover:bg-primary-600 focus:outline-none focus:ring-2 focus:ring-primary-500 focus:ring-offset-2"
    >
      Submit
    </button>
  </form>
</template>

<script lang="ts" setup>
const state = reactive({
  email: '',
  name: '',
  message: ''
})

const toast = useToast()

async function onSubmit() {
  const formData = new FormData()
  formData.append('form-name', 'contact-form')
  formData.append('email', state.email)
  formData.append('name', state.name)
  formData.append('message', state.message)

  try {
    await fetch('/', {
      method: 'POST',
      body: formData
    })
    toast.add({ title: 'Success', description: 'The form has been submitted.', color: 'success' })

    // reset the state
    state.email = ''
    state.name = ''
    state.message = ''
  } catch (error) {
    toast.add({ title: 'Error', description: 'Failed to submit form.', color: 'error' })
  }
}
</script>
