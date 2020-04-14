---
title: Müşteri indirimlerini oluşturma ve işleme
description: Bu prosedür, müşteri indirimlerinin talep oluşturulmasından, alacak hesaplarına tahakkuk edilmesi noktasına kadar nasıl işleneceğini göstermektedir.
author: omulvad
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PdsRebateAgreement, SalesTableListPage, SalesCreateOrder, SalesTable, MCRPriceHistory, SalesEditLines,  PdsRebateTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73bc22949d0b19fa04bf27e6fd7df7b27832795b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148596"
---
# <a name="generate-and-process-customer-rebates"></a>Müşteri indirimlerini oluşturma ve işleme

[!include [banner](../../includes/banner.md)]

Bu prosedür, müşteri indirimlerinin talep oluşturulmasından, alacak hesaplarına tahakkuk edilmesi noktasına kadar nasıl işleneceğini göstermektedir. Belirli bir örnek üzerinden, indirim satırlarındaki çeşitli şartların müşteriye alacak olarak kaydedilecek son tutarları nasıl etkilediğini adım adım gösterecektir. USMF demo verileri şirketini kullanmalısınız ve Rehber başlamadan önce aşağıdaki görevleri gerçekleştirmiş olmanız gerekir: (1) Alacak hesapları parametreleri sayfasına gidin ve Fiyatlar öğesi ve sonra Fiyat yyrıntılar öğesini açın ve Fiyat ayrıntılarını etkinleştir seçeneğinin Evet olarak ayarlanmış olduğundan emin olun. (2) İndirim anlaşmaları sayfasına gidin ve müşteri indirim anlaşması USMF-000001'i seçin. Eğer İş akışı onay durumu alanı Onaylandı olarak ayarlanmamışsa, onaylamak için Eylem Bölmesinde Doğrulama seçeneğine tıklamanız gereklidir.


## <a name="review-a-customer-rebate-agreement"></a>Müşteri indirim sözleşmesini gözden geçirin
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Müşteri indirimleri > İndirim sözleşmeleri**'ne gidin.
    - Sonraki birkaç adım, USMF-000001 anlaşmasının koşullarına göz atacaktır. Bu daha sonra prosedürde, müşteri kredi değerinin nasıl hesaplandığını anlamayı kolaylaştıracaktır.  
    - Anlaşma bu örnekte US-009 olan tek bir müşteri içindir.  
    - İndirimler müşteriye belirli bir ürün aldıklarında verilir. Bu durumda, söz konusu bu ürünün madde numarası T0020'dir.   
    - İndirim miktarının tahmin edilmesinde müşterinin satış performansı karşılık alınır ve haftalık olarak toplanır.  
    - "Fiyatın alındığı yer" ayarı brüttür, bu da satırın satış miktarının talebin indirim satırından faydalanmıyor olduğu anlamına gelir.  
    - İndirim satır kırılma türü alanı indirimlerin hesaplanma yöntemini gösterir. Bu durumda, indirimlerin tahmin edileceği satış hedefi Miktar olarak ayarlanır.   
    - Anlaşmanın satırları indirim tutarı türünü, gerçek indirim değerini ve eşikleri belirtir. Bu örnekte müşteri, haftalık satın almaları 1 ila 50 ürün arasında kalırsa, satılan ürün başına 20 ABD doları tutarında ve eğer satın almaları 50 birim ürünün üzerinde olursa, 40 ABD doları tutarında bir indirime hak kazanır.  
2. Sayfayı kapatın.

