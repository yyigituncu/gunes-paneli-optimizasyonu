# gunes-paneli-optimizasyonu# Güneş Paneli Yerleşimi Optimizasyonu (Genetik Algoritma)

Bu proje, bir belediyenin güneş enerjisi sistemi kurulumunda enerji verimini maksimize etmek amacıyla geliştirilmiştir. Panellerin optimum **eğim açısı ($x_1$)** ve **yön açısı ($x_2$)**, Genetik Algoritma (GA) kullanılarak belirlenmiştir.

## 📋 Proje Bilgileri
* **Öğrenci:** Sami Yiğit Uncu
* **Okul No:** 2212721051
* **Senaryo:** 1 (Güneş Paneli Optimizasyonu)

## 🎯 Problem Tanımı ve Matematiksel Model
Amaç, panellerden alınan toplam enerji verimini maksimize etmektir.

**Amaç Fonksiyonu:**
$$y = 6x_1 + 4x_2 - 0.1x_1^2$$

**Değişken Sınırları:**
* **Eğim ($x_1$):** 10° - 45°
* **Yön ($x_2$):** 15° - 90° *(Kısıt gereği alt sınır 15 alınmıştır)*

**Kısıtlar (Constraints):**
Projede **Ceza (Penalty) Yöntemi** kullanılmıştır.
1.  `x1 + 0.5x2 <= 60` (Fiziksel Kurulum Sınırı)
2.  Bu sınır aşılırsa algoritmaya yüksek ceza puanı verilerek çözüm elenir.

## ⚙️ Kurulum ve Çalıştırma
Proje Python dilinde, Jupyter Notebook üzerinde geliştirilmiştir. Çalıştırmak için aşağıdaki kütüphaneler gereklidir:

```bash
pip install geneticalgorithm matplotlib numpy
