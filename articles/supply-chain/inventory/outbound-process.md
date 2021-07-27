---
title: Giden işleme genel bakış
description: Bu konu, Stok Yönetimi'nde giden işlemine genel bakış sağlar.
author: perlynne
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "274363"
- intro-internal
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 29029cfa032f36c4dc0590ff76f44417dc056ef8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348817"
---
# <a name="outbound-process-overview"></a>Giden işleme genel bakış

[!include [banner](../includes/banner.md)]

Bu konu, Stok Yönetimi'nde giden işlemine genel bakış sağlar.

## <a name="output-orders"></a>Çıkış emirleri

Çıkış siparişleri, satış siparişi satırlarını ve transfer siparişi satırlarını giden çekme listelerini kullanan çekme işlemleri ile bağlamak için kullanılır.

Çekme listeleri satış siparişleri veya nakil siparişlerinden oluşturulduğunda, çıkış emirleri ve sevkiyatlar otomatik olarak oluşturulur. Bir çekme listesinin bir sevkiyat ile birebir bir ilişkisi vardır. Bir transfer emri sevkiyatı veya satış siparişi sevk irsaliyesi, sevkiyattan işlenebilir. 

Aşağıdaki diyagram, giden siparişler için işlemin genel bakışını gösterir. 

[![Giden sipariş işlemine genel bakış.](./media/outbound-order.png)](./media/outbound-order.png)

Programın çıkış sürecini nasıl uygulanacağını tanımlamak için çıkış kuralları ayarlayabilirsiniz. Sevkiyat sürecini denetlemek için bu kuralları kullanabilirsiniz. Özellikle, bir sevkiyatın gönderilebileceği işlemin aşamasını denetlemek için bu kuralları kullanabilirsiniz. Aşağıdaki ayarlar, giden işlemlerin nasıl işleneceğini tanımlar.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Satış siparişleri ve transfer emirleri için çekme rotası 

**Alacak hesapları** \> **Kurulum** \> **Alacak hesapları parametreleri**'ne gidin ve sonra **Güncelleştirmeler** sekmesinde, **Çekme rotası durumu** alanında bir değer seçin.

[![Satış siparişleri için çekme rotası durum alanı.](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

**Çekme rotası durumu** alanı **Tamamlandı** olarak ayarlandıysa, çekme işlemi çekme listesi oluşturma işleminin parçası olarak otomatik gerçekleşir. Alan **Etkinleştirildi** olarak ayarlandıysa, malzeme çekme listesi satırlarının el ile güncelleştirilmesi gerekir.

Aynı kurulum transfer emirlerine de uygulanır. **Stok yönetimi** \> **Kurulum** \> **Stok ve ambar yönetim parametreleri**'ne gidin ve sonra **Taşıma** sekmesinde, **Çekme rotası durumu** alanında bir değer seçin.

[![Transfer emirleri için çekme rotası durum alanı.](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Stok çıkış emirlerini sonlandır

**Stok yönetimi** \> **Kurulum** \> **Stok ve ambar yönetimi parametreleri**'ne gidin ve sonra **Genel** sekmesinde, **Çıkış stok siparişini sonlandır** seçeneğini ayarlayın.

[![Stok çıkış emrini sonlandır seçeneği.](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Ambar çalışanı malzeme çekme listesi miktarlarını azalttığında, karşılık gelen stok sipariş miktarları sevkiyattan çıkarılır. Malzeme çekme listesi belirli bir zamanda güncelleştirildiğinde, **Stok çıkış siparişini sonlandır** seçeneği **Evet** olarak ayarlanmışsa kalan miktarlar siparişe geri bildirilir. **Stok çıkış siparişini sonlandır** seçeneği **Hayır** olarak ayarlanmışsa, kalan miktarlar açık çıkış siparişi miktarı olarak tutulur ve yeni bir malzeme çekme listesine **Açık çıkış siparişleri** işlevinin bir parçası olarak eklenmelidir. 

[![İşlevler menüsünde açık çıkış emirleri komutu.](./media/open-output-order.png)](./media/open-output-order.png)

[![Açık çıkış emirleri sayfasındaki İşlevler menüsü.](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Miktarı azalt

Malzeme çekme listelerini oluşturmak işleminin parçası olarak kullanabileceğiniz üçüncü parametre **Miktarı azalt** parametresidir. Bu parametreyi ayarlamak, ambara serbest bırakmayı rezervasyon işlemini tetikleyen **Rezervasyon** ayarı ile birlikte çalışır.

[![Miktar azaltma parametresi.](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Bir satış siparişi için çıkan işleme örnek

Bu örnekte, iki madde için bir satış siparişi vardır. Malzeme çekme listesi oluşturulmasında **Miktarı azalt** parametresini seçebilirsiniz. Bu nedenle, yalnızca eldeki stok için serbest bırakır ve çekme satırlarını oluşturursunuz. Çekme, malzeme çekme listeleri için bir kayıt işlemi olarak raporlanması gerekir (**Çekme rotası durumu** = **Etkinleştirildi**).

Malzeme çekme listesi oluşturulması sırasında halihazırda rezerve edilmemiş olan stok. Kullanılabilir stok satış siparişinden çıkartılabilir veya çekmek için kullanılabilir olduğunda daha sonra işlenmek üzere ambara serbest bırakılabilir.

[![Malzeme çekme listesini güncelleştirme.](./media/update-picking-list.png)](./media/update-picking-list.png)

Tüm çekme satırları **Çekme listesi kayıt** sayfası üzerinde çekildikten sonra, ilişkilendirilen sevkiyat tamamlanır. Daha sonra satış siparişi sevk irsaliyeleri için işlem, çekilen stoka dayalı olarak başlatılabilir.

[![Giden sevkiyatları güncelleştirme.](./media/outbound-shipments.png)](./media/outbound-shipments.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]