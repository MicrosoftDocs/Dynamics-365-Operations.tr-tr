---
title: "Vardiya ve kasa çekmecesi yönetimi"
description: "Bu makalede paylaşılan ve bağımsız olmak üzere iki perakende satış noktası (POS) vardiyası türünün nasıl ayarlanacağı ve kullanılacağı açıklanmaktadır. Paylaşılan vardiyalar birden fazla yerdeki çok sayıda kullanıcı tarafından kullanılabilir, bağımsız vardiyalar ise aynı anda yalnızca bir çalışan tarafından kullanılabilir."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailHardwareProfile, RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b8e12f3f4c2f8f5a596c8994f2a4571d8a907062
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="shift-and-cash-drawer-management"></a>Vardiya ve kasa çekmecesi yönetimi

[!include[banner](includes/banner.md)]


Bu makalede paylaşılan ve bağımsız olmak üzere iki perakende satış noktası (POS) vardiyası türünün nasıl ayarlanacağı ve kullanılacağı açıklanmaktadır. Paylaşılan vardiyalar birden fazla yerdeki çok sayıda kullanıcı tarafından kullanılabilir, bağımsız vardiyalar ise aynı anda yalnızca bir çalışan tarafından kullanılabilir.

Bağımsız ve paylaşılan olmak üzere iki tür satış noktası (POS) vardiyası bulunmaktadır. Bağımsız vardiyalar bir seferde yalnızca bir çalışan tarafından kullanılabilir. Paylaşılan vardiyalar birden çok yerde birden çok kullanıcı tarafından kullanılabilir. Bu nedenle bir mağazadaki çok sayıda çalışan için tek bir vardiyayı etkin bir şekilde oluştururlar.

## <a name="standalone-shifts"></a>Bağımsız vardiyalar
Bağımsız vardiyalar nakit parada her POS yazar kasası için bağımsız olarak mutabakata varılan geleneksel, sabit POS senaryosunda kullanılır. Örneğin bir market ortamında, genelde birkaç adet sabit POS yazar kasası vardır ve her bir yazar kasa için bir kasiyer atanmıştır. Bu durumda büyük olasılıkla her kayıt bağımsız vardiya kullanıyordur ve bu kayda ait kasa çekmecesi veya fiziksel paradan kasiyer sorumludur. Bağımsız bir vardiya kasiyerin çalışma vardiyası sırasında o kasadaki tüm etkinliği kapsar. Etkinlikler kasa çekmecesine eklenen açılış tutarı, bankaya yatırılan paralar ve kasa devri girişleri gibi işlemlerde kasada yapılan para ekleme ve para çekme hareketleri ve vardiyanın sonundaki kasa sayımı gibi işlemleri içerebilir.

### <a name="set-up-a-stand-alone-shift"></a>Bağımsız vardiya ayarlama

Bağımsız bir vardiya kasa çekmecesi düzeyinde atanır. Bu prosedürde bir POS yazar kasasında bağımsız vardiya ayarlama işlemi açıklanmaktadır.

1.  **Perakende** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım profilleri**'ne tıklayın.
2.  Bağımsız vardiya için kullanılacak donanım profilini seçin.
3.  **Çekmece** Hızlı Sekmesinde, **Paylaşılan vardiya çekmecesi** seçeneğinin **Hayır** olarak ayarlandığını doğrulayın.
4.  **Kaydet**'i tıklatın.
5.  **Perakende** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Kayıtlar** üzerine tıklayın.
6.  Bağımsız vardiya gerektiren yazar kasayı seçin ve **Düzenle**'ye tıklayın.
7.  **Donanım profili** alanında, 2. adımda belirlediğiniz donanım profilini seçin.
8.  **Kaydet**'i tıklatın.
9.  **Perakende** &gt; **Perakende BT** &gt; **Dağıtım planı** öğesine tıklayın.
10. **1090** dağıtım planını seçin ve ardından POS değişikliklerini eşitlemek için **Şimdi çalıştır** seçeneğine tıklayın.

### <a name="use-a-stand-alone-shift"></a>Bağımsız vardiya kullanma

1.  POS'ta oturum açın.
2.  Açık bir vardiya yoksa **Yeni bir vardiya aç** seçeneğini belirleyin.
3.  **Başlangıç tutarını beyan et** işlemine gidin ve iş gününü başlatmak için çekmeceye eklenen nakit tutarını belirtin.
4.  Birkaç hareket gerçekleştirin.
5.  Günün sonunda, kasa çekmecesinde kalan nakit tutarını beyan etmek için **Kasa sayımı beyan et** seçeneğini belirleyin.
6.  Nakit tutarını girin ve kasa sayımı beyanını kaydetmek için **Kaydet**'e tıklayın.
7.  Vardiyayı kapatmak için **Vardiyayı kapat** seçeneğini belirleyin.

