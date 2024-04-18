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
        user: {} // Objeto para almacenar los datos del usuario
      };
    },
    mounted() {
      // Cuando el componente se monta, asignamos los datos del usuario
      this.user = {
        given_name: "Carlos Eduardo",
        family_name: "López Piña",
        nickname: "20213tn070",
        name: "Carlos Eduardo López Piña",
        picture: "https://lh3.googleusercontent.com/a/ACg8ocK1wiW2GViBwr9CN6m_7_hTeu_Y8ERBkUdOT6FvTw0JHJqYcMPp=s96-c",
        locale: "es",
        updated_at: "2024-04-18T23:29:05.734Z",
        email: "20213tn070@utez.edu.mx",
        email_verified: true,
        sub: "google-oauth2|106737134679895823484"
      };
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
  
