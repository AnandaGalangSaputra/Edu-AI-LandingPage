<template>
  <section class="cta-section py-6 bg-white position-relative">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col-lg-10 col-12">
          
          <!-- Immersive Gradient Box -->
          <div class="cta-banner-card text-center p-5 rounded-5 overflow-hidden position-relative shadow-lg">
            <!-- Glow effect elements inside the card -->
            <div class="cta-glow-orb orb-1"></div>
            <div class="cta-glow-orb orb-2"></div>
            
            <div class="position-relative z-1 py-3">
              <span class="badge bg-yellow text-dark-80 fw-bold px-3 py-2 rounded-pill text-uppercase tracking-wider mb-4" style="background-color: var(--brand-yellow);">
                Uji Coba Gratis
              </span>
              
              <h2 class="fw-extrabold display-5 text-white mb-3">
                Siap Naik Level Dalam Belajar?
              </h2>
              
              <p class="text-white-80 max-w-lg mx-auto mb-5 font-sm fs-5 leading-relaxed">
                Bergabunglah dengan puluhan ribu siswa dan mahasiswa yang telah beralih ke cara belajar cerdas 10x lebih cepat dengan Edu AI.
              </p>
              
              <div class="d-flex flex-wrap gap-3 justify-content-center">
                <router-link to="/other" class="btn btn-light-custom btn-lg rounded-pill px-5 py-3 shadow fw-semibold transition-all">
                  Mulai Secara Gratis
                </router-link>
                <a href="#pricing" class="btn btn-outline-light-custom btn-lg rounded-pill px-4 py-3 fw-semibold transition-all">
                  Lihat Paket Harga
                </a>
              </div>
            </div>
            
          </div>
          
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.cta-section {
  padding: 6rem 0 !important;
  font-family: var(--font-sans);
}

.fw-extrabold {
  font-weight: 800;
}

.font-sm {
  font-size: 0.95rem;
}

.max-w-lg {
  max-width: 600px;
}

/* Immersive Card Banner */
.cta-banner-card {
  background: linear-gradient(135deg, #2e1065 0%, #1e1b4b 50%, #0f172a 100%);
  border: 1px solid rgba(124, 58, 237, 0.2);
}

.text-white-80 {
  color: rgba(255, 255, 255, 0.8) !important;
}

/* Glow Orbs Inside Card */
.cta-glow-orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(80px);
  pointer-events: none;
  z-index: 0;
  opacity: 0.45;
}

.orb-1 {
  width: 250px;
  height: 250px;
  background: #7c3aed;
  top: -20%;
  left: -10%;
}

.orb-2 {
  width: 200px;
  height: 200px;
  background: #fbbf24;
  bottom: -20%;
  right: -5%;
}

/* Custom Buttons for dark theme CTA */
.btn-light-custom {
  background-color: #ffffff;
  color: #1e1b4b;
  border: 2px solid #ffffff;
  transition: all 0.3s cubic-bezier(0.165, 0.84, 0.44, 1);
}

.btn-light-custom:hover {
  background-color: #f3f4f6;
  border-color: #f3f4f6;
  transform: translateY(-3px);
  box-shadow: 0 10px 25px rgba(255, 255, 255, 0.15);
}

.btn-outline-light-custom {
  background-color: transparent;
  color: #ffffff;
  border: 2px solid rgba(255, 255, 255, 0.4);
  transition: all 0.3s cubic-bezier(0.165, 0.84, 0.44, 1);
}

.btn-outline-light-custom:hover {
  border-color: #ffffff;
  background-color: rgba(255, 255, 255, 0.08);
  transform: translateY(-3px);
}

@media (max-width: 575.98px) {
  .cta-banner-card {
    padding: 3rem 1.5rem !important;
  }
}
</style>
