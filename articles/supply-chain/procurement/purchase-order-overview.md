---
title: Satınalma siparişine genel bakış
description: Bu makale, satınalma siparişleri (PO) ve bir PO'nun geçtiği çeşitli aşamalarla ilgili ek makalelere bağlantılar hakkında genel bilgi verir.
author: Henrikan
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder, PurchConfirmationRequestJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "93083"
- intro-internal
ms.assetid: e9b7bc5b-1d7e-4ec2-97be-d655274b0613
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b2e01f73aa78c0fabf0f5a1e0acd3bbc4f69cfc4
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982316"
---
# <a name="purchase-order-overview"></a>Satınalma siparişine genel bakış

[!include [banner](../includes/banner.md)]

Bu makale, satınalma siparişleri (PO) ve bir PO'nun geçtiği çeşitli aşamalarla ilgili ek makalelere bağlantılar hakkında genel bilgi verir.

Satınalma siparişi (PO) mallar veya hizmetler satın almak için bir satıcıyla yapılan anlaşmayı temsil eden bir belgedir. Ayrıca belge, ürün girişlerinin siparişe uygun yapıldığının ve sonrasında siparişe uygun olarak satıcı faturalarının muhasebesinin yapıldığının takip edilmesine yardımcı olur.  

**Satınalma siparişleri** sayfası, mevcut siparişlerin bir özetini içerir ve bu siparişleri değiştirmenize olanak tanır. Bir PO açtığınızda, satıcı detayları gibi her PO için yalnızca bir kez tanımlanan bilgileri içeren **Başlık** görünümünü seçebilirsiniz. Alternatif olarak, sipariş satırlarında değişiklik yapabileceğiniz **Satırlar** görünümünü seçebilirsiniz. Genellikle, satınalma siparişlerini değiştirirken bu iki görünüm arasında geçiş yaparsınız. Giderler doğrudan **Satınalma siparişleri** sayfasında listelenmez, ancak sipariş başlığı ve satırları menüleri aracılığıyla erişilir.  

PO'lar, ürün girişleri ve satıcı faturaları hakkındaki bilgileri görüntüleyebileceğiniz birçok rapor bulunur. Bu raporlar, **Tedarik ve kaynak atama** ve **Borç hesapları** modüllerinde bulunur.  

**Satınalma siparişi hazırlama** ve **Satınalma siparişi girişi ve izleme** çalışma alanları ilerlemiş oldukları çeşitli aşamalarda bulunan PO'ların listesini görüntülemenize olanak tanır. Ayrıca alınması gereken eylemlerin bir özetini de sağlar. **Satınalma siparişi hazırlama** çalışma alanı, PO oluşturma ve gözden geçirme, siparişten onaya kadar işleme ve satıcı onayı işlemlerine odaklanır. **Satınalma sipariş girişi ve takip** çalışma alanı PO karşılığında mal veya hizmet girişini işlemeye odaklanır. Vadesi geçmiş ya da tedarikçi tarafından teslim edilmesi gereken süre yakında sona erecek olan girişler hakkında bilgi veren listeleri içerir. Bu çalışma alanları, ambarda gerçekleştirilen ilgili giriş eylemleri için kullanılmaz. Bu eylemler, **Stok yönetimi** ve **Ambar yönetimi** modüllerindeki sayfalar kullanılarak gerçekleştirilir. Satıcı faturalarının işlenmesi **Satıcı faturası girişi** çalışma alanı kullanılarak yapılmalıdır ve ödemeler de **Satıcı ödemeleri** çalışma alanı kullanılarak yapılmalıdır.  

Aşağıdaki makaleler, bir PO'nun geçtiği çeşitli aşamalara genel bir bakış sağlar:

-   [Satınalma siparişleri oluşturma](purchase-order-creation.md)
-   [Satınalma siparişlerini onaylama](purchase-order-approval-confirmation.md)
-   [Ürün girişi ve satınalma siparişleri karşılaştırması](product-receipt-against-purchase-orders.md)
-   [Satıcı faturalarına genel bakış](../../finance/accounts-payable/vendor-invoices-overview.md)

## <a name="types-of-purchase-orders"></a>Satınalma siparişlerinin türleri
Üç tip satınalma siparişi vardır: Bir satınalma siparişi oluşturduğunuzda türünü belirtmeniz gerekir. Yeni siparişler için varsayılan sipariş türünü **Tedarik ve kaynak atama parametreleri** sayfasından ayarlayabilirsiniz.

