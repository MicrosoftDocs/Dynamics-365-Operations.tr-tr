---
title: Konsinye
description: "Bu konuda, gelen konsinye stok işlemlerinin nasıl yapılacağı açıklanır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchVendorPortalConfirmedOrders
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: d9dcdd63649d6dbff96efe2eec7cad34025ab2ee
ms.lasthandoff: 03/31/2017


---

# <a name="consignment"></a>Konsinye

Bu konuda, gelen konsinye stok işlemlerinin nasıl yapılacağı açıklanır.

Konsinye stok, satıcıya ait olan ancak tesisinizde depolanan stoktur. Stoğu tüketmeye veya kullanmaya hazır olduğunuzda stoğun sahipliği size geçer. Bu konu, eldeki stokun satıcıya ait genel muhasebe hareketlerini oluşturmadan fiziksel olarak alma hakkında bilgi içerir nasıl burada satıcıya ait stok fiziksel olarak rezerve üretim işlemi başlatılır. Ve tüketimi üretim emri işlem bir parçası olarak işlem yapabilmek için hammadde sahipliğini değiştirmek nasıl. Satıcıların, satıcı iş birliği arabirimini kullanarak nasıl kendi stok tüketimlerini izleyebilecekleri hakkında bazı bilgiler de bulunur. Gelen konsinye işlemlerini etkinleştirme ve yapılandırma hakkında daha fazla bilgi için bkz. [Konsinyeyi ayarlama](set-up-consignment.md).

## <a name="overview-of-the-consignment-process"></a>Konsinye işlemine genel bakış
Bu örnek senaryoda, USMF şirketinin ABD-104 satıcısıyla hammadde M9211CI üzerine bir konsinye sözleşmesi bulunuyor.

1.  Konsinye stok yenileme siparişi, beklenen talebe göre USMF'den bir kişi tarafından el ile oluşturulur. Bu sipariş ABD-104 satıcısı için oluşturulur ve MS9211CI maddesi için bir satır eklenir.
2.  Satıcı, beklenen teslim hakkında bilgilendirilir. Bu, aşağıdaki üç yoldan biriyle yapılabilir:
    -   USMF'de çalışan biri, satıcıya sipariş bilgilerini gönderir.
    -   Satıcı, satıcı iş birliği arabirimini kullanarak beklenen eldeki stoğu izler.
    -   USMF'de çalışan birisi **Eldeki stok** sayfasındaki verileri yalnızca giriş durumu **Sipariş edildi** olan ABD-104 satıcısına ait kayıtları göstermek için verileri filtreler ve bu bilgileri satıcıya gönderir.

3.  Stok, ABD-104'ten USMF'ye teslim edilir.
4.  Malzeme USMF'ye geldiğinde, konsinye stok yenileme siparişi ürün girişiyle güncelleştirilir. Yalnızca satıcıya ait stoğun fiziksel miktarları kaydedilir. Stok hala satıcıya ait olduğu için oluşturulmuş genel muhasebe hareketleri yoktur.
5.  Satıcı, eldeki fiziksel stok güncelleştirmelerini **Eldeki konsinye stok** sayfasından görüntüler.
6.  Fiziksel stok ele geçtikten sonra, üretim işlemi satıcıya ait stok olarak ayrılır ve M9211CI hammaddesini tüketecek olan mamul mallar için üretim emri verilir.
7.  Bugünün üretiminde tüketilecek rezerve edilmiş hammaddelerin sahibi ABD-104 iken USMF olarak değiştirilir. Bu, Stok sahipliği değişiklik günlüğü kullanılarak yapılır. Bu işlem, **Kaynak** alanı **Konsinye** olarak ayarlanan satınalma siparişlerini oluşturur.
8.  Satıcı, tüketimi (mülkiyet değişikliğini) **Konsinye stoktan alınan ürünler** sayfasından izler ve iki şirket arasındaki sözleşmelere göre bir fatura hazırlar.
9.  Üretim süreci, üretim malzeme çekme listesi aracılığıyla hammaddeyi tüketir. Fiziksel rezervasyon, eldeki stok sahibinin USMF olduğunu yansıtmak için otomatik olarak güncellenir.
10. ABD-104'ten gelen fatura, stok sahipliği değişiklik günlüğü işleme alındığında otomatik oluşturulan satınalma siparişleri göz önüne alınarak işlenir. Tüketilen stok için satıcı ABD-104'e ödeme yapılır.

