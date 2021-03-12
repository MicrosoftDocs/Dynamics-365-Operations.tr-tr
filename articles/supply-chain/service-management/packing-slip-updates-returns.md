---
title: İadeler için sevk irsaliyesi güncelleştirmeleri
description: İade edilen maddelerin stoka alınabilmesi için, ait oldukları sevk irsaliyesinin güncelleştirilmesi gerekir.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c82e43beddb8bae0a56b0894ce484ca7605b42e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006728"
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

  


