<template>
  <div class="main" style="background-color: #004ea1; height: 47vh; width: 100%; margin:0; padding: 0;">
    <NavBar />
    <h1>h</h1>
      <div class="username"> Welcome back, <div class="userName">{{ username }}</div></div>
    <div id="App">
      <div class="container">
        <div class="stats">
          <div class="box"> <h2>Total Emails</h2> <div class="value">{{ totalEmails }}</div></div>
          <div class="box"> <h2>Total Contacts #</h2> <div class="value">{{ totalContacts }}</div></div>
          <div class="box"> <h2>Total News</h2> <div class="value">{{ totalNews }}</div></div>
          <div class="box"> <h2>Total Locations</h2> <div class="value">{{ totalLocations }}</div></div>
          <div class="box"> <h2>Total Organizations</h2> <div class="value">{{ totalOrganizations }}</div></div>
          <div class="box"> <h2>Total Individual Profiles</h2> <div class="value">{{ totalIndividualProfiles }}</div></div>
          <div class="box data-statistics">
            <h1>Data Statistics</h1>
            
          </div>
          <li class="clickme" style="align-self: flex-end; padding: 23px; margin-left: 80px; list-style-type: none; ">
            <button style="background-color:#52c604; border: none; padding: 8px; width: 190px;"><a href="#" style="align-items: center; text-decoration: none; color: white; justify-content: center;">See What's Running</a></button></li>
          </div>
        </div>
    </div>
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'; 

export default {
  components: {
    NavBar,
  },
  data() {
    return {
      totalEmails: 0,
      totalContacts: 0,
      totalNews: 0,
      totalLocations: 0,
      totalOrganizations: 0,
      totalIndividualProfiles: 0,
      username: "Justin",
    };
  },
  mounted() {
    this.fetchData();
  },
  methods: {
    fetchData() {
      this.totalEmails = '145, 872'; 
      this.totalContacts = '300, 872';
      this.totalNews = '187, 015';
      this.totalLocations = '280, 111';
      this.totalOrganizations = '416, 100';
      this.totalIndividualProfiles = '692, 288';
    },
  },
};
</script>
<style scoped>
body {
  font-family: sans-serif;
}
.main {
  margin: 0;
  padding: 0;
}
.template {
  overflow-y: auto;
}

.username {
  justify-content: center;
  display: flex;
  margin-top: 6%;
  padding: 0;
  font-size: 37px;
  color: white;
  font-family: sans-serif;
}

.box h2 {
  margin-top: -10px;
  font-size: 22px;
  justify-content: center;
  display: flex;
  
}

.container {
  display: flex;
  justify-content: center; /*Center the content horizontally */
  align-items: center; 
  height: 100%; /* Ensure it takes full height */
} 

.value {
  font-size: 40px;
  justify-content: center;
  display: flex;
  font-weight: bold;

}

.stats {
  margin-top: 10vh;
  justify-content: space-between;
  display: grid; /* Change to grid layout */
  grid-template-columns: repeat(3, 1fr); /* 3 columns */
  grid-template-rows: repeat(2, auto); /* 2 rows */
  gap: 15px;
  row-gap: 25px;
  column-gap: 15px;
  font-size: 15px;
  font-family: sans-serif;
}

.box {
  border: 1px solid #ccc; 
  padding: 70px; 
  border-radius: 10px;
  background-color: white;
   
}

.userName {
  font-weight: bold;
  margin-left: 10px;
}

.box.data-statistics {
  display: grid;
  width: 271%;
  margin-bottom: 100px;
  margin-top: 40px;
  padding-bottom: 550px;
 
}

.box.data-statistics h1 {
  align-self: flex-start;
  margin-left: 0;
  margin-top: -30px;
  font-size: 22px;
  margin-left: -20px;
}

</style>