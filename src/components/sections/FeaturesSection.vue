<template>
  <section id="features" class="features-section py-6 bg-white position-relative">
    <div class="container">

      <!-- Section Header -->
      <div class="row justify-content-center mb-5 text-center">
        <div class="col-lg-7">
          <span
            class="badge bg-primary-light text-primary-purple px-3 py-2 rounded-pill fw-bold text-uppercase tracking-wider mb-3">Fitur
            Edu AI</span>
          <h2 class="fw-extrabold display-5 text-dark mb-3">Sering belajar lama
            tapi tetap <span class="highlight-text">nggak paham?</span></h2>
          <p class="text-muted fs-5">
            Edu AI dirancang khusus untuk memotong waktu belajar Anda hingga setengahnya dengan hasil yang jauh lebih
            maksimal.
          </p>
        </div>
      </div>

      <!-- Features Cards Grid -->
      <div class="row g-4 justify-content-center">

        <!-- Feature 1: Penjelasan Simpel -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="premium-card h-100 text-start d-flex flex-column justify-content-between">
            <div>
              <div class="feature-icon-box bg-peach-gradient text-white mb-4 shadow-sm">
                <!-- Chat & Explain Icon -->
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"
                  stroke-linecap="round" stroke-linejoin="round">
                  <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z" />
                </svg>
              </div>
              <h4 class="fw-bold text-dark mb-3">AI Penjelasan Materi</h4>
              <p class="text-muted lh-base font-sm">
                Pahami materi lebih cepat dengan penjeasn AI yang sederhana, interaktif, dan mudah dipaham kapan saja
              </p>
            </div>
            <div class="pt-3 border-top border-light mt-3">
              <a href="#"
                class="text-decoration-none text-primary-purple fw-semibold font-sm d-flex align-items-center gap-1">
                Pelajari Selengkapnya <i class="bi bi-arrow-right"></i>
              </a>
            </div>
          </div>
        </div>

        <!-- Feature 2: Rangkuman Otomatis -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="premium-card h-100 text-start d-flex flex-column justify-content-between">
            <div>
              <div class="feature-icon-box bg-purple-gradient text-white mb-4 shadow-sm">
                <!-- Summary File Icon -->
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"
                  stroke-linecap="round" stroke-linejoin="round">
                  <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z" />
                  <polyline points="14 2 14 8 20 8" />
                  <line x1="16" y1="13" x2="8" y2="13" />
                  <line x1="16" y1="17" x2="8" y2="17" />
                  <polyline points="10 9 9 9 8 9" />
                </svg>
              </div>
              <h4 class="fw-bold text-dark mb-3">Rangkuman Otomatis</h4>
              <p class="text-muted lh-base font-sm">
                Unggah modul PDF panjang, rekaman dosen, atau video YouTube. Edu AI akan merangkum materi
                berlembar-lembar menjadi poin penting terstruktur dalam 5 detik saja.
              </p>
            </div>
            <div class="pt-3 border-top border-light mt-3">
              <a href="#"
                class="text-decoration-none text-primary-purple fw-semibold font-sm d-flex align-items-center gap-1">
                Pelajari Selengkapnya <i class="bi bi-arrow-right"></i>
              </a>
            </div>
          </div>
        </div>

        <!-- Feature 3: Jadwal Rapi -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="premium-card h-100 text-start d-flex flex-column justify-content-between">
            <div>
              <div class="feature-icon-box bg-yellow-gradient text-white mb-4 shadow-sm">
                <!-- Calendar Smart Schedule Icon -->
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"
                  stroke-linecap="round" stroke-linejoin="round">
                  <rect x="3" y="4" width="18" height="18" rx="2" ry="2" />
                  <line x1="16" y1="2" x2="16" y2="6" />
                  <line x1="8" y1="2" x2="8" y2="6" />
                  <line x1="3" y1="10" x2="21" y2="10" />
                </svg>
              </div>
              <h4 class="fw-bold text-dark mb-3">Jadwal yang Rapi</h4>
              <p class="text-muted lh-base font-sm">
                Rancang rutinitas belajar anti-stres. AI kami membagi porsi belajar Anda secara merata berdasarkan
                tanggal ujian, tingkat kesulitan, serta ritme biologis harian Anda.
              </p>
            </div>
            <div class="pt-3 border-top border-light mt-3">
              <a href="#"
                class="text-decoration-none text-primary-purple fw-semibold font-sm d-flex align-items-center gap-1">
                Pelajari Selengkapnya <i class="bi bi-arrow-right"></i>
              </a>
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
.features-section {
  padding: 6rem 0 !important;
  font-family: var(--font-sans);
}

.fw-extrabold {
  font-weight: 800;
}

.tracking-wider {
  letter-spacing: 0.08em;
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
</style>
