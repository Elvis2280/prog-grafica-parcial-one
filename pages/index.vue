<template>
  <div class="min-h-screen bg-black-ui text-black-ui relative font-lato flex items-center justify-center">
    <LoginCard />
    <img src="../static/login-wave.svg" class="absolute bottom-0 w-full">
  </div>
</template>

<script>
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
const firebaseConfig = {
  apiKey: "AIzaSyB6wdseFqh4CjV7fSdzACJXyD8mf0zGohM",
  authDomain: "parcial1-64bb7.firebaseapp.com",
  projectId: "parcial1-64bb7",
  storageBucket: "parcial1-64bb7.appspot.com",
  messagingSenderId: "357346939942",
  appId: "1:357346939942:web:c34cee101cc4b4f5f2c2e7"
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);

export default {}
</script>
