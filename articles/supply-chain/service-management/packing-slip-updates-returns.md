---
title: İadeler için sevk irsaliyesi güncelleştirmeleri
description: İade edilen maddelerin stoka alınabilmesi için, ait oldukları sevk irsaliyesinin güncelleştirilmesi gerekir.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 021cf6c0ff606e4b5a7139285fe7508283fb9fe2
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675697"
---
# <a name="packing-slip-updates-for-returns"></a>İadeler için sevk irsaliyesi güncelleştirmeleri  

[!include [banner](../includes/banner.md)]


İade edilen maddelerin stoka alınabilmesi için, ait oldukları sevk irsaliyesinin güncelleştirilmesi gerekir. Fatura güncelleştirme süreci nasıl mali hareketin güncelleştirilmesi ise, sevk irsaliyesi güncelleştirme süreci de stok kaydının fiziksel olarak güncelleştirilmesidir; başka bir deyişle, değişiklikleri stoka kaydeder. İadelerde ise, elden çıkarma eylemine atanan adımlar, sevk irsaliyesinin güncelleştirilmesi sırasında uygulanır.

Sevk irsaliyesi güncelleştirmesi, madde geliş günlüğünde veya iade siparişinde işlenebilir.

Sevk irsaliyesi deftere nakletme sürecinin bir parçası olarak, müşterinin sevkiyat belgelerindeki sevk irsaliyesi referans numarası sipariş satırlarıyla ilişkilendirilebilir. Bu ilişkilendirme isteğe bağlıdır ve yalnızca referans amaçlıdır. Bu, herhangi bir hareket güncelleştirmesi oluşturmaz.

Beklenen tüm iade edilen maddeler gelmediyse, yalnızca sevk irsaliyesi güncelleştirmesinde alınan miktarı dahil etmeniz gerekir. İade sevkiyatının geri kalanı gelene kadar kalan maddeleri siparişte bırakın.

Bir madde karantinadan Sevkiyat ve Teslim Alma departmanına gönderildiyse (karantina denetçisinin maddeyi stokta nereye depolayacağını bilmediği durumlar gibi), karantinanın bir sonucu olarak belirtilen elden çıkarma kodunu uygun şekilde kaydetmek ve uygun işlemi yapmak için ilgili sevk irsaliyesinin güncelleştirilmesi gerekir.

Bir satış sözleşmesindeki iade edilen madde için sevk irsaliyesini güncelleştirildiğinizde, bu maddeye ilişkin satış sözleşmesi taahhüdü tutar veya miktar değişikliğini yansıtmak için otomatik olarak güncelleştirilir. 

## <a name="see-also"></a>Ayrıca bkz.

[İadeler için fatura güncelleştirmeleri gerçekleştirme](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]