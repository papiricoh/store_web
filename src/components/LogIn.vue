<script>
export default {
  data() {
    return {
        login_email: "",
        login_password: "",
        login_identifier: null
    }
  },
  methods: {
    async attempt_login(login_email, login_password) {
        await fetch('http://localhost:8080/api/login/', {
            method: 'post',
            headers: {
                'Content-Type': 'application/json'
            },
            body: JSON.stringify({ email: login_email, password: login_password })
        }).then(function(response) {
            if (!response.ok) {
                throw new Error(`HTTP error! status: ${response.status}`);
            }
            return response.json();
        }).then(function(data) {
            console.log('Tried to Log In');
        });
    }
  }
}
</script>

<template>
    <div class="flex_center">
        <div class="box flex_column">
            <h2 class="title">Log-In</h2>
            <p>Email And Password required</p>
            <input v-model="login_email" class="input_bar" type="email" placeholder="ecomerce@gmail.com">
            <input v-model="login_password" class="input_bar" type="password" placeholder="********">
            <button @click="attempt_login(login_email, login_password)">SUBMIT</button>
        </div>
    </div>
</template>
