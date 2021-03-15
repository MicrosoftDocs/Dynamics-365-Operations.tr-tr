---
title: Ön ödeme faturaları ve ön ödemeler karşılaştırması
description: Bu konuda kuruluşların peşin ödemeler (ön ödemeler) için kullanabileceği iki yöntem açıklanmış ve karşılaştırılmıştır. Birinci yöntemde bir satın alma emriyle ilişkilendirilmiş bir ön ödeme faturası oluşturursunuz. İkinci yöntemde ise günlük girişleri oluşturup ön ödeme günlüğü fişleri olarak işaretleyerek ön ödeme günlüğü fişleri oluşturursunuz.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c29529aa57eb7685e36f5407f4279544fdb701
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979550"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Ön ödeme faturaları ve ön ödemeler karşılaştırması

[!include [banner](../includes/banner.md)]

Bu konuda kuruluşların peşin ödemeler (ön ödemeler) için kullanabileceği iki yöntem açıklanmış ve karşılaştırılmıştır. Birinci yöntemde bir satın alma emriyle ilişkilendirilmiş bir ön ödeme faturası oluşturursunuz. İkinci yöntemde ise günlük girişleri oluşturup ön ödeme günlüğü fişleri olarak işaretleyerek ön ödeme günlüğü fişleri oluşturursunuz.

Kuruluşlar, satıcılara mal veya hizmetleri için bu mal veya hizmetler karşılanmadan önce ön ödeme (avans ödeme) yapabilirler. Satıcılara ön ödeme yapmak için iki yöntem kullanılabilir. Riski en aza indirmek için, bir satınalma emrine ön ödeme tanımlayarak ön ödemeleri izleyebilirsiniz. Bu yöntem için satınalma emriyle ilişkilendirilmiş bir ön ödeme faturası oluşturmanız gerekir. Bu yöntem ön ödeme faturalandırması olarak adlandırılır. Ön ödemeleri yakında takip etmek istemeyen veya satıcılarından ön ödeme faturası almayan kuruluşlar, ön ödeme faturalandırması yöntemi yerine ön ödeme günlüğü fişleri kullanabilirler. Günlük girişleri oluşturup ön ödeme günlüğü fişleri olarak işaretleyerek ön ödeme günlüğü fişleri oluşturabilirsiniz. Bu yöntemde, bir satıcıya hangi ön ödemelerin hangi satınalma emirlerine karşı yapıldığını takip edemezsiniz. Ancak, deftere nakledilen bir ön ödemeyi bir satınalma emrine karşı kapatma olarak işaretleyebilirsiniz.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Ön ödeme faturalandırması - ön ödemeler ne zaman kullanılır

| Ön ödeme faturalandırması                                                                | Ön ödemeler                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Satınalma emrine bir ön ödeme değeri tanımlayın.                                    | Satınalma emrine hiçbir ön ödeme değeri tanımlanmamıştır.                    |
| Anahtar: Peşinat faturası ve nihai fatura deftere nakledilmelidir.                       | Deftere hiçbir ön ödeme faturası nakledilmemelidir.                                    |
| Ön ödeme yükümlülüğü ön ödeme hesabında tutulur, AP hesabında değil. | Ön ödeme yükümlülüğü AP hesabında tutulur.                  |
| Satıcı bakiyesi ön ödeme değerini işlem boyunca yansıtmaz.     | Satıcı bakiyesi ön ödeme değerini işlem boyunca yansıtır. |
| Ön ödeme faturalandırması yalnızca Borç hesaplarında kullanılabilir.                         | Ön ödemeler Borç hesabında ve Alacak hesaplarında kullanılabilir.    |

## <a name="overview-of-the-prepayment-process"></a>Ön ödeme işlemine genel bakış
Birçok ülke/bölgedeki muhasebe uygulamaları, bir müşteriden veya satıcıdan gelen peşinatların müşteri veya satıcı için normal özet hesaplara nakledilmemesini gerektirir. Bunun yerine, bu ön ödemeler, ön ödemeler için olan özel genel muhasebe hesaplarına nakledilir. Bir satış siparişi veya satın alma siparişi oluşturulduğunda, müşteriye bir fatura düzenler veya satıcıdan alınır. Fatura ödenirken, ön ödeme genel muhasebe hesaplarındaki ön ödeme ve satış vergisi ön ödemesi fişi ters çevrilir ve fatura tutarları otomatik olarak genel özet hesaplarına nakledilir. Bir ön ödeme oluşturmak için şu adımları izleyin.

