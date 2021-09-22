---
title: Satış siparişi satırında bir madde yapılandırıldığında metnin üzerine yazılıyor
description: Satış siparişi satırında bir ürün yapılandırıldığında standart metin, değiştirilen metnin üzerine yazılıyor. Metni satırı yapılandırmadan önce değil, yapılandırdıktan sonra değiştirin.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 20239b9b0eecb355274e909a8b8b39450e468c7e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477802"
---
# <a name="item-text-is-overwritten-when-a-product-is-configured-on-a-sales-order-line"></a>Satış siparişi satırındaki bir ürün yapılandırıldığında madde metninin üzerine yazılıyor

## <a name="symptoms"></a>Belirtiler

Bu sorun, yapılandırılabilir bir madde için satış siparişi satırı oluşturup madde metnini değiştirdiğinizde oluşur. Maddeyi yapılandırıp **Tamam**'ı seçtiğinizde standart metin, metnin üzerine yazılıyor.

## <a name="resolution"></a>Çözüm

Bu davranış beklenmektedir. Metin alanı, yalnızca satır yapılandırıldıktan sonra doldurulan varyant adını içerir. Bu nedenle, metni satırı yapılandırmadan önce değil, sonra değiştirmeniz gerekir.
