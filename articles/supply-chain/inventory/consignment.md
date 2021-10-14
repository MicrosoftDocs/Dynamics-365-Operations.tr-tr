---
title: Konsinye ayarlama
description: Bu konuda, gelen konsinye stok işlemlerinin nasıl yapılacağı açıklanır.
author: yufeihuang
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchTablePart, PurchVendorPortalConfirmedOrders, DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4a1b96d18048a1ae6e380374f32d2bfa2270ae24
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577732"
---
# <a name="set-up-consignment"></a>Konsinye ayarlama

[!include [banner](../includes/banner.md)]

Bu konuda, gelen konsinye stok işlemlerinin nasıl yapılacağı açıklanır.

Konsinye stok, satıcıya ait olan ancak tesisinizde depolanan stoktur. Stoğu tüketmeye veya kullanmaya hazır olduğunuzda stoğun sahipliği size geçer. Bu konu, genel muhasebe defteri hareketleri oluşturmadan satıcının sahip olduğu eldeki stoku fiziksel olarak alma, satıcının sahip olduğu stokun fiziksel olarak ayrılabildiği bir üretimi başlatma hakkında bilgiler içerir. ve hammadde sahipliğinin, tüketimi, üretim siparişi işlemini yapabilmek için nasıl değiştirilebileceği. Satıcıların, satıcı iş birliği arabirimini kullanarak nasıl kendi stok tüketimlerini izleyebilecekleri hakkında bazı bilgiler de bulunur.

## <a name="overview-of-the-consignment-process"></a>Konsinye işlemine genel bakış

Bu örnek senaryoda, USMF şirketinin ABD-104 satıcısıyla hammadde M9211CI üzerine bir konsinye sözleşmesi bulunuyor.

1. Konsinye stok yenileme siparişi, beklenen talebe göre USMF'den bir kişi tarafından el ile oluşturulur. Bu sipariş ABD-104 satıcısı için oluşturulur ve MS9211CI maddesi için bir satır eklenir.
1. Satıcı, beklenen teslim hakkında bilgilendirilir. Bu, aşağıdaki üç yoldan biriyle yapılabilir:
    - USMF'de çalışan biri, satıcıya sipariş bilgilerini gönderir.
    - Satıcı, satıcı iş birliği arabirimini kullanarak beklenen eldeki stoğu izler.
    - USMF'de çalışan birisi **Eldeki stok** sayfasındaki verileri yalnızca giriş durumu **Sipariş edildi** olan ABD-104 satıcısına ait kayıtları göstermek için verileri filtreler ve bu bilgileri satıcıya gönderir.
1. Stok, ABD-104'ten USMF'ye teslim edilir.
1. Malzeme USMF'ye geldiğinde, konsinye stok yenileme siparişi ürün girişiyle güncelleştirilir. Yalnızca satıcıya ait stoğun fiziksel miktarları kaydedilir. Stok hala satıcıya ait olduğu için oluşturulmuş genel muhasebe hareketleri yoktur.
1. Satıcı, eldeki fiziksel stok güncelleştirmelerini **Eldeki konsinye stok** sayfasından görüntüler.
1. Fiziksel stok ele geçtikten sonra, üretim işlemi satıcıya ait stok olarak ayrılır ve M9211CI hammaddesini tüketecek olan mamul mallar için üretim emri verilir.
1. Bugünün üretiminde tüketilecek rezerve edilmiş hammaddelerin sahibi ABD-104 iken USMF olarak değiştirilir. Bu, Stok sahipliği değişiklik günlüğü kullanılarak yapılır. Bu işlem, **Kaynak** alanı **Konsinye** olarak ayarlanan satınalma siparişlerini oluşturur.
1. Satıcı, tüketimi (mülkiyet değişikliğini) **Konsinye stoktan alınan ürünler** sayfasından izler ve iki şirket arasındaki sözleşmelere göre bir fatura hazırlar.
1. Üretim süreci, üretim malzeme çekme listesi aracılığıyla hammaddeyi tüketir. Fiziksel rezervasyon, eldeki stok sahibinin USMF olduğunu yansıtmak için otomatik olarak güncellenir.
1. ABD-104'ten gelen fatura, stok sahipliği değişiklik günlüğü işleme alındığında otomatik oluşturulan satınalma siparişleri göz önüne alınarak işlenir. Tüketilen stok için satıcı ABD-104'e ödeme yapılır.

USMF ilave periyodik işlemleri gerçekleştirir:

- Satıcıya ait stoğun farklı ambarlar arasındaki fiziksel hareketi, transfer günlüğü kullanılarak işlenir.
- Eldeki fiziksel stok,**Madde sayımı** günlüğü kullanılarak güncelleştirilir. Sayım, satıcının izni varsa eldeki stok güncelleştirmesi için de kullanılabilir.

Satıcı, ABD-104 **Eldeki konsinye stok** sayfasını kullanarak güncelleştirmeleri izleyebilir.

## <a name="consignment-replenishment-orders"></a>Konsinye stok yenileme siparişleri

