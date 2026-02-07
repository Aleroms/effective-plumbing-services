<template>
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

<script
    lang="ts"
    setup
  >
import * as z from 'zod'
import type { FormSubmitEvent } from '@nuxt/ui'

const schema = z.object({
  email: z.email('Invalid email'),
  name: z.string('Name is required'),
  message: z.string('Message is required')
})

type Schema = z.output<typeof schema>

const state = reactive<Partial<Schema>>({
  email: undefined,
  name: undefined,
  message: undefined
})

const toast = useToast()

async function onSubmit(event: FormSubmitEvent<Schema>) {
  toast.add({ title: 'Success', description: 'The form has been submitted.', color: 'success' })
  console.log(event.data)
}
</script>
