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
                Pahami materi lebih cepat dengan penjelasan AI yang sederhana, interaktif, dan mudah dipahami kapan saja.
              </p>
            </div>
            <div class="pt-3 border-top border-light mt-3">
              <a href="#"
                class="text-decoration-none text-primary-purple fw-semibold font-sm d-flex align-items-center gap-1"
                @click.prevent="openFeature(1)">
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
                class="text-decoration-none text-primary-purple fw-semibold font-sm d-flex align-items-center gap-1"
                @click.prevent="openFeature(2)">
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
                class="text-decoration-none text-primary-purple fw-semibold font-sm d-flex align-items-center gap-1"
                @click.prevent="openFeature(3)">
                Pelajari Selengkapnya <i class="bi bi-arrow-right"></i>
              </a>
            </div>
          </div>
        </div>

      </div>

    </div>

    <!-- Interactive Feature Modal -->
    <div v-if="activeFeatureId" class="modal-overlay d-flex align-items-center justify-content-center" @click.self="closeFeature">
      <div class="modal-card glass-panel text-start position-relative animate-slide-up p-4 p-md-5">
        <!-- Close Button -->
        <button class="btn-close-modal border-0 bg-transparent text-muted" @click="closeFeature">
          <i class="bi bi-x-lg"></i>
        </button>

        <div class="row g-4 align-items-stretch">
          <!-- Left Column: Feature Info -->
          <div class="col-lg-5 col-12 d-flex flex-column justify-content-between">
            <div>
              <span class="badge bg-primary-light text-primary-purple px-3 py-2 rounded-pill fw-bold text-uppercase tracking-wider mb-3">
                Demo Simulator
              </span>
              <h3 class="fw-extrabold text-dark mb-3">{{ currentFeature.title }}</h3>
              <p class="text-muted lh-base font-sm mb-4">{{ currentFeature.description }}</p>
            </div>
            <div class="mt-auto">
              <div class="p-3 bg-light rounded-3 border border-light-2 mb-4">
                <h6 class="fw-bold text-dark font-sans-sm mb-2" style="font-size: 0.85rem;">
                  <i class="bi bi-lightbulb-fill text-warning me-1"></i> Keunggulan Utama:
                </h6>
                <ul class="list-unstyled d-flex flex-column gap-1.5 font-sans-xs text-muted mb-0" style="font-size: 0.75rem;">
                  <li v-for="(benefit, index) in currentFeature.benefits" :key="index">
                    <i class="bi bi-check-circle-fill text-success me-1"></i> {{ benefit }}
                  </li>
                </ul>
              </div>
              <router-link to="/other" class="btn btn-primary rounded-pill px-4 w-100 py-2.5 fw-bold" @click="closeFeature">
                Mulai Belajar Sekarang (Gratis)
              </router-link>
            </div>
          </div>

          <!-- Right Column: Interactive Simulator Interface -->
          <div class="col-lg-7 col-12">
            <div class="simulator-container rounded-4 border p-4 bg-slate-50 d-flex flex-column justify-content-between h-100">
              
              <!-- SIMULATOR 1: AI PENJELASAN MATERI (CHATBOT) -->
              <div v-if="activeFeatureId === 1" class="chatbot-simulator d-flex flex-column justify-content-between h-100">
                <div class="chat-messages p-2 overflow-y-auto mb-3" ref="chatContainer">
                  <div v-for="(msg, i) in chatState.messages" :key="i" class="d-flex mb-2.5" :class="msg.role === 'user' ? 'justify-content-end' : 'justify-content-start'">
                    <div class="chat-bubble rounded-3 px-3 py-2 font-sans-xs text-start" :class="msg.role === 'user' ? 'bg-primary text-white' : 'bg-white border text-dark shadow-sm'">
                      <strong v-if="msg.role === 'assistant'" class="d-block font-sans-xs text-violet-light mb-1" style="font-size: 0.7rem; color: var(--brand-primary);">🤖 AI Tutor:</strong>
                      <span>{{ msg.content }}</span>
                    </div>
                  </div>
                  <div v-if="chatState.isTyping" class="d-flex mb-2.5 justify-content-start">
                    <div class="chat-bubble bg-white border rounded-3 px-3 py-2 shadow-sm font-sans-xs text-muted">
                      🤖 AI Tutor sedang mengetik <span class="typing-dots">...</span>
                    </div>
                  </div>
                </div>

                <div class="chat-prompt-suggestions text-start">
                  <p class="font-sans-xs text-muted fw-bold mb-2" style="font-size: 0.75rem;">Pilih contoh pertanyaan untuk diuji:</p>
                  <div class="d-flex flex-column gap-2">
                    <button 
                      v-for="(suggestion, idx) in chatSuggestions" 
                      :key="idx" 
                      class="btn btn-outline-primary btn-sm rounded-pill text-start py-2 px-3 font-sans-xs text-truncate"
                      :disabled="chatState.isTyping"
                      @click="simulateChat(suggestion)"
                      style="font-size: 0.75rem;"
                    >
                      <i class="bi bi-question-circle me-1"></i> {{ suggestion.q }}
                    </button>
                  </div>
                </div>
              </div>

              <!-- SIMULATOR 2: RANGKUMAN OTOMATIS (PDF DRAG/DROP) -->
              <div v-if="activeFeatureId === 2" class="summarizer-simulator d-flex flex-column justify-content-between h-100">
                <div class="text-center py-4 px-2" v-if="summarizeState.stage === 'idle'">
                  <div class="upload-dropzone border border-dashed rounded-4 p-4 d-flex flex-column align-items-center justify-content-center cursor-pointer" @click="simulateUpload">
                    <i class="bi bi-file-earmark-pdf-fill text-danger mb-3" style="font-size: 2.8rem;"></i>
                    <h6 class="fw-bold text-dark font-sans-sm mb-1">Simulasikan Unggah File PDF</h6>
                    <p class="text-muted font-sans-xs mb-3">Klik di sini untuk mengunggah berkas "Modul_Kecerdasan_Buatan.pdf"</p>
                    <button class="btn btn-primary btn-sm rounded-pill px-4 font-sans-xs">Pilih File</button>
                  </div>
                </div>

                <div class="text-center py-5" v-else-if="summarizeState.stage === 'uploading'">
                  <div class="spinner-border text-primary mb-3" role="status">
                    <span class="visually-hidden">Loading...</span>
                  </div>
                  <h6 class="fw-bold text-dark font-sans-sm mb-1">Membaca Dokumen PDF...</h6>
                  <p class="text-muted font-sans-xs mb-3">Mengekstrak teks & menganalisis poin penting</p>
                  <div class="progress mx-auto" style="width: 200px; height: 6px;">
                    <div class="progress-bar progress-bar-striped progress-bar-animated bg-primary" role="progressbar" :style="`width: ${summarizeState.progress}%`" aria-valuenow="0" aria-valuemin="0" aria-valuemax="100"></div>
                  </div>
                </div>

                <div class="summary-output text-start h-100 d-flex flex-column justify-content-between" v-else-if="summarizeState.stage === 'done'">
                  <div class="card bg-white border border-light-2 rounded-3 p-3 shadow-sm flex-grow-1 overflow-y-auto mb-3" style="max-height: 240px;">
                    <div class="d-flex align-items-center justify-content-between mb-2 pb-2 border-bottom">
                      <div class="d-flex align-items-center gap-1.5">
                        <i class="bi bi-file-earmark-check-fill text-success" style="font-size: 1.1rem;"></i>
                        <span class="fw-bold text-dark font-sans-xs" style="font-size: 0.75rem;">Rangkuman AI: Modul_Kecerdasan_Buatan.pdf</span>
                      </div>
                      <span class="badge bg-success text-white font-sans-xs px-2 py-1 bg-success" style="font-size: 0.65rem;">Sukses</span>
                    </div>
                    <ul class="list-unstyled d-flex flex-column gap-2 font-sans-xs text-muted mb-0" style="font-size: 0.75rem;">
                      <li><strong>🧠 Jaringan Saraf Tiruan (ANN)</strong>: Model komputasi yang meniru cara kerja jaringan saraf biologis manusia untuk memecahkan masalah kompleks.</li>
                      <li><strong>⚡ Struktur Utama</strong>: Terdiri dari tiga lapisan utama yaitu Input Layer (menerima data), Hidden Layer (memproses bobot data), dan Output Layer (menghasilkan prediksi).</li>
                      <li><strong>🔄 Proses Pembelajaran</strong>: Menggunakan metode Backpropagation untuk melatih model dengan menghitung error output dan menyesuaikan bobot koneksi saraf ke belakang.</li>
                      <li><strong>📈 Aplikasi Praktis</strong>: Digunakan luas untuk pengenalan gambar, deteksi suara, analisis sentimen, serta mobil otonom.</li>
                    </ul>
                  </div>
                  <button class="btn btn-outline-secondary btn-sm w-100 rounded-pill font-sans-xs" @click="resetSummarizer">
                    <i class="bi bi-arrow-counterclockwise me-1"></i> Ulangi Simulasi Unggah
                  </button>
                </div>
              </div>

              <!-- SIMULATOR 3: JADWAL YANG RAPI (CALENDAR GENERATOR) -->
              <div v-if="activeFeatureId === 3" class="scheduler-simulator d-flex flex-column justify-content-between h-100">
                <div class="scheduler-placeholder text-center py-5 px-3" v-if="!schedulerState.generated">
                  <div class="bg-primary-light text-primary-purple rounded-circle d-flex align-items-center justify-content-center mx-auto mb-3" style="width: 58px; height: 58px;">
                    <i class="bi bi-calendar3 text-primary-purple" style="font-size: 1.6rem;"></i>
                  </div>
                  <h6 class="fw-bold text-dark font-sans-sm mb-1">Rancang Jadwal Belajar Pintar Anda</h6>
                  <p class="text-muted font-sans-xs mb-4">Kami akan membagi materi Anda ke dalam slot harian cerdas berdasarkan tingkat kesulitan dan ritme biologis.</p>
                  <button class="btn btn-primary rounded-pill px-4 font-sans-xs" @click="generateSchedule">
                    <i class="bi bi-magic me-1"></i> Simulasikan Pembuatan Jadwal
                  </button>
                </div>

                <div class="scheduler-loading text-center py-5" v-else-if="schedulerState.generating">
                  <div class="spinner-border text-primary mb-3" role="status">
                    <span class="visually-hidden">Loading...</span>
                  </div>
                  <h6 class="fw-bold text-dark font-sans-sm mb-1">AI Sedang Memproses Ritme Belajar...</h6>
                  <p class="text-muted font-sans-xs">Menyesuaikan slot waktu & waktu istirahat (Pomodoro)</p>
                </div>

                <div class="scheduler-calendar text-start h-100 d-flex flex-column justify-content-between" v-else-if="schedulerState.generated">
                  <div class="calendar-card bg-white border border-light-2 rounded-3 p-3 shadow-sm mb-3">
                    <div class="d-flex align-items-center justify-content-between mb-3 pb-2 border-bottom">
                      <div class="d-flex align-items-center gap-1.5">
                        <i class="bi bi-calendar-check-fill text-primary" style="font-size: 1.1rem;"></i>
                        <span class="fw-bold text-dark font-sans-xs" style="font-size: 0.75rem;">Rencana Studi Cerdas (Hari Ini)</span>
                      </div>
                      <span class="badge text-primary bg-primary-light font-sans-xs" style="font-size: 0.75rem;">4 Jam Belajar</span>
                    </div>

                    <div class="d-flex flex-column gap-2">
                      <div class="time-slot-item border-start border-4 border-violet bg-violet-light p-2 rounded-3 d-flex justify-content-between align-items-center animate-fade-in">
                        <div class="text-start">
                          <span class="d-block fw-bold text-dark font-sans-xs" style="font-size: 0.75rem;">Sesi 1: Belajar Jaringan Saraf (ANN)</span>
                          <span class="text-muted font-sans-xs" style="font-size: 0.65rem;"><i class="bi bi-clock me-1"></i> 09.00 - 10.30 (90 menit)</span>
                        </div>
                        <span class="badge bg-primary text-white font-sans-xxs" style="font-size: 0.6rem;">Prioritas Tinggi</span>
                      </div>

                      <div class="time-slot-item border-start border-4 border-success bg-success-light-2 p-2 rounded-3 d-flex justify-content-between align-items-center animate-fade-in" style="animation-delay: 0.2s;">
                        <div class="text-start">
                          <span class="d-block fw-bold text-dark font-sans-xs" style="font-size: 0.75rem;">Istirahat: Pomodoro Coffee Break</span>
                          <span class="text-muted font-sans-xs" style="font-size: 0.65rem;"><i class="bi bi-clock me-1"></i> 10.30 - 10.45 (15 menit)</span>
                        </div>
                        <span class="badge bg-success text-white font-sans-xxs" style="font-size: 0.6rem;">Relaksasi</span>
                      </div>

                      <div class="time-slot-item border-start border-4 border-warning bg-warning-light-2 p-2 rounded-3 d-flex justify-content-between align-items-center animate-fade-in" style="animation-delay: 0.4s;">
                        <div class="text-start">
                          <span class="d-block fw-bold text-dark font-sans-xs" style="font-size: 0.75rem;">Sesi 2: Kuis Uji Coba ANN Lesson 41</span>
                          <span class="text-muted font-sans-xs" style="font-size: 0.65rem;"><i class="bi bi-clock me-1"></i> 14.00 - 14.45 (45 menit)</span>
                        </div>
                        <span class="badge bg-warning text-dark font-sans-xxs" style="font-size: 0.6rem;">Latihan Soal</span>
                      </div>
                    </div>
                  </div>

                  <button class="btn btn-outline-secondary btn-sm w-100 rounded-pill font-sans-xs" @click="resetScheduler">
                    <i class="bi bi-arrow-counterclockwise me-1"></i> Rancang Ulang Jadwal
                  </button>
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
import { ref, reactive, computed, nextTick } from 'vue'

