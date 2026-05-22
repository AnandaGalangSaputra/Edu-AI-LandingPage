<template>
  <section id="home"
    class="hero-section bg-glow-section py-5 d-flex align-items-center min-vh-100 position-relative overflow-hidden">
    <!-- Glow effects background -->
    <div class="glow-orb glow-orb-1"></div>
    <div class="glow-orb glow-orb-2"></div>

    <div class="container pt-5">
      <div class="row align-items-center g-5 pt-4">

        <!-- Left Text Content -->
        <div class="col-lg-6 col-12 text-start">
          <div class="animate-fade-in-up">
            <h1 class="hero-title mb-5">
              Edu AI: Belajar<br>
              Lebih Cepat,<br>
              Dengan Bantuan
              <span class="highlight-container">
                <span class="highlight-text">AI</span>
                <svg class="highlight-curve" viewBox="0 0 200 15" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path d="M10 10 Q125 -15 240 10" stroke="var(--brand-yellow)" stroke-width="4.5"
                    stroke-linecap="round" fill="none" />
                </svg>
              </span>
            </h1>

            <p class="fs-5 text-muted mb-5 pe-lg-5 fw-normal lh-base">
              Belajar jadi lebih terarah dengan penjelasan simpel, rangkuman otomatis, dan jadwal yang rapi.
            </p>

            <div class="d-flex flex-wrap gap-4 align-items-center">
              <a href="#contact"
                class="btn btn-primary btn-lg rounded-pill px-4 py-3 shadow-md fw-semibold transition-all">
                Coba Sekarang
              </a>
              <a href="#"
                class="d-flex align-items-center gap-2 text-decoration-none play-demo-btn fw-bold text-dark-50"
                @click.prevent="showDemoModal">
                <div class="play-icon-wrapper">
                  <svg width="34" height="34" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <circle cx="12" cy="12" r="11" stroke="currentColor" stroke-width="1.8" fill="none" />
                    <path d="M10.25 8.5L15.75 12L10.25 15.5V8.5Z" fill="currentColor" />
                  </svg>
                </div>
                <span class="demo-text">Lihat demo</span>
              </a>
            </div>
          </div>
        </div>

        <!-- Right Dashboard Image/Mockup Template -->
        <div class="col-lg-6 col-12">
          <div class="position-relative float-animation px-3 px-lg-0">

            <!-- Floating badge top-left: Flag -->
            <div class="floating-badge badge-top-left">
              <i class="bi bi-flag-fill"></i>
            </div>

            <!-- Floating badge top-right: Stack -->
            <div class="floating-badge badge-top-right">
              <i class="bi bi-database-fill"></i>
            </div>

            <!-- Floating badge bottom-left: Active Users -->
            <div class="floating-badge badge-active-users glass-panel">
              <div class="icon-avatar bg-primary-light d-flex align-items-center justify-content-center">
                <i class="bi bi-people-fill text-primary-purple"></i>
              </div>
              <div class="text-start">
                <div class="text-muted-xs">Pengguna Aktif</div>
                <div class="fw-bold fs-6 text-dark d-flex align-items-center gap-2">
                  20.000
                  <svg width="22" height="14" viewBox="0 0 22 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <rect x="2" y="8" width="2.5" height="4" rx="1.25" fill="#22c55e" />
                    <rect x="7" y="5" width="2.5" height="7" rx="1.25" fill="#22c55e" />
                    <rect x="12" y="2" width="2.5" height="10" rx="1.25" fill="#22c55e" />
                    <rect x="17" y="6" width="2.5" height="6" rx="1.25" fill="#22c55e" />
                  </svg>
                </div>
              </div>
            </div>


            <div class="dashboard-mockup">
              <!-- Browser Header -->
              <div class="dashboard-header d-flex align-items-center justify-content-between">
                <div class="d-flex align-items-center gap-1.5">
                  <span class="header-dot dot-red"></span>
                  <span class="header-dot dot-yellow"></span>
                  <span class="header-dot dot-green"></span>
                </div>
                <div
                  class="browser-address-bar font-sans-xs text-muted text-center px-4 py-0.5 rounded bg-white overflow-hidden text-truncate"
                  style="max-width: 50%; font-size: 0.75rem;">
                  https://edu-ai-blond.vercel.app/
                </div>
                <div style="width: 30px;"></div>
              </div>

              <!-- Main Dashboard Workspace -->
              <div class="dashboard-grid bg-dashboard">
                <!-- Sidebar -->
                <aside class="dashboard-sidebar p-3 border-end">
                  <div class="brand-sidebar mb-4 d-flex align-items-center gap-1.5">
                    <span class="fw-bold font-sans-sm text-white">edu <span class="text-violet-light">AI</span></span>
                  </div>
                  <ul class="list-unstyled d-flex flex-column gap-2 mb-0">
                    <li class="sidebar-item active"><i class="bi bi-grid-1x2-fill"></i>Dashboard</li>
                    <li class="sidebar-item"><i class="bi bi-book"></i>Courses</li>
                    <li class="sidebar-item"><i class="bi bi-chat-left-dots"></i>AI Tutor</li>
                    <li class="sidebar-item"><i class="bi bi-calendar3"></i>Calendar</li>
                    <li class="sidebar-item"><i class="bi bi-bar-chart-line"></i>Progress</li>
                    <li class="sidebar-item"><i class="bi bi-journal-check"></i>Assignments</li>
                    <li class="sidebar-item"><i class="bi bi-envelope"></i>Messages</li>
                  </ul>
                </aside>

                <!-- Dashboard Content Area -->
                <main class="dashboard-content p-3 text-start">
                  <!-- Header -->
                  <header class="d-flex justify-content-between align-items-center mb-3">
                    <div>
                      <h6 class="fw-bold mb-0 text-white" style="font-size: 0.95rem;">Welcome back, Parjo!</h6>
                    </div>
                    <div class="d-flex align-items-center gap-2">
                      <i class="bi bi-search text-white-50 cursor-pointer"></i>
                      <i class="bi bi-bell text-white-50 cursor-pointer"></i>
                      <img
                        src="https://images.unsplash.com/photo-1494790108377-be9c29b29330?auto=format&fit=crop&q=80&w=64"
                        alt="Sarah Profile" class="profile-avatar-mock" />
                    </div>
                  </header>

                  <h6 class="fw-bold text-white-50 mb-3" style="font-size: 0.8rem;">My Learning Dashboard</h6>

                  <!-- Inner Cards Area -->
                  <div class="row g-3">
                    <!-- Left Column: Video Course Playing -->
                    <div class="col-8">
                      <div class="card bg-card-dark border-0 p-3 rounded-3 text-white">
                        <div class="text-muted-xs text-uppercase tracking-wider font-semibold mb-1 text-violet-light">
                          Current Course</div>
                        <div class="fw-bold font-sans-sm mb-2 text-white">AI Fundamentals: Lesson 41: Neural Networks
                        </div>
                        <div class="progress mb-3 bg-progress-dark" style="height: 6px;">
                          <div class="progress-bar bg-primary-purple" role="progressbar" style="width: 62%"
                            aria-valuenow="62" aria-valuemin="0" aria-valuemax="100"></div>
                        </div>

                        <!-- Video Placeholder Layout -->
                        <div
                          class="video-mockup rounded-3 position-relative d-flex align-items-center justify-content-center">
                          <img
                            src="https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?auto=format&fit=crop&q=80&w=400"
                            alt="Neural Net Graphic" class="video-thumbnail" />
                          <div class="overlay-video"></div>
                          <button
                            class="btn btn-sm btn-primary rounded-pill px-3 py-1.5 play-badge d-flex align-items-center gap-1.5">
                            <i class="bi bi-play-fill"></i> Resume Lesson
                          </button>
                        </div>
                      </div>
                    </div>

                    <!-- Right Column: Lesson Notes & Quick Stats -->
                    <div class="col-4">
                      <div
                        class="card bg-card-dark border-0 p-3 rounded-3 text-white h-100 d-flex flex-column justify-content-between">
                        <div>
                          <div class="fw-bold font-sans-xs text-white mb-2">Lesson Notes</div>
                          <p class="text-white-50 lh-sm mb-3" style="font-size: 0.7rem;">
                            Generative Artificial Neural Network (ANN) mimics human brains to analyze and learn complex
                            data distributions...
                          </p>
                        </div>
                        <div
                          class="network-chart-mock rounded-3 p-2 bg-black-20 d-flex align-items-center justify-content-center">
                          <!-- Minimal SVG network connection visual -->
                          <svg width="100%" height="50" viewBox="0 0 100 50">
                            <circle cx="10" cy="25" r="4" fill="#a78bfa" />
                            <circle cx="45" cy="12" r="4" fill="#818cf8" />
                            <circle cx="45" cy="38" r="4" fill="#818cf8" />
                            <circle cx="80" cy="25" r="4" fill="#fbbf24" />
                            <line x1="14" y1="25" x2="41" y2="14" stroke="#4b5563" stroke-width="1.5" />
                            <line x1="14" y1="25" x2="41" y2="36" stroke="#4b5563" stroke-width="1.5" />
                            <line x1="49" y1="14" x2="76" y2="23" stroke="#4b5563" stroke-width="1.5" />
                            <line x1="49" y1="36" x2="76" y2="27" stroke="#4b5563" stroke-width="1.5" />
                          </svg>
                        </div>
                      </div>
                    </div>
                  </div>
                </main>
              </div>
            </div>

          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
