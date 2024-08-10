<template>
    <nav>
      <div><img src="../assets/logo.png" alt="Logo" class="logo" /></div>
      <ul>
        <li><a href="#">Organization</a></li>
        <li><a href="#">Data Statistics</a></li>
        <li><a href="#">Emails</a></li>
        <li><a href="#">Contact Number</a></li>
        <li><a href="#">News</a></li>
        <li><a href="#">Location</a></li>
        <li><a href="#">Profile</a></li>
        <li class="avatar-menu">
          <img src="path/to/avatar.png" alt="Avatar" class="avatar" />
          <span class="userName" style="font-size: 0.8em;">{{ username }} </span>
        
          <button @click="toggleDropdown" style="background-color: #004ea1; border: none; padding:0;"><h1 style="color:white; margin-left: 4px; font-size: 12px; height:1px; margin-bottom: 5px;">▼</h1></button>
          <ul class="dropdown-menu" v-show="isDropdownVisible">
          </ul>
        </li>
      </ul>
      <h1 style="font-size: 0.5em; margin-top: -2px; margin-right: -115px;">Administrator</h1>
      <h1 class="date">{{ new Date().toLocaleDateString(undefined, { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' }) }}</h1>
    </nav>

  </template>
  
  <script>
  export default {
    name: 'NavBar',
    data() {
      return {
        username: 'Justin Cipriano',
        isDropdownVisible: false,
      };
    },
    methods: {
      toggleDropdown() {
        this.isDropdownVisible = !this.isDropdownVisible;
      }
    }
  };
  </script>
  
  <style scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

 nav {
  background-color: #004ea1;
  color: white;
  padding:30px;
  position: absolute;
  top: 0;
  left: 0;
  height:90px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  overflow-x: hidden; 
  font-family: sans-serif;
  overflow: hidden;
  font-weight: lighter;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  display: flex;
  gap: 30px;
  align-items: center;
  width: 100%;
  flex-wrap: wrap;
  margin-left: 35px; /* Allow items to wrap to the next line */
}

li {
  display: inline;
}

a {
  color: white;
  text-decoration: none;
  font-size: 0.8em;
}

img {
  height: 30px;
}

.logo {
  height: 100px; /* Adjust height as needed */
  width: 150px;
  object-fit: cover;
  margin-left: -3px;
   /* Maintain aspect ratio */
}

.avatar-menu {
  display: flex;
  align-items: center;
  position: absolute;
  top: 10px; /* Adjusted from 5px to 10px */
  right: 20px;
  margin-right: 10px; /* Adjusted from 10px to 20px */
}

.avatar {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  margin-right: 10px;
  padding: 1px;
}

.dropdown-menu {
  display: none;
  position: absolute;
  top: 100%;
  right: 0;
  background-color: #004ea1;
  list-style: none;
  padding: 10px;
  margin: 0;
}

.avatar-menu:hover .dropdown-menu {
  display: block;
}
.date {
  display: inline;
  font-size: 12px;
  margin-top: 60px;
  font-weight: lighter;
  margin-right: 55px;
}
</style>