const activeFeatureId = ref(null)

const featuresData = {
  1: {
    title: 'AI Penjelasan Materi',
    description: 'Dapatkan penjelasan yang sangat simpel, interaktif, dan mudah dimengerti dari asisten AI Tutor kami yang siap membantu Anda belajar 24 jam non-stop.',
    benefits: [
      'Gunakan analogi sederhana buatan AI',
      'Tanya berkali-kali tanpa batas',
      'Penjelasan terstruktur per sub-bab',
      'Bahasa yang santai & mudah dimengerti'
    ]
  },
  2: {
    title: 'Rangkuman Otomatis',
    description: 'Ubah modul PDF ratusan halaman, transkrip perkuliahan, rekaman suara, atau video YouTube menjadi rangkuman poin-poin penting terstruktur dalam sekejap.',
    benefits: [
      'Mendukung PDF, DOCX, dan audio',
      'Rangkum video YouTube lewat URL',
      'Konsep utama & glosarium instan',
      'Akurasi ekstraksi informasi tinggi'
    ]
  },
  3: {
    title: 'Jadwal yang Rapi',
    description: 'Sistem perencana studi cerdas (Smart Study Planner) yang secara otomatis menyusun jadwal belajar yang optimal dan bebas stres sesuai beban ujian Anda.',
    benefits: [
      'Integrasi Metode Pomodoro otomatis',
      'Sesuaikan dengan target tanggal ujian',
      'Pengingat sesi belajar berkala',
      'Penyeimbangan ritme belajar & istirahat'
    ]
  }
}