1.  Ön ödemeler için deftere nakil profilleri ayarlayın.
2.  Alacak hesapları parametreleri Borç hesapları parametrelerinde, **Genel muhasebe ve satış vergisi** altında, **Ön ödemeli ödeme günlüğü için deftere nakil profili** parametresini kullanarak yeni deftere nakil profilini seçin.
3.  Bir ödeme günlüğü oluşturun ve sonra yeni ödemeyi oluşturun.
4.  Ödemeyi ön ödeme olarak işaretleyebilirsiniz. Bir ödeme peşinat olarak işaretlenirse ödeme, 1 ve 2. adımlarda ayarladığınız deftere nakil profilinde tanımlı genel muhasebe hesaplarına nakledilir. Ek olarak, ödeme ön ödeme olarak işaretlenmişse, vergiler de hesaplanır. Bazı hükümetler, fatura olmasa ön ödeme kaydedildiğinde vergilerin ödenmesini gerektirir.
5.  Ön ödemeyi nakledin.
6.  İsteğe bağlı: Faturayı oluşturmadan önce ön ödemeleri satın alma siparişi veya satış siparişi karşılığında kapatabilirsiniz. Satış siparişi veya satın alma siparişi sayfasında, Eylem Bölmesi'nde **Hareketleri kapat**'ı kullanın.
7.  Satıcı mal veya hizmetleri teslim ettikten sonra faturayı kaydedin. 6. adımda satınalma emrine veya satış emrine karşı ön ödemeyi kapattıysanız, ön ödeme oluşturduğunuz faturaya karşı otomatik olarak kapatılır. Ön ödemeyi satın alma siparişi veya satış siparişi karşılığında kapatmadıysanız müşteri veya satıcı sayfasındaki **Hareketleri kapat**'ı kullanarak fatura karşılığında el ile kapatabilirsiniz. Ardından ön ödeme tutarı, geçici olarak AP/AR genel muhasebesinden tersine çevrilir. Ek olarak, vergiler hesaplandıysa bunlar tersine çevrilir çünkü fatura gerçek vergileri içerir.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Ön ödeme faturalandırma işlemine genel bakış
Ön ödeme faturaları yaygın bir iş uygulamasıdır. Bir satıcı, satınalma emri karşılanmadan önce satınalma teminatı istemek için ön ödeme faturaları çıkarır. Örneğin, bazı satıcılar özel mallar veya hizmetler için ön ödeme gerektirir. Bir satıcı ön ödeme gerektiren bir fatura çıkarırsa, ön ödeme faturalandırma özelliğini kullanabilirsiniz. Satın alma siparişinde bir ön ödeme değeri tanımlanabilir, ön ödeme faturası kaydedilir ve ödenir ve ardından ön ödeme faturası son faturaya uygulanır. Bir ön ödeme oluşturmak için şu adımları izleyin.

1.  Satınalma temsilcisi, satıcının ön ödeme istediği bir satınalma emrini oluşturur, onaylar ve ardından gönderir. Ön ödeme değeri, satınalma emrinde anlaşmasının parçası olarak tanımlıdır.
2.  Satıcı bir ön ödeme faturası gönderir.
3.  Borç hesapları koordinatörü, satınalma emrine karşı ön ödeme faturasını kaydeder ve ardından ön ödeme faturası ödenir.
4.  Satıcı mal veya hizmetleri sağladıktan ve ilgili satıcı faturaları alındıktan sonra, Borç hesapları koordinatörü faturaya karşı zaten ödenmiş olan ön ödeme tutarını uygular.
5.  Borç hesapları koordinatörü faturanın kalan tutarını öder ve kapatır.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]