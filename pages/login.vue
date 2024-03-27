
<template>
  <div class="flex items-center justify-center min-h-screen w-full">
    <div class="rounded bg-sidebar w-1/4 p-5">
      <h1 class="text-2xl font-bold text-center mb-5">Login</h1>

      <form>
        <UiInput placeholder='Email' type="email" class="mb-3" v-model='EmailRef'/>
        <UiInput placeholder='Email' type="password" class="mb-3" v-model='PasswordRef'/>
        <UiInput placeholder='Email' type="name" class="mb-3" v-model='NameRef'/>
        <div class="flex items-center justify-center gap-5">
          <UiButton type="button">Login</UiButton>
          <UiButton type="button">Register</UiButton>
        </div>
      </form>
    </div>
  </div>
</template>

<script setup lang="ts">

  import {useIsLoadingStore} from "~/store/auth.store";

  useSeoMeta({
        title: "Login",
      }
  )

  const emailRef = ref('')
  const passwordRef = ref('')
  const nameRef = ref('')

  const isLoadingStore = useIsLoadingStore()

  const router = useRouter()

  const login = async () => {
    isLoadingStore.set(true)
    await accont.createEmailSession(emailRef.value, passwordRef.value)
    // const response = await account.get()
  }

</script>

<style lang="scss" scoped>

</style>