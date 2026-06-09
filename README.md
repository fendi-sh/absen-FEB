<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portal Launch Pad FEB UNNES</title>
  
  <!-- Tailwind CSS CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- Google Fonts: Inter & Orbitron -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=Orbitron:wght@500;700;900&display=swap" rel="stylesheet">
  
  <!-- Lucide Icons -->
  <script src="https://unpkg.com/lucide@latest"></script>

  <script>
    if (typeof tailwind !== 'undefined') {
      tailwind.config = {
        theme: {
          extend: {
            fontFamily: {
              sans: ['Inter', 'sans-serif'],
              tech: ['Orbitron', 'sans-serif'],
            },
            colors: {
              unnesBlue: '#1e3c72',
              unnesBlueDark: '#122548',
              unnesGold: '#f1c40f',
              unnesGoldDark: '#d97706',
              cyberSlateLight: 'rgba(255, 255, 255, 0.75)',
              cyberBorderLight: 'rgba(30, 60, 114, 0.15)',
            }
          }
        }
      }
    }
  </script>

  <style>
    body {
      font-family: 'Inter', sans-serif;
      /* Gradasi Biru, Kuning, dan Putih Cerah Premium */
      background: linear-gradient(135deg, #f0f9ff 0%, #bae6fd 35%, #fef08a 75%, #ffffff 100%);
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      overflow: hidden;
    }

    /* Efek Grid Taktis Cerah Fiktif */
    .bg-tech-grid-light {
      background-size: 24px 24px;
      background-image: 
        linear-gradient(to right, rgba(30, 60, 114, 0.04) 1px, transparent 1px),
        linear-gradient(to bottom, rgba(30, 60, 114, 0.04) 1px, transparent 1px);
    }
    
    /* Efek Kaca Frosted Cemerlang dengan Isi Gradasi Transparan Emas-Biru Mewah */
    .glass-card-light {
      background: linear-gradient(135deg, rgba(255, 255, 255, 0.75) 0%, rgba(241, 196, 15, 0.08) 50%, rgba(30, 60, 114, 0.08) 100%);
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
      border: 1px solid rgba(255, 255, 255, 0.4);
      box-shadow: 
        0 8px 32px 0 rgba(31, 38, 135, 0.06),
        inset 0 1px 1px 0 rgba(255, 255, 255, 0.8);
    }

    /* Pendaran Cahaya Lembut Emas & Biru */
    .glow-unnes-gold-soft {
      box-shadow: 0 0 25px rgba(241, 196, 15, 0.3), inset 0 0 10px rgba(241, 196, 15, 0.1);
    }
    .glow-unnes-blue-soft {
      box-shadow: 0 8px 30px rgba(30, 60, 114, 0.15);
    }
    .text-glow-gold-dark {
      text-shadow: 0 0 8px rgba(217, 119, 6, 0.25);
    }

    /* Animasi Radar Pulse Lingkaran Belakang Tombol */
    @keyframes radar-ping {
      0% {
        transform: scale(0.9);
        opacity: 0.6;
        box-shadow: 0 0 0 0 rgba(30, 60, 114, 0.2);
      }
      50% {
        opacity: 0.2;
      }
      100% {
        transform: scale(1.18);
        opacity: 0;
        box-shadow: 0 0 0 20px rgba(30, 60, 114, 0);
      }
    }
    .radar-pulse-effect {
      animation: radar-ping 3.5s infinite ease-out;
    }

    /* Animasi Laser Scanner Pemindai */
    @keyframes scan-laser {
      0% { top: 0%; opacity: 0.15; }
      50% { top: 100%; opacity: 0.5; }
      100% { top: 0%; opacity: 0.15; }
    }
    .scanner-line {
      animation: scan-laser 4s infinite ease-in-out;
    }
  </style>
</head>
<body class="bg-tech-grid-light relative w-full h-full">

  <!-- GLOW DECORATIONS (ORBS HOLOGRAFIS CERAH BIRU & EMAS) -->
  <div class="absolute w-[80vw] h-[80vw] md:w-[400px] md:h-[400px] rounded-full bg-sky-200/40 blur-[100px] pointer-events-none -top-10 -left-10 animate-pulse"></div>
  <div class="absolute w-[70vw] h-[70vw] md:w-[350px] md:h-[350px] rounded-full bg-yellow-100/45 blur-[90px] pointer-events-none -bottom-10 -right-10"></div>

  <!-- CONTAINER HOLOGRAM CARD (TEMA GRADASI KACA FEB CERAH) -->
  <div class="w-full max-w-sm mx-4 p-6 text-center relative z-10 glass-card-light border border-cyberBorderLight rounded-3xl glow-unnes-blue-soft overflow-hidden">
    
    <!-- Laser scanner vertikal tipis estetis -->
    <div class="absolute left-0 right-0 h-[1.5px] bg-gradient-to-r from-transparent via-unnesGold/40 to-transparent scanner-line z-0"></div>

    <!-- HEADER TELEMETRY / IDENTITAS INSTANSI -->
    <div class="mb-5 space-y-1.5 z-10 relative">
      <div class="flex justify-center items-center gap-2 text-unnesBlue">
        <i data-lucide="satellite" class="w-4.5 h-4.5 text-unnesBlueDark animate-pulse"></i>
        <span class="font-tech text-[10px] tracking-widest uppercase font-black text-glow-gold-dark text-unnesBlueDark">FEB UNNES PORTAL SYSTEM</span>
      </div>
      <p class="text-[9px] text-slate-500 font-tech tracking-widest uppercase">GEOLOCATION SYNC & GPS GATEWAY</p>
    </div>

    <!-- AREA UTAMA TOMBOL (A TAG MURNI DENGAN TARGET TOP) -->
    <div id="panel-inapp" class="space-y-4 z-10 relative py-2">
      <div class="relative inline-block">
        <!-- Lingkaran denyut radar fiktif di belakang tombol -->
        <div class="absolute inset-0 rounded-2xl bg-unnesBlue/5 radar-pulse-effect"></div>
        
        <!-- PENGGUNAAN TAG 'A' MURNI DENGAN TARGET '_top' UNTUK MENGHANCURKAN IFRAME GOOGLE SITES -->
        <a id="btn-launch" target="_top" href="#" class="relative inline-flex bg-gradient-to-r from-unnesBlue to-[#254d8c] hover:from-unnesBlueDark hover:to-unnesBlue text-slate-100 hover:text-white font-tech font-bold text-xs tracking-wider py-4 px-6 rounded-2xl shadow-md hover:shadow-lg transition-all duration-300 items-center justify-center gap-2.5 border border-unnesGold hover:border-unnesGoldDark glow-unnes-gold-soft active:scale-95 group">
          <i data-lucide="fingerprint" class="w-5 h-5 text-unnesGold group-hover:text-white transition animate-pulse"></i>
          <span>LAUNCH PRESENSI</span>
        </a>
      </div>
      
      <p id="info-pembantu" class="text-[10px] text-slate-500 font-tech tracking-wider leading-relaxed">
        SINKRONISASI GEOLOKASI MANDATORY (100M)
      </p>
    </div>

    <!-- AREA INSTRUKSI KHUSUS IPHONE DI DALAM WHATSAPP (Aesthetic Warning Amber) -->
    <div id="guide-ios" class="hidden mt-4 p-4 bg-amber-500/10 border border-amber-500/30 rounded-2xl text-left space-y-2 z-10 relative">
      <div class="flex items-start gap-2 text-amber-700">
        <i data-lucide="alert-circle" class="w-4.5 h-4.5 shrink-0 mt-0.5 animate-pulse"></i>
        <span class="text-[10px] font-tech font-bold uppercase tracking-widest text-glow-gold-dark">SECURITY ENVIRONMENT DETECTED</span>
      </div>
      <p class="text-[10px] text-slate-600 leading-relaxed font-medium">
        Browser internal iOS WhatsApp memblokir akses GPS otomatis. Silakan ketuk **ikon kompas/Safari** di pojok **kanan bawah** layar WhatsApp saat ini untuk memindahkan akses secara aman.
      </p>
    </div>

  </div>

  <script {csp-nonce}>
    // =================================================================
    // KONFIGURASI UTAMA: MASUKKAN URL GOOGLE APPS SCRIPT PRESENSI ANDA
    // =================================================================
    const TARGET_WEB_APP_URL = "https://script.google.com/a/macros/mail.unnes.ac.id/s/AKfycbz0e7xOvP_VN2GgDN21f2FdSOfREpOTuo0etfbpm99F0YPXDeYZE0Frvf74QPhm-uIN/exec"; 

    const ua = navigator.userAgent || navigator.vendor || window.opera;

    function isInsideInAppBrowser() {
      return (
        ua.includes("FBAN") || 
        ua.includes("FBAV") || 
        ua.includes("Instagram") || 
        ua.includes("WhatsApp") || 
        ua.includes("Messenger") || 
        ua.includes("Line") || 
        ua.includes("Telegram")
      );
    }

    function isAndroid() {
      return /Android/i.test(ua);
    }

    function isIOS() {
      return /iPhone|iPad|iPod/i.test(ua);
    }

    window.onload = function() {
      if (typeof lucide !== 'undefined') {
        lucide.createIcons();
      }

      const btnLaunch = document.getElementById('btn-launch');

      // Konfigurasi dinamis link penembus iFrame Google Sites
      if (isInsideInAppBrowser()) {
        if (isAndroid()) {
          // Android: Gunakan intent murni untuk mementalkan Chrome dari WhatsApp induk
          const cleanUrl = TARGET_WEB_APP_URL.replace("https://", "").replace("http://", "");
          const intentUrl = `intent://${cleanUrl}#Intent;scheme=https;package=com.android.chrome;end`;
          
          btnLaunch.setAttribute('href', intentUrl);
          // target="_top" akan menghancurkan iFrame Google Sites dan mengeksekusi intent langsung pada induk WhatsApp
          btnLaunch.setAttribute('target', '_top');
        } else if (isIOS()) {
          // iOS: WhatsApp tidak mendukung intent pental, tampilkan panduan Safari Kompas di pojok kanan bawah
          btnLaunch.setAttribute('href', '#');
          btnLaunch.addEventListener('click', function(e) {
            e.preventDefault();
            document.getElementById('guide-ios').classList.remove('hidden');
            document.getElementById('info-pembantu').innerText = "MENUNGGU SINKRONISASI SAFARI KELUAR...";
            document.getElementById('info-pembantu').classList.remove('text-slate-500');
            document.getElementById('info-pembantu').classList.add('text-unnesBlueDark');
          });
        } else {
          // Fallback umum di dalam WhatsApp
          btnLaunch.setAttribute('href', TARGET_WEB_APP_URL);
          btnLaunch.setAttribute('target', '_top');
        }
      } else {
        // Jika dibuka langsung di browser eksternal sejak awal
        btnLaunch.setAttribute('href', TARGET_WEB_APP_URL);
        btnLaunch.setAttribute('target', '_blank'); // Buka tab baru di browser eksternal asli
      }
    };
  </script>
</body>
</html>
