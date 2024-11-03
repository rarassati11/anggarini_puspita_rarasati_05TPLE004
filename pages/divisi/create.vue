<template>
  <div class="p-8 bg-gray-50 min-h-screen">
    <div class="max-w-3xl mx-auto bg-white p-6 rounded shadow-md">
      <h2 class="text-xl font-semibold mb-6">Tambah Data Karyawan</h2>
  
      <form>
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="nama_lengkap">
            Kode Divisi
          </label>
          <input
            type="text"
            id="kode_divisi"
            placeholder="Kode Divisi"
            class="w-full p-2 border border-gray-300 rounded"
          />
        </div>

        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="nama_lengkap">
            Nama Divisi
          </label>
          <input
            type="text"
            id="nama_divisi"
            placeholder="Nama Divisi"
            class="w-full p-2 border border-gray-300 rounded"
          />
        </div>

        <div class="flex justify-end mt-6">
          <NuxtLink 
            to="/divisi"
            class="bg-green-500 text-white px-4 py-2 rounded mr-2 hover:bg-green-600"
          >
            Simpan
          </NuxtLink>
          <NuxtLink 
            to="/divisi"
            class="bg-red-500 text-white px-4 py-2 rounded hover:bg-red-600"
          >
            Batal
          </NuxtLink>
        </div>
      </form>
    </div>
  </div>
</template>
