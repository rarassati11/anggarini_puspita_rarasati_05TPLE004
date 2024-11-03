<template>
  <div class="bg-gray-100 min-h-screen flex">
    <Sidebar />

    <div class="flex-1 ml-64">
      <Navbar />

      <main class="">
        <slot />
      </main>
    </div>
  </div>
</template>
