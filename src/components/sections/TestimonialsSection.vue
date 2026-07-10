<template>
  <section id="testimonials" class="testimonials-section py-6 bg-white position-relative">
    <div class="container">

      <!-- Section Header -->
      <div class="row justify-content-center mb-5 text-center">
        <div class="col-lg-7">
          <span
            class="badge bg-primary-light text-primary-purple px-3 py-2 rounded-pill fw-bold text-uppercase tracking-wider mb-3">
            Testimoni
          </span>
          <h2 class="fw-extrabold display-5 text-dark mb-3">
            Cerita Sukses dari <span class="highlight-text">Sahabat Edu AI</span>
          </h2>
          <p class="text-muted fs-5">
            Lihat bagaimana ribuan pelajar dan mahasiswa meningkatkan IPK dan menghemat jam belajar mereka bersama kami.
          </p>
        </div>
      </div>

      <!-- Testimonial Grid -->
      <div class="row g-4 justify-content-center">
        <!-- Testimonial 1: Amikom -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="testimonial-card premium-card h-100 d-flex flex-column justify-content-between">
            <div>
              <div class="rating-stars mb-3 text-warning">
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
              </div>
              <p class="text-muted lh-base mb-4 font-sm">
                "Edu AI membantu saya merangkum video presentasi dan modul PDF tebal dalam hitungan detik. Dari yang tadinya belajar sampai begadang, sekarang bisa selesai 2 jam sebelum tidur."
              </p>
            </div>
            <div class="d-flex align-items-center gap-3 pt-3 border-top border-light">
              <img src="https://images.unsplash.com/photo-1534528741775-53994a69daeb?auto=format&fit=crop&q=80&w=120"
                alt="Naufal Anggara" class="user-avatar" />
              <div class="text-start">
                <h6 class="fw-bold text-dark mb-0">Naufal Anggara</h6>
                <span class="text-muted font-xs">Sistem Informasi, Amikom</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Testimonial 2: UI -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="testimonial-card premium-card h-100 d-flex flex-column justify-content-between">
            <div>
              <div class="rating-stars mb-3 text-warning">
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
              </div>
              <p class="text-muted lh-base mb-4 font-sm">
                "Fitur AI Tutor-nya sangat interaktif! Ketika saya tidak mengerti kode rumit di kuliah Algoritma, AI ini menjelaskan dengan analogi masak kue yang super simpel dan gampang masuk otak."
              </p>
            </div>
            <div class="d-flex align-items-center gap-3 pt-3 border-top border-light">
              <img src="https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&q=80&w=120"
                alt="Sheva Pajar" class="user-avatar" />
              <div class="text-start">
                <h6 class="fw-bold text-dark mb-0">Sheva Pajar</h6>
                <span class="text-muted font-xs">Teknik Informatika, UI</span>
              </div>
            </div>
          </div>
        </div>

        <!-- Testimonial 3: ITB -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="testimonial-card premium-card h-100 d-flex flex-column justify-content-between">
            <div>
              <div class="rating-stars mb-3 text-warning">
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
                <i class="bi bi-star-fill"></i>
              </div>
              <p class="text-muted lh-base mb-4 font-sm">
                "Jadwal belajar otomatis dari Edu AI sangat membantu saya membagi waktu antara organisasi dan tugas kuliah yang padat. Nilai IPK saya naik dari 3.2 ke 3.75 semester ini!"
              </p>
            </div>
            <div class="d-flex align-items-center gap-3 pt-3 border-top border-light">
              <img src="https://images.unsplash.com/photo-1492562080023-ab3db95bfbce?auto=format&fit=crop&q=80&w=120"
                alt="Azzam Al-Fikri" class="user-avatar" />
              <div class="text-start">
                <h6 class="fw-bold text-dark mb-0">Azzam Al-Fikri</h6>
                <span class="text-muted font-xs">Sains Data, ITB</span>
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
.testimonials-section {
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

.font-xs {
  font-size: 0.8rem;
}

.user-avatar {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid var(--brand-primary-light);
}

.testimonial-card {
  border: 1px solid rgba(124, 58, 237, 0.08) !important;
  background: #ffffff;
  box-shadow: 0 10px 30px rgba(31, 38, 135, 0.02);
  transition: all 0.4s cubic-bezier(0.165, 0.84, 0.44, 1);
  padding: 2.2rem;
  border-radius: 20px;
}

.testimonial-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 45px rgba(124, 58, 237, 0.08);
  border-color: rgba(124, 58, 237, 0.2) !important;
}

.rating-stars i {
  font-size: 0.9rem;
  margin-right: 2px;
}
</style>
