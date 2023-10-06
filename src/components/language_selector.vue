<template>
    <div class="language-selector">
      <button class="language-dropdown-button" @click="toggleDropdown" aria-haspopup="listbox" :aria-expanded="isDropdownOpen">
        <div class="language-dropdown-content">
          <img :src="imageURL" alt="Globe Icon" class="globe-icon" />
          <div class="selected-language">{{ selectedLanguage }}</div>
        </div>
      </button>
      <ul class="dropdown-content" :class="{ 'open': isDropdownOpen }">
        <li v-for="option in languageOptions" :key="option.value" @click="selectLanguage(option.value)">
          {{ option.label }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        imageURL: require('../assets/globe_asia.svg'),
        selectedLanguage: 'ID',
        isDropdownOpen: false,
        languageOptions: [
          { value: 'ID', label: 'Bahasa Indonesia (ID)' },
          { value: 'EN', label: 'English (EN)' },
        ],
      };
    },
    methods: {
      toggleDropdown() {
        this.isDropdownOpen = !this.isDropdownOpen;
      },
      changeLanguage() {
        this.isDropdownOpen = false;
        console.log(this.selectedLanguage);
      },
      selectLanguage(value) {
        this.selectedLanguage = value;
        this.isDropdownOpen = false;
      },
    },
  };
  </script>

  
<style scoped>
.language-selector {
  display: inline-block;
  font-size: 15px;
  position: relative;
}

.language-dropdown-button {
  display: inline-flex;
  align-items: center;
  cursor: pointer;
  position: relative;
  border: none;
  background: none;
  padding: 0;
}

.language-dropdown-content {
  display: flex;
  align-items: center;
  gap:3px;
}

.globe-icon {
  width: 15px;
  height: 24px;
}

.selected-language {
  font-size: 13px;
  cursor: pointer;
}

.dropdown-content {
  position: absolute;
  top: 100%;
  left: 0;
  background-color: #ffffff;
  border: #ccc 1px solid;
  border-radius: 10px;
  padding: 10px;
  z-index: 1;
  display: none;
  overflow-x: hidden;
  cursor: pointer;
}

.dropdown-content.open {
  display: block;
  margin-top: 2px;
}

.dropdown-content li {
  padding: 10px;
  display: block;
  text-align: left;
  font-size: 12px;
  cursor: pointer;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  transition: color 0.2s;
  border-bottom: 1px solid #d8d8d8; 
}

.dropdown-content li:last-child {
  border-bottom: none;
}

.dropdown-content li:hover {
  color: #2070f2;
}
</style>