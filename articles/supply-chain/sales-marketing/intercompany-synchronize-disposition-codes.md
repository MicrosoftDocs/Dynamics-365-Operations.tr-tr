---
title: Değerlendirme kodlarını eşitleme
description: Bu konuda, şirketlerarası ticaret için değerlendirme kodlarının eşitlenmesi açıklanmaktadır
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
ms.openlocfilehash: 27b587e576900f2b7f7fed7ee2a27a282306f0fe
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671772"
---
# <a name="synchronize-intercompany-disposition-codes"></a>Şirketlerarası değerlendirme kodlarını eşitleme

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management şirketlerarası iadeleri desteklemek için harici olarak tanımlanmış değerlendirme kodlarını karşılık gelen dahili değerlendirme kodlarına eşitlemenize olanak tanır. Şirketlerarası bir zincir kurulurken birbirine eşitlenen iki şirketteki değerlendirme eylemleri aynı olmalıdır. Farklılarsa eşitleme süreci başarısız olacaktır.

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>Üç taraflı doğrudan iadelerin değerlendirme kodları hakkında

Değerlendirme kodları şirketlerarası satış siparişi satırından alınarak özgün satış siparişi satırıyla eşitlenir. Ancak, eşitlemenin özgün satış siparişi satırı üzerinde yalnızca bir adet anlık etkisi vardır. Bu etki, A Şirketinde oluşturulan değerlendirme koduna ve çeşitli masraflara dayalı olarak çeşitli satır masraflarının silinmesidir. A Şirketi, iade siparişini oluşturan şirkettir.

Üç taraflı bir doğrudan teslimat zincirinde tüm değerlendirme eylemleri şirketlerarası satış siparişi satırında desteklenir. Ancak, bir ürün müşteriye iade ediliyorsa iade siparişindeki teslimat adresinin özgün siparişte belirtilen müşteri teslimat adresiyle eşleştiğini teyit etmelisiniz.

> [!NOTE]
> Değerlendirme kodları satın alma siparişleri için mevcut değildir. Bu nedenle, şirketlerarası satış siparişinden alınan değerlendirme kodlarının özgün iade siparişine eşitlemesi, satış siparişinden satış siparişine gerçekleştirilmelidir.

## <a name="replacing-returned-items"></a>İade edilen maddelerin yenilenmesi

İade edilen madde yenilenirse ve Şirket B'de bir yenileme siparişi zaten oluşturulmuşsa bir değerlendirme kodu seçilemez ve Şirket A'da hiçbir ilave yenileme siparişi oluşturulamaz.

## <a name="rules-for-intercompany-direct-deliveries"></a>Şirketlerarası doğrudan teslimatlar için kurallar

Şirketlerarası doğrudan teslimatları içeren senaryolardaki özgün iade siparişleri için aşağıdaki genel kurallar geçerlidir:

- Özgün satış siparişi satırındaki temel değerlendirme eylemi Alacak ve Hurda, Alacak veya Müşteriye İade ise Alacak değerlendirme eylemi uygulanır. Ancak, Müşteriye İade eylem kodu mevcut satırdaki ve şirketlerarası satış siparişinden alınmış yeni eşitlenen satırdaki net tutarı 0 (sıfır) olarak belirler. Ayrıca, hurda satırları hiçbir zaman eşitlenmez. Şirketlerarası satış siparişine bir satır eklendiğinde bu hiçbir zaman pozitif miktara sahip bir satış siparişiyle ve Hurda'nın değerlendirme eylemiyle eşitlenmez (örneğin, Alacak ve Hurda veya Yenile ve Hurda).
- Alacak ve Yenile veya Hurda ve Yenile'nin temel değerlendirme eylemi geçersiz kılınamaz. Bu, Alacak ve Yenile veya Hurda ve Yenile'nin bir değerlendirme eylemi olarak kabul edilir. Bu kural, A Şirketinde hiçbir hurda satırı oluşturulmasa ve B Şirketinde (iade edilen ürünü alan şirket) herhangi bir yenileme siparişi oluşturulmasa bile geçerlidir. Yenileme siparişi Şirket A'da yalnızca bir sevk irsaliyesi güncelleştirmesi gerçekleştirildiğinde oluşturulur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
