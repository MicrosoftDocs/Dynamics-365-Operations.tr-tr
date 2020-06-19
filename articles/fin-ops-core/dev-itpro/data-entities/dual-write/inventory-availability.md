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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: dd0995eb8c70ed06cdc3c0f6a28b13b117297533
ms.sourcegitcommit: be7e4378c8122c6e7cfc4e7991efbdffee45e006
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2020
ms.locfileid: "3426994"
---
# <a name="inventory-availability"></a>Stok kullanılabilirliği

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Stok kullanılabilirliğini kullanarak, Dynamics 365 ' te model odaklı uygulamalardaki bir ürünü **tekliflere**, **siparişlere** veya **faturalara** eklemek için Stoğunuzu kontrol edebilirsiniz. Örneğin, stok denetimi ve tam bir tarihi belirleme [aday müşteri nakit](dual-write-prospect-to-cash.md) işlemindeki anahtar görevdir . Yeterli stoğa sahip değilseniz, tahmini stok alış irsaliyelerine ve çıkışlarına göre bir teslimat tarihi tahmin edebilirsiniz. Ayrıca, ATP miktarını önceden tanımlanmış zaman diliminden bulabileceğiniz, maddenin taahhüt edilebilir (ATP) bilgilerini de denetleyebilirsiniz.

## <a name="on-hand-inventory"></a>Eldeki Stok 

Dynamics 365 Sales içindeki **teklif**, **sipariş** veya **fatura** formlarının üstbilgisinde Yeni bir düğme **Eldeki stok** eklenir. Düğmeyi tıklattığınızda, bir iletişim kutusu görüntülenir ve eldeki stoğu denetlemek istediğiniz şirketi ve ürünü belirtebilirsiniz. Stok bilgilerini Dynamics 365 Supply Chain Management'den döndürür ve [eldeki stokla](../../../../supply-chain/inventory/tasks/check-availability-stock.md) aynı bilgileri gösterir . Bilgiler şu miktarları içerir:

- **Eldeki Miktar**
- **Kaydedilen Eldeki Miktar**
- **Kullanılabilir Eldeki Miktar**
- **Sipariş verilen miktarı**
- **Siparişteki Miktar**
- **Ayrılan sipariş edilen miktar**
- **Toplam kullanılabilir miktar**

## <a name="atp-information"></a>KM bilgileri

Dynamics 365 Sales içindeki **teklif**, **sipariş** veya **fatura** formlarının üstbilgisinde Yeni bir düğme **ATP bilgileri** eklenir. Düğmeyi tıklattığınızda, bir iletişim kutusu görüntülenir ve şirketi, envanter sahasını, envanter deposunu ve sipariş miktarını belirtebilirsiniz. Supply Chain Management'tan **ATP bilgileri** iade edin ve [sipariş taahhüdünden](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) alınan ayarları gösterir . Bu bilgiler **ATP miktarını**, **giriş miktarını**, **Stok çıkış miktarını** ve **Eldeki miktarı** içerir.
