<template>
  <!-- Hidden HTML form for Netlify to detect at build time -->
  <form
    name="contact-form"
    data-netlify="true"
    data-netlify-honeypot="bot-field"
    hidden
  >
    <input
      type="text"
      name="name"
    >
    <input
      type="email"
      name="email"
    >
    <textarea name="message" />
  </form>

  <UForm
    :schema="schema"
    :state="state"
    class="space-y-4"
    @submit="onSubmit"
  >
    <UFormField
      label="Email"
      name="email"
    >
      <UInput
        v-model="state.email"
        class="w-xs"
      />
    </UFormField>
    <UFormField
      label="Name"
      name="name"
    >
      <UInput
        v-model="state.name"
        type="text"
        class="w-xs"
      />
    </UFormField>
    <UFormField
      label="Message"
      name="message"
    >
      <UTextarea
        v-model="state.message"
        class="w-xs"
      />
    </UFormField>
    <UButton type="submit">
      Submit
    </UButton>
  </UForm>
</template>

<script lang="ts" setup>
import * as z from 'zod'
import type { FormSubmitEvent } from '@nuxt/ui'

const schema = z.object({
  email: z.string().email('Invalid email'),
  name: z.string().min(1, 'Name is required'),
  message: z.string().min(1, 'Message is required')
})

type Schema = z.output<typeof schema>

const state = reactive<Partial<Schema>>({
  email: undefined,
  name: undefined,
  message: undefined
})

const toast = useToast()

async function onSubmit(event: FormSubmitEvent<Schema>) {
  const formData = new FormData()
  formData.append('form-name', 'contact-form')
  formData.append('email', event.data.email)
  formData.append('name', event.data.name)
  formData.append('message', event.data.message)

  try {
    await fetch('/', {
      method: 'POST',
      headers: { 'Content-Type': 'application/x-www-form-urlencoded' },
      // eslint-disable-next-line @typescript-eslint/no-explicit-any
      body: new URLSearchParams(formData as any).toString()
    })
    toast.add({ title: 'Success', description: 'The form has been submitted.', color: 'success' })

    // reset the state
    state.email = undefined
    state.name = undefined
    state.message = undefined
  } catch (error) {
    toast.add({ title: 'Error', description: 'Failed to submit form.', color: 'error' })
    console.log(error)
  }
}
</script>
