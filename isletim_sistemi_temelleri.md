# İşletim Sistemi Temelleri (OS Basics)

## 1. Kernel Nedir?
Kernel, işletim sisteminin çekirdeği olup donanım ile yazılım arasındaki köprü görevini üstlenir. 
- **Görevleri:** Bellek yönetimi, süreçlerin çalıştırılması, cihaz sürücülerinin kontrolü, dosya sistemine erişim.
- **Çeşitleri:**
  - **Monolitik Kernel:** Tüm temel işlevler tek bir büyük çekirdek içinde bulunur.
  - **Mikro Kernel:** Çekirdek minimum işlevleri üstlenir, diğer servisler kullanıcı alanında çalışır.
- **Önemi:** Kernel olmadan yazılım donanımla iletişim kuramaz. Yazılımın “nerede çalıştığını” anlamak için kernel kavramı kritik bir başlangıçtır.

---

## 2. Süreç (Process) ve İş Parçacığı (Thread) Farkı
- **Process (Süreç):**
  - Çalışan bir programın bellekteki bağımsız örneği.
  - Kendi adres alanı, dosya tanıtıcıları ve kaynakları vardır.
  - Bir süreç çökerse diğer süreçler etkilenmez.
- **Thread (İş Parçacığı):**
  - Bir sürecin içindeki daha küçük yürütme birimi.
  - Aynı sürecin belleğini ve kaynaklarını paylaşır.
  - Daha hafif, daha hızlı ve paralel çalışmayı kolaylaştırır.
- **Fark:**
  - Process bağımsızdır, thread ise süreç içinde paralel çalışmayı sağlar.
  - Çok çekirdekli CPU’larda thread kullanımı performansı artırır.

---

## 3. Bellek Yönetimi
Bellek yönetimi, işletim sisteminin RAM’i verimli kullanmasını sağlar.
- **Bellek Tahsisi (Allocation):** Programlara ihtiyaç duydukları kadar bellek ayrılır.
- **Sanal Bellek (Virtual Memory):** Fiziksel RAM yetersiz kaldığında disk alanı RAM gibi kullanılır.
- **Sayfalama (Paging):** Bellek sabit boyutlu bloklara (sayfa) bölünür, süreçler bu sayfaları kullanır.
- **Segmentasyon:** Bellek mantıksal bölümlere ayrılır (kod, veri, yığın).
- **Koruma:** Programların birbirinin alanına müdahale etmesini engeller.
- **Örnek:** Bir tarayıcı ve bir oyun aynı anda çalışırken birbirinin belleğini bozamaz.

---

## 4. CPU Zamanlayıcıları
CPU zamanlayıcıları, hangi sürecin ne zaman çalışacağını belirleyen algoritmalardır.
- **Round Robin:** Her sürece sırayla zaman dilimi verilir.
- **Priority Scheduling:** Önceliği yüksek olan süreç önce çalışır.
- **Shortest Job First:** En kısa işi önce çalıştırır.
- **Multilevel Queue:** Süreçler farklı kuyruklara ayrılır (ör. etkileşimli vs. arka plan).
- **Amaç:** CPU kullanımını adil, verimli ve kullanıcı deneyimini kesintisiz hale getirmek.

---

## 5. Öğrenilenler
Bu bölümde işletim sistemi temellerinden elde edilen kazanımlar özetlenmiştir:

- Yazılımın donanım üzerinde **nerede ve nasıl çalıştığı** artık net bir şekilde öğrenildi.
- Sadece kod yazmakla kalmayıp, sistemin mantığını kavrama becerisi kazanıldı.
- Optimizasyon, hata ayıklama ve performans artırma konularında daha bilinçli hareket etme yetkinliği edinildi.
- Kernel, süreç, iş parçacığı, bellek yönetimi ve CPU zamanlayıcıları arasındaki ilişkiler kavranarak bütünsel bir bakış açısı geliştirildi.