const currentFeature = computed(() => {
  return featuresData[activeFeatureId.value] || { title: '', description: '', benefits: [] }
})

// Chatbot simulator state
const chatState = reactive({
  messages: [
    { role: 'assistant', content: 'Halo! Saya adalah AI Tutor Anda. Apa konsep atau materi sulit yang ingin saya jelaskan dengan cara yang sangat simpel hari ini?' }
  ],
  isTyping: false
})

const chatSuggestions = [
  { q: 'Jelaskan konsep Neural Networks dengan simpel', a: 'Jaringan Saraf Tiruan (Neural Network) itu mirip seperti sekelompok teman yang bekerja sama memecahkan teka-teki. Bayangkan Anda punya teman yang ahli menebak warna, teman ahli menebak bentuk, dan teman ahli menebak ukuran. Saat Anda memberi mereka gambar hewan, mereka saling berbisik memberikan tebakan terkecil mereka, menggabungkan tebakan itu, dan di ujungnya mereka sepakat: "Ini adalah kucing!" Semakin sering mereka menebak salah dan dikoreksi, kerja sama mereka semakin pintar. Itulah cara Neural Network belajar!' },
  { q: 'Apa itu OOP (Pemrograman Berorientasi Objek)?', a: 'Bayangkan Pemrograman Berorientasi Objek (OOP) itu seperti membuat mobil mainan dari Lego. Alih-alih membuat satu cetakan mobil utuh sekali jadi, OOP membagi mobil menjadi objek-objek kecil terpisah: Roda, Mesin, dan Setir. Setiap objek Lego ini punya kemampuan sendiri (misal: Roda bisa berputar, Mesin bisa menyala). Keuntungan OOP adalah jika Anda ingin mengganti warna Roda, Anda tidak perlu membongkar seluruh Mesin mobil! Anda cukup mengganti objek Rodanya saja. Sangat rapi dan mudah dikelola!' }
]

