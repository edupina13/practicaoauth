<template>
    <div class="oauth-profile">
      <div class="profile-info">
        <img :src="user.picture" alt="User Avatar" class="avatar" />
        <div>
          <h2>{{ user.name }}</h2>
          <p>{{ user.email }}</p>
        </div>
      </div>
    
      <div class="profile-details">
        <h3>User Details</h3>
        <ul>
          <li><strong>Given Name:</strong> {{ user.given_name }}</li>
          <li><strong>Family Name:</strong> {{ user.family_name }}</li>
          <li><strong>Nickname:</strong> {{ user.nickname }}</li>
          <li><strong>Locale:</strong> {{ user.locale }}</li>
          <li><strong>Updated At:</strong> {{ user.updated_at }}</li>
          <li><strong>Email Verified:</strong> {{ user.email_verified }}</li>
          <li><strong>Sub:</strong> {{ user.sub }}</li>
        </ul>
      </div>
    </div>
  </template>
  
 <script>
  export default {
    data() {
      return {
        user: {}, // Objeto para almacenar los datos del usuario
        userData: '' // String para almacenar los datos del usuario en formato JSON
      };
    },
    mounted() {
      // Cuando el componente se monta, asignamos los datos del usuario
      this.user = this.$auth.user;
      this.userData = JSON.stringify(this.$auth.user, null, 2);
    }
  };
  </script>
  
  <style scoped>
  .oauth-profile {
    max-width: 600px;
    margin: 0 auto;
    padding: 20px;
  }
  
  .profile-info {
    display: flex;
    align-items: center;
    margin-bottom: 20px;
  }
  
  .avatar {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    margin-right: 20px;
  }
  
  .profile-details {
    background-color: #f5f5f5;
    padding: 20px;
    border-radius: 5px;
  }
  
  .profile-details ul {
    list-style-type: none;
    padding: 0;
  }
  
  .profile-details li {
    margin-bottom: 10px;
  }
  </style>
  
