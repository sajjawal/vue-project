<script setup>
function handleUpdatedStudentform() {
    console.log("updated");
}

</script>

<template>
    <div class="shadow-md pb-6">
      <div class="bg-indigo-600 p-4">
        <h1 class="text-3xl font-bold text-center text-white">Edit Student</h1>
      </div>
  
      <form
        @submit.prevent="handleUpdatedStudentform"
        class="w-full">
        <div class="flex items-center m-6">
          <div class="w-1/5">
            <label class="font-medium" for="stuid"> ID : </label>
          </div>
          <div class="w-4/5">
            <input
              type="text"
              id="stuId"
              class="border-2 border-gray-200 w-full py-2 px-4"
              placeholder="write your name"
              disabled
            />
          </div>
        </div>
        <div class="flex items-center m-6">
          <div class="w-1/5">
            <label class="font-medium" for="stuname"> Name : </label>
          </div>
          <div class="w-4/5">
            <input
              type="text"
              id="stuname"
              
              class="border-2 border-gray-200 w-full py-2 px-4"
              placeholder="write your name"
              required
            />
          </div>
        </div>
        <div class="flex items-center m-6">
          <div class="w-1/5">
            <label class="font-medium" for="email"> Email : </label>
          </div>
          <div class="w-4/5">
            <input
              type="email"
              id="email"
              class="border-2 border-gray-200 w-full py-2 px-4"
              placeholder="write your email"
              required
            />
          </div>
        </div>
  
        <div class="m-8 flex justify-center">
          <button
            type="submit"
            class="bg-purple-700 text-white font-medium py-2 rounded-md px-6 hover:bg-purple-800 mr-6"
          >
            Save
          </button>
  
          <RouterLink :to="{ name: 'list' }">
            <button
              type="button"
              class="bg-emerald-700 text-white font-medium p-2 rounded-md hover:bg-emerald-800"
            >
              Back to Home
            </button>
          </RouterLink>
        </div>
      </form>
      <!-- <div
        class="p-4 mb-4 text-sm text-red-700 bg-red-100 rounded-lg font-medium"
        role="alert"
        v-if="error"
      >
        Oops! Error encountered: {{ error.message }}
      </div>
      <div
        class="p-4 mb-4 text-sm text-red-700 bg-red-100 rounded-lg font-medium"
        role="alert"
        v-if="statusCode === 201"
      >
        Student Added Successfully
      </div> -->
    </div>
  </template>

<style scoped>


</style>