const showDemoModal = () => {
  alert('Memutar Demo Edu AI... Video demonstrasi akan terbuka.')
}
</script>

<style scoped>
.hero-section {
  padding-bottom: 7rem !important;
}

.glow-orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(120px);
  z-index: -1;
  pointer-events: none;
}

.glow-orb-1 {
  width: 400px;
  height: 400px;
  background: rgba(124, 58, 237, 0.12);
  top: 10%;
  right: -10%;
}

.glow-orb-2 {
  width: 300px;
  height: 300px;
  background: rgba(251, 191, 36, 0.08);
  bottom: 10%;
  left: -5%;
}

.play-demo-btn {
  color: var(--text-dark);
  transition: all 0.3s ease;
}

.play-demo-btn:hover {
  color: var(--brand-primary) !important;
}

.play-icon-wrapper {
  color: var(--brand-primary);
  transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}

.play-demo-btn:hover .play-icon-wrapper {
  transform: scale(1.15) rotate(10deg);
}

.demo-text {
  font-size: 1.1rem;
}

/* Floating Avatar Icon Inside badge */
.icon-avatar {
  width: 38px;
  height: 38px;
  border-radius: 50%;
  background: var(--brand-primary-light);
}

.text-primary-purple {
  color: var(--brand-primary);
}