const chatContainer = ref(null)

const simulateChat = (suggestion) => {
  // Push user message
  chatState.messages.push({ role: 'user', content: suggestion.q })
  chatState.isTyping = true
  
  // Scroll chat
  scrollToBottom()

  setTimeout(() => {
    chatState.isTyping = false
    chatState.messages.push({ role: 'assistant', content: suggestion.a })
    scrollToBottom()
  }, 1500)
}

const scrollToBottom = () => {
  nextTick(() => {
    if (chatContainer.value) {
      chatContainer.value.scrollTop = chatContainer.value.scrollHeight
    }
  })
}

// Summarizer simulator state
const summarizeState = reactive({
  stage: 'idle', // idle, uploading, done
  progress: 0
})

const simulateUpload = () => {
  summarizeState.stage = 'uploading'
  summarizeState.progress = 0
  
  const interval = setInterval(() => {
    summarizeState.progress += 10
    if (summarizeState.progress >= 100) {
      clearInterval(interval)
      setTimeout(() => {
        summarizeState.stage = 'done'
      }, 400)
    }
  }, 150)
}

const resetSummarizer = () => {
  summarizeState.stage = 'idle'
  summarizeState.progress = 0
}

// Scheduler simulator state
const schedulerState = reactive({
  generating: false,
  generated: false
})

