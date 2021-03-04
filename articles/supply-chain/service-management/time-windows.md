---
title: Zaman pencereleri
description: Servis siparişi satırlarının planlamasını en iyi duruma getirmek için zaman aralıkları kullanabilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d79e3d3756b8dc402d6f293437209b2e108be38e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439458"
---
# <a name="time-windows"></a>Zaman pencereleri  

[!include [banner](../includes/banner.md)]

Servis siparişi satırlarının planlamasını en iyi duruma getirmek için zaman aralıkları kullanabilirsiniz. Sistemi otomatik olarak sistem siparişleri oluşturacak şekilde ayarlayabilirsiniz. Zaman aralığı tarafından belirlenen ölçütleri temel alarak olabildiğince az sayıda servis siparişine olabildiğince çok servis siparişi satırı bağlayabilirsiniz.

Zaman aralıkları, servis siparişi satırının hesaplanan tarih itibariyle ne kadar ilerlediğini belirtir. Hesaplanan tarih, servis siparişi satırının gerçekleştirilmesinin planlandığı tarihtir. Tarih, aralık ayarı ve **Servis siparişleri oluşturma** sayfasında tanımladığınız servis dönemini temel alır. Zaman aralığını aşağıdaki tablodaki değerleri kullanarak tanımlarsınız.

| Yöntem | Tanım                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hafta   | Servis siparişi satırı, ilk hesaplanan tarihle aynı hafta içindeki herhangi bir açık güne taşınabilir.                                                                                                                                                                                    |
| Ay  | Servis siparişi satırı, ilk hesaplanan tarihle aynı ay içindeki herhangi bir açık güne taşınabilir. Örneğin, servis siparişi satırının hesaplanan tarihi 15 Şubat 2017 olsun. Servis siparişi satırı 1 Şubat ile 28 Şubat 2017 tarihleri arasındaki herhangi bir haftaya planlanabilir. |
| El ile | Servis siparişi satırının ilk hesaplanan tarihten önce veya sonra taşınabileceği maksimum gün sayısını tanımlarsınız.                                                                                                                                                                           |

Servis sözleşmesi satırı için zaman aralığı belirtmediyseniz servis sözleşmesinden türetilen servis siparişi satırı tam olarak ilk planlandığı tarihte olmalıdır.

## <a name="related-topics"></a>İlgili konular

[Zaman pencereleri oluşturma](create-time-windows.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]