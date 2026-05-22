<template>
  <nav class="navbar navbar-expand-lg fixed-top glass-navbar py-3">
    <div class="container">
      <!-- Brand Logo & Name -->
      <router-link class="navbar-brand d-flex align-items-center gap-2" to="/">
        <div class="logo-wrapper d-flex align-items-center justify-content-center">
          <img src="../assets/logo.svg" alt="Edu AI Logo" class="custom-logo" />
        </div>
      </router-link>

      <!-- Toggle Button for Mobile -->
      <button class="navbar-toggler border-0 focus-none" type="button" data-bs-toggle="collapse"
        data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <!-- Nav Links & CTA -->
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav mx-auto mb-2 mb-lg-0 gap-1 gap-lg-3 text-center">
          <li class="nav-item">
            <a class="nav-link-custom nav-link" href="#home" @click="handleNavClick($event, 'home')">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link-custom nav-link" href="#pricing" @click="handleNavClick($event, 'pricing')">Pricing</a>
          </li>
          <li class="nav-item">
            <a class="nav-link-custom nav-link" href="#contact" @click="handleNavClick($event, 'contact')">Contact</a>
          </li>
        </ul>
        <div class="d-flex justify-content-center">
          <router-link to="/other" class="btn btn-primary px-4 py-2 shadow-sm rounded-pill fw-semibold">
            Signup
          </router-link>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { useRouter, useRoute } from 'vue-router'

const router = useRouter()
const route = useRoute()

const handleNavClick = (event, sectionId) => {
  // If we are not on the homepage, route to home with hash
  if (route.path !== '/') {
    event.preventDefault()
    router.push({ path: '/', hash: `#${sectionId}` })
  } else {
    // Let HTML standard smooth-scroll handle it or trigger it programmatically
    event.preventDefault()
    const element = document.getElementById(sectionId)
    if (element) {
      const navbarHeight = 85
      const elementPosition = element.getBoundingClientRect().top
      const offsetPosition = elementPosition + window.pageYOffset - navbarHeight

      window.scrollTo({
        top: offsetPosition,
        behavior: 'smooth'
      })
    }
  }
}
</script>

<style scoped>
.fw-extrabold {
  font-weight: 800;
}

.tracking-tight {
  letter-spacing: -0.03em;
}

.focus-none:focus {
  box-shadow: none !important;
  outline: none !important;
}

@media (max-width: 991.98px) {
  .navbar-collapse {
    background: rgba(255, 255, 255, 0.98);
    border-radius: 16px;
    padding: 1.5rem;
    margin-top: 1rem;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
    border: 1px solid rgba(124, 58, 237, 0.1);
  }

  .nav-link-custom::after {
    display: none;
  }
}
</style>
