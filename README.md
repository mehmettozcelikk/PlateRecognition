# 📎 Plaka Konumu Bulma (Plate Recognition)

Bu repo, **ISSD Bilişim Elektronik A.Ş.** stajım kapsamında geliştirdiğim **plaka konumu bulma** çalışmasını içerir. Projede; görüntü ön işleme, kenar tespiti, morfolojik işlemler, kontur analizi ve kural tabanlı filtreler kullanılarak plaka bölgesi tespit edilir.

## 📌 Yöntem Özeti
1. Görüntü okuma ve yeniden boyutlandırma
2. Griye çevirme
3. Gürültü azaltma (bilateral + median)
4. Otsu eşiğiyle **Canny** alt/üst eşiklerinin belirlenmesi
5. Kenar bulma (Canny)
6. Morfolojik kapama (close) ile gürültü temizliği
7. Kontur bulma
8. Aday dikdörtgenlerin **en-boy oranı**, **boyut**, **ortalama parlaklık** ve **standart sapma** kriterleri ile filtrelenmesi

> Not: En-boy oranı (2–6), minimum genişlik/yükseklik ve ROI mean/std gibi eşikler veri setine göre ayarlanabilir.

## 📦 Kurulum
```bash
git clone https://github.com/mehmettozcelikk/PlateRecognition.git
cd plate-recognition
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