.text-muted-xs {
  font-size: 0.75rem;
  color: #78716c;
  font-weight: 500;
}

/* SVG curve adjustment */
.highlight-curve {
  position: absolute;
  left: 50%;
  transform: translateX(-120%);

  bottom: -40px;

  width: 280px;
  height: auto;

  overflow: visible;
}

/* Dashboard Dark Inner Mockup Styles */
.bg-dashboard {
  background: #0f172a;
  display: grid;
  grid-template-columns: 140px 1fr;
  min-height: 380px;
}

.dashboard-sidebar {
  background: #0b0f19;
}

.text-violet-light {
  color: #a78bfa;
}

.sidebar-item {
  color: #94a3b8;
  font-size: 0.75rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.4rem 0.6rem;
  border-radius: 6px;
  cursor: pointer;
  transition: all 0.2s ease;
}

.sidebar-item:hover,
.sidebar-item.active {
  background: #1e1b4b;
  color: #ffffff;
}

.profile-avatar-mock {
  width: 26px;
  height: 26px;
  border-radius: 50%;
  object-fit: cover;
  border: 1.5px solid #a78bfa;
}

.bg-card-dark {
  background: #1e293b;
}

.bg-progress-dark {
  background: #334155;
}

.video-mockup {
  height: 120px;
  background: #0f172a;
  overflow: hidden;
}

.video-thumbnail {
  width: 100%;
  height: 100%;
  object-fit: cover;
  opacity: 0.6;
  transition: all 0.5s ease;
}

.video-mockup:hover .video-thumbnail {
  transform: scale(1.05);
}

.overlay-video {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0) 0%, rgba(0, 0, 0, 0.4) 100%);
}

.play-badge {
  position: absolute;
  z-index: 2;
  font-size: 0.75rem;
  padding: 0.4rem 0.8rem;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
}

.bg-black-20 {
  background: rgba(0, 0, 0, 0.2);
}

.cursor-pointer {
  cursor: pointer;
}

.font-sans-sm {
  font-size: 0.85rem;
}

.font-sans-xs {
  font-size: 0.75rem;
}

.text-white-50 {
  color: rgba(255, 255, 255, 0.6) !important;
}

/* Animations Trigger */
.animate-fade-in-up {
  animation: fadeInUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }

  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 767.98px) {
  .hero-section {
    padding-top: 6rem !important;
    text-align: center;
  }

  .hero-title {
    font-size: 2.5rem;
  }

  .badge-active-users {
    bottom: 5%;
    left: 2%;
  }

  .badge-top-left {
    left: 2%;
  }

  .badge-top-right {
    right: 2%;
  }

  .bg-dashboard {
    grid-template-columns: 1fr;
  }

  .dashboard-sidebar {
    display: none;
  }

  .highlight-curve {
    position: absolute;
    left: 50%;
    transform: translateX(-10%);

    bottom: -40px;

    width: 240px;
    height: auto;

    overflow: visible;
  }
}
</style>
