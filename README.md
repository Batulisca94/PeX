# 🚀 p!loader EGL — Pasha Network Launcher (README GÜNCEL DEĞİLDİR !)

> Modern Game + Network + System Utility Launcher

---

## 🧠 Sistem Hakkında

p!loader, oyun yönetimi + sistem araçları + ağ analiz + remote auth + Discord presence katmanlarını tek bir runtime içinde birleştiren modüler bir launcher altyapısıdır.

Bu sistem klasik bir “game launcher” değil, **çok katmanlı kullanıcı workspace shell** mimarisidir.

---

## 🧩 Mimari Bileşenler

- 🔐 Key Sistemi
- 📦 Oyun Kütüphanesi
- ⚡ Epic Games Başlatıcısı
- 🧬 DLL integrity validation layer
- 🌐 Network scanning subsystem
- 🧠 System utility toolkit
- 🎮 Epic Games integration bridge
- 📡 Discord Rich Presence (RPC) state sync

---

## 🔒 Güvenlik Sistemi

Launcher başlamadan önce runtime integrity kontrolü yapılır:

### ✔ DLL Integrity Check
- MD5 + SHA256 doğrulama
- Bozulmuş / değiştirilmiş modülleri bloklar

### ✔ Runtime Load Validation
- ctypes tabanlı native module binding
- başarısız load → safe exit

---

## 🧾 Giriş Sistemi

Kullanıcı doğrulaması remote key server üzerinden yapılır:

- Kullanıcı adı + şifre doğrulama
- Dynamic user list fetch
- Online doğrulama zorunludur

---

## 🎮 Oyun Sistemi

### 📌 Oyun Ekle
- İsim + exe path kaydı
- JSON tabanlı local storage

### 📚 Kütüphane
- Indexed game list
- Direct subprocess launcher

### 🔍 Oyun Ara
- Case-insensitive search filter
- Local library query engine

### 🟣 Epic Games Entegrasyonu
- URI scheme üzerinden direkt başlatma:
  - `com.epicgames.launcher://`

---

## 🧰 Araçlar Modülü (NEW)

p!loader artık sadece launcher değil, **system utility hub**:

### 🧲 MAC Address Toolkit
- Network adapter listeleme
- MAC görüntüleme & kopyalama
- Registry tabanlı MAC değiştirme
- Random MAC üretimi (LAA format)

### 🧬 HWID Spoof Engine
- MachineGuid override
- Hardware profile GUID değişimi
- System identity masking (registry layer)
- Reboot sonrası aktif olur

---

## 🎯 System Service Controller (NEW)

### 🧨 Service Management
- Process sonlandırma
- Windows service stop/start kontrolü
- Boot-time servis davranışı düzenleme

---

## 🌐 Network Toolkit (NEW)

### 📡 Npcap Installer
- Otomatik indirme + kurulum başlatma

### 🔎 Nmap Integration
- Local subnet discovery
- Gateway detection
- Host discovery scan (`-sn`)

### 📶 Wi-Fi Scanner
- `netsh wlan` BSSID tarama
- Aktif ağ keşfi

---

## ⚙️ Download Engine (NEW)

### ⬇ aria2c Integration
- Otomatik bootstrap
- ZIP fallback extraction
- Multi-source download support

### 🎮 Game Downloader
- Torrent tabanlı indirme akışı
- İndirilen exe otomatik bulma
- subprocess ile otomatik başlatma

---

## 📡 Discord RPC (NEW)

Gerçek zamanlı aktivite senkronizasyonu:

- Menü state tracking
- Alt seçim tracking
- Thread tabanlı update loop
- Custom Discord asset desteği
- Session timestamp tracking

---

## 🧠 Sistem Davranışı

- Multi-threaded RPC subsystem
- Persistent JSON registry
- Admin privilege escalation layer
- Windows native API entegrasyonu (winreg, ctypes)
- subprocess tabanlı process execution

---

## ⚠️ Notlar

- Sistem Windows platformuna özeldir
- Bazı modüller admin yetkisi gerektirir
- Network ve system modülleri reboot sonrası etkili olabilir
- DLL doğrulama başarısız olursa sistem kapanır

---

## 🧪 Versiyon Felsefesi

p!loader EGL artık:

> “Launcher” değil  
> → **Hybrid system shell + game runtime + utility framework**
