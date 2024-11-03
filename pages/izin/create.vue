<template>
  <div class="p-8 bg-gray-50 min-h-screen">
    <div class="max-w-3xl mx-auto bg-white p-6 rounded shadow-md">
      <h2 class="text-xl font-semibold mb-6">Data Hadir Karyawan </h2>
  
      <form>
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="nama_lengkap">
            Kode Izin
          </label>
          <input
            type="text"
            id="kode_izin"
            placeholder="Kode Izin"
            class="w-full p-2 border border-gray-300 rounded"
          />
        </div>

        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="nama_lengkap">
            Izin
          </label>
          <input
            type="text"
            id="izin"
            placeholder="izin"
            class="w-full p-2 border border-gray-300 rounded"
          />
        </div>

        <div class="flex justify-end mt-6">
          <NuxtLink 
            to="/izin"
            class="bg-green-500 text-white px-4 py-2 rounded mr-2 hover:bg-green-600"
          >
            Simpan
          </NuxtLink>
          <NuxtLink 
            to="/izin"
            class="bg-red-500 text-white px-4 py-2 rounded hover:bg-red-600"
          >
            Batal
          </NuxtLink>
        </div>
      </form>
    </div>
  </div>
</template>
