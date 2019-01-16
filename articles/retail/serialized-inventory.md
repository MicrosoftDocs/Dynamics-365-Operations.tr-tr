---
title: "Serileştirilmiş ürünler için satış noktası (POS) geliştirmeleri"
description: "Bu konu, seri ürünler üzerinde size zaman kazandıracak ve verimliliğinizi artıracak geliştirmeleri listeler."
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-08-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 17cd46ba9ee972c92db8950eea1cd258d67c2e92
ms.contentlocale: tr-tr
ms.lasthandoff: 01/04/2019

---

# <a name="point-of-sale-pos-improvements-for-serialized-products"></a>Serileştirilmiş ürünler için satış noktası (POS) geliştirmeleri

[!include [banner](includes/banner.md)]

## <a name="overview"></a>Genel bakış

Perakende merkezindeki ayarlara dayanarak, ürünler seri veya seri değil olarak sınıflandırılabilir. Ürünler seri hale getirildiğinde, garantileri takip etmek, maddeleri izlemek ve sahipliği onaylamaya yardımcı olmak için her bir maddeye benzersiz bir numara atanabilir. Modern/Bulut Satış Noktası (POS) içerisinde seri haldeki ürünler için seri numaralar sağlama özelliği zaten bulunuyor olsa da, bir dizi geliştirme yapılarak kasiyerlere zaman kazandırma ve verimliliği artırmak hedeflenmiştir.

## <a name="pos-improvements"></a>POS geliştirmeleri

- **Seri numaraları ödemeye kadar gerekli değil** – Önceden, bir seri haldeki ürünü harekete ekleyen bir kasiyerin bir seri numarası eklemesi gerekiyordu. Bu gereksinim, kasiyerlerin up-sell yapma fırsatı olduğunda müşteri kayırma senaryoları söz konusu olduğunda bir sorun haline geldi. Ürünler, çoğu zaman sepette ödeme adımına kadar güncelleştiriliyordu. Bu nedenle, bir kasiyer her defasında yeni bir ürün eklediğinde, sistem ona seri numarası soruyordu. Seri numarası iletişim kutusu şimdi bir **Sonra ekle** düğmesi içeriyor. Bu nedenle, satış personeli maddeleri harekete ekleyebiliyor ancak seri numarasını sonra sağlayabiliyor. Satış sorumluları, sepette seri halde ürünleri hızlıca ekleyebilir ve değiştirebilir ve sonra seri numarasını ödemeden hemen önce sağlayabilir. Seri numarası herhangi bir seri haldeki ürün için sağlanmamışsa, hareketi tamamlamaya çalışan kasiyer bir hata iletisi alır. Bu mesaj, devam etmeden önce kasiyerin eksik seri numarasını girmesi gerektiğini belirtir.

    Seri numarasının atlandığı her bir seri haldeki ürün için bir yorum hareket satırının altında görüntülenir. Bu yorum, seri numarasının madde için sağlanmamış olduğunu belirtir. Bu nedenle, kasiyer seri numarası eksik ürünleri hızlıca bulabilir.

    Yeni **Seri numarası ekle** işlemi ayrıca seri numarası eksik maddeler için seri numarası sağlar. Seri numarası verildikten sonra düzenlenemez. Kasiyerin satırı hükümsüz kılması ve ürünü yeniden eklemesi gerekir.
    
- **Seri numaraları müşteri siparişlerini eklemek için gerekli değildir** – Müşteri siparişleri bir mağazadan eklenip başka bir mağazadan gerçekleştirilebilir. Bir müşteri siparişi ekleyen bir kasiyerin seri numarasını eklemesi gerekmez. Seri numarası malzeme çekme veya toplama adımı sırasında sağlanır. Ancak, **Alıp git** teslimat türünün seçilmiş olduğu tüm satır maddeleri için bir seri numarasının verilmiş olması gerekir. Aksi durumda, işlem tamamlanamaz.
- **Seri hale getirilen ürünler hareket ekranında toplanmaz** – **İşlev profili** sayfasındaki **Terminal** alanı grubundaki **Ürünleri topla** ayarı, hareket ekranında seri halde olmayan aynı ürünleri toplamanıza olanak sağlar. Aynı ürünler toplanırken, hareket kılavuzunda görülmeleri daha kolaydır. Ancak, seri numaraları genellikle benzersiz olduğunda ve satış sorumlularının ödeme adımına kadar seri numarası girmek zorunda olmadıklarından **Ürünleri topla** ayarı seri haldeki ürünlere uygulanmaz. Bu nedenle seri haldeki ürünler hareket ekranında **Ürünleri topla** ayarı seçiliyse toplanmayacaktır.
- **Günlükleri seri numarasına göre arama yeteneği** – Günlükler artık seri numaralarına göre de aranabilir. Bunu yapmak için "Günlükler" işlemini açın ve uygulama çubuğundaki "Gelişmiş arama" düğmesine basın. "Filtre ekle" düğmesini kullanarak, seri numarası aramasına bir filtre de uygulanabilir.

