<template>
  <section id="how-it-works" class="how-it-works-section py-6 bg-glow-section position-relative">
    <div class="container">

      <!-- Section Header -->
      <div class="row justify-content-center mb-5 text-center">
        <div class="col-lg-7">
          <span
            class="badge bg-primary-light text-primary-purple px-3 py-2 rounded-pill fw-bold text-uppercase tracking-wider mb-3">
            Cara Kerja
          </span>
          <h2 class="fw-extrabold display-5 text-dark mb-3">
            Belajar Pintar Hanya Dalam <span class="highlight-text">3 Langkah</span>
          </h2>
          <p class="text-muted fs-5">
            Edu AI memotong kompleksitas belajar Anda menjadi alur sederhana yang cepat, cerdas, dan efisien.
          </p>
        </div>
      </div>

      <!-- Steps Cards Grid -->
      <div class="row g-4 justify-content-center position-relative step-cards-row">
        <!-- Connecting Line (Desktop Only) -->
        <div class="step-connecting-line d-none d-lg-block"></div>

        <!-- Step 1: Upload Modul -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="premium-card h-100 text-start position-relative step-card">
            <div class="step-number">01</div>
            <div class="feature-icon-box bg-peach-gradient text-white mb-4 shadow-sm">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"
                stroke-linecap="round" stroke-linejoin="round">
                <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4" />
                <polyline points="17 8 12 3 7 8" />
                <line x1="12" y1="3" x2="12" y2="15" />
              </svg>
            </div>
            <h4 class="fw-bold text-dark mb-3">Unggah Materi Belajar</h4>
            <p class="text-muted lh-base font-sm">
              Masukkan modul PDF, rekaman audio perkuliahan, atau tautan video YouTube ke dashboard belajar Edu AI Anda.
            </p>
          </div>
        </div>

        <!-- Step 2: AI Process -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="premium-card h-100 text-start position-relative step-card">
            <div class="step-number">02</div>
            <div class="feature-icon-box bg-purple-gradient text-white mb-4 shadow-sm">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"
                stroke-linecap="round" stroke-linejoin="round">
                <path d="M12 2v2M12 20v2M4.93 4.93l1.41 1.41M17.66 17.66l1.41 1.41M2 12h2M20 12h2M6.34 17.66l-1.41 1.41M19.07 4.93l-1.41 1.41" />
                <circle cx="12" cy="12" r="4" />
              </svg>
            </div>
            <h4 class="fw-bold text-dark mb-3">Analisis AI Pintar</h4>
            <p class="text-muted lh-base font-sm">
              AI menganalisis materi Anda dalam hitungan detik untuk membuat rangkuman ringkas, glosarium istilah, dan peta konsep visual.
            </p>
          </div>
        </div>

        <!-- Step 3: Learn -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="premium-card h-100 text-start position-relative step-card">
            <div class="step-number">03</div>
            <div class="feature-icon-box bg-yellow-gradient text-white mb-4 shadow-sm">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"
                stroke-linecap="round" stroke-linejoin="round">
                <path d="M22 11.08V12a10 10 0 1 1-5.93-9.14" />
                <polyline points="22 4 12 14.01 9 11.01" />
              </svg>
            </div>
            <h4 class="fw-bold text-dark mb-3">Mulai Belajar Efisien</h4>
            <p class="text-muted lh-base font-sm">
              Tanyakan bagian sulit ke AI Tutor, uji pemahaman lewat kuis interaktif otomatis, dan ikuti jadwal belajar cerdas Anda.
            </p>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.how-it-works-section {
  padding: 6rem 0 !important;
  font-family: var(--font-sans);
  overflow: hidden;
}

.fw-extrabold {
  font-weight: 800;
}

.bg-primary-light {
  background-color: var(--brand-primary-light);
}

.text-primary-purple {
  color: var(--brand-primary);
}

.font-sm {
  font-size: 0.95rem;
}

.feature-icon-box {
  width: 52px;
  height: 52px;
  border-radius: 14px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.bg-peach-gradient {
  background: linear-gradient(135deg, #ff8a7a 0%, #f43f5e 100%);
}

.bg-purple-gradient {
  background: linear-gradient(135deg, #7c3aed 0%, #4f46e5 100%);
}

.bg-yellow-gradient {
  background: linear-gradient(135deg, #fbbf24 0%, #d97706 100%);
}

/* Step Card Styles */
.step-card {
  border: 1px solid rgba(124, 58, 237, 0.08) !important;
  background: #ffffff;
  z-index: 2;
  box-shadow: 0 10px 30px rgba(31, 38, 135, 0.02);
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  padding: 2.2rem;
  border-radius: 20px;
}

.step-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 45px rgba(124, 58, 237, 0.08);
  border-color: rgba(124, 58, 237, 0.2) !important;
}

.step-number {
  position: absolute;
  top: 1.5rem;
  right: 2.2rem;
  font-size: 3rem;
  font-weight: 800;
  color: rgba(124, 58, 237, 0.06);
  line-height: 1;
  transition: all 0.3s ease;
}

.step-card:hover .step-number {
  color: rgba(124, 58, 237, 0.15);
  transform: translateY(-5px);
}

/* Connecting Line */
.step-cards-row {
  position: relative;
}

.step-connecting-line {
  position: absolute;
  top: 4.5rem;
  left: 15%;
  width: 70%;
  height: 2px;
  background: dotted rgba(124, 58, 237, 0.25);
  z-index: 1;
}
</style>
