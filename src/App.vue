<template>
  <div :class="{ 'dark-mode': isDarkMode }">
    <!-- Subheadings -->
    <div class="subheadings">
      <div class="subheadingsLeft">
        <p>About</p>
        <p>Store</p>
      </div>
      <div class="subheadingsRight">
        <p>Gmail</p>
        <p>Images</p>

        <!-- Search Labs -->
        <svg width="32" height="32">
          <polygon points="16,6 26,26 6,26" fill="#888" />
        </svg>

        <!-- Google Apps -->
        <svg width="36" height="36">
          <circle cx="6" cy="6" r="4" fill="#888" />
          <circle cx="18" cy="6" r="4" fill="#888" />
          <circle cx="30" cy="6" r="4" fill="#888" />
          <circle cx="6" cy="18" r="4" fill="#888" />
          <circle cx="18" cy="18" r="4" fill="#888" />
          <circle cx="30" cy="18" r="4" fill="#888" />
          <circle cx="6" cy="30" r="4" fill="#888" />
          <circle cx="18" cy="30" r="4" fill="#888" />
          <circle cx="30" cy="30" r="4" fill="#888" />
        </svg>

        <!-- PFP -->
        <svg width="32" height="32" style="position: relative;">
          <circle cx="16" cy="16" r="12" fill="#8B0000" stroke="#000" stroke-width="1" />
          <text x="16" y="21" text-anchor="middle" font-size="16" font-family="Arial" fill="#fff" font-weight="bold">P</text>
        </svg>
      </div>
    </div>

    <!-- Title -->
    <div class="center">
      <div class="title">
        <span style="color:#4285F4;">G</span>
        <span style="color:#EA4335;">o</span>
        <span style="color:#FBBC05;">o</span>
        <span style="color:#4285F4;">g</span>
        <span style="color:#34A853;">l</span>
        <span style="color:#EA4335;">e</span>
      </div>

      <!-- Search Bar -->
      <div class="search-container">
        <input type="text" class="search-bar" placeholder="Search Google or type a URL" />
      </div>
    </div>

    <!-- Bottom Bar -->
    <footer>
      <div class="bottom-bar">
        <div class="bottom-content">
          <div class="bottom-left">
            <p>Advertising</p>
            <p>Business</p>
            <p>How Search Works</p>
          </div>

          <div class="bottom-center">
            <p>Applying AI towards science and the environment</p>
          </div>

          <div class="bottom-right">
            <p>Privacy</p>
            <p>Terms</p>
            <p @click="toggleDarkMode" style="cursor: pointer;">Settings</p>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const isDarkMode = ref(false)

function toggleDarkMode() {
  isDarkMode.value = !isDarkMode.value
}
</script>

<style>
@import url("https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css");

body,
html {
  margin: 0;
  padding: 0;
  font-family: 'Arial';
  background-color: #f8f9fa;
}

.dark-mode {
  background-color: #121212;
  color: #e0e0e0;
}

.center {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  margin-top: -180px;
}

h1 {
  color: #343a40;
}

.dark-mode h1,
.dark-mode .title span {
  color: #e0e0e0 !important;
}

.search-bar {
  width: 600px;
  height: 32px;
  border: 2px solid black;
  padding: 10px;
  font-size: 16px;
  vertical-align: middle;
  border-radius: 24px;
}

div.dark-mode, .dark-mode {
  min-height: 100vh;
  background-color: #121212 !important;
  color: #e0e0e0;
}

.dark-mode .search-bar {
  background: #222;
  color: #e0e0e0;
  border-color: #444;
}

.subheadings {
  display: flex;
  justify-content: space-between;
  margin-bottom: 20px;
}

.subheadingsLeft {
  display: flex;
  gap: 20px;
  padding: 24px;
}

.subheadingsRight {
  display: flex;
  gap: 20px;
  align-items: center;
  padding-right: 24px;
}

.title {
  font-family: 'Product Sans', Arial, sans-serif;
  font-size: 70px;
  font-weight: bold;
  letter-spacing: -6px;
}

/* Bottom Bar styles */
.bottom-bar {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 40px;
  border-top: none;
  box-shadow: none;
  background-color: #e0e0e0;
  z-index: 100;
  transition: background 0.3s, color 0.3s;
}

.bottom-content {
  position: fixed;
  left: 0;
  bottom: 0;
  width: 100%;
  height: 40px;
  background-color: #e0e0e0;
  border-top: none;
  box-shadow: none;
  z-index: 100;
  display: flex;
  align-items: center;
}

.bottom-bar,
.bottom-content {
  border-top: none !important;
  box-shadow: none !important;
  background-color: #e0e0e0;
  margin: 0;
  padding: 0;
}


.dark-mode .bottom-bar,
.dark-mode .bottom-content {
  background-color: #222 !important;
  color: #e7d9d9 !important;
  border-top: none !important;
  box-shadow: none !important;
}

.bottom-left {
  display: flex;
  gap: 20px;
  justify-content: flex-start;
  flex: 1;
  padding: 0 24px;
}

.bottom-right {
  justify-content: flex-end;
  display: flex;
  gap: 20px;
  flex: 1;
  padding-right: 24px;
}

.bottom-center {
  text-align: center;
  font-size: 14px;
  flex: 1;
  display: flex;
  justify-content: center;
}

.bottom-bar p {
  margin: 0;
  font-size: 14px;
  color: #333;
}

.dark-mode .bottom-bar p {
  color: #ebebeb; /*WHERE PROBLEM WAS I HATE THIS STUPID LINE OF CODE, IT MADE ME LOSE 2 HOURS OF MY LIFE*/
}
footer {
  border-top: none !important;
  box-shadow: none !important;
  background: transparent !important;
  margin: 0 !important;
  padding: 0 !important;
}

.dark-mode footer {
  border-top: none !important;
  box-shadow: none !important;
  background: transparent !important;
  margin: 0 !important;
  padding: 0 !important;
}

</style>
