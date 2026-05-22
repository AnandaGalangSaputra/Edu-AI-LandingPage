<template>
  <footer class="footer bg-dark text-white pt-5 pb-4 mt-5 border-top border-secondary">
    <div class="container">
      <div class="row g-4 justify-content-between">

        <!-- Brand Info -->
        <div class="col-lg-4 col-md-6">
          <div class="d-flex align-items-center gap-2 mb-3">
            <div class="logo-wrapper d-flex align-items-center justify-content-center">
              <img src="../assets/logo.svg" alt="Edu AI Logo" class="custom-logo" />
            </div>
          </div>
          <p class="text-white-50 mb-4 pe-lg-4 font-sans-sm">
            Platform pembelajaran pintar bertenaga AI yang membantu Anda belajar 10x lebih cepat, merangkum modul
            otomatis, dan merancang jadwal belajar paling optimal.
          </p>
          <div class="d-flex gap-3">
            <a href="#" class="social-icon-btn"><i class="bi bi-instagram"></i></a>
            <!-- <a href="#" class="social-icon-btn"><i class="bi bi-tiktok"></i></a> -->
            <!-- <a href="#" class="social-icon-btn"><i class="bi bi-github"></i></a>
            <a href="#" class="social-icon-btn"><i class="bi bi-youtube"></i></a> -->
          </div>
        </div>

        <!-- Links Column 1: Fitur -->
        <div class="col-lg-2 col-md-6 col-6">
          <h6 class="text-uppercase fw-bold text-white mb-3 tracking-wider text-xs">Fitur Utama</h6>
          <ul class="list-unstyled d-flex flex-column gap-2 text-white-50 font-sans-sm">
            <li><a href="#" class="footer-link">Rangkuman AI</a></li>
            <li><a href="#" class="footer-link">Penjelasan Cepat</a></li>
            <li><a href="#" class="footer-link">Smart Schedule</a></li>
            <li><a href="#" class="footer-link">Integrasi Modul</a></li>
          </ul>
        </div>

        <!-- Links Column 2: Perusahaan -->
        <div class="col-lg-2 col-md-6 col-6">
          <h6 class="text-uppercase fw-bold text-white mb-3 tracking-wider text-xs">Perusahaan</h6>
          <ul class="list-unstyled d-flex flex-column gap-2 text-white-50 font-sans-sm">
            <li><a href="#" class="footer-link">Tentang Kami</a></li>
            <li><a href="#" class="footer-link">Karir</a></li>
            <li><a href="#" class="footer-link">Blog Edukasi</a></li>
            <li><a href="#" class="footer-link">Kebijakan Privasi</a></li>
          </ul>
        </div>

        <!-- Newsletter Column -->
        <div class="col-lg-3 col-md-6">
          <h6 class="text-uppercase fw-bold text-white mb-3 tracking-wider text-xs">Berlangganan Newsletter</h6>
          <p class="text-white-50 mb-3 font-sans-sm">Dapatkan tips belajar efektif dan pembaruan AI edukasi secara
            gratis.</p>
          <form @submit.prevent="handleSubscribe">
            <div class="input-group">
              <input type="email" class="form-control bg-dark border-secondary text-white font-sans-sm"
                placeholder="Email Anda" required style="border-radius: 8px 0 0 8px; font-size: 0.9rem;" />
              <button class="btn btn-primary" type="submit" style="border-radius: 0 8px 8px 0; padding: 0.5rem 1rem;">
                <i class="bi bi-send-fill"></i>
              </button>
            </div>
          </form>
        </div>

      </div>

      <hr class="my-4 border-secondary opacity-25" />

      <!-- Copyright -->
      <div class="row">
        <div class="col-md-6 text-center text-md-start text-white-50 font-sans-xs">
          <span>&copy; 2026 Edu AI. Hak Cipta Dilindungi Undang-Undang.</span>
        </div>
        <div class="col-md-6 text-center text-md-end text-white-50 mt-2 mt-md-0 font-sans-xs">
          <a href="#" class="footer-link me-3">Syarat & Ketentuan</a>
          <a href="#" class="footer-link">Hubungi Kami</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
const handleSubscribe = () => {
  alert('Terima kasih telah berlangganan newsletter kami!')
}
</script>

<style scoped>
.footer {
  background-color: #0f0e17 !important;
  font-family: var(--font-sans);
}

.text-xs {
  font-size: 0.8rem;
}

.tracking-wider {
  letter-spacing: 0.08em;
}

.font-sans-sm {
  font-size: 0.9rem;
}

.font-sans-xs {
  font-size: 0.8rem;
}

.footer-link {
  color: rgba(255, 255, 255, 0.6);
  text-decoration: none;
  transition: all 0.3s ease;
  font-size: 0.9rem;
}

.footer-link:hover {
  color: #a78bfa;
  padding-left: 4px;
}

.social-icon-btn {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 36px;
  height: 36px;
  border-radius: 50%;
  background-color: rgba(255, 255, 255, 0.05);
  color: rgba(255, 255, 255, 0.7);
  font-size: 1.1rem;
  transition: all 0.3s ease;
  text-decoration: none;
}

.social-icon-btn:hover {
  background-color: var(--brand-primary);
  color: white;
  transform: translateY(-3px);
}
</style>