const generateSchedule = () => {
  schedulerState.generating = true
  setTimeout(() => {
    schedulerState.generating = false
    schedulerState.generated = true
  }, 1500)
}

const resetScheduler = () => {
  schedulerState.generating = false
  schedulerState.generated = false
}

// Modal open/close actions
const openFeature = (id) => {
  activeFeatureId.value = id
  
  // Reset simulators
  chatState.messages = [
    { role: 'assistant', content: 'Halo! Saya adalah AI Tutor Anda. Apa konsep atau materi sulit yang ingin saya jelaskan dengan cara yang sangat simpel hari ini?' }
  ]
  chatState.isTyping = false
  
  summarizeState.stage = 'idle'
  summarizeState.progress = 0
  
  schedulerState.generating = false
  schedulerState.generated = false
}

const closeFeature = () => {
  activeFeatureId.value = null
}
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

/* Modal overlay styling */
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(15, 23, 42, 0.45);
  backdrop-filter: blur(8px);
  -webkit-backdrop-filter: blur(8px);
  z-index: 9999;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1.5rem;
}

.modal-card {
  background: #ffffff;
  border-radius: 24px;
  border: 1px solid rgba(124, 58, 237, 0.15);
  width: 100%;
  max-width: 900px;
  max-height: 90vh;
  overflow-y: auto;
  box-shadow: 0 30px 60px rgba(124, 58, 237, 0.15);
  animation: slideUp 0.4s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  z-index: 10000;
}

@keyframes slideUp {
  from {
    opacity: 0;
    transform: translateY(40px) scale(0.95);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

.btn-close-modal {
  position: absolute;
  top: 1.5rem;
  right: 1.5rem;
  font-size: 1.25rem;
  transition: color 0.3s;
  z-index: 10;
}

.btn-close-modal:hover {
  color: var(--brand-primary) !important;
}

/* Simulator elements styling */
.simulator-container {
  background-color: #f8fafc;
  border: 1px solid #e2e8f0 !important;
  min-height: 380px;
  max-height: 420px;
  display: flex;
  flex-direction: column;
}

/* Chatbot styles */
.chat-messages {
  background-color: #f1f5f9;
  border-radius: 12px;
  flex-grow: 1;
  height: 200px;
  border: 1px solid #e2e8f0;
}

.chat-bubble {
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.02);
  max-width: 85%;
}

.bg-primary {
  background-color: var(--brand-primary) !important;
}

/* Summarizer styles */
.upload-dropzone {
  border-color: #cbd5e1 !important;
  background-color: #ffffff;
  transition: all 0.3s;
}

.upload-dropzone:hover {
  background-color: var(--brand-primary-light);
  border-color: var(--brand-primary) !important;
}

/* Scheduler/Calendar styles */
.time-slot-item {
  transition: all 0.3s;
}

.time-slot-item:hover {
  transform: translateX(4px);
}

.border-violet {
  border-color: #8b5cf6 !important;
}

.bg-violet-light {
  background-color: #f5f3ff !important;
}

.bg-success-light-2 {
  background-color: #ecfdf5 !important;
}

.bg-warning-light-2 {
  background-color: #fffbeb !important;
}

.font-sans-xxs {
  font-size: 0.65rem;
}

/* Animations */
.animate-fade-in {
  animation: fadeIn 0.4s ease forwards;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

.typing-dots {
  animation: flash 1.4s infinite;
}

@keyframes flash {
  0%, 100% { opacity: 0.2; }
  50% { opacity: 1; }
}

/* Adjust layout on mobile */
@media (max-width: 991.98px) {
  .modal-card {
    max-height: 95vh;
  }
  .simulator-container {
    min-height: 320px;
  }
}
</style>
