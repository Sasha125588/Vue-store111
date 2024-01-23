<script setup>
defineProps({
  totalPrice: Number
})

const emit = defineEmits(['openDrawer'])
</script>

<template>
  <header class="flex justify-between border-b border-slate-200 px-8 py-5">
    <div class="flex items-center gap-4">
      <img src="/apple-logo.png" alt="Logo" class="w-10" />
      <div>
        <h2 class="text-xl font-bold uppercase">Vue Store</h2>
        <p class="text-slate-400">Smartphones Store</p>
      </div>
    </div>

    <ul class="flex items-center gap-10">
      <li
        @click="() => emit('openDrawer')"
        class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black"
      >
        <img src="/cart.svg" alt="Cart" />
        <b>{{ totalPrice }} ₴</b>
      </li>

      <li class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black">
        <img src="/heart.svg" alt="Cart" />
        <span>Закладки</span>
      </li>

      <li class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black">
        <img src="/profile.svg" alt="Cart" />
        <span>Profile</span>
      </li>
    </ul>
  </header>
</template>
