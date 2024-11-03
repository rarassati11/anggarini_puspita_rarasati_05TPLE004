<script setup>
const data = ref([
  { kode: 'DIV001', nama: 'Umum' },
  { kode: 'DIV002', nama: 'BAUK' },
  { kode: 'DIV003', nama: 'IT' },
  { kode: 'DIV004', nama: 'Keuangan' },
  { kode: 'DIV005', nama: 'SDM' },
  { kode: 'DIV006', nama: 'Akademik' },
  { kode: 'DIV007', nama: 'Kemahasiswaan' },
  { kode: 'DIV008', nama: 'Perpustakaan' },
  { kode: 'DIV009', nama: 'Laboratorium' },
  { kode: 'DIV010', nama: 'Humas' }
])

const itemsPerPage = ref(10)
const currentPage = ref(1)
const search = ref('')

const filteredData = computed(() => {
  if (search.value) {
    return data.value.filter(
      item =>
        item.kode.toLowerCase().includes(search.value.toLowerCase()) ||
        item.nama.toLowerCase().includes(search.value.toLowerCase())
    )
  }
  return data.value
})

const totalPages = computed(() => Math.ceil(filteredData.value.length / itemsPerPage.value))

const paginatedData = computed(() => {
  const start = (currentPage.value - 1) * itemsPerPage.value
  const end = start + itemsPerPage.value
  return filteredData.value.slice(start, end)
})
</script>
<template>
  <div class="p-4">
    <div class="flex items-center justify-between mb-4">
      <h2 class="text-xl font-semibold">Data Divisi</h2>
      <NuxtLink to="/divisi/create" class="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">
        + Tambah Divisi
      </NuxtLink>
    </div>
  
    <div class="mb-4 flex items-center">
      <label for="entries" class="mr-2">Show</label>
      <select id="entries" class="border rounded p-1" v-model="itemsPerPage">
        <option value="10">10</option>
        <option value="25">25</option>
        <option value="50">50</option>
        <option value="100">100</option>
      </select>
      <span class="ml-2">entries</span>
  
      <div class="ml-auto">
        <label for="search" class="sr-only">Search</label>
        <input
          type="text"
          id="search"
          placeholder="Search by nama Divisi"
          class="border rounded p-1 ml-4"
          v-model="search"
        />
      </div>
    </div>
  
    <div class="overflow-x-auto">
      <table class="min-w-full bg-white border border-gray-200">
        <thead>
          <tr class="bg-gray-100 text-gray-600 uppercase text-sm leading-normal">
            <th class="py-3 px-6 text-left">No</th>
            <th class="py-3 px-6 text-left">Kode Divisi</th>
            <th class="py-3 px-6 text-left">Nama Divisi</th>
            <th class="py-3 px-6 text-center">Aksi</th>
          </tr>
        </thead>
        <tbody class="text-gray-600 text-sm font-light">
          <tr
            v-for="(item, index) in paginatedData"
            :key="item.kode"
            class="border-b border-gray-200 hover:bg-gray-100"
          >
            <td class="py-3 px-6 text-left">{{ index + 1 + (currentPage - 1) * itemsPerPage }}</td>
            <td class="py-3 px-6 text-left">{{ item.kode }}</td>
            <td class="py-3 px-6 text-left">{{ item.nama }}</td>
            <td class="py-3 px-6 text-center">
              <div class="flex items-center justify-center space-x-2">
                <button class="flex items-center space-x-1 text-blue-500 hover:text-blue-600 transform hover:scale-110">
                  <i class="fas fa-edit"></i>
                  <span>Edit</span>
                </button>
                <button class="flex items-center space-x-1 text-red-500 hover:text-red-600 transform hover:scale-110">
                  <i class="fas fa-trash"></i>
                  <span>Delete</span>
                </button>
              </div>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  
    <div class="mt-4 flex items-center justify-between">
      <span class="text-sm text-gray-600">
        Showing {{ (currentPage - 1) * itemsPerPage + 1 }} to
        {{ Math.min(currentPage * itemsPerPage, filteredData.length) }} of
        {{ filteredData.length }} entries
      </span>
      <div class="flex items-center space-x-2">
        <button
          @click="currentPage--"
          :disabled="currentPage === 1"
          class="px-3 py-1 rounded border border-gray-300 text-gray-600 hover:bg-gray-100"
        >
          Previous
        </button>
        <button
          v-for="page in totalPages"
          :key="page"
          @click="currentPage = page"
          :class="{
            'px-3 py-1 rounded border border-blue-500 text-white bg-blue-500': currentPage === page,
            'px-3 py-1 rounded border border-gray-300 text-gray-600 hover:bg-gray-100': currentPage !== page
          }"
        >
          {{ page }}
        </button>
        <button
          @click="currentPage++"
          :disabled="currentPage === totalPages"
          class="px-3 py-1 rounded border border-gray-300 text-gray-600 hover:bg-gray-100"
        >
          Next
        </button>
      </div>
    </div>
  </div>
</template>
