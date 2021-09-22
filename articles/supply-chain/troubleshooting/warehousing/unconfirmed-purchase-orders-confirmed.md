---
title: Ürün girişlerini güncelleştirme görevi, onaylanmamış siparişleri onaylıyor
description: Ürün girişlerini güncelleştirme işlemini çalıştırdıktan sonra sistem, Kayıtlı durumunda olan onaylanmamış siparişleri onaylıyor. Bu sorunu düzelten özellik hakkında bilgi edinin.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477813"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Ürün girişlerini güncelleştirme işlemini çalıştırdıktan sonra onaylanmamış siparişler onaylanıyor

## <a name="symptoms"></a>Belirtiler

*Ürün girişlerini güncelleştir* periyodik görevini çalıştırdıktan sonra, sistem, stok hareket durumu *Kayıtlı* olan onaylanmamış satın alma siparişlerini otomatik olarak onaylar.

## <a name="resolution"></a>Çözüm

*Yük miktarlarını aşırı alma* adlı yeni bir özellikle bu sorunu düzeltilmiştir. Bu özelliği açmak için [Özellik yönetimi](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) çalışma alanına gidin ve aşağıdaki özellikleri listelendikleri sırada açın:

1. Satınalma siparişi stok hareketlerini yükle ilişkilendir
2. Yük miktarlarının fazlasını alma

Daha fazla bilgi için bkz. [Kayıtlı ürün miktarlarını satınalma siparişlerine göre deftere nakletme](/dynamics365/supply-chain/warehousing/inbound-load-handling).
