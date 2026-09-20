<template>
  <div class="window-height row">
    
    <!-- First Div: Login Page (Left Side) -->
    <div class="col-12 col-md-6 flex flex-center q-pa-xl bg-white">
      
      <!-- Form Container -->
      <div style="width: 100%; max-width: 400px;">
        <div class="text-h4 text-weight-bold q-mb-xs">Welcome back</div>
        <div class="text-grey-7 q-mb-lg">Please enter your details</div>

        <!-- Email Input -->
        <div class="q-mb-md">
          <div class="text-weight-medium q-mb-xs">Email address</div>
          <q-input outlined v-model="email" dense placeholder="Enter your email" />
        </div>

        <!-- Password Input -->
        <div class="q-mb-md">
          <div class="text-weight-medium q-mb-xs">Password</div>
          <q-input outlined v-model="password" type="password" dense placeholder="Enter your password" />
        </div>

        <!-- Remember Me & Forgot Password -->
        <div class="row items-center justify-between q-mb-lg">
          <q-checkbox v-model="remember" label="Remember for 30 days" dense color="deep-purple-7" />
          <a href="#" class="text-deep-purple-7 text-weight-medium" style="text-decoration: none; font-size: 13px;">Forgot password</a>
        </div>

        <!-- Sign In Button -->
        <q-btn unelevated color="deep-purple-7" class="full-width q-mb-md" label="Sign in" no-caps />
        
        <!-- Sign in with Google Button -->
        <q-btn outline color="grey-4" text-color="dark" class="full-width q-mb-lg" no-caps>
          <q-img src="https://cdn1.iconfinder.com/data/icons/google-s-logo/150/Google_Icons-09-512.png" width="20px" height="20px" class="q-mr-sm" />
          Sign in with Google
        </q-btn>

        <!-- Sign Up Link -->
        <div class="text-center text-grey-7 text-caption">
          Don't have an account? <a href="#" class="text-deep-purple-7 text-weight-medium" style="text-decoration: none;">Sign up</a>
        </div>
      </div>
    </div>

    <!-- Second Div: Image Background (Right Side) -->
    <div class="col-12 col-md-6 q-pa-none">
      <!-- Image is set to cover the entire right column -->
      <q-img 
        src="/login_page_image.jpg.png" 
        class="fit"
        fit="cover"
      />
    </div>

  </div>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')
const password = ref('')
const remember = ref(false)
</script>