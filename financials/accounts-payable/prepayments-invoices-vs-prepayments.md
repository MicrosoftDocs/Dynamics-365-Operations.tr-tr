---
title: "Ön ödeme faturaları - ön ödemeler"
description: "Bu makalede kuruluşların peşin ödemeler (ödemeler) için kullanabileceği iki yöntem açıklanmış ve karşılaştırılmıştır. Birinci yöntemde bir satın alma emriyle ilişkilendirilmiş bir ön ödeme faturası oluşturursunuz. İkinci yöntemde ise günlük girişleri oluşturup ön ödeme günlüğü fişleri olarak işaretleyerek ön ödeme günlüğü fişleri oluşturursunuz."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: Shiva.Pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c4f127007cea1d8ccd0b4e9ea637f0674775278d
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017

---

# <a name="prepayment-invoices-vs-prepayments"></a>Ön ödeme faturaları - ön ödemeler

[!include[banner](../includes/banner.md)]


Bu makalede kuruluşların peşin ödemeler (ödemeler) için kullanabileceği iki yöntem açıklanmış ve karşılaştırılmıştır. Birinci yöntemde bir satın alma emriyle ilişkilendirilmiş bir ön ödeme faturası oluşturursunuz. İkinci yöntemde ise günlük girişleri oluşturup ön ödeme günlüğü fişleri olarak işaretleyerek ön ödeme günlüğü fişleri oluşturursunuz.

Kuruluşlar, satıcılara mal veya hizmetleri için bu mal veya hizmetler karşılanmadan önce ön ödeme (avans ödeme) yapabilirler. Satıcılara ön ödeme yapmak için iki yöntem kullanılabilir. Riski en aza indirmek için, bir satınalma emrine ön ödeme tanımlayarak ön ödemeleri izleyebilirsiniz. Bu yöntem için satınalma emriyle ilişkilendirilmiş bir ön ödeme faturası oluşturmanız gerekir. Bu yöntem ön ödeme faturalandırması olarak adlandırılır. Ön ödemeleri yakında takip etmek istemeyen veya satıcılarından ön ödeme faturası almayan kuruluşlar, ön ödeme faturalandırması yöntemi yerine ön ödeme günlüğü fişleri kullanabilirler. Günlük girişleri oluşturup ön ödeme günlüğü fişleri olarak işaretleyerek ön ödeme günlüğü fişleri oluşturabilirsiniz. Bu yöntemde, bir satıcıya hangi ön ödemelerin hangi satınalma emirlerine karşı yapıldığını takip edemezsiniz. Ancak, deftere nakledilen bir ön ödemeyi bir satınalma emrine karşı kapatma olarak işaretleyebilirsiniz.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Ön ödeme faturalandırması - ön ödemeler ne zaman kullanılır
| Ön ödeme faturalandırması                                                                | Ön ödemeler                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Satınalma emrine bir ön ödeme değeri tanımlayın.                                    | Satınalma emrine hiçbir ön ödeme değeri tanımlanmamıştır.                    |
| Anahtar: Ön ödeme faturası ve son fatura deftere nakledilmelidir.                       | Deftere hiçbir ön ödeme faturası nakledilmemelidir.                                    |
| Ön ödeme yükümlülüğü ön ödeme hesabında tutulur, AP hesabında değil. | Ön ödeme yükümlülüğü AP hesabında tutulur.                  |
| Satıcı bakiyesi ön ödeme değerini işlem boyunca yansıtmaz.     | Satıcı bakiyesi ön ödeme değerini işlem boyunca yansıtır. |
| Ön ödeme faturalandırması yalnızca Borç hesaplarında kullanılabilir.                         | Ön ödemeler Borç hesabında ve Alacak hesaplarında kullanılabilir.    |

