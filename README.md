# 🌔 Ay'ın Evreleri ve Kavram Yanılgıları Simülatörü

> **MEB 5. Sınıf Fen Bilimleri Müfredatına Uygun • Etkileşimli 2D Canvas Web Simülatörü**

Bu proje, 5. sınıf öğrencilerinin en yaygın kavram yanılgılarından biri olan **"Ay'ın evrelerinin Dünya'nın gölgesinden kaynaklandığı"** düşüncesini görsel ve deneysel olarak çürütmek amacıyla geliştirilmiş interaktif bir eğitim yazılımıdır.

[![GitHub Pages](https://img.shields.io/badge/Demo-Canlı%20İzle-38bdf8?style=for-the-badge&logo=github)](https://soveyik.github.io/ayin-evreleri-simulatoru/)
[![Vanilla JS](https://img.shields.io/badge/Vanilla-HTML5%20%2F%20Canvas%202D-facc15?style=for-the-badge&logo=javascript)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![MEB Uyumlu](https://img.shields.io/badge/MEB-5.%20Sınıf%20Fen-10b981?style=for-the-badge)](https://www.meb.gov.tr)

---

## 🎯 Pedagojik Hedef ve Temel Mantık

### ❌ Kavram Yanılgısı
Öğrenciler genellikle Ay'ın evrelerinin Dünya'nın gölgesinden kaynaklandığını düşünür (Ay evreleri ile Ay tutulmasını karıştırırlar).

### ✅ Bilimsel Gerçek & Kırılma Mekaniği
1. **Uzaydan Görünüm (Panel A):** Güneş ışığı sağdan paralel geldiği için Ay yörüngesinde nerede olursa olsun **Güneş'e bakan sağ yarısı her zaman %100 aydınlıktır.**
2. **Dünya'dan Görünüm (Panel B):** Evrelerin değişmesinin tek nedeni, Dünya'daki gözlemcinin bu aydınlık yüzün ne kadarını gördüğüdür (Trigonometrik faz formülü: $k = \frac{1 - \cos\theta}{2}$).
3. **Dünya'nın Gölgesi Butonu:** Dünya'nın arkasında uzanan gerçek gölge konisi (umbra/penumbra) açıldığında öğrenci; Ay'ın yalnızca Dolunay ($\theta = 180^\circ$) anında gölge hizasına gelebileceğini, Hilal veya İlk Dördün gibi evrelerde gölgenin Ay ile **hiçbir temasının olmadığını** bizzat görür.

---

## ✨ Özellikler

- 🪐 **Panel A (Uzaydan Kuşbakışı):**
  - Sağdan gelen paralel Güneş ışınları.
  - Merkezde mavi-yeşil Dünya (sağ yarısı gündüz, sol yarısı gece ve şehir ışıkları).
  - Ay'ın dairesel yörüngesi ve dönüş yönü göstergeleri.
  - Yörüngede hareket eden Ay (sağ yarısı daima beyaz, sol yarısı daima koyu).
  - Dünya'dan Ay'a uzanan dinamik görüş vektörü.
  - **Sürükle-Bırak (Drag & Drop):** Ay doğrudan fare veya parmakla tutulup yörüngede gezdirilebilir.
  - **Dünya'nın Gölge Konisi (Toggle):** Kırmızı yarı saydam umbra/penumbra alanı ve anlık tutulma analizi.

- 🔭 **Panel B (Dünya'dan Görünüm - Gece Gökyüzü Teleskobu):**
  - Dairesel teleskop vizörü ve nişangah göstergeleri.
  - Pürüzsüz matematiksel faz eğrileri (hilal, ilk dördün, şişkin ay, dolunay, yeni ay).
  - Gerçekçi Ay dokusu (kraterler, Ay denizleri - Maria, Tycho ışınları).
  - **Kütleçekim Kilidi (Tidal Locking):** Ay'ın Dünya'ya daima aynı yüzünün bakması simüle edilmiştir.
  - Canlı evre ismi, ana/ara evre rozeti ve aydınlanma yüzdesi.

- 🎛️ **Kontrol Paneli:**
  - $0^\circ - 360^\circ$ hassas yörünge açısı slider'ı.
  - **8 Hızlı Evre Butonu:** Yeni Ay ($0^\circ$), Hilal ($45^\circ$), İlk Dördün ($90^\circ$ - "D" harfi), Şişkin Ay ($135^\circ$), Dolunay ($180^\circ$), Şişkin Ay ($225^\circ$), Son Dördün ($270^\circ$ - "Ters D" harfi), Hilal ($315^\circ$ - "C" harfi).
  - **Otomatik Yörünge Oynatıcı:** 60 FPS akıcı orbital animasyon.
  - **Ses Efektleri:** Web Audio API ile harici dosya gerektirmeyen uzaysal sesli geri bildirimler.

- 🎯 **5. Sınıf Keşif Görevleri (Mini Quiz):**
  - "D" harfi kuralı, hilal yakalama ve kavram yanılgısı deney görevleri.

---

## 🚀 Canlı Demo & GitHub Pages Kurulumu

Projeyi doğrudan tarayıcınızda çalıştırmak için:
1. Bu depoyu GitHub'da açın.
2. **Settings (Ayarlar) > Pages** sekmesine gidin.
3. **Branch** kısmından `main` veya `master` seçip **Save** butonuna tıklayın.
4. Birkaç dakika içinde aşağıdaki bağlantıda canlıya alınacaktır:
   👉 **`https://soveyik.github.io/ayin-evreleri-simulatoru/`**

---

## 💻 Yerel Olarak Çalıştırma

Hiçbir kurulum veya paket yöneticisi (npm vb.) gerekmez. Saf HTML5'tir:

```bash
# 1. Depoyu klonlayın
git clone https://github.com/soveyik/ayin-evreleri-simulatoru.git

# 2. Klasöre girin
cd ayin-evreleri-simulatoru

# 3. index.html dosyasını herhangi bir tarayıcıda açın
# (Windows)
start index.html
```

---

## 📐 Matematiksel Model

- **Faz Açısı:** $\theta \in [0, 2\pi]$
- **Aydınlanma Oranı:** $k = \frac{1 - \cos\theta}{2}$
- **Terminatör Elips Yarıçapı:** $r_x = R \cdot |\cos\theta|$
- $\theta \in [0, \pi]$: Büyüyen evreler (Sağ taraf aydınlık - İlk Dördün = "D" harfi).
- $\theta \in [\pi, 2\pi]$: Küçülen evreler (Sol taraf aydınlık - Son Dördün = Ters "D" harfi).

---

## 📜 Lisans

Bu proje [MIT Lisansı](LICENSE) kapsamında açık kaynak olarak sunulmuştur. Eğitim amaçlı serbestçe kullanılabilir ve geliştirilebilir.
