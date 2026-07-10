<template>
  <section id="faq" class="faq-section py-6 bg-glow-section position-relative">
    <div class="container">

      <!-- Section Header -->
      <div class="row justify-content-center mb-5 text-center">
        <div class="col-lg-7">
          <span
            class="badge bg-primary-light text-primary-purple px-3 py-2 rounded-pill fw-bold text-uppercase tracking-wider mb-3">
            FAQ
          </span>
          <h2 class="fw-extrabold display-5 text-dark mb-3">
            Pertanyaan yang <span class="highlight-text">Sering Diajukan</span>
          </h2>
          <p class="text-muted fs-5">
            Berikut adalah jawaban cepat atas beberapa pertanyaan paling umum yang ditanyakan kepada kami.
          </p>
        </div>
      </div>

      <!-- FAQ Accordion Layout -->
      <div class="row justify-content-center">
        <div class="col-lg-8 col-12">
          <div class="d-flex flex-column gap-3">

            <!-- FAQ Item 1 -->
            <div class="faq-item-card glass-panel" :class="{ 'faq-active': activeIndex === 0 }">
              <button class="faq-trigger w-100 border-0 bg-transparent py-3 px-4 d-flex align-items-center justify-content-between text-start" @click="toggleFAQ(0)">
                <span class="faq-question fw-bold text-dark font-sm">Bagaimana cara Edu AI merangkum modul PDF?</span>
                <span class="faq-icon-wrapper">
                  <i class="bi bi-chevron-down"></i>
                </span>
              </button>
              <div class="faq-collapse" :style="activeIndex === 0 ? 'max-height: 200px; opacity: 1;' : 'max-height: 0px; opacity: 0;'">
                <div class="faq-answer px-4 pb-4 pt-1 text-muted font-sm">
                  Edu AI menggunakan teknologi Natural Language Processing (NLP) canggih untuk menganalisis konteks dokumen PDF Anda. Kami tidak hanya memotong teks, melainkan mengekstrak inti informasi utama, merumuskan konsep rumit menjadi analogi sederhana, dan menyusunnya dalam poin-poin yang mudah dibaca.
                </div>
              </div>
            </div>

            <!-- FAQ Item 2 -->
            <div class="faq-item-card glass-panel" :class="{ 'faq-active': activeIndex === 1 }">
              <button class="faq-trigger w-100 border-0 bg-transparent py-3 px-4 d-flex align-items-center justify-content-between text-start" @click="toggleFAQ(1)">
                <span class="faq-question fw-bold text-dark font-sm">Apakah saya bisa menggunakan Edu AI secara gratis?</span>
                <span class="faq-icon-wrapper">
                  <i class="bi bi-chevron-down"></i>
                </span>
              </button>
              <div class="faq-collapse" :style="activeIndex === 1 ? 'max-height: 200px; opacity: 1;' : 'max-height: 0px; opacity: 0;'">
                <div class="faq-answer px-4 pb-4 pt-1 text-muted font-sm">
                  Ya! Edu AI menyediakan Paket Free secara gratis selamanya. Anda akan mendapatkan kuota merangkum 10 modul per bulan, 50 chat AI Tutor per hari, dan akses ke sistem jadwal belajar standar. Jika membutuhkan fitur tanpa batas, Anda bisa beralih ke Paket Pro kapan saja.
                </div>
              </div>
            </div>

            <!-- FAQ Item 3 -->
            <div class="faq-item-card glass-panel" :class="{ 'faq-active': activeIndex === 2 }">
              <button class="faq-trigger w-100 border-0 bg-transparent py-3 px-4 d-flex align-items-center justify-content-between text-start" @click="toggleFAQ(2)">
                <span class="faq-question fw-bold text-dark font-sm">Apakah AI Tutor bisa membantu mengerjakan tugas kuliah?</span>
                <span class="faq-icon-wrapper">
                  <i class="bi bi-chevron-down"></i>
                </span>
              </button>
              <div class="faq-collapse" :style="activeIndex === 2 ? 'max-height: 200px; opacity: 1;' : 'max-height: 0px; opacity: 0;'">
                <div class="faq-answer px-4 pb-4 pt-1 text-muted font-sm">
                  AI Tutor dirancang khusus untuk memandu Anda memahami materi dan metode penyelesaian tugas secara interaktif (seperti guru privat), bukan sekadar memberikan jawaban langsung. Ini membantu Anda benar-benar menguasai materi agar siap saat ujian.
                </div>
              </div>
            </div>

            <!-- FAQ Item 4 -->
            <div class="faq-item-card glass-panel" :class="{ 'faq-active': activeIndex === 3 }">
              <button class="faq-trigger w-100 border-0 bg-transparent py-3 px-4 d-flex align-items-center justify-content-between text-start" @click="toggleFAQ(3)">
                <span class="faq-question fw-bold text-dark font-sm">Format berkas apa saja yang didukung oleh Edu AI?</span>
                <span class="faq-icon-wrapper">
                  <i class="bi bi-chevron-down"></i>
                </span>
              </button>
              <div class="faq-collapse" :style="activeIndex === 3 ? 'max-height: 200px; opacity: 1;' : 'max-height: 0px; opacity: 0;'">
                <div class="faq-answer px-4 pb-4 pt-1 text-muted font-sm">
                  Kami mendukung berkas dokumen berupa PDF, DOCX, TXT, rekaman audio (MP3/WAV) untuk materi perkuliahan dosen, serta tautan video YouTube (yang memiliki teks/transkrip) maupun halaman artikel web.
                </div>
              </div>
            </div>

          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const activeIndex = ref(0)

const toggleFAQ = (index) => {
  if (activeIndex.value === index) {
    activeIndex.value = null
  } else {
    activeIndex.value = index
  }
}
</script>

<style scoped>
.faq-section {
  padding: 6rem 0 !important;
  font-family: var(--font-sans);
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

/* FAQ Item Styling */
.faq-item-card {
  border-radius: 16px;
  border: 1px solid rgba(124, 58, 237, 0.08);
  background: #ffffff;
  overflow: hidden;
  transition: all 0.3s ease;
}

.faq-item-card:hover {
  border-color: rgba(124, 58, 237, 0.2);
  box-shadow: 0 10px 25px rgba(124, 58, 237, 0.04);
}

.faq-active {
  border-color: rgba(124, 58, 237, 0.25);
  box-shadow: 0 12px 30px rgba(124, 58, 237, 0.08);
}

.faq-trigger {
  outline: none !important;
}

.faq-question {
  transition: color 0.3s ease;
}

.faq-trigger:hover .faq-question,
.faq-active .faq-question {
  color: var(--brand-primary) !important;
}

.faq-icon-wrapper {
  color: #94a3b8;
  font-size: 1.1rem;
  transition: transform 0.3s ease, color 0.3s ease;
}

.faq-trigger:hover .faq-icon-wrapper,
.faq-active .faq-icon-wrapper {
  color: var(--brand-primary);
}

.faq-active .faq-icon-wrapper {
  transform: rotate(180deg);
}

/* Dropdown transition */
.faq-collapse {
  overflow: hidden;
  transition: max-height 0.35s cubic-bezier(0.4, 0, 0.2, 1), opacity 0.3s ease;
}

.faq-answer {
  line-height: 1.6;
}
</style>