## <a name="overview-of-the-prepayment-process"></a>Ön ödeme işlemine genel bakış
Birçok ülkedeki/bölgedeki muhasebe uygulamaları, müşteriden satıcıya yapılan ön ödemelerin müşteri veya satıcı için genel özet hesaplarına nakledilmemesini gerektirir. Bunun yerine, bu ön ödemeler, ön ödemeler için olan özel genel muhasebe hesaplarına nakledilir. Bir satış emri veya satınalma emri oluşturulduğunda, müşteriye veya satıcıdan bir fatura çıkarılır. Fatura ödenirken, ön ödeme genel muhasebe hesaplarındaki ön ödeme ve satış vergisi ön ödemesi fişi ters çevrilir ve fatura tutarları otomatik olarak genel özet hesaplarına nakledilir. Bir ön ödeme oluşturmak için şu adımları izleyin.

1.  Ön ödemeler için deftere nakil profilleri ayarlayın.
2.  Alacak hesapları parametreleri Borç hesapları parametrelerinde, **Genel muhasebe ve satış vergisi** altında, **Ön ödemeli ödeme günlüğü için deftere nakil profili** parametresini kullanarak yeni deftere nakil profilini seçin.
3.  Bir ödeme günlüğü oluşturun, sonra da yeni ödeme oluşturun.
4.  Ödemeyi ön ödeme olarak işaretleyebilirsiniz. Bir ödeme ön ödeme olarak işaretlenmişse ödeme, 1 ve 2. adımlarda ayarladığınız deftere nakil profilinde tanımlanan genel muhasebe hesaplarına nakledilir. Ek olarak, ödeme ön ödeme olarak işaretlenmişse, vergiler de hesaplanır. Bazı devletler, bir ön ödeme kaydedildiğinde, fatura olmasa bile vergilerin ödenmesini gerekir.
5.  Ön ödemeyi nakledin.
6.  İsteğe bağlı: Faturayı oluşturmadan önce ön ödemeyi satınalma siparişine veya satış siparişine karşılık kapatabilirsiniz. Satış siparişi veya satınalma siparişi sayfasında, Eylem bölmesindeki **Hareketleri kapat**'ı kullanın.
7.  Satıcı mal veya hizmetleri teslim ettikten sonra faturayı kaydedin. 6. adımda satınalma emrine veya satış emrine karşı ön ödemeyi kapattıysanız, ön ödeme oluşturduğunuz faturaya karşı otomatik olarak kapatılır. Satınalma emrine veya satış emrine karşı ön ödemeyi kapatmadıysanız, müşteri veya satıcı sayfasındaki **Hareketleri kapat** seçeneğini kullanarak, faturaya karşı manuel olarak kapatabilirsiniz. Ardından ön ödeme tutarı, geçici olarak AP/AR genel muhasebesinden tersine çevrilir. Ek olarak, vergiler hesaplandıysa bunlar tersine çevrilir çünkü fatura gerçek vergileri içerir.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Ön ödeme faturalandırma işlemine genel bakış
Ön ödeme faturaları yaygın bir iş uygulamasıdır. Bir satıcı, satınalma emri karşılanmadan önce satınalma teminatı istemek için ön ödeme faturaları çıkarır. Örneğin, bazı satıcılar özel mal veya hizmetler için bir ön ödeme ister. Bir satıcı ön ödeme gerektiren bir fatura çıkarırsa, ön ödeme faturalandırma özelliğini kullanabilirsiniz. Satınalma emrine bir ön ödeme değeri tanımlanabilir, bir ön ödeme faturası kaydedilir ve ödenir, ardından ön ödeme faturaları son faturaya uygulanır. Bir ön ödeme oluşturmak için şu adımları izleyin.

1.  Satınalma temsilcisi, satıcının ön ödeme istediği bir satınalma emrini oluşturur, onaylar ve ardından gönderir. Ön ödeme değeri, satınalma emrinde anlaşmasının parçası olarak tanımlıdır.
2.  Satıcı bir ön ödeme faturası gönderir.
3.  Borç hesapları koordinatörü, satınalma emrine karşı ön ödeme faturasını kaydeder ve ardından ön ödeme faturası ödenir.
4.  Satıcı mal veya hizmetleri sağladıktan ve ilgili satıcı faturaları alındıktan sonra, Borç hesapları koordinatörü faturaya karşı zaten ödenmiş olan ön ödeme tutarını uygular.
5.  Borç hesapları koordinatörü faturanın kalan tutarını öder ve kapatır.





