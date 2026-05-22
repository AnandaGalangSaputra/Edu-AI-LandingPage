<template>
  <section id="pricing" class="pricing-section py-6 bg-glow-section position-relative">
    <div class="container">
      
      <!-- Section Header -->
      <div class="row justify-content-center mb-5 text-center">
        <div class="col-lg-7">
          <span class="badge bg-primary-light text-primary-purple px-3 py-2 rounded-pill fw-bold text-uppercase tracking-wider mb-3">Paket Belajar</span>
          <h2 class="fw-extrabold display-5 text-dark mb-3">Investasi Terbaik untuk Masa Depan</h2>
          <p class="text-muted fs-5">
            Pilih paket yang paling pas untuk tingkat studi Anda. Mulai secara gratis dan tingkatkan kapan saja.
          </p>

          <!-- Bulanan / Tahunan billing Toggle -->
          <div class="d-flex align-items-center justify-content-center gap-3 mt-4">
            <span class="fw-semibold text-dark" :class="{ 'opacity-50': isYearly }">Bulanan</span>
            <div class="form-check form-switch custom-toggle-switch m-0">
              <input class="form-check-input" type="checkbox" id="billingToggle" v-model="isYearly">
            </div>
            <span class="fw-semibold text-dark d-flex align-items-center gap-1.5" :class="{ 'opacity-50': !isYearly }">
              Tahunan 
              <span class="badge bg-yellow text-dark-80 fw-bold" style="font-size: 0.7rem; background-color: var(--brand-yellow);">Hemat 20%</span>
            </span>
          </div>
        </div>
      </div>

      <!-- Pricing Cards Grid -->
      <div class="row g-4 align-items-stretch justify-content-center">
        
        <!-- Tier 1: Free -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="premium-card h-100 text-start d-flex flex-column justify-content-between">
            <div>
              <div class="d-flex justify-content-between align-items-center mb-4">
                <span class="text-uppercase fw-bold tracking-wider text-muted font-sm">Free</span>
              </div>
              <h3 class="fw-extrabold text-dark mb-2">Rp 0</h3>
              <p class="text-muted font-xs mb-4">Akses dasar untuk mencoba fitur AI</p>
              
              <hr class="opacity-10 my-4" />
              
              <ul class="list-unstyled d-flex flex-column gap-3 font-sm text-dark mb-4">
                <li><i class="bi bi-check-circle-fill text-success me-2"></i> 10 Rangkuman Modul / bulan</li>
                <li><i class="bi bi-check-circle-fill text-success me-2"></i> Tanya AI Tutor (50 chat / hari)</li>
                <li><i class="bi bi-check-circle-fill text-success me-2"></i> Jadwal Belajar Standar</li>
                <li class="opacity-50"><i class="bi bi-x-circle-fill text-danger me-2"></i> Rangkum video YouTube / Link</li>
                <li class="opacity-50"><i class="bi bi-x-circle-fill text-danger me-2"></i> Prioritas server AI tinggi</li>
              </ul>
            </div>
            <div>
              <button class="btn btn-outline-primary w-100 rounded-pill py-2.5 fw-semibold mt-4">Mulai Sekarang</button>
            </div>
          </div>
        </div>

        <!-- Tier 2: Pro (Active/Highlighted) -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="premium-card active-plan h-100 text-start d-flex flex-column justify-content-between position-relative overflow-hidden">
            <!-- Popular badge banner -->
            <div class="popular-ribbon">POPULER</div>
            
            <div>
              <div class="d-flex justify-content-between align-items-center mb-4">
                <span class="text-uppercase fw-bold tracking-wider text-white-50 font-sm" style="color: rgba(255,255,255,0.7) !important;">Pro</span>
              </div>
              <h3 class="fw-extrabold text-white mb-2">
                Rp {{ isYearly ? '79.000' : '99.000' }}
                <span class="font-xs fw-normal opacity-75" style="font-size: 0.95rem;">/ bln</span>
              </h3>
              <p class="text-white-50 font-xs mb-4" style="color: rgba(255,255,255,0.7) !important;">
                {{ isYearly ? 'Tagihan Rp 948.000 / tahun' : 'Tagihan bulanan fleksibel' }}
              </p>
              
              <hr class="opacity-20 my-4" />
              
              <ul class="list-unstyled d-flex flex-column gap-3 font-sm text-white mb-4">
                <li><i class="bi bi-check-circle-fill text-white me-2"></i> Rangkuman Modul Tanpa Batas</li>
                <li><i class="bi bi-check-circle-fill text-white me-2"></i> Unlimited AI Tutor Chat</li>
                <li><i class="bi bi-check-circle-fill text-white me-2"></i> Smart Schedule Otomatis</li>
                <li><i class="bi bi-check-circle-fill text-white me-2"></i> Support Rangkuman YouTube & PDF</li>
                <li><i class="bi bi-check-circle-fill text-white me-2"></i> Respon Server Prioritas Kilat</li>
              </ul>
            </div>
            <div>
              <button class="btn btn-outline-primary w-100 rounded-pill py-2.5 fw-bold mt-4 shadow-sm">Pilih Paket Pro</button>
            </div>
          </div>
        </div>

        <!-- Tier 3: Enterprise -->
        <div class="col-lg-4 col-md-6 col-12">
          <div class="premium-card h-100 text-start d-flex flex-column justify-content-between">
            <div>
              <div class="d-flex justify-content-between align-items-center mb-4">
                <span class="text-uppercase fw-bold tracking-wider text-muted font-sm">Enterprise</span>
              </div>
              <h3 class="fw-extrabold text-dark mb-2">
                Rp {{ isYearly ? '239.000' : '299.000' }}
                <span class="font-xs fw-normal" style="font-size: 0.95rem; color: var(--text-muted);">/ bln</span>
              </h3>
              <p class="text-muted font-xs mb-4">
                {{ isYearly ? 'Tagihan Rp 2.868.000 / tahun' : 'Untuk kampus, sekolah & tim' }}
              </p>
              
              <hr class="opacity-10 my-4" />
              
              <ul class="list-unstyled d-flex flex-column gap-3 font-sm text-dark mb-4">
                <li><i class="bi bi-check-circle-fill text-success me-2"></i> Semua Fitur Pro</li>
                <li><i class="bi bi-check-circle-fill text-success me-2"></i> Kolaborasi Tim / Grup Kelas</li>
                <li><i class="bi bi-check-circle-fill text-success me-2"></i> Admin Panel & Laporan Kemajuan</li>
                <li><i class="bi bi-check-circle-fill text-success me-2"></i> Kustom AI dengan materi kustom</li>
                <li><i class="bi bi-check-circle-fill text-success me-2"></i> Pendamping Khusus & SLA 24/7</li>
              </ul>
            </div>
            <div>
              <button class="btn btn-outline-primary w-100 rounded-pill py-2.5 fw-semibold mt-4">Hubungi Sales</button>
            </div>
          </div>
        </div>

      </div>

    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const isYearly = ref(false)
</script>

<style scoped>
.pricing-section {
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

.font-xs {
  font-size: 0.85rem;
}

/* Custom form toggle styling */
.custom-toggle-switch .form-check-input {
  width: 3.5rem;
  height: 1.85rem;
  cursor: pointer;
  background-color: #cbd5e1;
  border-color: #cbd5e1;
  transition: all 0.3s ease;
}

.custom-toggle-switch .form-check-input:focus {
  box-shadow: 0 0 0 4px rgba(124, 58, 237, 0.15);
  border-color: var(--brand-primary);
}

.custom-toggle-switch .form-check-input:checked {
  background-color: var(--brand-primary);
  border-color: var(--brand-primary);
}

/* Popular Ribbon styling */
.popular-ribbon {
  position: absolute;
  top: 15px;
  right: -30px;
  background: var(--brand-yellow);
  color: var(--text-dark);
  font-weight: 800;
  font-size: 0.65rem;
  padding: 0.25rem 2.5rem;
  transform: rotate(45deg);
  letter-spacing: 0.1em;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
}
</style>
