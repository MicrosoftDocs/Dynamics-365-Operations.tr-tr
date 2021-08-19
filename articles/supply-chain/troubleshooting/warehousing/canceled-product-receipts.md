---
title: İptal edilen ürün girişleri hareket durumunu Kaydedildi olarak güncelleştirmez
description: Gelen yükteki ürün girişlerini iptal ettikten sonra, sistem stok hareket durumunu otomatik olarak Alındı yerine Sipariş Edildi olarak güncelleştirir.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eae703ce0b2c981518b18c4badd4f90031b902ece62f3ca0837427b306d618b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731115"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>İptal edilen ürün girişleri hareket durumunu Kaydedildi olarak güncelleştirmez

## <a name="symptoms"></a>Belirtiler

Gelen yükteki **Ürün girişlerini iptal et** eylemini çalıştırdıktan sonra, sistem stok hareketlerinin durumunu otomatik olarak *Alındı* yerine *Sipariş Edildi* olarak güncelleştirir.

## <a name="resolution"></a>Çözüm

Sevk irsaliyeleri giden yükler için iptal edildiğinde, stok hareketlerinin durumu *Çekildi* olarak kalır. Ancak, gelen yükten gelen ürün girişleri iptal edildiğinde, stok hareketlerinin durumu *Kayıtlı* durumuna geri döndürülmez. Bu nedenle, gelen yükten gelen bir ürün girişi iptal edildikten sonra, ambar çalışanının madde miktarlarını yükler için yeniden kaydetmesi gerekir.

Daha fazla bilgi için bkz. [Bir gelen yükte gelen madde miktarlarını kaydetme](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).
