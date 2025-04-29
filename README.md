# Sosyal Ağ Analizi (C ile Red-Black Tree & DFS)

Bu proje, sosyal ağ üzerindeki kullanıcı ilişkilerini **Red-Black Tree (Kırmızı-Siyah Ağaç)** yapısı ile düzenleyerek kullanıcı kimliklerini dengeli bir yapıda saklar. Ayrıca arkadaşlık ilişkileri graf yapısı şeklinde modellenmiş ve bu yapı üzerinden çeşitli analizler yapılmıştır.

##  Özellikler

- Kullanıcılar Red-Black Tree ile kimlik bazlı sıralı ve dengeli yapıda saklanır.
- Arkadaşlık ilişkileri dizi ve bağlantılarla temsil edilmiştir.
- Aşağıdaki analizler desteklenmektedir:
  - Depth-First Search (DFS) ile belirli derinlikteki arkadaşları bulma
  - Ortak arkadaş analizi
  - Kullanıcının etki alanı (kaç kişiye ulaşabildiği)
  - Topluluk tespiti (bağlı alt ağlar)
- `veriseti.txt` adlı dosyaya kullanıcılar ve ilişkiler kaydedilir.

## 📄 Örnek Giriş

```txt
Kac kullanici eklemek istersiniz? 5
Kullanici ID girin: 101
Kullanici ID girin: 102
Kullanici ID girin: 103
Kullanici ID girin: 104
Kullanici ID girin: 105

Kac arkadaslik iliskisi tanimlanacak? 5
Arkadaslik (id1 id2): 101 102
Arkadaslik (id1 id2): 101 103
Arkadaslik (id1 id2): 102 104
Arkadaslik (id1 id2): 103 104
Arkadaslik (id1 id2): 104 105
```
##Çıktı Örnekleri
```
Kullanici 101 derinlik 0
Kullanici 102 derinlik 1
Kullanici 104 derinlik 2
Kullanici 103 derinlik 1


Ortak Arkadaslar: 104


Toplam Etki Alani: 5 kullanıcı
```

#Veriseti.txt Dosyası

Girilen kullanıcı idleri ve arkadaşlık ilişkileri veriseti.txt dosyasına kaydedilir.Örnek kayıt şekli;
```
#Kullanicilar
KULLANICI 101
KULLANICI 102
KULLANICI 103
KULLANICI 104
KULLANICI 105

#Arkadaşlık Ilişkileri
Arkadas 101 102
Arkadas 101 103
Arkadas 102 104
Arkadas 103 104
Arkadas 104 105
```
#Derleme
gcc sosyal_ag.c -o sosyal_ag
./sosyal_ag
#Notlar
MAX_KULLANICI sabiti 100 olarak tanımlanmıştır, dilerseniz artırabilirsiniz.

Kırmızı-Siyah Ağaç yapısı, kullanıcı aramalarının log(n) sürede gerçekleşmesini sağlar.

DFS derinliği dfs() fonksiyonunda parametre olarak tanımlıdır.
