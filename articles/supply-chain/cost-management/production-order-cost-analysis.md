---
title: Üretim emri maliyet analizi
description: Bu makalede, tamamlanmış ve geçerli üretim emirleri için yapabileceğiniz maliyet analizi hakkında bilgiler sağlanmıştır. Tahmini maliyetleri ve gerçek maliyetleri Fiyat hesaplaması sayfasını veya Maliyet tahminleri ve maliyetlendirmeler raporunu kullanarak analiz edebilirsiniz. Her bir bileşen maddesine, rota operasyonuna ve dolaylı maliyete yönelik tahmini ve gerçek maliyetler (ve miktar) hakkındaki bilgileri görüntüleyebilirsiniz.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage, ProdSetupHistoricalCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79634
ms.assetid: ded5da04-f787-49f7-b5e5-75c2a2b92930
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0858e0e9ed0f09a47954274a05f6da1a2537c4a3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967295"
---
# <a name="production-order-cost-analysis"></a>Üretim emri maliyet analizi

[!include [banner](../includes/banner.md)]

Bu makalede, tamamlanmış ve geçerli üretim emirleri için yapabileceğiniz maliyet analizi hakkında bilgiler sağlanmıştır. Tahmini maliyetleri ve gerçek maliyetleri Fiyat hesaplaması sayfasını veya Maliyet tahminleri ve maliyetlendirmeler raporunu kullanarak analiz edebilirsiniz. Her bir bileşen maddesine, rota operasyonuna ve dolaylı maliyete yönelik tahmini ve gerçek maliyetler (ve miktar) hakkındaki bilgileri görüntüleyebilirsiniz.

Bir üretim emri için gerçek maliyetler raporlanan malzeme tüketimi ve rota operasyonlarına dayanır. Bir üretim emrine yönelik malzeme tüketimi, rota operasyonları ve dolaylı maliyetler hakkındaki ayrıntılı hareketlere **Üretim deftere nakil** sayfasından erişebilirsiniz.

## <a name="variance-analysis-for-a-completed-production-order"></a>Tamamlanmış bir üretim emrindeki farkları analiz etme
Farklar, raporlanan üretim faaliyetleri ile üretim maddesinin standart maliyet hesaplaması arasındaki karşılaştırmayı yansıtır. Farklar, üretim emrinin tahmini maliyetleri ile karşılaştırmayı yansıtmaz. Raporlanan üretim faaliyetleri, ilişkilendirilmiş dolaylı maliyetler ve bitmiş olarak raporlanan miktarla birlikte malzeme tüketimini ve rota operasyonlarını içerir. Aşağıdaki dört fark türü hesaplanır:

-   Lot büyüklüğü farkı
-   Üretim miktar farkı
-   Üretim fiyat farkı
-   Üretim yedekleme farkı

Aşağıdaki diyagramda, bir üretim emrinin gerçek maliyetleriyle, üretim emrinin sonlandırılması anında maddenin maliyet kaydı içersindeki hesaplanan maliyetler arasındaki farkı açıklayan dört fark gösterilmektedir. 

![Tamamlanmış bir üretim emrindeki farklılıkları dikkate alan farklar](./media/control.jpg) 

**Fark** sayfasını veya **Üretim farkı** raporunu kullanarak üretim farklarını analiz edebilirsiniz. Ayrıntılı farkları maddeye ve operasyon kaynağına veya maliyet grubuna göre görüntülemek için görüntüleme seçeneklerini kullanın. Stok parametrelerindeki maliyet kırılımına yönelik ilke, farkların maliyet grubunca izlenip izlenmeyeceğini belirler. Özetlenmiş farkları görüntülemek için **tekli**, **çoklu** ve **toplam** görüntüleme seçeneklerini de kullanabilirsiniz. Ayrıntılı fark bilgileri, her farkın kaynağını anlamanıza yardımcı olur. Bir üretim emrini sonlandırmadan önce farkları tahmin etmek için, **Maliyet tahminleri ve maliyetlendirme** raporunda sağlanan ayrıntılı bilgileri analiz edin.

## <a name="cost-analysis-for-current-production-orders"></a>Geçerli üretim emirleri için maliyet analizi
Ayrı raporlar, her hareket tipi için bilgi sağlar. Raporlanan üretim faaliyetleri için maliyetleri analiz etmek için bu raporları kullanın. Yalnızca **Başlatıldı** veya **Bitmiş olarak raporlandı** durumuna sahip geçerli üretim emirlerine yönelik bilgiler görüntülenir.

-   **Süren malzemeler**− Bu rapor, belirtilen bir hareket tarihi itibariyle geçerli üretim emirlerine yönelik olarak raporlanan malzeme çekme listesi hareketlerini listeler. Rapor, çıkarılan bir bileşenin miktarını ve her bir hareket için maliyet tutarını gösterir. Tek bir bileşen maddesi için seçim ölçütünü kullanın. Örneğin, bileşenin geçerli üretim emirlerine karşı çıkarılan miktarı hakkındaki bilgileri yazdırabilirsiniz. Çıkarılan miktar, üst madde için bitmiş olarak raporlanan miktarlar ile güncellenmez. Bu nedenle, işlem gören hammaddelerin gerçek miktarı fazla gösterilebilir.
-   **Süren iş** − Bu rapor, belirtilmiş bir hareket tarihi itibariyle geçerli üretim emirlerine karşı raporlanmış rota hareketlerini (veya iş hareketlerini) listeler. Rapor, her bir hareket için raporlanan saatleri, tutarı ve miktarı (hem sağlam ürün miktarı hem de hata miktarı) gösterir. Ayrıca operasyon numarası, operasyon kimliği ve operasyon kaynağı gibi bilgileri de içerir. Aynı zamanda bu rapor, üretim emrine karşı tüm hareketler için toplam zamanı ve tutarı ve bitmiş olarak raporlanan miktarı da gösterir.
-   **Süren dolaylı maliyetler** − Bu rapor, üretim emirlerine karşı tahakkuk eden dolaylı maliyetleri listeler. Bu veri, belirtilen bir hareket tarihi itibariyle rota operasyonlarının ve bileşenlerin raporlanan tüketimine dayalıdır. Rapor dolaylı maliyetin tipini (ek talep veya oran), dolaylı maliyetin maliyetlendirme tablosu kodunu ve her hareketin maliyet tutarını gösterir. Bu rapor, dolaylı maliyeti oluşturan rota kartı veya malzeme çekme listesi hareketiyle ilgili bilgi sağlamaz.
-   **Süren üretim maliyeti** − Bu rapor belirtilen bir hareket tarihi itibariyle üretim emirlerine karşı malzeme, rota operasyonları ve dolaylı maliyetlerin birleşik tüketimini listeler.
-   **Süren bitmiş maddeler** − Bu rapor, belirtilen bir hareket tarihi itibariyle geçerli üretim emirlerini ve bitmiş olarak raporlanan hareketleri listeler.


<a name="additional-resources"></a>Ek kaynaklar
--------

[Üretim farklarının ortak kaynakları](common-sources-of-production-variances.md)



