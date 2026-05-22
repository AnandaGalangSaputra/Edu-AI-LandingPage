<template>
  <section id="contact" class="contact-section py-6 bg-white position-relative">
    <div class="container">

      <!-- Section Header -->
      <div class="row justify-content-center mb-5 text-center">
        <div class="col-lg-7">
          <span
            class="badge bg-primary-light text-primary-purple px-3 py-2 rounded-pill fw-bold text-uppercase tracking-wider mb-3">Hubungi
            Kami</span>
          <h2 class="fw-extrabold display-5 text-dark mb-3">Kami Siap Membantu Anda</h2>
          <p class="text-muted fs-5">
            Punya pertanyaan mengenai fitur, integrasi, atau paket berlangganan? Kirimkan pesan Anda langsung di bawah
            ini.
          </p>
        </div>
      </div>

      <!-- Contact Content Grid -->
      <div class="row g-5 align-items-center">

        <!-- Left Side: Contact Information Cards -->
        <div class="col-lg-5 col-12 text-start">
          <div class="d-flex flex-column gap-4">

            <!-- Card 1: Email Support -->
            <div class="contact-info-card d-flex align-items-start gap-3 p-4 border rounded-4 bg-light-glow">
              <div
                class="info-icon bg-primary-light text-primary-purple d-flex align-items-center justify-content-center shadow-sm">
                <i class="bi bi-envelope-open-fill"></i>
              </div>
              <div>
                <h5 class="fw-bold text-dark mb-1">Email Layanan</h5>
                <p class="text-primary-purple fw-semibold mb-1" style="font-size: 0.95rem;">support@edu-ai.com</p>
                <span class="text-muted font-xs">Dapatkan balasan ramah kami dalam 2-4 jam kerja.</span>
              </div>
            </div>

            <!-- Card 2: Office / Location -->
            <div class="contact-info-card d-flex align-items-start gap-3 p-4 border rounded-4">
              <div
                class="info-icon bg-peach-light text-peach d-flex align-items-center justify-content-center shadow-sm">
                <i class="bi bi-geo-alt-fill"></i>
              </div>
              <div>
                <h5 class="fw-bold text-dark mb-1">Kantor Pusat</h5>
                <p class="text-dark-50 fw-semibold mb-1" style="font-size: 0.95rem;">Tech Hub Yogyakarta, Indonesia</p>
                <span class="text-muted font-xs">Mancasan Kidul, Condongcatur, Depok, Sleman, Yogyakarta
                </span>
              </div>
            </div>

            <!-- Card 3: Support Hours -->
            <div class="contact-info-card d-flex align-items-start gap-3 p-4 border rounded-4">
              <div
                class="info-icon bg-yellow-light text-yellow-dark d-flex align-items-center justify-content-center shadow-sm">
                <i class="bi bi-instagram"></i>
              </div>
              <div>
                <h5 class="fw-bold text-dark mb-1">Instagram</h5>
                <p class="text-dark-50 fw-semibold mb-1" style="font-size: 0.95rem;">@edu.ai
                </p>
                <span class="text-muted font-xs">Layanan konsultasi AI & integrasi API tim.</span>
              </div>
            </div>

          </div>
        </div>

        <!-- Right Side: Contact Form -->
        <div class="col-lg-7 col-12">
          <div class="contact-form-panel p-4 p-md-5 border rounded-4 shadow-sm bg-white position-relative">

            <!-- Success Overlay State -->
            <div v-if="submitted"
              class="success-overlay d-flex flex-column align-items-center justify-content-center text-center p-4">
              <div class="success-icon-box bg-success text-white mb-4 animate-bounce">
                <i class="bi bi-check-lg" style="font-size: 2.2rem;"></i>
              </div>
              <h3 class="fw-bold text-dark mb-2">Pesan Terkirim!</h3>
              <p class="text-muted max-w-sm mb-4">
                Terima kasih, <strong>{{ form.name }}</strong>. Tim support Edu AI telah menerima pesan Anda dan akan
                menghubungi Anda dalam waktu dekat.
              </p>
              <button class="btn btn-primary rounded-pill px-4" @click="resetForm">
                Kirim Pesan Baru
              </button>
            </div>

            <!-- Form Content -->
            <form v-else @submit.prevent="handleSubmit">
              <div class="row g-3">

                <!-- Nama -->
                <div class="col-md-6 col-12">
                  <label for="name" class="form-label fw-semibold font-xs text-dark">Nama Lengkap</label>
                  <input type="text" id="name" v-model="form.name" class="form-control premium-form-control"
                    placeholder="Uzumaki Parjo" required />
                </div>

                <!-- Email -->
                <div class="col-md-6 col-12">
                  <label for="email" class="form-label fw-semibold font-xs text-dark">Alamat Email</label>
                  <input type="email" id="email" v-model="form.email" class="form-control premium-form-control"
                    placeholder="UzumakiParjo@gmail.com" required />
                </div>

                <!-- Subject -->
                <div class="col-12">
                  <label for="subject" class="form-label fw-semibold font-xs text-dark">Subjek Pesan</label>
                  <input type="text" id="subject" v-model="form.subject" class="form-control premium-form-control"
                    placeholder="Tanya Paket Belajar / Kerja Sama" required />
                </div>

                <!-- Pesan -->
                <div class="col-12">
                  <label for="message" class="form-label fw-semibold font-xs text-dark">Isi Pesan Anda</label>
                  <textarea id="message" v-model="form.message" rows="5" class="form-control premium-form-control"
                    placeholder="Tuliskan pertanyaan detail Anda di sini..." required></textarea>
                </div>

                <!-- Submit Button -->
                <div class="col-12 mt-4 text-end">
                  <button type="submit"
                    class="btn btn-primary btn-lg w-100 rounded-pill py-3 d-flex align-items-center justify-content-center gap-2"
                    :disabled="loading">
                    <span v-if="loading" class="spinner-border spinner-border-sm" role="status"
                      aria-hidden="true"></span>
                    <i v-else class="bi bi-cursor-fill"></i>
                    {{ loading ? 'Mengirimkan pesan...' : 'Kirim Pesan Sekarang' }}
                  </button>
                </div>

              </div>
            </form>

          </div>
        </div>

      </div>

    </div>
  </section>
