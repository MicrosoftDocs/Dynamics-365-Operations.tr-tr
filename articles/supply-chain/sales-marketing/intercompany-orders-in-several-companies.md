---
title: Birkaç şirkette şirketlerarası satın alma ve satış siparişleri oluşturma
description: Bu konuda, birkaç şirkette şirketlerarası satın alma siparişlerinin veya satış siparişlerinin nasıl oluşturulacağı açıklanmaktadır
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 8458a08c1a2e5e656c496eb74188d0e2e7257020
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673732"
---
# <a name="creating-intercompany-purchase-and-sales-orders-in-several-companies"></a>Birkaç şirkette şirketlerarası satın alma ve satış siparişleri oluşturma

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management, yalnızca bir üretim şirketini ve birkaç satış şirketini işlemekle sınırlı değildir. Kurulumları şirketlerarası olarak yapılan tüm şirketler hem ticaret şirketleri hem de üretim şirketleri olabilirler.

Aynı maddeyi birden çok şirket sağlayabiliyorsa hangisinden satın alacağınızı serbestçe seçebilirsiniz ve bir satış siparişi birden fazla satın alma siparişi haline gelse de güncelleştirmeler işlenir.

Aynı şekilde, otomatik olarak bir şirketlerarası satın alma siparişi oluşturduğunuzda şirketinizde özgün bir satış siparişi oluşturabilir ve çeşitli şirketlerarası satıcı firmaların birden fazla satın alma siparişi oluşturarak siparişi karşılamalarını sağlayabilirsiniz. Microsoft Dynamics 365 Supply Chain Management, satış şirketlerinde otomatik olarak şirketlerarası satış siparişleri oluşturur.

Bunu yapmak için tüm şirketler ticari ilişkiler olarak kurulmalıdır. Satıcı şirketler, Microsoft Dynamics 365 Supply Chain Management uygulamasında şirketlerarası satıcılar olarak ayarlanmalı ve ilgili madde için birincil satıcı olmalıdır. Satış siparişindeki **Başlık görünümü**'nde, **Şirketlerarası siparişleri otomatik oluştur** alanını ve **Şirketlerarası ayarlar** hızlı sekmesinde **Doğrudan teslimat** alanını seçmelisiniz. Bu, varsayılan ayardır.

Satış satırlarını her zamanki gibi oluşturursunuz. Kayıttan çıktığınızda şirketlerarası satın alma siparişlerinin ve şirketlerarası satış siparişlerinin oluşturulduğunu bildiren bir ileti görüntülenir. İleti, yeni siparişlere bağlantılar içerir. Satış şirketlerinizde oluşturulan şirketlerarası satış siparişlerini görüntülemek için özgün satış siparişini açın ve **Genel** sekmesinde **İlgili bilgiler** grubunda **Referanslar**'ı seçin.

Satıcılar için şirketlerarası satın alma siparişlerini açarsanız Microsoft Dynamics 365 Supply Chain Management uygulamasının her bir satıcı için özgün satış siparişi numarasını ve şirketlerarası satış siparişi numarasını otomatik olarak doldurduğunu görürsünüz.

Benzer şekilde, satıcılar için şirketlerarası satış siparişlerini açarsanız Microsoft Dynamics 365 Supply Chain Management uygulamasının her satıcı için özgün satış siparişi numarasını ve şirketlerarası satın alma siparişi numarasını otomatik olarak doldurduğunu görürsünüz.

> [!NOTE]
> Siparişteki maddeler şirketlerarası satış şirketlerinizden birinde mevcut diğerinde mevcut değilse Microsoft Dynamics 365 Supply Chain Management, maddelerin mevcut olduğu satıcı şirket için şirketlerarası siparişleri oluşturur ancak diğer şirket için sipariş oluşumunu durdurur. Bu durumda bir bildirim iletisi görüntülenir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
