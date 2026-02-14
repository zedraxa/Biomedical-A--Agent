Kullanmış olduğum işletim sisteminde(parrotOS) localde openclaw kullanmamın zahmetli olması, autogpt'nin de api'a olan bağlılığı sebebiyle tatilde başladığım ihtiyaca yönelik AI agent projesi. (henüz başarıya ulaşmadı)
Ollama ile localde bulunan bir model kullanarak çalışıyor.
Ben qwen2.5:7b-instruct kullanıyorum
direkt klasör halinde google drive linkinden indrilip kurulabilir
https://drive.google.com/drive/folders/1KiGFjYKPrYTkNX68Vb8W07MAqU8X_xOm?usp=drive_link

Kullanım 
cd ~/ai-agent
source venv/bin/activate
python agent.py
kodlarını terminale girdikten sonra agentın açılmasını bekleyin 
daha sonrasında talebinizi girin,eğer talebiniz web araması içeriyorsa talebinize ALLOW_WEB_SEARCH komutunu ekleyin
terminale exit yazarak çıkılabilir

Örnek Senaryo:
 çalıştırmak için:
  cd ~/ai-agent
  source venv/bin/activate
  python agent.py --model qwen2.5:7b-instruct

 prompt:
  PROJECT: wine_quality ALLOW_WEB_SEARCH | UCI Wine Quality datasetini bul; indirilebilir CSV linkini çıkar ve data/raw/ içine indir; src/train.py yaz: pandas+sklearn ile baseline model eğit, accuracy ve ROC-AUC hesapla; results/metrics.json ve report.md üret; sonra training scriptini çalıştır.
