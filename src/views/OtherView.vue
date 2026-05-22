<template>
  <div class="other-view bg-glow-section py-6 min-vh-100 d-flex align-items-center justify-content-center">
    <div class="container pt-5">
      <div class="row justify-content-center pt-5">
        <div class="col-lg-5 col-md-8 col-12">
          
          <!-- Back Link -->
          <div class="text-start mb-3">
            <router-link to="/" class="text-decoration-none text-primary-purple fw-semibold font-xs d-flex align-items-center gap-1.5">
              <i class="bi bi-arrow-left"></i> Kembali ke Beranda
            </router-link>
          </div>

          <!-- Signup Card Mock -->
          <div class="premium-card text-start shadow-lg bg-white border p-4 p-md-5">
            <div class="text-center mb-4">
              <h3 class="fw-extrabold text-dark mb-1">Mulai Belajar Cerdas</h3>
              <p class="text-muted font-sm">Daftarkan akun Edu AI Anda dalam 1 menit gratis.</p>
            </div>

            <!-- Social Signup -->
            <div class="d-grid gap-2 mb-4">
              <button class="btn btn-outline-dark d-flex align-items-center justify-content-center gap-2 py-2.5 rounded-pill font-sm" style="border-color: #cbd5e1;">
                <i class="bi bi-google text-danger"></i> Daftar dengan Google
              </button>
            </div>

            <div class="d-flex align-items-center gap-2 mb-4">
              <hr class="flex-grow-1 opacity-10 m-0" />
              <span class="text-muted font-xs text-uppercase tracking-wider">atau email</span>
              <hr class="flex-grow-1 opacity-10 m-0" />
            </div>

            <!-- Signup Form -->
            <form @submit.prevent="handleSignup">
              <div class="row g-3">
                <div class="col-12">
                  <label for="reg-name" class="form-label fw-semibold font-xs text-dark">Nama Pengguna</label>
                  <input type="text" id="reg-name" class="form-control premium-form-control" placeholder="sarah123" required />
                </div>
                
                <div class="col-12">
                  <label for="reg-email" class="form-label fw-semibold font-xs text-dark">Alamat Email</label>
                  <input type="email" id="reg-email" class="form-control premium-form-control" placeholder="sarah@email.com" required />
                </div>

                <div class="col-12">
                  <label for="reg-pass" class="form-label fw-semibold font-xs text-dark">Kata Sandi</label>
                  <input type="password" id="reg-pass" class="form-control premium-form-control" placeholder="••••••••" required />
                </div>

                <div class="col-12 mt-4">
                  <button type="submit" class="btn btn-primary w-100 rounded-pill py-3 fw-bold">
                    Buat Akun Sekarang
                  </button>
                </div>
              </div>
            </form>

            <div class="text-center mt-4">
              <span class="text-muted font-xs">Sudah memiliki akun? </span>
              <a href="#" class="text-primary-purple fw-semibold font-xs text-decoration-none" @click.prevent="alertLogin">Masuk</a>
            </div>

          </div>

        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const handleSignup = () => {
  alert('Pendaftaran berhasil! Akun uji coba Anda telah siap.')
}

const alertLogin = () => {
  alert('Fitur login sedang dikonfigurasi.')
}
</script>

<style scoped>
.other-view {
  font-family: var(--font-sans);
}

.fw-extrabold {
  font-weight: 800;
}

.text-primary-purple {
  color: var(--brand-primary);
}

.font-sm {
  font-size: 0.9rem;
}

.font-xs {
  font-size: 0.8rem;
}
</style>
