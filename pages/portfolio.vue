<template>
    <Navbar/>
  
    <!-- Tabs (Radio buttons) -->
    <div class="flex justify-center items-center">
      <div class="radio-inputs flex rounded-lg bg-gray-200 p-1 w-[300px] text-sm shadow-md">
        <label class="radio flex-1 text-center">
          <input type="radio" name="radio" id="uiux-tab" v-model="selectedTab" value="uiux" class="hidden" />
          <span class="name cursor-pointer flex items-center justify-center py-2 px-4 rounded-lg transition duration-150 ease-in-out text-gray-700 hover:bg-white focus:bg-white">UI / UX Design</span>
        </label>
        <label class="radio flex-1 text-center">
          <input type="radio" name="radio" id="videoedit-tab" v-model="selectedTab" value="videoedit" class="hidden" />
          <span class="name cursor-pointer flex items-center justify-center py-2 px-4 rounded-lg transition duration-150 ease-in-out text-gray-700 hover:bg-white focus:bg-white">Video Editing</span>
        </label>
        <label class="radio flex-1 text-center">
          <input type="radio" name="radio" id="ytauth-tab" v-model="selectedTab" value="ytauth" class="hidden" />
          <span class="name cursor-pointer flex items-center justify-center py-2 px-4 rounded-lg transition duration-150 ease-in-out text-gray-700 hover:bg-white focus:bg-white">YouTube Automations</span>
        </label>
      </div>
    </div>
  
    <!-- Content sections for each tab -->
    <div class="text-white">
      <div class="tab-content mt-4">
        <div v-if="selectedTab === 'uiux'" class="content p-5 bg-transparent rounded-lg shadow-md">
          <h2 class="text-xl font-semibold mb-4">UI / UX Design Content</h2>
          <p>This is the UI/UX Design content that will be shown when the UI / UX Design tab is selected.</p>
        </div>
        <div v-if="selectedTab === 'videoedit'" class="content p-5 bg-transparent rounded-lg shadow-md">
          <h2 class="text-xl font-semibold mb-4">Video Editing Content</h2>
          <p>This is the Video Editing content that will be shown when the Video Editing tab is selected.</p>
        </div>
        <div v-if="selectedTab === 'ytauth'" class="content p-5 bg-transparent rounded-lg shadow-md">
          <h2 class="text-xl font-semibold mb-4">YouTube Automations Content</h2>
          <p>This is the YouTube Automations content that will be shown when the YouTube Automations tab is selected.</p>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        selectedTab: 'uiux',  // Default selected tab
      };
    },
  };
  </script>
  