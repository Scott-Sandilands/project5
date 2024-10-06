<template>
  <nav class="bg-green-900 h-20 items-center text-white flex justify-center space-x-4">
    <RouterLink to="/">Home</RouterLink>
  </nav>
</template>

<style lang="postcss" scoped>
nav {
  @apply flex justify-center space-x-4;

  & .router-link-active {
    @apply underline underline-offset-4;
  }
}
</style>
