Görev 2. Ürün Teslimatı



task-2.js dosyasında bu görevi yerine getirin. getShippingMessage adında bir fonksiyon tanımlayın. Bu fonksiyon, çağrılırken aşağıdaki değerlere sahip olan üç parametreyi almalidir.

country - Birinci parametre teslimatın yapılacağı ülkeyi içeren bir string olmali
price - Ikinci parametre toplam ürün maliyetini içeren bir number olmali
deliveryFee - Üçüncü parametre ürün teslimat maliyetini içeren bir number olmali


Fonksiyonun kodunu, kullanıcının ülkesine ürün teslimatı hakkında bir mesaj içeren bir string döndürecek şekilde tamamlayın: "Shipping to <country> will cost <totalPrice> credits", burada:

<country> - Teslimat ülkesidir
<totalPrice> - Ürün ve teslimat maliyetini içeren toplam sipariş maliyetidir


Aşağıdaki kodu al ve fonksiyonunu tamamladiktan sonra doğruluğunu kontrol etmek için altina yapıştır. Konsola fonksiyonun çıktıları yazdırılacaktır.



console.log(getShippingMessage("Australia", 120, 50)); // "Shipping to Australia will cost 170 credits"
console.log(getShippingMessage("Germany", 80, 20)); // "Shipping to Germany will cost 100 credits"
console.log(getShippingMessage("Sweden", 100, 20)); // "Shipping to Sweden will cost 120 credits"



Bu kodu mentor tarafından kontrol edilmesi için bırak.

Kontrol sırasında mentorun dikkat edeceği noktalar:

getShippingMessage(country, price, deliveryFee) adında bir fonksiyon tanımlanmıştir.
getShippingMessage("Australia", 120, 50) çağrısı "Shipping to Australia will cost 170 credits" yanıtını döndürür.
getShippingMessage("Germany", 80, 20) çağrısı "Shipping to Germany will cost 100 credits" yanıtını döndürür.
getShippingMessage("Sweden", 100, 20) çağrısı "Shipping to Sweden will cost 120 credits" yanıtını döndürür.
Herhangi geçerli argümanlarla getShippingMessage çağrısı doğru değeri döndürür.


Görev 3. Öğe Genişliği

task-3.js dosyasında bu görevi yerine getirin.

Çağrıldığında üç parametre bekleyen getElementWidth adında bir fonksiyon tanımlayın:

content— İçerik genişliği olan ilk parametre
padding — Her bir kenar için dolgu değeri olan ikinci parametre
border — Her bir kenar için border kalınlığı değeri olan üçüncü parametre
Tüm parametrelerin değerleri Npx biçiminde olacak, burada N herhangi bir tam veya ondalık sayıdır.



Fonksiyonun öğenin toplam genişliğini döndürmelidir. Toplam genişliği hesaplarken, box-sizing değerinin border-box olduğunu varsay.



Aşağıdaki kodu al ve fonksiyonunu tamamladiktan sonra doğruluğunu kontrol etmek için altina yapıştır. Konsola fonksiyonun çıktıları yazdırılacaktır.



console.log(getElementWidth("50px", "8px", "4px")); // 74
console.log(getElementWidth("60px", "12px", "8.5px")); // 101
console.log(getElementWidth("200px", "0px", "0px")); // 200



Bu kodu mentor tarafından kontrol edilmesi için bırak.



Kontrol sırasında mentorun dikkat edeceği noktalar:

getElementWidth(content, padding, border) adlı fonksiyon tanımlanmıştır.
getElementWidth("50px", "8px", "4px") çağrısı 74 sayısını döndürür.
getElementWidth("60px", "12px", "8.5px") çağrısı 101 sayısını döndürür.
getElementWidth("200px", "0px", "0px") çağrısı 200 sayısını döndürür.
Herhangi geçerli argümanlarla yapılan getElementWidth çağrısı doğru değeri döndürür.

Ödev ipuçları

Genel amaç
Bu ödevde, fonksiyon yazma, string mesaj formatlama, number hesaplama, px string → number dönüşümü pratik ediyorsun.
Proje/Teslim standardı
Repo: goit-js-hw-01
Dosya/klasör yapısı şemaya birebir uyacak (aksi halde kabul yok).
Prettier format, canlı sayfada console hata/uyarı yok.
Teslim: 2 link → GitHub repo + GitHub Pages canlı sayfa.

— Droid siparişi (task-1.js)
Amaç: makeTransaction(quantity, pricePerDroid) fonksiyonu yazıp toplam fiyatı hesaplayarak mesaj üretmek.
Ne yapacaksın?
2 parametre al:
quantity (number)
pricePerDroid (number)
totalPrice = quantity * pricePerDroid
Template literal ile şu formatta string döndür:
You ordered <quantity> droids worth <totalPrice> credits!
Dikkat
Çıktı tırnak, boşluk, ünlem dahil birebir aynı olmalı.
return string olmalı, console.log sadece test kodu.
Mentor checklist
Fonksiyon adı doğru: makeTransaction
Doğru hesap: 5×3000=15000 vb.
Test console.log satırları duruyor.
Sık hata
totalPrice’ı string birleştirme ile yanlış üretmek
Template literal yerine yanlış concat/boşluk hatası

— Ürün teslimatı (task-2.js)
Amaç: Ürün + kargo ücretini toplayıp ülkeye göre mesaj üretmek.
Ne yapacaksın?
Fonksiyon: getShippingMessage(country, price, deliveryFee)
totalPrice = price + deliveryFee
Döndür: Shipping to <country> will cost <totalPrice> credits
Dikkat
country string olarak yazıldığı gibi mesajda görünmeli.
totalPrice sadece toplam sayı.
Mentor checklist
Fonksiyon adı/doğru parametreler
Test çağrılarında birebir çıktı
Sık hata
price ile deliveryFee’yi string gibi toplamak (ör. "120" + "50" = "12050")

— Öğe genişliği (task-3.js)
Amaç: "Npx" formatındaki stringlerden sayıları alıp toplam genişliği bulmak (border-box varsayımı).
Ne yapacaksın?
Fonksiyon: getElementWidth(content, padding, border)
Parametreler "50px", "8.5px" gibi gelir.
parseFloat ile sayı kısmını al.
border-box total width = content + 2*padding + 2*border
Dikkat
parseFloat burada kritik çünkü 8.5px var.
Number.parseInt kullanırsan 8.5 → 8 olur, sonuç bozulur.
Mentor checklist
Çıktılar: 74, 101, 200
Sık hata
padding/border’ı tek taraf sanmak (2 ile çarpmayı unutmak)
