<template>
  <div class="p-8 bg-gray-50 min-h-screen">
    <div class="max-w-3xl mx-auto bg-white p-6 rounded shadow-md">
      <h2 class="text-xl font-semibold mb-6">Tambah Data Karyawan</h2>
  
      <form>
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="nama_lengkap">
            Nama Lengkap
          </label>
          <input
            type="text"
            id="nama_lengkap"
            placeholder="Nama Lengkap"
            class="w-full p-2 border border-gray-300 rounded"
          />
        </div>
  
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="jenis_kelamin">
            Jenis Kelamin
          </label>
          <select
            id="jenis_kelamin"
            class="w-full p-2 border border-gray-300 rounded"
          >
            <option value="">---</option>
            <option value="Laki-Laki">Laki-Laki</option>
            <option value="Perempuan">Perempuan</option>
          </select>
        </div>
  
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="email">
            Email
          </label>
          <input
            type="email"
            id="email"
            placeholder="Email"
            class="w-full p-2 border border-gray-300 rounded"
          />
        </div>
  
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="no_hp">
            No HP
          </label>
          <input
            type="text"
            id="no_hp"
            placeholder="No HP"
            class="w-full p-2 border border-gray-300 rounded"
          />
        </div>
  
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="alamat">
            Alamat
          </label>
          <textarea
            id="alamat"
            placeholder="Alamat"
            class="w-full p-2 border border-gray-300 rounded h-24"
          ></textarea>
        </div>
  
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
            Password
          </label>
          <input
            type="password"
            id="password"
            placeholder="Password"
            class="w-full p-2 border border-gray-300 rounded"
          />
        </div>
  
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="jabatan">
            Jabatan
          </label>
          <select
            id="jabatan"
            class="w-full p-2 border border-gray-300 rounded"
          >
            <option value="">---</option>
            <option value="Staff">Staff</option>
            <option value="Manager">Manager</option>
          </select>
        </div>
  
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="divisi">
            Divisi
          </label>
          <select
            id="divisi"
            class="w-full p-2 border border-gray-300 rounded"
          >
            <option value="">---</option>
            <option value="IT">IT</option>
            <option value="HR">HR</option>
          </select>
        </div>
  
        <div class="flex justify-end mt-6">
          <NuxtLink 
            to="/karyawan"
            class="bg-green-500 text-white px-4 py-2 rounded mr-2 hover:bg-green-600"
          >
            Simpan
          </NuxtLink>
          <NuxtLink 
            to="/karyawan"
            class="bg-red-500 text-white px-4 py-2 rounded hover:bg-red-600"
          >
            Batal
          </NuxtLink>
        </div>
      </form>
    </div>
  </div>
</template>
