# Güneş Paneli Yerleşimi Optimizasyonu (Genetik Algoritma)

Bir belediye güneş enerjisi kurulumu senaryosunda enerji verimini maksimize eden optimum **eğim açısı ($x_1$)** ve **yön açısı ($x_2$)** değerlerini Genetik Algoritma (GA) ile belirleyen optimizasyon çalışması.

## Matematiksel Model

**Amaç Fonksiyonu (Maksimizasyon):**

$$y = 6x_1 + 4x_2 - 0.1x_1^2$$

**Değişken Sınırları:**
- **Eğim açısı ($x_1$):** $[10^\circ, 45^\circ]$
- **Yön açısı ($x_2$):** $[15^\circ, 90^\circ]$

**Kısıtlar ve Ceza Yöntemi:**
- Fiziksel kurulum kısıtı: $x_1 + 0.5x_2 \le 60$
- `geneticalgorithm` paketi minimizasyon yaptığı için amaç fonksiyonu $-y$ olarak tanımlanmıştır; sınırı aşan aday çözümlere sabit ceza (`10000`) uygulanır.

## Algoritma Parametreleri ve Örnek Çıktı

Notebook'taki `100` iterasyon, `50` popülasyon boyutu, `0.1` mutasyon ve `0.5` uniform çaprazlama parametreleriyle elde edilen kayıtlı çalıştırma sonucu:

| Metrik | Değer |
| :--- | :--- |
| **Optimum Eğim ($x_1$)** | `15.3142°` |
| **Optimum Yön ($x_2$)** | `89.3302°` |
| **Maksimum Enerji ($y$)** | `425.7533 birim` |
| **Kısıt Kontrolü ($x_1 + 0.5x_2 \le 60$)** | `59.9792` (Sağlanıyor) |

## Kurulum ve Çalıştırma

```bash
git clone https://github.com/yyigituncu/gunes-paneli-optimizasyonu.git
cd gunes-paneli-optimizasyonu
pip install -r requirements.txt
jupyter notebook gunes-paneli-optimizasyonu.ipynb
```

## Lisans

Bu proje [MIT Lisansı](LICENSE) ile lisanslanmıştır.
