---
title: Çift yazılarda stok kullanılabilirliği
description: Bu konu, çift yazmada envanter kullanılabilirliğini kontrol etme hakkında bilgi sağlar.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458251"
---
# <a name="inventory-availability-in-dual-write"></a>Çift yazılarda stok kullanılabilirliği

[!include [banner](../../includes/banner.md)]

Stok kullanılabilirliğini kullanarak, bir ürünü Microsoft Dynamics 365 Sales'te model temelli uygulamalardaki **Teklifler**, **Siparişler** veya **Faturalar** sayfasına eklemeden önce Stoğunuzu kontrol edebilirsiniz. Örneğin, stok denetimi ve karşılama tarihi belirleme [aday müşteriden nakde](dual-write-prospect-to-cash.md) işlemindeki anahtar görevdir.

Yeterli stoğa sahip değilseniz, tahmini stok alış girişlerine ve çıkışlarına göre bir teslimat tarihi tahmin edebilirsiniz. Ayrıca, ATP miktarını önceden tanımlanmış zaman diliminden bulabileceğiniz, maddenin taahhüt edilebilir (ATP) bilgilerini de denetleyebilirsiniz.

## <a name="on-hand-inventory"></a>Eldeki stok

Dynamics 365 Sales'te **Teklifler**, **Siparişler** ve **Fatura** sayfalarının başlığına yen bir **Eldeki stok** düğmesi eklenmiştir. Bu düğmeyi seçtiğinizde, bir iletişim kutusu görüntülenir ve eldeki stoğu denetlemek istediğiniz şirketi ve ürünü burada belirtebilirsiniz. Bu iletişim kutusu [Eldeki stok](../../../../supply-chain/inventory/tasks/check-availability-stock.md) ile aynı bilgileri gösterir.

İletişim kutusu Dynamics 365 Supply Chain Management'tan stok bilgilerini getirir. Bilgiler aşağıdaki miktarları içerir:

- Eldeki miktar
- Tersine çevrilen eldeki miktar
- Kullanılabilir eldeki miktar
- Sipariş miktarı
- Siparişteki miktar
- Ayrılan sipariş edilen miktar
- Toplam kullanılabilir miktar

## <a name="atp-information"></a>KM bilgileri

Sales'te **Teklifler**, **Siparişler** ve **Faturalar** sayfalarındaki satır öğelerine yeni bir **ATP Bilgileri** düğmesi eklenmiştir. Bu düğmeyi seçtiğinizde, bir iletişim kutusu görüntülenir ve şirketi, stok tesisini, stok ambarını ve sipariş miktarını burada belirtebilirsiniz. Bu iletişim kutusu, [Sipariş taahhüdü](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) bölümünde açıklananlarla aynı ayarlara sahiptir.

İletişim kutusu, Supply Chain Management'taki ATP bilgilerini döndürür. Bilgiler aşağıdaki miktarları içerir:

- KM miktarı
- Giriş  miktarı
- Çıkış miktarı
- Eldeki miktar


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]