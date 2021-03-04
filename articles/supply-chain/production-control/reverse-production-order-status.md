---
title: Üretim emri durumunu tersine çevirme
description: Bu konuda, üretim emri durumunun tersine çevrilmesi açıklanmaktadır.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdParmStatusDecrease, ProdSetupStatusDecrease
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7529e6c2bd7cb6b8386565c9f19075e56a65d3c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439283"
---
# <a name="reverse-the-production-order-status"></a>Üretim emri durumunu tersine çevirme

[!include [banner](../includes/banner.md)]

Bu konuda, üretim emri durumunun tersine çevrilmesi açıklanmaktadır. 

Bir üretim emrinin durumunu tersine çevirirseniz, emrin kendisi ve rotalarla ilişkili tüm operasyonlar üretim döngüsündeki önceki bir adıma geri döner. Örneğin, bir üretim emrinin durumunu **Planlandı** ise ve durumu yeniden **Oluşturuldu** olarak değiştirirseniz. Bu durumda, sistem önce durumu **Tahmini** olarak değiştirir ki bu **Planlandı**'nın hemen öncesindeki durumdur. Daha sonra durumu istediğiniz **Oluşturuldu** durumuna değiştirebilir. **Not:** Emriniz **Tamamlandı bildirimi** durumuna geldiyse, yine de önceki bir duruma geri döndürebilirsiniz. Ancak emirdeki bilgileri güncellemek için tahmini ve operasyon planlamasını, iş planlamasını veya her iki planlama türünü yeniden çalıştırmanız gerekir. Bu adım gereklidir çünkü kalan madde tüketimi ve operasyon kaynakları tüketimi rezervasyonları da sıfırlanmalıdır. Bu makalenin geri kalanında, bir üretim emrini aşağıdaki şekillerde tersine çevirdiğinizde neler olduğu anlatılmaktadır:

-   **Tahmin**'den **Oluşturuldu**'ya
-   **Planlandı**'dan **Tahmin**'e
-   **Serbest bırakıldı**'dan **Planlandı**'ya
-   **Başlatıldı**'dan **Serbest bırakıldı**'ya

## <a name="from-estimated-to-created"></a>Tahmin'den Oluşturuldu'ya
Bir üretim emrinin durumunu **Tahmin**'den **Oluşturuldu**'ya çevirdiğinizde, ürün reçetesindeki maddeler için hesaplanan madde tüketimi kaldırılır. Üretim satırındaki stok hareketleri silinir ve üretim emri ürün reçetesi satırlarındaki **Artık durumu** alanı **Bitti** olarak sıfırlanır. **Türetilmiş satınalmalar** ve **Türetilmiş üretim** seçenekleri seçildiğinde, altta yatan satınalma emirleri veya üretim emirleri silinir. Üretim emrinin maliyetini tahmin ettiyseniz veya maddeleri üretimde kullanılabilmeleri için manuel olarak ters çevirdiyseniz, bu hareketler kaldırılır.

## <a name="from-scheduled-to-estimated"></a>Planlandı'dan Tahmin'e
Bir üretim emrinin durumunu **Planlandı**'dan **Tahmin**'e çevirirseniz, planlanan başlangıç ve bitiş tarihleri ve saatleri kaldırılır. Planlama sırasında yapılan kapasite rezervasyonları kaldırılır ve iş planlama sırasında oluşturulan işler silinir. Operasyon planlaması ve iş planlaması ile ilgili olarak **Üretim emri ayrıntıları** sayfasında kayıtlı tüm bilgiler sıfırlanır.

## <a name="from-released-to-scheduled"></a>Serbest bırakıldı'dan Planlandı'ya
Bir üretim emrinin durumunu **Serbest bırakıldı**'dan **Planlandı**'ya çevirirseniz, gerçekleşecek tek değişiklik durum alanındaki değerdir.

## <a name="from-started-to-released"></a>Başlatıldı'dan Serbest bırakıldı'ya
Bir üretim emrinin durumunu **Başlatıldı**'dan **Serbest bırakıldı**'ya çevirirseniz, bitmiş olarak raporlanan tüm maddeler tersine çevrilir. Malzeme alındıysa ve üretime gelen ve giden teslimatlar yapıldıysa, bu ayarlar tersine çevrilir. Üretim emrinin ürün reçetesi satırlarındaki **Artık durumu** alanı **Bitti**'den **Malzeme tüketimi**'ne değiştirilir. Saat kayda geçirildiyse veya üretim rotasındaki operasyonlar için miktarlar bitti şeklinde rapor edildiyse, bu ayarlar ters çevrilir. **Artık durumu** alanı, üretim rotasında **Bitti**'den **Rota tüketimi**'ne değiştirilir. Devam eden olarak veya süren iş olarak nakledilen tüm maddelere yönelik ayarlar ters çevrilir. **Üretim emri ayrıntıları** sayfasında, başlatılmış veya bitmiş olarak raporlanmış bir miktar gösteren alanlar sıfırlanır. Bu hareketlere yönelik tarihleri de sıfırlanır.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]