| PO türü        | Açıklama                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Günlük        | Taslak sipariş oluşturmak için bu türü kullanın. Bu tür, stok miktarlarını etkilemez veya stok hareketleri oluşturmaz. PO yevmiye defteri satırları, master planlamaya dahil değildir.                                                                                                       |
| Satın alma siparişi | Satıcı ile siparişler onaylandığında ve satıcıya ödeme yapılmadan önce girişten faturalamaya kadar siparişler işlendiğinde, PO'lar oluşturmak için bu türü kullanın. Bu PO türü en yayın olanıdır.                                                                          |
| İade edilen sipariş | Malları satıcıya iade ederken bu türü kullanın. Bu sipariş türü, satıcının size vereceği iade mal yetki (RMA) numarasını belirtmenizi gerektirir. PO'nun **Genel** sekmesinde RMA numarasını belirtin. Sipariş satırlarının negatif miktarları olmalıdır. |

## <a name="purchase-order-statuses"></a>Satınalma siparişi durumları
PO'lar, siparişin ilerlemesini gösteren çeşitli durum alanları içerir. Tüm bu alanlar, siparişin **Başlık** görünümünde görüntülenir ve ayrıca bunlardan bazıları tüm siparişlerin kılavuz genel görünümünde de görüntülenir. **Durum** alanı siparişteki miktarların durumunu gösterir. Aşağıdaki değerler kullanılabilir:

-   **Açık sipariş**: Siparişler oluşturuldu ve miktarlar sipariştedir.
-   **Alınan**: Miktarın bir kısmı alındı ancak henüz faturalanmadı.
-   **Faturalandı**: Siparişteki tüm miktar faturalandı. **Not:** Bir sipariş *kısmen* faturalandıysa ya **Alınan** durumu ya da **Faturalandı** durumu uygundur. Bu nedenle, sipariş durumu hala **Açık sipariş** olacaktır.
-   **İptal edildi**: Sipariş önce onaylandı ancak sonra iptal edildi. Bu nedenle, bu durum artık siparişte açık miktar olmadığını gösterir.

**Belge durumu** alanı işlenmiş belgeler açısından siparişin ilerlemesini hızlıca gözden geçirmenize yardımcı olur. Sipariş için tamamlanan en son belgenin durumunu gösterir. Aşağıdaki değerler kullanılabilir:

-   **Yok**: Sipariş için henüz hiç belge işlenmedi.
-   **Satınalma sorgusu**: Bir satınalma sorgusu oluşturuldu ve sipariş satıcıdan geri bildirim bekliyor.
-   **Satınalma siparişi**: Onay, sipariş üzerinde işlendi.
-   **Ürün girişi**: Ürün girişi sipariş üzerinde işlendi.
-   **Fatura**: Bir faturanın siparişte maliyet muhasebesi yapıldı.

**Onay durumu** alanı, PO bir gözden geçirme süreci veya iş akışından geçerse kullanılır. Aşağıdaki değerler kullanılabilir:

-   **Taslak**, **İncelemede** ve **Reddedildi**: Bu durumlar, yalnızca PO için bir onay iş akışı olduğunda kullanılır.
-   **Onaylandı**: Bu durum, iş akışı onayını tamamlayan siparişlere atanır. Onay iş akışı kullanılmadan oluşturulan siparişler hemen **Onaylandı** durumuna geçer.
-   **Harici incelemede**: Bu durum satıcının PO'nun koşullarını onaylayabilmesi için satıcıya satınalma talebi gönderildiği senaryolarda kullanılır. Bu durum ayrıca **Onay talebi** eylemiyle başlatılan işlemde de kullanılır. Bu işlem için, satıcının sisteminize bağlanması ve siparişi onayladığını veya reddettiğini kaydederek PO koşullarını onaylaması istenir.
-   **Onaylandı**: Bu durum, sipariş onaylandıktan sonra atanır. Normalde, bu durum bir siparişe atanan en son onay durumudur.


## <a name="additional-resources"></a>Ek kaynaklar

[Satınalma siparişleri oluşturma](purchase-order-creation.md)

[Satınalma siparişlerini onaylama](purchase-order-approval-confirmation.md)

[Ürün girişi ve satınalma siparişleri karşılaştırması](product-receipt-against-purchase-orders.md)

[Satıcı faturalarına genel bakış](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]