## <a name="generate-rebate-claims"></a>İndirim talepleri oluşturun
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Satış siperişler > Tüm satış siparişleri**'ne gidin.
2. **Yeni**'ye tıklayın. İndirim talepleri gerçekleşen durumu taklit etmek için bir sonraki görevde, söz konusu müşterinin indirime hak kazanacağı miktar ve ürünün bulunduğu bir satış emri oluşturulacak.    
3. **Müşteri hesabı** alanında bir değer girin veya seçin.
4. **Tamam**'a tıklayın.
5. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
6. **Miktar**'ı '40' olarak ayarlayın.
7. **Satış siparişi satırları** bölümü altında **Satış siparişi satırı**'na tıklayın.
8. **Fiyat ayrıntıları**'na tıklayın. Bu seçeneği görmüyorsanız kılavuzu başlatmadan önce **Fiyat ayrıntılarını etkinleştir** seçeneğini Evet olarak ayarlamamış olabilirsiniz.     
9. **İndirimler** bölümünü genişletin. **İndirimler** sekmesinde mevcut sipariş hattı için geçerli olan tüm indirim sözleşmeleri listelenir ve tahmini indirim tutarı gösterilir. Görüntülenen tutarların, sadece gelecekte hangi indirim talep edilebileceğinin göstergeleri olduğunu unutmayın. Gerçek indirim tutarları şunlara bağlı olarak farklı olabilir: müşteri tarafından bir dönemsel indirim anlaşması kapsamında elde edilen toplam satış hacmi, müşterinin tümünü mü yoksa kısmi miktarları mı iade ettiği; ve uygulanabilir satış siparişinin faturalanmış olup olmadığı.
10. Sayfayı kapatın.
11. **Satır ekle**'ye tıklayın.
12. **Madde numarası** alanına bir değer girin veya bu alanda bir değer seçin.
13. **Miktar**'ı '60' olarak ayarlayın.
14. **Kaydet**'e tıklayın.
15. **Eylem Bölmesinde** **Fatura** öğesine tıklayın.
16. **Fatura** öğesine tıklayın.
17. **Parametreler** bölümünü genişletin.
18. **Miktar** alanında "Tümü"nü seçin.
19. **Tamam**'a tıklayın.
20. **Tamam**'a tıklayın.

## <a name="process-rebate-claims"></a>İndirim taleplerini işleyin
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Müşteri indirimleri > İndirimler**'e gidin.
    - İndirimler sayfası, indirim taleplerini incelemek, onaylamak ve işlemek için bir çalışma ortamı işlevini yerine getirir. Şimdi indirim anlaşması USMF-000001'e konu olan US-009 müşterisi için bir satış siparişi faturalamasının sonucu olarak oluşturulan talepleri işleyeceksiniz.   
    - İlk satır 800 ABD doları olarak hesaplanan bir indirim talebini temsil etmektedir. Bu da T0020 ürününden 40 birimlik satışa dayanmaktadır ve birim başına 20 ABD doları olarak hesaplanır. Bu, indirim anlaşmasındaki ilk miktar kırılma koşullarıyla eşleşmektedir.  
    - İkinci talep 2.400 ABD doları içindir, 60 birim T0020 ürününe dayanır, anlaşmadaki ikinci miktar kırılması uyarınca 40 ABD doları birim fiyatından hesaplanmıştır.  
    - Her iki talep de "Hesaplanacak" durumdadır. Bu da, periyodik olarak müşterinin satış performansını periyodik olarak izleyen bir anlaşma ile ilişkili olduğunu ve bunlarla ilgili dönem içindeki toplam satış hacminin yeniden hesaplanacak olmak zorunda olduğu anlamına gelir.   
2. **Biriktir**'e tıklayın.
3. **Müşteri** alanına bir değer girin veya buradan bir değer seçin.
4. **Başlangıç tarihi** alanında bugünün tarihini seçin.
5. **Tamam**'a tıklayın. **Biriktir** işlevinin çalıştırılması sonucunda tahmini talep tutarı, şimdi müşterinin ilgili dönemde toplam satış hacminin, indirimin ilk oluşturulduğu zaman göre daha yüksek olduğu gerçeğine göre ayarlanır. Daha detaya girmek gerekirse, satılan toplam miktar 100 birime ulaştığı için, müşteri artık ürün başına 40 ABD doları (anlaşmanın ikinci miktar kırılması uyarınca) veya toplam 400 ABD doları toplam indirim miktarına hak kazanmıştır. Fark ek 800 USD için bir yeni talep için "ayarlama" olarak kaydedilir. Biriktirme güncelleştirmesinde dahil edilen indirim talebinin durumu şimdi Hesaplandı olarak ayarlanmıştır. 
6. Listede, tüm satırları işaretleyin.
7. **Onayla**'ya tıklayın.
8. **İşle**'ye tıklayın.
9. **Müşteri** alanına bir değer girin veya buradan bir değer seçin.
10. **Tamam**'a tıklayın. İndirimin başarıyla işlendiğine dair bir mesaj gösterilir ve talebin durumu İşaretlendi olarak değişir. Bu, bir İndirim tahakkuk günlüğünün deftere nakledilme sonucu olarak gelir:
    - Talepler, artık kesintiler olarak geçici müşteri bakiyesine aktarıldı.
    - İndirim tahakkuk hesabı, müşterinin gelecekteki borcunu temsil etmek üzere alacaklandırıldı.
    - İndirim gider hesabı, satışlarla bağlantılı olarak tahakkuk eden maliyeti tanımak üzere borçlandırıldı.   