**Not:** Kullanılan iş süreçlerine bağlı olarak vardiya sırasında başka işlemler de kullanılabilir. Gün içinde veya vardiya kapatıldıktan sonra çekmeceden para çekmek için **Kasaya para nakli**, **Bankaya para nakli** ve **Ödeme kaldırma** işlemleri kullanılabilir. Kasada nakit azalırsa, kasaya nakit eklemek için **Kasa devri girişi** işlemi kullanılabilir.

## <a name="shared-shifts"></a>Paylaşılan vardiyalar
Paylaşılan bir vardiya çok sayıda kasiyerin veya iş günü içinde bir grup kasiyerin bir kasa çekmecesini paylaştığı durumlarda kullanılır. Genellikle paylaşılan vardiya mobil POS ortamlarında kullanılır. Mobil ortamda her kasiyer tek bir kasa çekmecesine atanmaz ve tek bir kasa çekmecesinden sorumlu tutulmaz. Bunun yerine tüm kasiyerler bir satış için ödeme alabilmeli ve kendilerine en yakın kasa çekmecesine nakit ekleyebilmelidir. Bu senaryoda, kasiyerler tarafından paylaşılan kasa çekmeceleri paylaşılan bir vardiyaya dahil edilmiştir. Paylaşılan bir vardiyadaki tüm kasa çekmeceleri o vardiyanın nakit yönetimiyle ilgili etkinlikler için aynı vardiyaya dahil edilir. Bu nedenle, vardiyanın başlangıç tutarı paylaşılan vardiya kapsamındaki tüm kasa çekmecelerinde bulunan tüm nakit parayı içermelidir. Aynı şekilde, kasa sayımı beyanı da paylaşılan vardiya kapsamındaki tüm kasa çekmecelerinde bulunan tüm nakit paranın toplamı olmalıdır. **Not:** Her mağazada aynı anda yalnızca bir paylaşılan vardiya açılabilir. Aynı mağazada paylaşılan vardiyalar ve bağımsız vardiyalar kullanılabilir.

### <a name="set-up-a-shared-shift"></a>Paylaşılan vardiya ayarlama

1.  **Perakende** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **Donanım profilleri**'ne tıklayın.
2.  Paylaşılan vardiya için kullanılacak donanım profilini seçin.
3.  **Çekmece** Hızlı Sekmesinde, **Paylaşılan vardiya çekmecesi** seçeneğini **Evet** olarak ayarlayın.
4.  **Kaydet**'i tıklatın.
5.  **Perakende** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **Kayıtlar** üzerine tıklayın.
6.  Paylaşılan vardiya gerektiren yazar kasayı seçin ve **Düzenle**'ye tıklayın.
7.  **Donanım profili** alanında, 2. adımda belirlediğiniz donanım profilini seçin.
8.  **Kaydet**'i tıklatın.
9.  **Perakende** &gt; **Perakende BT** &gt; **Dağıtım planı** öğesine tıklayın.
10. **1090** dağıtım planını seçin ve ardından POS değişikliklerini eşitlemek için **Şimdi çalıştır** seçeneğine tıklayın.

### <a name="use-a-shared-shift"></a>Paylaşılan vardiya kullanma

1.  POS'ta oturum açın.
2.  POS henüz donanım istasyonuna bağlanmadıysa, **Çekmece işlemi olmayan bir işlem** seçeneğini ve ardından paylaşılan vardiya için donanım istasyonunu etkinleştirmek için **Donanım istasyonu seç** öğesini belirleyin. Bu adım yalnızca yazar kasa paylaşılan vardiya ortamına ilk kez eklendiğinde gereklidir.
3.  POS oturumunu kapatın ve tekrar oturum açın.
4.  **Yeni vardiya oluştur**'u seçin.
5.  **Başlangıç tutarını beyan et**'i seçin.
6.  Mağazada paylaşılan vardiyanın parçası olan tüm kasa çekmecelerindeki başlangıç tutarını girin ve **Kaydet**'e tıklayın.
    -   Başlangıç tutarının bir kısmını sonraki kasa çekmecelerine eklemek üzere donanım istasyonunu etkinleştirmek için **Donanım istasyonu seç** işlemini kullanın.
    -   Belirli bir kasa çekmecesine kasa eklemek için **Çekmeceyi aç** işlemini kullanın.
    -   Paylaşılan vardiyadaki tüm kasa çekmeceleri başlangıç tutarından kendi paylarını alana kadar bu işleme devam edin.

7.  Günün sonunda tüm kasa çekmecelerini açın ve nakit parayı çıkarın.
8.  Son kasa çekmecesindeki nakit parayı da çıkardıktan sonra tüm kasa çekmecelerinden alınan nakit parayı sayın.
9.  Paylaşılan vardiya kapsamındaki tüm kasa çekmecelerinden alınan nakit paranın toplam tutarını beyan etmek için **Kasa sayımı beyan et** işlemini kullanın.
10. Paylaşılan vardiyayı kapatmak için **Vardiyayı kapat** işlemini kullanın.





