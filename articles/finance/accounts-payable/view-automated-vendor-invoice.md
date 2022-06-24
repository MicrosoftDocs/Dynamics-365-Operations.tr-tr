---
title: Satıcı faturası otomasyonu sonuçlarını görüntüleme (önizleme)
description: Bu makale, otomatik iş akışına gönder işlemindeki satıcı faturalarının durumunun nasıl görüntüleneceğini açıklamaktadır.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd9b74d2ed34399aff455563504c296a5a25a874
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895181"
---
# <a name="view-vendor-invoice-automation-results"></a>Satıcı faturası otomasyonu sonuçlarını görüntüleme

[!include [banner](../includes/banner.md)]

Bu makale, otomatik iş akışına gönder işlemindeki satıcı faturalarının durumunun nasıl görüntüleneceğini açıklamaktadır. Her içe aktarılan satıcı faturası için otomasyon geçmişinin ayrıntıları korunur. Otomatikleştirdiğiniz iş süreçlerine bağlı olarak, **Bekleyen satıcı faturaları** sayfası **Otomatik giriş eşleştirme durumu** ve **Otomatik iş akışına gönderme durumu** değerlerini gösterir. Otomatik adımda başarısız olan faturalara odaklanmak için detayları görüntüleyebilir ve bir plan yapabilirsiniz. Daha sonra, sorunu düzelttikten sonra içe aktarılan fatura için otomatik işlemi devam ettirebilirsiniz.

Gönderilen bir faturayı düzenlemeden önce otomatik işlemeyi duraklatmanız gerekir. Otomatik iş akışına gönderme işlemindeki bir faturanın duraklatılması gerekiyorsa, **Otomatik işlemeye dahil et** alanını **Satıcı faturaları** sayfasında **Hayır** olarak ayarlayın. **Otomatik işleme dahil et** **Evet** olarak ayarlanana kadar otomasyon çalışmayacaktır. Bir fatura, henüz iş akışı sisteminde değilse ve otomatikleştirilmiş süreç tarafından kullanılmıyorsa, daha fazla otomasyon yapılmamak üzere duraklatılabilir.

İçe aktarılan bir fatura iş akışına gönder işlemine tabi ise, faturanın **Otomasyon durumu** değerini **Satıcı faturaları** sayfasında görebilirsiniz. Aşağıdaki durumlar izlenir:

- **Dahil edildi** – **Borç hesapları parametreleri** sayfasında tanımlanan otomatik işlemler doğru çalışıyor, ancak henüz tamamlanmadı.
- **Duraklatıldı** – **Borç hesapları parametreleri** sayfasında tanımlanan otomatik işlemler çalıştı ancak işlemde en az bir adım başarısız oldu. **Duraklatıldı** durumu **Otomatik işleme dahil et** alanı **Hayır** olarak ayarlanmışsa da geçerli olur. **En son sonuçları görüntüle**'yi seçerek hataları görüntüleyebilirsiniz.
- **İş akışında** – İçe aktarılan fatura, otomatik iş akışına gönderme işlemi tarafından veya el ile iş akışı sistemine gönderildi.
- **İş akışı tamamlandı** – İçe aktarılan fatura için iş akışı işlemi tamamlandı.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
