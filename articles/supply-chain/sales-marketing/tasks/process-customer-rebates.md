--- 
title: "Müşteri indirimlerini oluşturma ve işleme"
description: "Bu prosedür, müşteri indirimlerinin talep oluşturulmasından, alacak hesaplarına tahakkuk edilmesi noktasına kadar nasıl işleneceğini göstermektedir."
author: omulvad
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 348793abc6d219f38bcdc2629b77343d93927005
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="generate-and-process-customer-rebates"></a>Müşteri indirimlerini oluşturma ve işleme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu prosedür, müşteri indirimlerinin talep oluşturulmasından, alacak hesaplarına tahakkuk edilmesi noktasına kadar nasıl işleneceğini göstermektedir. Belirli bir örnek üzerinden, indirim satırlarındaki çeşitli şartların müşteriye alacak olarak kaydedilecek son tutarları nasıl etkilediğini adım adım gösterecektir. USMF demo verileri şirketini kullanmalısınız ve Rehber başlamadan önce aşağıdaki görevleri gerçekleştirmiş olmanız gerekir: (1) Alacak hesapları parametreleri sayfasına gidin ve Fiyatlar öğesi ve sonra Fiyat yyrıntılar öğesini açın ve Fiyat ayrıntılarını etkinleştir seçeneğinin Evet olarak ayarlanmış olduğundan emin olun. (2) İndirim anlaşmaları sayfasına gidin ve müşteri indirim anlaşması USMF-000001'i seçin. Eğer İş akışı onay durumu alanı Onaylandı olarak ayarlanmamışsa, onaylamak için Eylem Bölmesinde Doğrulama seçeneğine tıklamanız gereklidir.


## <a name="review-a-customer-rebate-agreement"></a>Müşteri indirim sözleşmesini gözden geçirin
1. Sales and marketing > Customer rebates > Rebate agreements (Satış ve pazarlama > Müşteri indirimleri > İndirim anlaşmaları) menüsüne gidin.
    * Sonraki birkaç adım, USMF-000001 anlaşmasının koşullarına göz atacaktır. Bu daha sonra prosedürde, müşteri kredi değerinin nasıl hesaplandığını anlamayı kolaylaştıracaktır.  
    * Anlaşma bu örnekte US-009 olan tek bir müşteri içindir.  
    * İndirimler müşteriye belirli bir ürün aldıklarında verilir. Bu durumda, söz konusu bu ürünün madde numarası T0020'dir.   
    * İndirim miktarının tahmin edilmesinde müşterinin satış performansı karşılık alınır ve haftalık olarak toplanır.  
    * "Fiyatın alındığı yer" ayarı brüttür, bu da satırın satış miktarının talebin indirim satırından faydalanmıyor olduğu anlamına gelir.  
    * İndirim satır kırılma türü alanı indirimlerin hesaplanma yöntemini gösterir. Bu durumda, indirimlerin tahmin edileceği satış hedefi Miktar olarak ayarlanır.   
    * Anlaşmanın satırları indirim tutarı türünü, gerçek indirim değerini ve eşikleri belirtir. Bu örnekte müşteri, haftalık satın almaları 1 ila 50 ürün arasında kalırsa, satılan ürün başına 20 ABD doları tutarında ve eğer satın almaları 50 birim ürünün üzerinde olursa, 40 ABD doları tutarında bir indirime hak kazanır.  
2. Sayfayı kapatın.

## <a name="generate-rebate-claims"></a>İndirim talepleri oluşturun
1. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
2. Yeni'ye tıklayın.
    * İndirim talepleri gerçekleşen durumu taklit etmek için bir sonraki görevde, söz konusu müşterinin indirime hak kazanacağı miktar ve ürünün bulunduğu bir satış emri oluşturulacak.  
3. Müşteri hesabı alanında bir değer girin veya seçin.
4. Tamam'a tıklayın.
5. Madde numarası alanında bir değer girin veya seçin.
6. Miktarı '40' olarak ayarlayın.
7. Satış siparişi satırına tıklayın.
8. Fiyat ayrıntıları'na tıklayın.
    * Bu seçeneği görmüyorsanız, kılavuzu başlatmadan önce Fiyat ayrıntıları etkinleştir seçeneğini Evet olarak ayarlamadığınız içindir.  
