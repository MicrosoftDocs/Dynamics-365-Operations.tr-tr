---
title: İlke ihlallerini ve vakalarını denetleme
description: Makalede, denetim ilkesi kuralları ihlallerinden nasıl denetim çalışmaları oluşturulduğu açıklanmaktadır. Makalede, denetim ilkelerinin belge seçim tarihi aralığını kullanmasının çeşitli yolları da yer almaktadır.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: kfend
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbef92865c0a463b3922d7cc6c3f46759ffdc9ad
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711131"
---
# <a name="audit-policy-violations-and-cases"></a>İlke ihlallerini ve vakalarını denetleme

[!include [banner](../includes/banner.md)]

Makalede, denetim ilkesi kuralları ihlallerinden nasıl denetim çalışmaları oluşturulduğu açıklanmaktadır. Makalede, denetim ilkelerinin belge seçim tarihi aralığını kullanmasının çeşitli yolları da yer almaktadır.

## <a name="how-audit-cases-are-generated"></a>Denetim vakaları nasıl oluşturulur

Denetim ilkeleri, tanımladığınız ve denetim ilke kuralları olarak yapılandırdığınız iş kurallarına uymayan gider raporlarının, satın alma emirlerinin ve satıcı faturalarının tanımlanması için kullanılır. 

Denetim ilkeleri toplu iş modunda çalışır. Bir denetim İlkesini çalıştırdığınızda, bu ilkenin bir parçası olan tüm ilke kuralları aynı anda çalıştırılır.

Her bir ilke kuralı bir belgeler kümesini değerlendirir. İlke kuralı, belge seçim tarihi aralığında bulunan ve belirtilen ölçütle eşleşen belgeleri seçer. Örneğin, bir ilke kuralı 50.00 tutarını aşan yemek faturaları içeren gider raporlarını seçebilir. Başka bir ilke kuralı belirli bir satıcıya ödenecek satıcı faturalarını seçebilir. Kümede seçilen her bir belge için bir ihlal oluşturulur. Bu ihlal, örneğin fatura 12345 gibi belirli bir belgenin ilke kuralı ile uyumlu olmadığını gösteren bir kayıttır. 

Birden fazla denetim ihlali kaydı gruplandırılır ve denetim vakaları ile ilişkilendirilir. Varsayılan olarak, her denetim ilkesi için vakalar denetim ilkesi kuralına göre gruplandırılır. İsterseniz, **Vaka gruplandırma ölçütleri** sayfasını kullanarak diğer gruplandırma ölçütlerini de seçebileceğiniz. Örneğin, proje kodu ve satıcı faturaları gider üstbilgilerini satıcı hesabına göre gruplandırabilirsiniz. Bu durumda, aynı proje kimliğine sahip olan tüm gider başlığı ihlalleri aynı vakada gruplandırılır ve aynı satıcı hesabına sahip tüm satıcı faturaları aynı vakada gruplandırılır. 

> [!NOTE]
> Bir **Tekrarlanan** sorgu türüne dayalı denetim ilkesi kuralları için ihlaller, ilke kuralına veya **Vaka gruplandırma ölçütleri** sayfasında belirtilen ölçütlere göre gruplandırılmaz. Bunun yerine, denetim ilkesi kuralına entegre edilen ölçütlere göre gruplandırılır. Örneğin, bir ilke kuralı aynı tutar, satıcı kimliği ve tarih ile tekrarlanan giderler için gider raporlarını değerlendiriyorsa bu alanlarda aynı değerlere sahip olan tüm giderler bir vakada toplanır. Farklı değerlere sahip giderler ise ayrı bir vaka olur.

Denetim vakaları oluşturulduktan sonra standart vaka yönetimi süreçleri kullanılarak işlenir.

## <a name="document-selection-date-ranges"></a>Belge seçimi tarih aralıkları
Bir denetim ilkesi çalıştırıldığında her bir ilke kuralı, tarihi belge seçim tarihi aralığında bulunan, belirtilen türde belgeleri seçer. Belge seçimi tarih aralığı, **Ek seçenekler** sayfasında belirtilir. Birçok belge, kendileriyle ilişkilendirilmiş birden fazla tarih içerir. Denetim ilkesi kuralının kullandığı tarih alanı, **İlke kuralı türü** sayfasında belirtilir.

Burada, bir denetim ilkesinin, belge seçim tarihi aralığını nasıl başka şekillerde kullandığı verilmiştir:

-   İlke, belge seçim tarihi aralığının son gününde geçerli olan her bir ilke kuralının sürümünü kullanır. Her bir ilke kuralının geçerlilik tarihlerini **Denetim ilkeleri** listesi sayfasında bulabilirsiniz.
-   İlke, belge seçim tarihi aralığının son gününde politikayla ilişkilendirilmiş organizasyon düğümlerini kullanır. **Denetim ilkeleri** listesi sayfasında sadece mevcut durumda ilkeyle ilişkilendirilmiş organizasyon düğümleri görüntülenir.
-   Bir **Liste arama** sorgu türüne dayalı ilke kuralları için ilke, belge seçim tarihi aralığının son günü geçerli olan, takip edilen varlıklar için belgeleri değerlendirir.


Daha fazla bilgi için bkz: [Denetim İlkesi kuralları](audit-policy-rules.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