</template>

<script setup>
import { ref, reactive } from 'vue'

const loading = ref(false)
const submitted = ref(false)

const form = reactive({
  name: '',
  email: '',
  subject: '',
  message: ''
})

const handleSubmit = () => {
  loading.value = true

  // Simulate network request delayed by 1.5 seconds
  setTimeout(() => {
    loading.value = false
    submitted.value = true
  }, 1500)
}

const resetForm = () => {
  form.name = ''
  form.email = ''
  form.subject = ''
  form.message = ''
  submitted.value = false
}
</script>

<style scoped>
.contact-section {
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

.bg-peach-light {
  background-color: #fff1f0;
}

.text-peach {
  color: var(--brand-peach);
}

.bg-yellow-light {
  background-color: #fef3c7;
}

.text-yellow-dark {
  color: #b45309;
}

.text-primary-purple {
  color: var(--brand-primary);
}

.font-xs {
  font-size: 0.85rem;
}

.contact-info-card {
  transition: all 0.3s ease;
  border-color: #e2e8f0 !important;
}

.contact-info-card:hover {
  transform: translateY(-4px);
  border-color: rgba(124, 58, 237, 0.2) !important;
  box-shadow: 0 10px 25px rgba(124, 58, 237, 0.04);
}

.bg-light-glow {
  background: radial-gradient(circle at 100% 0%, rgba(124, 58, 237, 0.04) 0%, transparent 60%);
  border-color: rgba(124, 58, 237, 0.1) !important;
}

.info-icon {
  width: 48px;
  height: 48px;
  border-radius: 12px;
  font-size: 1.25rem;
  flex-shrink: 0;
}

.contact-form-panel {
  border-color: #e2e8f0 !important;
  min-height: 450px;
}

/* Success Overlay Style */
.success-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: #ffffff;
  border-radius: 16px;
  z-index: 5;
}

.success-icon-box {
  width: 72px;
  height: 72px;
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.max-w-sm {
  max-width: 400px;
}

@keyframes bounce {

  0%,
  100% {
    transform: translateY(0);
  }

  50% {
    transform: translateY(-8px);
  }
}

.animate-bounce {
  animation: bounce 2s infinite ease-in-out;
}
</style>
