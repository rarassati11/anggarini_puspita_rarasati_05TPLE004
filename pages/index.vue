<template>
  <div class="p-6 bg-gray-100 h-full">
    <div class="bg-blue-600 text-white p-6 rounded-lg mb-6">
      <h2 class="text-2xl font-bold">Sistem Informasi Manajemen Karyawan</h2>
      <p class="text-lg">Admin Dashboard</p>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-6">
      <div class="bg-white p-4 rounded-lg shadow-md flex flex-col items-center">
        <div class="text-blue-500 w-12 h-12 flex items-center justify-center bg-blue-100 rounded-full mb-4">
          <i class="fas fa-users fa-lg"></i>
        </div>
        <h3 class="text-lg font-bold text-gray-700">Data Pegawai</h3>
        <p class="text-2xl font-semibold text-gray-800">13</p>
      </div>

      <div class="bg-white p-4 rounded-lg shadow-md flex flex-col items-center">
        <div class="text-green-500 w-12 h-12 flex items-center justify-center bg-green-100 rounded-full mb-4">
          <i class="fas fa-calendar-check fa-lg"></i>
        </div>
        <h3 class="text-lg font-bold text-gray-700">Absensi Hari Ini</h3>
        <p class="text-gray-600">11 May 2023</p>
        <p class="text-2xl font-semibold text-gray-800">0</p>
      </div>

      <div class="bg-white p-4 rounded-lg shadow-md flex flex-col items-center">
        <div class="text-blue-500 w-12 h-12 flex items-center justify-center bg-blue-100 rounded-full mb-4">
          <i class="fas fa-clipboard-check fa-lg"></i>
        </div>
        <h3 class="text-lg font-bold text-gray-700">Izin Menunggu Konfirmasi</h3>
        <p class="text-2xl font-semibold text-gray-800">2</p>
      </div>

      <div class="bg-white p-4 rounded-lg shadow-md flex flex-col items-center">
        <div class="text-purple-500 w-12 h-12 flex items-center justify-center bg-purple-100 rounded-full mb-4">
          <i class="fas fa-clock fa-lg"></i>
        </div>
        <h3 class="text-lg font-bold text-gray-700">Lembur Menunggu Konfirmasi</h3>
        <p class="text-2xl font-semibold text-gray-800">1</p>
      </div>
    </div>
  </div>
</template>
