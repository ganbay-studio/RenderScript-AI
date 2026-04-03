# RenderScript AI - Prompt Generator (BETA)

> Archviz Prompt Generator for NanoBanana Pro

RenderScript AI adalah aplikasi web berbasis HTML yang digunakan untuk menghasilkan prompt JSON terstruktur untuk rendering arsitektur visual (archviz) menggunakan AI NanoBanana Pro. Aplikasi ini memungkinkan pengguna untuk mengkonfigurasi berbagai aspek scene arsitektur mulai dari environment, lighting, material, hingga pengaturan kamera.

## ✨ Fitur Utama

- **Scene & Environment Configuration** - Atur tipe scene, fungsi bangunan, waktu, dan cuaca
- **Lighting System** - Kontrol pencahayaan natural dan artificial, global illumination, shadow quality
- **Environment Outside** - Detail lingkungan luar, atmosfer, dan visibilitas
- **Architecture Details** - Style arsitektur, material, warna, dan detail konstruksi
- **Human Elements** - Kehadiran manusia dengan etnisitas, pakaian, dan aktivitas
- **Camera & Composition** - Pengaturan kamera lengkap (lens, aperture, ISO, white balance)
- **Render Style & Mood** - Kualitas render, post-processing, tone mapping, color grading
- **Constraints & AI Behavior** - Kontrol ketat terhadap interpretasi AI
- **JSON Output** - Generate, copy, dan download prompt dalam format JSON
- **Real-time Statistics** - Counter prompt, karakter, kata, dan waktu generate terakhir

## 🚀 Cara Menggunakan

### 1. Akses Aplikasi

**Opsi A - GitHub Pages (Online)**
```
Kunjungi: https://ganbay-studio.github.io/RenderScript-AI/
```
### 2. Konfigurasi Scene
Panel kiri berisi accordion dengan berbagai kategori konfigurasi:

| Section | Deskripsi |
|---------|-----------|
| **Scene & Environment** | Tipe scene, fungsi bangunan, waktu, cuaca |
| **Lighting** | Pencahayaan natural & artificial, global illumination |
| **Environment Outside** | Lingkungan luar, atmosfer, visibilitas |
| **Architecture** | Style, material, warna, detail arsitektur |
| **Human Elements** | Kehadiran manusia, penampilan, aktivitas |
| **Composition & Camera** | Posisi kamera, perspektif, pengaturan lensa |
| **Render Style & Mood** | Kualitas render, post-processing, mood |
| **Constraints & AI Behavior** | Batasan dan perilaku AI |

### 3. Generate Prompt
1. Isi semua field konfigurasi sesuai kebutuhan
2. Klik tombol **"Generate Prompt"** di panel kanan
3. JSON output akan muncul di textarea

### 4. Copy atau Download
- **Copy** - Salin JSON ke clipboard
- **Download** - Unduh sebagai file `renderscript-prompt.json`

### 🌐 Deploy ke GitHub Pages

1. Push repository ke GitHub
2. Buka **Settings** > **Pages**
3. Pilih branch `main` dan folder `/ (root)`
4. Klik **Save**
5. Aplikasi akan tersedia di `https://ganbay-studio.github.io/RenderScript-AI/`

## 📁 Struktur File

```
RenderScript-AI/
├── main_new.html          # Aplikasi utama RenderScript AI
└── backup/                # Folder backup versi sebelumnya
    └── ...
```

## 🛠️ Tech Stack

- **HTML5** - Struktur aplikasi
- **CSS3** - Styling dengan CSS Variables, Grid, Flexbox
- **JavaScript (Vanilla)** - Logika aplikasi tanpa dependencies
- **Font Awesome 6.4.0** - Ikon
- **Google Fonts (Inter)** - Tipografi

## 📋 JSON Output Structure

Prompt yang dihasilkan memiliki struktur berikut:

```json
{
  "scene_type": "string",
  "function": "string",
  "time_of_day": "string",
  "weather": "string",
  "lighting": {
    "type": "string",
    "natural_light": { "source", "intensity", "direction", "color_temperature", "effect" },
    "artificial_light": { "type", "color_temperature", "intensity", "placement", "effect" },
    "global_illumination": "string",
    "shadow_quality": "string"
  },
  "environment_outside": { "type", "details", "atmosphere", "visibility", "lighting_match" },
  "architecture": {
    "style": "string",
    "floors": number,
    "color_palette": ["array"],
    "materials": { "main_wall", "accent", "railing", "gate", "glass", "roof" },
    "details": { "secondary_skin", "balcony", "imperfections" }
  },
  "human_elements": {
    "presence": boolean,
    "density": "string",
    "activity": ["array"],
    "appearance": { "ethnicity", "age_range", "clothing", "expression" },
    "motion": { "some_blur", "others" }
  },
  "environment_details": { "road", "ground", "props", "cleanliness" },
  "composition": { "camera_position", "perspective", "symmetry", "leading_lines", "depth" },
  "camera_settings": { "camera_type", "lens", "aperture", "iso", "shutter_speed", "white_balance", "focus", "dynamic_range" },
  "render_style": {
    "quality": "string",
    "sharpness": "string",
    "contrast": "string",
    "saturation": "string",
    "post_processing": { "tone_mapping", "color_grading", "bloom", "vignette" }
  },
  "mood": { "feeling", "ambience", "temperature_feel" },
  "constraints": { "exact_geometry", "locked_camera", "no_redesign", "match_sketch_exactly", ... },
  "ai_behavior": { "instruction", "geometry_interpretation", "creativity_level", "environment_blend", "realism_priority" }
}
```

## 🎨 UI Features

- **Dark Theme** - Interface gelap yang nyaman untuk penggunaan lama
- **Responsive Grid** - Layout dua panel (Configuration + JSON Output)
- **Accordion Menu** - Navigasi konfigurasi yang terorganisir
- **Fixed Buttons** - Tombol Generate, Copy, Download tetap terlihat
- **Toast Notifications** - Feedback visual untuk setiap aksi
- **Statistics Bar** - Menampilkan statistik prompt yang dihasilkan

## 📝 Default Configuration

Aplikasi datang dengan konfigurasi default untuk scene arsitektur tropis modern:
- **Scene**: Modern tropical residential house
- **Lighting**: Natural daylight 5500K-6000K
- **Environment**: Indonesian suburban neighborhood
- **Architecture**: Modern minimalist box house (3 floors)
- **Materials**: Grey cement, dark wood, black metal
- **Camera**: 24-35mm architectural lens, f/8-f/11

## 🔄 Reset Form

Klik tombol **Reset** (ikon redo) di header panel Configuration untuk mengembalikan semua nilai ke default.

## ⚠️ Catatan Penting

- Aplikasi ini berjalan sepenuhnya di browser (client-side)
- Tidak memerlukan server atau instalasi
- Semua data konfigurasi bersifat lokal
- File JSON yang dihasilkan siap digunakan dengan NanoBanana Pro

## 📄 Lisensi

&copy; 2026 Copyright by **Ganbay Studio**

## 🙏 Credits

Dibuat dengan ❤️ oleh Ganbay Studio untuk kebutuhan arsitektur visual rendering.
