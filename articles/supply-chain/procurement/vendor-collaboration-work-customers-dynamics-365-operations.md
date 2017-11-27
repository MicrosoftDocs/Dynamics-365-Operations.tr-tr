---
title: "Müşterilerle satıcı iş birliği"
description: "Bu konu, Finance and Operations'da PO'lar ile çalışmak ve konsinye stoğu görüntülemek için satıcı iş birliğini nasıl kullanabileceğinizi açıklar."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ad7c4f14cf60b2f59124ac98d55c4b92edabb47
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-collaboration-with-customers"></a>Müşterilerle satıcı iş birliği

[!include[banner](../includes/banner.md)]


Bu konu, Finance and Operations'da PO'lar ile çalışmak ve konsinye stoğu görüntülemek için satıcı iş birliğini nasıl kullanabileceğinizi açıklar.

Bu konu, Microsoft Finance and Operations'da müşteriler ile çalışmak için satıcı iş birliğini nasıl kullanabileceğinizi açıklar. Satınalma siparişlerinin nasıl izleneceği ve yanıtlanacağı, konsinye envanterin nasıl izleneceği hakkında bilgiler içerir. Faturalarla çalışmak için satıcı işbirliğini kullanmak da mümkündür. Daha fazla bilgi için bkz. [Satıcı işbirliği faturalama çalışma alanı](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).

## <a name="working-with-purchase-orders"></a>Satınalma siparişleriyle çalışma
**Satınalma siparişi onayı** çalışma alanı gözden geçirme için tarafınıza gönderilen PO'ları yanıtlamanıza olanak tanır. Ayrıca, müşteriden eylem bekleyen PO'lar ve onaylandıkları halde hala açık olan PO'lar hakkında bilgileri görüntülemenizi sağlar. **Satınalma siparişi onayı** çalışma alanında üç liste bulunur:

-   **İncelenecek satınalma siparişleri**: Bu liste size gönderilmiş ve sizden bir yanıt bekleyen satınalma siparişlerini gösterir. Siz yanıtladıktan sonra satınalma siparişi listeden kaybolur. Siz önceki sürümüne yanıt vermeden önce müşteri PO'nun yeni bir sürümünü gönderirse yalnızca en son sürüm gösterilir.
-   **Müşteri eylemi bekleniyor**: Bu liste, yanıtladığınız ancak müşteri tarafından henüz onaylanmamış PO'ları görmenize olanak tanır. PO'yı kabul ederseniz durumu **Onaylandı**'ya değişene kadar PO'yu bu listede izleyebilirsiniz. PO'yu reddettiyseniz veya değişikliklerle kabul ettiyseniz müşteri yeni bir sürümünü gönderene kadar PO'yu burada izleyebilirsiniz.
-   **Açık onaylanan satınalma siparişleri**: Bu liste, hesabınız için durumu **Onaylandı** olan tüm PO'ları içerir. PO'da bulunan ürünlerin veya hizmetlerin tamamı alındığında PO listeden kaybolur.

Aşağıdaki liste satınalma siparişleriyle çalışabileceğiniz dört sayfası gösterir. Bunlardan ikisi çalışma alanındaki listelerle aynı bilgileri içerir:

-   **İncelenecek satınalma siparişleri** (yukarıya bakın)
-   **Satınalma siparişi satıcı onay geçmişi**: Bu sayfa, satıcıya gönderilen tüm PO'ları ve tüm PO sürümlerini ve satıcıdan alınan tüm yanıtları içerir.
-   **Açık onaylanan satınalma siparişleri** (yukarıya bakın)
-   **Tüm onaylanan satınalma siparişleri**: Bu sayfa, ürünleri veya hizmetleri alınmış olanlar da dahil olmak üzere onaylanan tüm PO'ları içerir. Hangi PO'lar için fatura gönderebileceğinizi izlemek için bu listeyi kullanabilirsiniz.

### <a name="responding-to-purchase-orders"></a>Satınalma siparişlerine yanıt verme

Müşterinin inceleme için gönderdiği satınalma siparişleri **Satınalma siparişi onayı** çalışma alanında ve **İncelenecek satınalma siparişleri** sayfasında görünür. Bir satınalma siparişini açtıktan sonra bunu kabul etmeyi, reddetmeyi veya değişikliklerle kabul etmeyi seçebilirsiniz. PO başlığında veya tek tek satırlarda ekler olabilir. Ayrıca, PO başlığında veya tek tek satırlarda yanıt için bilgiler eklemeniz de mümkündür. Örneğin, satırlardan biri için alternatif bir madde önerebilirsiniz. **Önizleme/Yazdır** seçeneğini kullanarak PO'yu önizleyebilir ve PDF dosyası olarak yazdırabilirsiniz. **Boyutları görüntüle** eylemini kullanarak aşağıdaki boyut sütunlarını gizleyebilir veya gösterebilirsiniz: Tesis, Ambar, Renk, Ebat, Stil, Yapılandırma. **Değişikliklerle kabul et** seçeneğini kullanırsanız, tek tek satırları kabul edebilir veya reddedebilirsiniz. Satırlarda aşağıdaki değişiklikleri de yapabilirsiniz:

-   Tarihleri veya miktarları değiştirebilirsiniz. Tüm satırlarda onaylanan teslimat tarihini güncelleştirmek isterseniz PO başlığında **Teslimat tarihini güncelleştir** seçeneğini kullanabilirsiniz.
-   Farklı teslimat tarihleri veya miktarlar için satırları bölebilirsiniz
-   Bir maddenin yerine ikame ürün önerebilirsiniz. Bunu yapmak için **Harici** alanında **Satır ayrıntıları** bölümünde bir madde açıklamasını ve madde numaranızı girin.

Fiyatlandırma bilgilerini veya masrafları değiştiremezsiniz, ancak notları kullanarak bunlar için değişiklik önerileri yapabilirsiniz. Müşteriniz size PO'nun yeni bir sürümünü gönderirse Yeni SS'de önceden gönderilen SS'nin değiştirilmiş bir sürümü olduğunu belirtmek için bir sürüm soneki bulunur. **Satınalma siparişi satıcı onay geçmişi** sayfası her siparişin geçmişini izlemenize olanak tanır.

## <a name="monitoring-consignment-inventory"></a>Konsinye stoğu izleme
Konsinye stok kullanıyorsanız aşağıdaki sayfalarda bilgileri görüntülemek için satıcı iş birliği arabirimi kullanabilirsiniz:

-   **Konsinye stoğu tüketen satınalma siparişleri** - Konsinye stok için yapılan satınalma siparişleri, müşteri stoğun sahipliğini üstlenince üretilir. Bu konsinye satınalma siparişleri yalnızca **Konsinye stoğu tüketen satınalma siparişleri** sayfasında görüntülenir. **Tüm onaylanan satınalma siparişleri** sayfasında bulunmazlar.
-   **Konsinye stoktan alınan ürünler**: Bu sayfa ürünlerin sahipliğinin, stoğu tüketen şirkete aktarıldığı tüm hareketleri listeler. Bu bilgiyi müşteriye faturalamak için kullanabilirsiniz.
-   **Eldeki konsinye stok**: Bu sayfa müşterinin ambarında bulunan şirketinize ait eldeki konsinye stoğu gösterir.


<a name="see-also"></a>Ayrıca bkz.
--------

[Satıcı iş birliği kullanıcılarını yönetme](manage-vendor-collaboration-users.md)




