---
title: Satıcı faturası otomasyonu sonuçlarını görüntüleme (önizleme)
description: Bu konu, otomatik iş akışına gönder işleminde bulunan satıcı faturalarının durumunun nasıl görüntüleneceğini açıklamaktadır.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e7ec69177cdb4f6304b75016963f4111bbfde6ed975d66ffa702426a68dce640
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6728973"
---
# <a name="view-vendor-invoice-automation-results"></a>Satıcı faturası otomasyonu sonuçlarını görüntüleme

[!include [banner](../includes/banner.md)]

Bu konu, otomatik iş akışına gönder işleminde bulunan satıcı faturalarının durumunun nasıl görüntüleneceğini açıklamaktadır. Her içe aktarılan satıcı faturası için otomasyon geçmişinin ayrıntıları korunur. Otomatikleştirdiğiniz iş süreçlerine bağlı olarak, **Bekleyen satıcı faturaları** sayfası **Otomatik giriş eşleştirme durumu** ve **Otomatik iş akışına gönderme durumu** değerlerini gösterir. Otomatik adımda başarısız olan faturalara odaklanmak için detayları görüntüleyebilir ve bir plan yapabilirsiniz. Daha sonra, sorunu düzelttikten sonra içe aktarılan fatura için otomatik işlemi devam ettirebilirsiniz.

Gönderilen bir faturayı düzenlemeden önce otomatik işlemeyi duraklatmanız gerekir. Otomatik iş akışına gönderme işlemindeki bir faturanın duraklatılması gerekiyorsa, **Otomatik işlemeye dahil et** alanını **Satıcı faturaları** sayfasında **Hayır** olarak ayarlayın. **Otomatik işleme dahil et** **Evet** olarak ayarlanana kadar otomasyon çalışmayacaktır. Bir fatura, henüz iş akışı sisteminde değilse ve otomatikleştirilmiş süreç tarafından kullanılmıyorsa, daha fazla otomasyon yapılmamak üzere duraklatılabilir.

İçe aktarılan bir fatura iş akışına gönder işlemine tabi ise, faturanın **Otomasyon durumu** değerini **Satıcı faturaları** sayfasında görebilirsiniz. Aşağıdaki durumlar izlenir:

- **Dahil edildi** – **Borç hesapları parametreleri** sayfasında tanımlanan otomatik işlemler doğru çalışıyor, ancak henüz tamamlanmadı.
- **Duraklatıldı** – **Borç hesapları parametreleri** sayfasında tanımlanan otomatik işlemler çalıştı ancak işlemde en az bir adım başarısız oldu. **Duraklatıldı** durumu **Otomatik işleme dahil et** alanı **Hayır** olarak ayarlanmışsa da geçerli olur. **En son sonuçları görüntüle**'yi seçerek hataları görüntüleyebilirsiniz.
- **İş akışında** – İçe aktarılan fatura, otomatik iş akışına gönderme işlemi tarafından veya el ile iş akışı sistemine gönderildi.
- **İş akışı tamamlandı** – İçe aktarılan fatura için iş akışı işlemi tamamlandı.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]