9. İndirimler bölümünü genişletin.
    * İndirimler sekmesi mevcut sipariş hattı için geçerli tüm indirim sözleşmelerini listeler ve tahmini indirim tutarını gösterir. Görüntülenen tutarların, sadece gelecekte hangi indirim talep edilebileceğinin göstergeleri olduğunu unutmayın. Gerçek indirim tutarları şunlara bağlı olarak farklı olabilir: müşteri tarafından bir dönemsel indirim anlaşması kapsamında elde edilen toplam satış hacmi, müşterinin tümünü mü yoksa kısmi miktarları mı iade ettiği; ve uygulanabilir satış siparişinin faturalanmış olup olmadığı.  
10. Sayfayı kapatın.
11. Satır ekle'ye tıklayın.
12. Madde numarası alanında bir değer girin veya seçin.
13. Miktarı '60' olarak ayarlayın.
14. Kaydet'e tıklayın.
15. Eylem Bölmesinde, Fatura öğesine tıklayın.
16. Fatura'ya tıklayın.
17. Parametreler bölümünü genişletin.
18. Miktar alanında, 'Tümü' öğesini seçin.
19. Tamam'a tıklayın.
20. Tamam'a tıklayın.

## <a name="process-rebate-claims"></a>İndirim taleplerini işleyin
1. Sales and marketing > Customer rebates > Rebates (Satış ve pazarlama > Müşteri indirimleri > İndirimler) menüsüne gidin.
    * İndirimler sayfası, indirim taleplerini incelemek, onaylamak ve işlemek için bir çalışma ortamı işlevini yerine getirir. Şimdi indirim anlaşması USMF-000001'e konu olan US-009 müşterisi için bir satış siparişi faturalamasının sonucu olarak oluşturulan talepleri işleyeceksiniz.   
    * İlk satır 800 ABD doları olarak hesaplanan bir indirim talebini temsil etmektedir. Bu da T0020 ürününden 40 birimlik satışa dayanmaktadır ve birim başına 20 ABD doları olarak hesaplanır. Bu, indirim anlaşmasındaki ilk miktar kırılma koşullarıyla eşleşmektedir.  
    * İkinci talep 2.400 ABD doları içindir, 60 birim T0020 ürününe dayanır, anlaşmadaki ikinci miktar kırılması uyarınca 40 ABD doları birim fiyatından hesaplanmıştır.  
    * Her iki talep de "Hesaplanacak" durumdadır. Bu da, periyodik olarak müşterinin satış performansını periyodik olarak izleyen bir anlaşma ile ilişkili olduğunu ve bunlarla ilgili dönem içindeki toplam satış hacminin yeniden hesaplanacak olmak zorunda olduğu anlamına gelir.   
2. Biriktir'e tıklayın.
3. Müşteri alanına bir değer girin veya buradan bir değer seçin.
4. Başlangıç tarihi alanında, bugünün tarihini seçin.
5. Tamam'a tıklayın.
    * Biriktirme işlevinin çalıştırılması sonucunda, tahmini talep tutarı şimdi müşterinin ilgili dönemde toplam satış hacminin, indirimin ilk oluşturulduğu zaman göre daha yüksek olduğu gerçeğini göre ayarlanır. Daha detaya girmek gerekirse, satılan toplam miktar 100 birime ulaştığı için, müşteri artık ürün başına 40 ABD doları (anlaşmanın ikinci miktar kırılması uyarınca) veya toplam 400 ABD doları toplam indirim miktarına hak kazanmıştır. Fark ek 800 USD için bir yeni talep için "ayarlama" olarak kaydedilir. Biriktirme güncelleştirmesinde dahil edilen indirim talebinin durumu şimdi Hesaplandı olarak ayarlanmıştır.   
6. Listede, tüm satırları işaretleyin.
7. Onayla’yı tıklatın.
8. İşlemi'ı tıklatın.
9. Müşteri alanına bir değer girin veya buradan bir değer seçin.
10. Tamam'a tıklayın.
    * İndirimin başarıyla işlendiğine dair bir mesaj gösterilir ve talebin durumu İşaretlendi olarak değişir. Bu, İndirim tahakkuku günlüğünün nakledilmiş olmasının sonucunda a) talepler geçici müşteri bakiyesine kesinti olarak yansıtılmıştır b) İndirim tahakkuk hesabı müşterinin için gelecekteki pasifi temsil edecek şekilde alacaklandırılmıştır; ve c) İndirim gider hesabı, satışlardan doğacak borçlar göz önünde tutularak borçlandırılmıştır.   


