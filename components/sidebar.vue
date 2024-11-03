<template>
  <aside class="w-64 bg-white border-r border-gray-200 h-screen fixed">
    <div class="p-6">
      <h2 class="text-2xl font-bold text-blue-600">UNIVERSITAS<br>BUNG KARNO</h2>
    </div>
    <nav class="mt-4 p-4">
      <ul>
        <li>
          <NuxtLink to="/" class="flex items-center p-3 hover:text-blue-500 hover:bg-blue-100 rounded-lg">
            <svg class="w-6 h-6 mr-2" fill="currentColor" viewBox="0 0 20 20">
              <path d="M10 2a8 8 0 100 16 8 8 0 000-16z"></path>
            </svg>
            Dashboard
          </NuxtLink>
        </li>
        <li class="mt-4 text-gray-600 font-semibold">MENU KARYAWAN</li>
        <li>
          <NuxtLink 
            to="/karyawan" class="flex items-center p-3 text-gray-600 hover:text-blue-500 hover:bg-blue-100 rounded-lg">
            <svg class="w-6 h-6 mr-2" fill="currentColor" viewBox="0 0 20 20">
              <path d="M10 2a8 8 0 100 16 8 8 0 000-16z"></path>
            </svg>
            Karyawan
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/jabatan" class="flex items-center p-3 text-gray-600 hover:text-blue-500 hover:bg-blue-100 rounded-lg">
            <svg class="w-6 h-6 mr-2" fill="currentColor" viewBox="0 0 20 20">
              <path d="M10 2a8 8 0 100 16 8 8 0 000-16z"></path>
            </svg>
            Jabatan
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/divisi" class="flex items-center p-3 text-gray-600 hover:text-blue-500 hover:bg-blue-100 rounded-lg">
            <svg class="w-6 h-6 mr-2" fill="currentColor" viewBox="0 0 20 20">
              <path d="M10 2a8 8 0 100 16 8 8 0 000-16z"></path>
            </svg>
            Divisi
          </NuxtLink>
        </li>
      </ul>
    </nav>
  </aside>
</template>