Konsinye stok yenileme siparişi, satıcının sipariş edilen stok hareketleri oluşturarak belirli bir tarih aralığında teslim etmeyi planladığı ürün stok miktarlarının talebi ve takibi için kullanılan belgedir. Bu belge genellikle, belirli ürünlerin tahmini ve fiili talebine dayalıdır. Konsinye stok yenileme halinde alınacak stok, satıcının sahipliğinde kalır. Yalnızca fiziksel giriş güncelleştirmesine bağlı ürünlerin sahipliği kayıt altına alınır ve bu nedenle de genel muhasebe hareketi güncelleştirmeleri bulunmaz.

**Sahip** boyutu hangi stoğun satıcıya, hangisinin ise teslim alma tüzel kişiliğine ait oluğunu ayırmak için kullanılır. Konsinye stok yenileme emir satırları, satırların tam miktarı alınmadığı veya iptal edilmediği sürece **Açık sipariş** durumuna sahiptirler. Tam miktar alındığında veya iptal edildiğinde, durum **Tamamlandı** olarak değişir. Konsinye stok yenileme siparişiyle bağlantılı olan fiziksel eldeki stok, Kayıt işlemi veya Ürün girişi güncelleştirme işlemi kullanılarak kaydedilir. Madde varışı işleminin bir parçası olarak ya da sipariş satırları el ile güncelleştirilerek kayıt yapılır. Ürün girişi güncelleştirme işlemi kullanıldığında, satıcılara malların teslim alınma bilgilendirmesinde de kullanılabilen ürün girişi günlüğüne kayıt yapılır.

[![Konsinye stok yenileme siparişleri.](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Stok sahipliği değişiklik günlüğü

Konsinye stoğun sahipliğinin satıcıdan konsinye stoğu tüketecek tüzel kişiliğe transferini kaydetmek için **Stok sahipliği değişiklik** günlüğü kullanılır. Günlük için herhangi bir beklenen stok hareketi oluşturulmaz. Diğer stok günlükleri gibi bir stok günlüğü adı ile tanımlanmalıdır. Bu adlar **Stok günlüklerinin adları** sayfasında oluşturulur ve **Günlük türü**, **Sahiplik değişikliği** olarak ayarlanmalıdır.

Oluşturulan stok hareketleri, yalnızca nakledilen günlük ile ilişkili olanlardır. Günlük nakledildiğinde:

- Satıcıya ait stok, **Satıldı** durumu ile birlikte **Sahiplik değişikliği** başvurusuyla yayımlanır.
- Eldeki stok, satınalma siparişinde bir ürün girişiyle güncelleştirilmiş stok hareketi kullanarak tüketen tüzel kişilik tarafından alınır. Bu, sipariş durumunu **Alındı** olarak belirler. Konsinye için kullanılan satınalma siparişlerinin **Kaynak** alanı **Konsinye** olarak ayarlanır.

Sipariş oluşturulduktan sonra konsinye satınalma sipariş satırları miktarının güncelleştirilmesi mümkün değildir.

[![Stok sahibi değiştirme günlüğü.](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Konsinye işlemlerdeki satıcı iş birliği

Satıcılar, satıcı iş birliği arabirimini kullanıyorsa bunu, tesisinizdeki stoğun tüketimini izlemek için kullanabilirler. Gelen konsinye işlemlerle alakalı satıcı iş birliği arabiriminin üç sayfası vardır:

- **Konsinye stoğu tüketen** **satınalma siparişleri** - Konsinye işleminden kaynaklanan sahiplik değişikliğiyle ilişkili satınalma siparişi bilgilerini detaylı olarak gösterir.
- **Konsinye stoktan alınan ürünler**: Sahiplik değişikliği işlemi sırasında güncelleştirilen ürün girişleri bulunan maddeler ve miktarlar hakkında bilgileri gösterir.
- **Eldeki konsinye stok**: Teslim edilmesi beklenen konsinye maddeler ve müşterinin işyerinde halihazırda fiziksel olarak bulunan maddeler hakkında bilgileri gösterir.

Satıcı iş birliğini kullanmak için satıcıların ayarlanması hakkında daha fazla bilgi için bkz. [Satıcı portalı kullanıcı güvenliği](../procurement/configure-security-vendor-portal-users.md).

## <a name="inventory-owners"></a>Stok sahipleri

Fiziksel gelen konsinye stoğu kaydetmek için bir satıcı sahibi tanımlamanız gerekir. Bu **Stok sahibi** sayfasında yapılır. **Satıcı hesabı**'nı seçtiğinizde bu **Ad** ve **Sahip** alanları için varsayılan değerleri oluşturur. **Sahip** alanındaki değer satıcıya görünür olacaktır, bu nedenle satıcı hesabı adlarınız şirket dışı insanların tanımaları için kolay değilse değiştirmek isteyebilirsiniz. **Sahip** alanını yalnızca **Stok sahibi** kaydını kaydettiğiniz zamana kadar düzenlemek mümkündür. **Ad** alanı satıcı hesabının ilişkilendirildiği tarafın adıyla doldurulur ve değiştirilemez.

[![Stok sahipleri.](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>İzleme boyut grubu

Konsinye işlemlerinde kullanılacak maddeler **Sahip** boyutunun **Etkin** olarak ayarlandığı bir **İzleme boyut grubu** ile ilişkilendirilmelidir. Sahip boyutunda her zaman **Fiziksel stok** ve **Mali stok** seçenekleri seçili olmalıdır. **Boyuta göre tedarik planı** kesinlikle seçilmemelidir.

[![İzleme boyutu grubu.](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
