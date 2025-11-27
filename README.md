# 🦅 WiFi Kapsama Alanını Ölçme Aracı - AtmacaPro

![AtmacaPro Mobile Interface](https://raw.githubusercontent.com/bootkitt/atmaca-pro/refs/heads/main/screenshots/mobile.png)

**AtmacaPro** is an open-source, web-based WiFi coverage measurement tool designed to identify and solve WiFi coverage issues. Our goal is not just to identify problems, but to be the solution itself. Built with modern web technologies, it allows users to create heatmaps of WiFi coverage by walking around and automatically measuring signal strength.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Web](https://img.shields.io/badge/web-based-lightgrey.svg)](https://executeos.net/)
[![GitHub](https://img.shields.io/badge/GitHub-bootkitt-green.svg)](https://github.com/bootkitt/)

**🔗 Links:**
- **GitHub Repository:** [https://github.com/bootkitt/atmaca-pro](https://github.com/bootkitt/atmaca-pro)
- **Live Demo:** [index.html](index.html)

---

## 📋 Table of Contents

- [English](#english)
  - [Features](#features)
  - [How It Works](#how-it-works)
  - [Usage](#usage)
  - [Technical Details](#technical-details)
  - [Limitations](#limitations)
  - [Data Privacy & Security](#data-privacy--security)
  - [Contributing](#contributing)
  - [License](#license)
- [Türkçe](#türkçe)
  - [Özellikler](#özellikler)
  - [Nasıl Çalışır](#nasıl-çalışır)
  - [Kullanım](#kullanım)
  - [Teknik Detaylar](#teknik-detaylar)
  - [Kısıtlamalar](#kısıtlamalar)
  - [Veri Gizliliği ve Güvenlik](#veri-gizliliği-ve-güvenlik)
  - [Katkıda Bulunma](#katkıda-bulunma)
  - [Lisans](#lisans)

---

# English

## 🎯 Overview

AtmacaPro is a **web-based tool** designed to identify and solve WiFi coverage issues. Our mission is to detect problems arising from WiFi coverage areas and become the solution itself, not just identify the problem. It uses GPS tracking and network latency measurements to create visual heatmaps of WiFi coverage areas, providing professional-grade WiFi analysis capabilities.

### ⚠️ Important Notice

**AtmacaPro is designed for educational purposes.** Due to web technology limitations, it may not provide 100% stable results. For professional WiFi analysis, native mobile applications are recommended. The tool is developed in compliance with data security standards and privacy policies.

## ✨ Features

- **🔄 Automatic Signal Measurement**: Automatically measures WiFi signal strength as you move
- **🗺️ Real-time Heatmap**: Creates a Voronoi diagram-based heatmap visualization for professional WiFi analysis
- **📍 GPS Tracking**: Uses GPS coordinates for accurate location tracking
- **📊 Signal Visualization**: Color-coded heatmap showing signal strength in dBm
- **💾 Export Functionality**: Save your heatmap as a high-resolution PNG image
- **📐 Floor Plan Support**: Upload your floor plan image for better visualization
- **🎨 Modern UI**: Clean, modern interface with white/grey design
- **📱 Responsive Design**: Works on both desktop and mobile devices
- **🔒 Privacy-First**: All data stays in your browser, nothing is sent to servers

## 🚀 How It Works

1. **Start Recording**: Click the "Start" button to begin WiFi signal measurement
2. **Move Around**: Walk around your space while the app automatically tracks your movement
3. **Automatic Measurement**: The app measures WiFi signal strength at regular intervals based on movement
4. **Real-time Visualization**: A heatmap is generated in real-time using Voronoi triangulation
5. **Export**: Save your completed heatmap as an image

### Signal Measurement

Since web browsers don't expose actual WiFi dBm values, AtmacaPro uses network latency to a known endpoint (Google's `generate_204`) as a proxy for signal strength. Lower latency generally correlates with stronger WiFi signals.

## 📖 Usage

### Basic Usage

1. Open the application in a modern web browser
2. Grant location permissions when prompted
3. Click "Start" to begin recording
4. Walk around the area you want to map
5. Click "Stop" when finished
6. Click "Download" to save your heatmap

### Floor Plan Upload

1. Click the folder icon (📁) in the header
2. Upload your floor plan image
3. The floor plan will be displayed as the background for your heatmap

### Keyboard Controls (Desktop)

- **Arrow Keys**: Move the position indicator (for testing without GPS)

## 🔧 Technical Details

### Project Structure

```
AtmacaPro/
├── index.html          # Main HTML file
├── assets/
│   └── css/
│       └── style.css  # All CSS styles
├── README.md          # Project documentation
└── LICENSE            # MIT License
```

### Technologies Used

- **HTML5 Canvas**: For rendering the map and heatmap
- **D3-Delaunay**: For Voronoi diagram generation
- **Geolocation API**: For GPS tracking
- **Device Motion API**: For movement detection
- **Performance API**: For latency measurement

### Architecture

- **World Space & View Space**: Implements a coordinate system that allows infinite map expansion with auto-pan and auto-zoom
- **Voronoi Triangulation**: Creates cellular, continuous heatmap visualization
- **Low-pass Filtering**: Smooths sensor data for stable movement tracking
- **Re-visit Detection**: Updates signal data when revisiting previously mapped areas

### Color Coding

- **Cyan (-30 to -50 dBm)**: Excellent signal
- **Green (-50 to -60 dBm)**: Good signal
- **Light Green (-60 to -70 dBm)**: Fair signal
- **Yellow (-70 to -80 dBm)**: Weak signal
- **Orange (-80 to -85 dBm)**: Very weak signal
- **Red (< -85 dBm)**: Poor signal

## ⚠️ Limitations

Due to web browser limitations, the following features are **not available**:

- **AR/Wall Detection**: Requires native app development
- **Real WiFi API**: Web browsers don't expose actual WiFi dBm values (simulation is used)
- **LiDAR**: Not supported in web browsers
- **Precise GPS Accuracy**: Limited by browser restrictions
- **100% Stability**: Web-based applications may have performance variations

## 🔒 Data Privacy & Security

**Your data is safe - We emphasize the importance of data security:**

- ✅ All measurements and map data are stored **only in your browser**
- ✅ No data is sent to servers or external services
- ✅ GPS location data is used **only** for map generation
- ✅ Internet connection is used **only** for signal measurement (latency test)
- ✅ No tracking, analytics, or data collection
- ✅ User privacy and security are our priority
- ✅ Developed in compliance with data security standards and privacy policies

## 🇹🇷 National Technology

AtmacaPro is an **open-source project developed in Türkiye**. It contributes to the national technology ecosystem and supports local software development through community contributions.

## 🤝 Contributing

We welcome contributions! To contribute:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

### Support & Contact

- **GitHub**: [https://github.com/bootkitt/](https://github.com/bootkitt/)
- **Issues**: Report bugs or request features via GitHub Issues
- **Discussions**: Join discussions about the project

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

# Türkçe

**🔗 Bağlantılar:**
- **GitHub Repository:** [https://github.com/bootkitt/atmaca-pro](https://github.com/bootkitt/atmaca-pro)
- **Canlı Demo:** [index.html](index.html)

## 🎯 Genel Bakış

AtmacaPro, WiFi kapsama alanlarından kaynaklanan sorunları tespit edip çözmek için geliştirilmiş **web tabanlı bir araçtır**. Amacımız, sorunun kendisi değil çözümün kendisi olmaktır. GPS takibi ve ağ gecikme ölçümlerini kullanarak profesyonel WiFi analiz yetenekleri sunarak WiFi kapsama alanlarının görsel ısı haritalarını oluşturur.

### ⚠️ Önemli Uyarı

**AtmacaPro eğitim amaçlı tasarlanmıştır.** Web teknolojisi kısıtlamaları nedeniyle %100 stabil sonuçlar vermeyebilir. Profesyonel WiFi analizi için native mobil uygulamalar önerilir. Araç, veri güvenliği standartlarına ve gizlilik politikalarına uygun şekilde geliştirilmiştir.

## ✨ Özellikler

- **🔄 Otomatik Sinyal Ölçümü**: Hareket ederken WiFi sinyal gücünü otomatik olarak ölçer
- **🗺️ Anlık Isı Haritası**: Profesyonel WiFi analizi için Voronoi diyagram tabanlı ısı haritası görselleştirmesi
- **📍 GPS Takibi**: Doğru konum takibi için GPS koordinatları kullanır
- **📊 Sinyal Görselleştirme**: dBm cinsinden sinyal gücünü gösteren renk kodlu ısı haritası
- **💾 Dışa Aktarma**: Isı haritanızı yüksek çözünürlüklü PNG görüntüsü olarak kaydedin
- **📐 Kat Planı Desteği**: Daha iyi görselleştirme için kat planı görüntünüzü yükleyin
- **🎨 Modern Arayüz**: Beyaz/gri tasarımlı temiz, modern arayüz
- **📱 Responsive Tasarım**: Hem masaüstü hem mobil cihazlarda çalışır
- **🔒 Gizlilik Odaklı**: Tüm veriler tarayıcınızda kalır, sunuculara hiçbir şey gönderilmez

## 🚀 Nasıl Çalışır

1. **Kaydı Başlat**: WiFi sinyal ölçümüne başlamak için "Başlat" butonuna tıklayın
2. **Dolaşın**: Uygulama hareketinizi otomatik olarak takip ederken alanınızda dolaşın
3. **Otomatik Ölçüm**: Uygulama hareket temelinde düzenli aralıklarla WiFi sinyal gücünü ölçer
4. **Anlık Görselleştirme**: Voronoi üçgenleme kullanılarak gerçek zamanlı bir ısı haritası oluşturulur
5. **Dışa Aktar**: Tamamlanan ısı haritanızı görüntü olarak kaydedin

### Sinyal Ölçümü

Web tarayıcıları gerçek WiFi dBm değerlerini açığa çıkarmadığı için, AtmacaPro sinyal gücü için bir proxy olarak bilinen bir uç noktaya (Google'ın `generate_204`) ağ gecikmesini kullanır. Düşük gecikme genellikle daha güçlü WiFi sinyalleriyle ilişkilidir.

## 📖 Kullanım

### Temel Kullanım

1. Uygulamayı modern bir web tarayıcısında açın
2. İstenildiğinde konum izinlerini verin
3. Kayda başlamak için "Başlat"a tıklayın
4. Haritalamak istediğiniz alanda dolaşın
5. Bitirdiğinizde "Durdur"a tıklayın
6. Isı haritanızı kaydetmek için "İndir"e tıklayın

### Kat Planı Yükleme

1. Başlıktaki klasör simgesine (📁) tıklayın
2. Kat planı görüntünüzü yükleyin
3. Kat planı, ısı haritanız için arka plan olarak görüntülenecektir

### Klavye Kontrolleri (Masaüstü)

- **Ok Tuşları**: Konum göstergesini hareket ettirin (GPS olmadan test için)

## 🔧 Teknik Detaylar

### Proje Yapısı

```
AtmacaPro/
├── index.html          # Ana HTML dosyası
├── assets/
│   └── css/
│       └── style.css  # Tüm CSS stilleri
├── README.md          # Proje dokümantasyonu
└── LICENSE            # MIT Lisansı
```

### Kullanılan Teknolojiler

- **HTML5 Canvas**: Harita ve ısı haritası renderlaması için
- **D3-Delaunay**: Voronoi diyagram oluşturma için
- **Geolocation API**: GPS takibi için
- **Device Motion API**: Hareket algılama için
- **Performance API**: Gecikme ölçümü için

### Mimari

- **World Space & View Space**: Otomatik pan ve zoom ile sonsuz harita genişlemesine izin veren koordinat sistemi
- **Voronoi Üçgenleme**: Hücresel, sürekli ısı haritası görselleştirmesi oluşturur
- **Düşük Geçişli Filtreleme**: Stabil hareket takibi için sensör verilerini yumuşatır
- **Yeniden Ziyaret Algılama**: Daha önce haritalanmış alanları yeniden ziyaret edildiğinde sinyal verilerini günceller

### Renk Kodlaması

- **Cyan (-30 ile -50 dBm)**: Mükemmel sinyal
- **Yeşil (-50 ile -60 dBm)**: İyi sinyal
- **Açık Yeşil (-60 ile -70 dBm)**: Orta sinyal
- **Sarı (-70 ile -80 dBm)**: Zayıf sinyal
- **Turuncu (-80 ile -85 dBm)**: Çok zayıf sinyal
- **Kırmızı (< -85 dBm)**: Kötü sinyal

## ⚠️ Kısıtlamalar

Web tarayıcı kısıtlamaları nedeniyle, aşağıdaki özellikler **mevcut değildir**:

- **AR/Duvar Algılama**: Native uygulama geliştirme gerektirir
- **Gerçek WiFi API**: Web tarayıcıları gerçek WiFi dBm değerlerini açığa çıkarmaz (simülasyon kullanılır)
- **LiDAR**: Web tarayıcılarında desteklenmez
- **Kesin GPS Doğruluğu**: Tarayıcı kısıtlamaları nedeniyle sınırlıdır
- **%100 Stabilite**: Web tabanlı uygulamalar performans değişiklikleri gösterebilir

## 🔒 Veri Gizliliği ve Güvenlik

**Verileriniz güvende - Veri güvenliğinin önemini vurguluyoruz:**

- ✅ Tüm ölçümler ve harita verileri **yalnızca tarayıcınızda** saklanır
- ✅ Hiçbir veri sunuculara veya dış servislere gönderilmez
- ✅ GPS konum verileri **yalnızca** harita oluşturma için kullanılır
- ✅ İnternet bağlantısı **yalnızca** sinyal ölçümü (gecikme testi) için kullanılır
- ✅ Takip, analitik veya veri toplama yoktur
- ✅ Kullanıcı gizliliği ve güvenliği bizim için öncelikli
- ✅ Veri güvenliği standartlarına ve gizlilik politikalarına uygun geliştirilmiştir

## 🇹🇷 Milli Teknoloji

AtmacaPro, **Türkiye'de geliştirilen açık kaynak bir projedir**. Milli teknoloji ekosistemine katkı sağlar ve topluluk katkılarıyla yerli yazılım gelişimini destekler.

## 🤝 Katkıda Bulunma

Katkılarınızı bekliyoruz! Katkıda bulunmak için:

1. Depoyu fork edin
2. Bir özellik dalı oluşturun
3. Değişikliklerinizi yapın
4. Bir pull request gönderin

### Destek ve İletişim

- **GitHub**: [https://github.com/bootkitt/](https://github.com/bootkitt/)
- **Sorunlar**: GitHub Issues üzerinden hata bildirin veya özellik isteyin
- **Tartışmalar**: Proje hakkındaki tartışmalara katılın

## 📄 Lisans

Bu proje MIT Lisansı altında lisanslanmıştır - detaylar için LICENSE dosyasına bakın.

---

## 🙏 Acknowledgments

Special thanks to the open-source community and contributors who make projects like this possible.

## 📞 Contact

For questions, suggestions, or support, please visit our [GitHub repository](https://github.com/bootkitt/).

---

**Made with ❤️ in Türkiye 🇹🇷**