USMF ilave periyodik işlemleri gerçekleştirir:

-   Satıcıya ait stoğun farklı ambarlar arasındaki fiziksel hareketi, transfer günlüğü kullanılarak işlenir.
-   Eldeki fiziksel stok,** Madde sayımı **günlüğü kullanılarak güncelleştirilir. Sayım, satıcının izni varsa eldeki stok güncelleştirmesi için de kullanılabilir.

Satıcı, ABD-104 **Eldeki konsinye stok** sayfasını kullanarak güncelleştirmeleri izleyebilir.

## <a name="consignment-replenishment-orders"></a>Konsinye stok yenileme siparişleri
Konsinye stok yenileme siparişi, satıcının sipariş edilen stok hareketleri oluşturarak belirli bir tarih aralığında teslim etmeyi planladığı ürün stok miktarlarının talebi ve takibi için kullanılan belgedir. Bu belge genellikle, belirli ürünlerin tahmini ve fiili talebine dayalıdır. Konsinye stok yenileme halinde alınacak stok, satıcının sahipliğinde kalır. Yalnızca fiziksel giriş güncelleştirmesine bağlı ürünlerin sahipliği kayıt altına alınır ve bu nedenle de genel muhasebe hareketi güncelleştirmeleri bulunmaz. **Sahip** boyutu hangi stoğun satıcıya, hangisinin ise teslim alma tüzel kişiliğine ait oluğunu ayırmak için kullanılır. Konsinye stok yenileme emri satırları içerir bir **açık sipariş** durum satırları tam miktarı alınan veya iptal edildiği değil sürece. Tam miktarı alınan ya da iptal durumu değiştirildi **tamamlandı**. Konsinye stok yenileme siparişiyle bağlantılı olan fiziksel eldeki stok, Kayıt işlemi veya Ürün girişi güncelleştirme işlemi kullanılarak kaydedilir. Madde varışı işleminin bir parçası olarak ya da sipariş satırları el ile güncelleştirilerek kayıt yapılır. Ürün girişi güncelleştirme işlemi kullanıldığında, satıcılara malların teslim alınma bilgilendirmesinde de kullanılabilen ürün girişi günlüğüne kayıt yapılır. 

[![konsinye stok yenileme emri](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Stok sahipliği değişiklik günlüğü
Stok sahibinin satıcı yerine teslim alma tüzel kişiliği olarak değiştirilmesi, Stok sahipliği değişiklik günlüğü kullanılarak yapılır. Günlük için herhangi bir beklenen stok hareketi oluşturulmaz. Oluşturulan stok hareketleri, yalnızca nakledilen günlük ile ilişkili olanlardır. Günlük nakledildiğinde:

-   Satıcıya ait stok, **Satıldı** durumu ile birlikte **Sahiplik değişikliği ** başvurusuyla yayımlanır.
-   Eldeki stok, satınalma siparişinde bir ürün girişiyle güncelleştirilmiş stok hareketi kullanarak tüketen tüzel kişilik tarafından alınır. Bu, sipariş durumunu **Alındı** olarak belirler. Konsinye için kullanılan satınalma siparişlerinin **Kaynak** alanı **Konsinye** olarak ayarlanır.

Sipariş oluşturulduktan sonra konsinye satınalma sipariş satırları miktarının güncelleştirilmesi mümkün değildir. 

[![Stok mülkiyet değişiklik günlüğü](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Konsinye işlemlerdeki satıcı iş birliği
Gelen konsinye işlemlerle alakalı satıcı işbirliği arabiriminin üç sayfası vardır:

-   **Satınalma siparişleri****konsinye stok tüketme** -konsinye işleminden sahiplik değişikliğiyle ilgili sipariş bilgilerini gösterir ayrıntılı satın.
-   **Konsinye stoktan alınan ürünler**: Sahiplik değişikliği işlemi sırasında güncelleştirilen ürün girişleri bulunan maddeler ve miktarlar hakkında bilgileri gösterir.
-   **Eldeki konsinye stok**: Teslim edilmesi beklenen konsinye maddeler ve müşterinin işyerinde halihazırda fiziksel olarak bulunan maddeler hakkında bilgileri gösterir.



