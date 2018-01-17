---
title: "Müşterilerle satıcı iş birliği"
description: "Bu konu, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da PO'lar ile çalışmak ve konsinye stoğu görüntülemek için satıcı iş birliğini nasıl kullanabileceğinizi açıklar."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentProductReceiptLines, ConsignmentVendorPortalOnHand, PurchVendorPortalConfirmedOrders, PurchVendorPortalOriginalOrder, PurchVendorPortalResponsesHistoryList, PurchVendorPortalResponsesPart
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 221234
ms.assetid: 6e69fb8b-6d3a-46ef-88cf-6d01212aa7c3
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 7646b2e01ea1f9cdca58b9971c3dea21b99525e2
ms.contentlocale: tr-tr
ms.lasthandoff: 12/14/2017

---

# <a name="vendor-collaboration-with-customers"></a>Müşterilerle satıcı iş birliği

[!include[banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics 365 for Finance and Operations, Enterprise edition'da müşteriler ile çalışmak için satıcı iş birliğini nasıl kullanabileceğinizi açıklar. Satıcılar bir dizi iş sürecini aşağıdaki çalışma alanlarından gerçekleştirebilir:

- **Satınalma siparişi teyidi** – Satınalma siparişlerini (PO) izleyin ve yanıtlayın.
- **Satıcı teklifi** - Teklif taleplerini (RFQ) görüntüleyin ve tekliflere girerek yanıt verin.
- **Satıcı bilgileri** – Satıcı ana verilerini görüntüleyin ve güncelleştirin.
- **Faturalama** – Faturalar ile çalışın. Bu konu **Faturalama** çalışma alanını kapsamaz. Bu çalışma alanı hakkında daha fazla bilgi için bkz. [Satıcı işbirliği faturalama çalışma alanı](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md).

Satıcılar konsinye stok bilgilerini de izleyebilir.

## <a name="working-with-pos-in-the-purchase-order-confirmation-workspace"></a>Satınalma siparişi onayı çalışma alanında PO'larla çalışma

**Satınalma siparişi onayı** çalışma alanı gözden geçirme için tarafınıza gönderilen PO'ları yanıtlamanıza olanak tanır. Ayrıca, müşteriden eylem bekleyen PO'lar ve onaylandıkları halde hala açık olan PO'lar hakkında bilgileri görüntülemenizi sağlar.

**Satınalma siparişi onayı** çalışma alanında üç liste bulunur:

- **İncelenecek satınalma siparişleri**: Bu liste size gönderilmiş ve sizden bir yanıt bekleyen satınalma siparişlerini gösterir. Siz yanıtladıktan sonra satınalma siparişi listeden kaybolur. Siz önceki sürümüne yanıt vermeden önce müşteri PO'nun yeni bir sürümünü gönderirse yalnızca en son sürüm gösterilir.
- **Müşteri eylemi bekleniyor**: Bu liste, yanıtladığınız ancak müşteri tarafından henüz onaylanmamış PO'ları görmenize olanak tanır. PO'yu kabul ederseniz durumu **Onaylandı** olarak değişene kadar PO'yu bu listede izleyebilirsiniz. PO'yu reddederseniz veya değişikliklerle kabul ederseniz müşteri yeni bir sürümünü gönderene kadar PO'yu burada izleyebilirsiniz.
- **Açık onaylanan satınalma siparişleri**: Bu liste, hesabınız için durumu **Onaylandı** olan tüm PO'ları gösterir. PO'da bulunan ürünlerin veya hizmetlerin tamamı alındığında PO listeden kaybolur.

PO'larla çalışmak için aşağıdaki sayfaları kullanabilirsiniz:

- **İncelenecek satınalma siparişleri** – Bu sayfa çalışma alanındaki **İncelenecek satınalma siparişleri** listesiyle aynı bilgileri içerir. Bu konunun önceki bölümlerindeki açıklamaya bakın.
- **Satınalma siparişi satıcı onay geçmişi** – Bu sayfa satıcıya gönderilen tüm PO'ları ve PO sürümlerini içerir. Ayrıca satıcıdan gelen tüm yanıtları da içerir.
- **Açık onaylanan satınalma siparişleri** – Bu sayfa çalışma alanındaki **Açık onaylanan satınalma siparişleri** listesiyle aynı bilgileri içerir. Bu konunun önceki bölümlerindeki açıklamaya bakın.
- **Tüm onaylanan satınalma siparişleri** – Bu sayfa, onaylanan tüm PO'ları içerir. Bu sayfadaki PO'lar ürünlerin veya hizmetlerin alınmış olduğu PO'ları içerir. Hangi PO'lar için fatura gönderebileceğinizi izlemek için bu listeyi kullanabilirsiniz.

### <a name="responding-to-pos"></a>PO'ları yanıtlama

Müşterinin inceleme için gönderdiği satınalma siparişleri **Satınalma siparişi onayı** çalışma alanında ve **İncelenecek satınalma siparişleri** sayfasında görünür. Bir satınalma siparişini açtıktan sonra bunu kabul edebilir, reddedebilir veya değişikliklerle kabul edebilirsiniz. PO başlığında veya tek tek satırlarda ekler olabilir. Ayrıca, PO başlığında veya tek tek satırlarda yanıt için bilgiler eklemeniz de mümkündür. Örneğin, satırlardan biri için alternatif bir madde önerebilirsiniz.

**Önizleme/Yazdır** seçeneğini kullanarak PO'yu önizleyebilir ve PDF dosyası olarak yazdırabilirsiniz. **Boyutları görüntüle** eylemini kullanarak aşağıdaki boyut sütunlarını gizleyebilir veya gösterebilirsiniz: **Tesis**, **Ambar**, **Renk**, **Ebat**, **Stil** ve **Yapılandırma**. 

**Değişikliklerle kabul et** seçeneğini kullanırsanız, tek tek satırları kabul edebilir veya reddedebilirsiniz. Satırlarda aşağıdaki değişiklikleri de yapabilirsiniz:

- Tarihleri veya miktarları değiştirebilirsiniz. Tüm satırlarda onaylanan teslimat tarihini güncelleştirmek için PO başlığında **Teslimat tarihini güncelleştir** seçeneğini kullanabilirsiniz.
- Farklı teslimat tarihleri veya miktarlar için satırları bölebilirsiniz.
- Bir maddenin yerine ikame ürün önerebilirsiniz. **Satır ayrıntıları** bölümünde, **Harici** alanına bir madde açıklaması ve madde numarası girin.

Fiyatlandırma bilgilerini veya masrafları değiştiremezsiniz, ancak notları kullanarak bunlar için değişiklik önerileri yapabilirsiniz.

Müşteri size PO'nun yeni bir sürümünü gönderirse Yeni PO'da önceden gönderilen PO'nun değiştirilmiş bir sürümü olduğunu belirtmek için bir sürüm soneki bulunur. **Satınalma siparişi satıcı onay geçmişi** sayfası her siparişin geçmişini izlemenize olanak tanır.

## <a name="monitoring-consignment-inventory"></a>Konsinye stoğu izleme

Konsinye stok kullanıyorsanız aşağıdaki sayfalarda bilgileri görüntülemek için satıcı iş birliği arabirimi kullanabilirsiniz:

- **Konsinye stoğu tüketen satınalma siparişleri** - Konsinye stok için yapılan satınalma siparişleri, müşteri stoğun sahipliğini üstlenince üretilir. Bu konsinye stok PO'ları yalnızca bu sayfada görüntülenir. **Tüm onaylanan satınalma siparişleri** sayfasında bulunmazlar.
- **Konsinye stoktan alınan ürünler**: Bu sayfa ürünlerin sahipliğinin, stoğu tüketen şirkete aktarıldığı tüm hareketleri listeler. Bu bilgiyi müşteriye faturalamak için kullanabilirsiniz.
- **Eldeki konsinye stok**: Bu sayfa müşterinin ambarında bulunan şirketinize ait eldeki konsinye stoğu gösterir.

## <a name="working-with-rfqs-in-the-vendor-bidding-workspace"></a>Satıcı teklifi çalışma alanında RFQ'larla çalışma

**Satıcı teklifi** çalışma alanı, kuruluşunuzun yanıt vermek üzere davet edildiği RFQ'ları görmenizi sağlar. RFQ'lara yanıt da verebilirsiniz. 

Çalışma alanı ayrıca kazanmış veya kaybetmiş olduğunuz tüm RFQ'ları gösterir. Ayrıca, sistem Kamu sektörü için yapılandırılmışsa, çalışma alanı genel kullanıma açık olan RFQ'ları gösterir.

### <a name="viewing-rfqs"></a>RFQ'ları görüntüleme

**Satıcı teklifi** çalışma alanını açarak aşağıdaki bilgilere erişin:

- Şirketinizin yanıt vermek üzere davet edildiği RFQ'ları görmek için **Yeni teklif davetlerini** seçin. Bu konumdan bir RFQ görüntüleyebilir ve teklif işlemi başlatabilirsiniz. Ayrıca, yeni bir teklif gönderilmesi gereken düzeltilmiş RFQ'ları da görebilirsiniz.
- Müşterinin size iade ettiği teklifleri görmek için **İade edilen teklifler**'i seçebilir ve daha fazla bilgi verebilir veya teklifi güncelleştirebilirsiniz.
- Sizin veya şirketinizi temsil eden kişinin üzerinde çalıştığı ancak henüz göndermediği RFQ'ları görmek için **Devam eden teklifler**'i seçin.
- Müşterinin teklifinizdeki en az bir satır maddesini kabul ettiğini görmek için **Sunulan teklifler**'i seçin.
- Tüm satırların reddedildiği teklifleri görmek için **Kaybedilen teklifler**'i seçin.
- Satıcının tüm RFQ davetlerinin listesini ve gönderilen teklifleri görmek için **Teklif talebi** bağlantısını seçin. **Teklif talebi** sayfası, bir satıcının dahil olduğu tüm RFQ'ları gösterir. Duruma göre arayabilirsiniz.
- Bir satıcının ilgili kişisinin teklifi reddettiği tüm RFQ'ların listesini görmek için **Reddedilen teklifler** bağlantısını seçin.

### <a name="working-with-rfqs-that-are-publicly-available"></a>Genele açık olan RFQ'larla çalışma

Kamu sektöründe çalışan bir kişi, genele açık olarak sunulan açık ve süresi dolmuş RFQ'ları görebilir.

- Genele sunulan açık RFQ'ların listesini görmek için **Açık yayımlanan teklif talepleri** bağlantısını seçin. Açık bir RFQ henüz süresi dolmamış olan bir RFQ'dur. Bitiş tarihini ve saatini RFQ başlığında görebilirsiniz.

    Teklif vermek üzere davet edildiyseniz, aynı RFQ'yu **Yeni teklif davetleri** sayfasında da görebilirsiniz. Bazı durumlarda, açık olan ancak teklif vermek üzere davet edilmediğiniz bir RFQ için teklif vermek isteyebilirsiniz. Bu durumda, müşterinin RFQ servis talebi için kendi kendine daveti etkinleştirilmiş olması durumunda kendi kendinizi davet edebilirsiniz.

- Genele sunulan kapalı RFQ'ların listesini görmek için **Kapalı yayımlanan teklif talepleri** bağlantısını seçin. Kapalı bir RFQ süresi dolmuş bir RFQ'dur. Bitiş tarihini ve saatini RFQ başlığında görebilirsiniz.

    Kapalı bir RFQ satır düzeyinde tüm satıcı tekliflerini gösterir. Teklifler kabul ve reddedildiğinden, bu bilgi kapalı RFQ'da gösterilir. Teklife dahil edilen tüm ekler de kullanılabilir.

**Not:** Bu işlev yalnızca Kamu Sektörü yapılandırma etkinleştirilmişse kullanılabilir.

### <a name="bidding"></a>Teklif verme

- Bir RFQ için teklif vermeye başlamak üzere**Teklif ver**'e tıklayın.

    Bir RFQ'nun başlık ve satırlarındaki teklif alanları için düzenleme etkinleştirildiğinde, teklifinizi doğrudan satır ızgarasına girebilirsiniz. Ayrıca, satır ayrıntılarına eklenmesi gereken ek bilgileri de göz önünde bulundurmanız gerekir.

    Bir teklif üzerinde çalışmaya başladığınızda, teklif **Devam eden teklifler** bölümünde görünür.

    Sona erme tarihinden önce herhangi bir anda teklifi kaydedebilirsiniz. Daha sonra geri dönerek teklifi tamamlayabilir ve gönderebilirsiniz. Bir teklifi gönderdikten sonra, bitiş tarihine kadar teklifi geri çağırabilir ve güncelleştirebilirsiniz.

- Bir teklif için girdiğiniz verileri sıfırlamak ve başlangıçtaki RFQ'ya dönmek için **RFQ'dan sıfırla**'yı seçin. Başlığı veya satırı sıfırlayabilirsiniz.
- Alternatiflerle çalışmak için satır ızgarasında **Alternatif ekle** veya **Alternatifi kaldır**'ı seçin.

    Bazı RFQ'lar alternatif tekliflerine izin verir. Alternatif teklifleri yalnızca **Kategori** türündeki satırlar için belirtebilirsiniz çünkü belirli maddeler alternatif olarak eklenemez. 

- Müşterinin bir RFQ'ya eklediği ekleri açmak için **RFQ eki** veya **RFQ satırları eki**'ni seçin. Teklifle beraber ekler yüklemek için **Teklif ekleri**'ni veya **Teklif satırı ekleri**'ni seçin.

    Bir teklif gönderebilmeniz için soru formlarını yanıtlamanız gerekebilir.

- Teklif vermek istemiyorsanız **Reddet**'i seçin. **Reddet**'i seçtikten sonra eylemi geri çağırıp teklif giremezsiniz.

Bir RFQ düzeltilirse, yeni bir teklif girmeniz gerekir. Düzeltme hakkındaki bilgileri RFQ sayfasındaki **Düzeltmeler** sekmesinde bulabilirsiniz. Düzeltilen RFQ'lar **Yeni teklif davetleri** sayfasında gösterilir.

## <a name="accessing-vendor-master-data-in-the-vendor-information-workspace"></a>Satıcı bilgileri çalışma alanında satıcı ana verilerine erişme

Bir satıcı olarak, müşterinin satıcı ana kaydında koruduğu bilgilerin bir kısmına erişebilirsiniz.  Bu nedenle, bilgileri güncel tutabilirsiniz. Bilgileri güncelleştirmek için satıcı yönetici (dış) rolüne sahip olmanız gerekir.

Erişilebilir bilgiler şunlardır: satıcı adı, adresleri, iletişim bilgileri, ilgili kişiler ve bunların iletişim bilgileri, kimlik numaraları, vergi tescil numaraları, satıcının müşteriye satmak üzere onaylandığı tedarik kategorileri ve sertifikalar hakkında bilgiler.

## <a name="see-also"></a>Ayrıca bkz.

[Satıcı iş birliği kullanıcılarını yönetme](manage-vendor-collaboration-users.md)

