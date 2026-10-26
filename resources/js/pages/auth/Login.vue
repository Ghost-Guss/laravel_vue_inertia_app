<template>
  <fwb-card class="p-4">
    <fwb-heading class="text-center text-black" tag="h3"> Login Form </fwb-heading>
    <form>
      <fwb-input
        v-model="name"
        label="Name"
        placeholder="enter your first name"
        size="sm"
      />
      <fwb-input
        v-model="email"
        label="Email"
        placeholder="name@example.com"
        type="email"
        size="sm"
      />
      <fwb-input
        v-model="password"
        label="Password"
        placeholder="••••••••"
        type="password"
        size="sm"
      />
      <div class="p-2 text-sm flex gap-1">
        <p class="text-white">Don't have an account?</p><Link :href="route('register')" class="text-blue-400">Create an account</Link>
      </div>
      <fwb-button type="submit">
        Login
      </fwb-button>
    </form>
  </fwb-card>
</template>

<script setup>
import Layout from "../../layouts/GusetLayout.vue";
import { FwbCard, FwbInput, FwbHeading, FwbButton } from "flowbite-vue";

defineOptions({
  layout: Layout,
});
</script>
