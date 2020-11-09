---
title: Harici satıcılarla satıcı iş birliği
description: Bu konu, satınalma aracılarının satınalma siparişleri ve konsinye stok hakkında bilgileri paylaşmak için harici satıcılarla nasıl iş birliği yapabileceğini açıklar.
author: mkirknel
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart, PurchaseOrderResponseActionRemarks, PurchVendorPortalAllResponse, PurchOrderInExternalReview, PurchVendorPortalPendingResponsesPart, PurchVendorPortalResponses, PurchVendorPortalConfirmedOpenOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 82249f460e5ddce9b9d43906008a3248a80daafb
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018756"
---
# <a name="vendor-collaboration-with-external-vendors"></a>Harici satıcılarla satıcı iş birliği

[!include [banner](../includes/banner.md)]

**Satıcı iş birliği** modülü Microsoft Dynamics 365 Supply Chain Management ile elektronik veri alışverişi (EDI) tümleştirmesi olmayan satıcılar için tasarlanmıştır. Satıcıların satınalma siparişleri (PO'lar), faturalar, konsinye stok bilgileri ve teklif talepleri (RFQ'lar) ile çalışmasına ve satıcı ana verilerinin bir bölümüne erişebilmelerine olanak tanır. Bu konuda PO'lar, RFQ'lar ve konsinye stokla çalışmak için satıcı iş birliği arabirimini kullanan harici satıcılarla nasıl iş birliği yapabileceğiniz açıklanmaktadır. Ayrıca belirli bir satıcının satıcı iş birliğini kullanmak üzere nasıl etkinleştirileceği ve tüm satıcıların bir PO'ya yanıt verdiklerinde görecekleri bilgilerin nasıl tanımlanacağı da açıklanır.

Satıcıların harici satıcı iş birliği arabiriminde yapabilecekleri hakkında daha fazla bilgi için bkz. [Müşterilerle satıcı iş birliği](vendor-collaboration-work-customers-dynamics-365-operations.md).

> [!NOTE]
> Bu konudaki satıcı iş birliğiyle ilgili bilgiler, yalnızca Supply Chain Management'ın geçerli sürümü için geçerlidir. Microsoft Dynamics AX 7.0 (Şubat 2016) ve Microsoft Dynamics AX uygulaması 7.0.1 (Mayıs 2016) sürümünde, **Satıcı portalı** modülünü kullanarak satıcılarla iş birliği yapabilirsiniz. **Satıcı portalı** modülü hakkında bilgi için bkz. [Satıcılarla Satıcı portalını kullanarak iş birliği yapma](collaborate-vendors-vendor-portal.md).

Satıcıların faturalama işlemlerinde satıcı iş birliğini nasıl kullanacakları hakkında daha fazla bilgi için bkz. [Satıcı iş birliği faturalama çalışma alanı](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md). Yeni satıcı iş birliği kullanıcılarını hazırlama hakkında daha fazla bilgi için bkz. [Satıcı iş birliği kullanıcılarını yönetme](manage-vendor-collaboration-users.md).

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Satıcılara PO'lara yanıt verdiklerinde gösterilen bilgileri tanımlama

Satıcılar onlara gönderdiğiniz bir PO'yu yanıtladıklarında PO'yu kabul etme, reddetme veya değişikliklerle kabul etme onayı vermeleri gereken üç ileti kutusundan birini görürler. Bu noktada satıcıya gösterilmesi gereken bilgiler işletmenize özel olabileceğinden, her onay iletisinde görüntülenen metni belirleyebilirsiniz. Örneğin, metin satıcıya işlemin sonraki adımları veya hüküm ve koşullar hakkında bilgilendirebilir.

PO yanıtında görüntülenen metni tanımlamak için aşağıdaki adımları izleyin:

1. **PO'lara yanıt veren satıcılar için bilgiler** sayfasında yanıt türünü ve ardından **Düzenle** 'yi seçin.
2. **Bilgi iletisi** kutusuna, ileti kutusunda satıcılara gösterilmesi gereken bilgileri girin.

İletileri birden fazla dilde eklemeniz gerekirse ayrı iletiler oluşturun ve her biri için uygun dil kodunu belirtin. İleti satıcının kullandığı dilde gösterilir.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>Belirli bir satıcı için satıcı iş birliği seçeneklerini ayarlama

Bir yönetici Supply Chain Management'ta satıcı iş birliği için, iş birliği yaptığınız tüm satıcılar için kullanılabilir olan güvenlik rolleri gibi genel ayarları yapılandırır. Ancak, her satıcı hesabı için farklı olabilen ayarlar da bulunmaktadır. Bu ayarları yapılandırmanız gerekir.

- Satıcı iş birliğini etkinleştirin.
- Satıcının fiyat bilgilerini görmesine gerek olup olmadığını belirtin.

### <a name="enabling-vendor-collaboration"></a>Satıcı iş birliğini etkinleştirme

Harici bir satıcı için kullanıcı hesaplarının oluşturulabilmesi amacıyla, satıcı hesabını bu satıcının satıcı iş birliğini kullanmasına izin verecek şekilde yapılandırmanız gerekir. **Satıcılar** sayfasındaki **Genel** sekmesinde **İş birliğini etkinleştirme** alanını seçin. Aşağıdaki seçenekler kullanılabilir durumdadır:

- **Etkin (PO otomatik olarak onaylanır)** - PO'lar satıcılar değişiklik olmadan kabul ettiğinde otomatik olarak onaylanır.
- **Etkin (PO otomatik olarak onaylanmaz)** - PO'ların satıcı kabul ettikten sonra kuruluşunuz tarafından el ile onaylanması gerekir.

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Satıcının fiyat bilgilerini görmesine gerek olup olmadığını belirtme

PPO'lar için fiyat bilgilerini satıcı iş birliği arabirimi aracılığıyla paylaşmak için **Satınalma sipariş varsayılanları** sekmesindeki **Satınalma sipariş fiyatları/tutarı** seçeneğini satıcı hesabı için **Evet** olarak ayarlamanız gerekir. Fiyat bilgileri birim fiyatı, iskontoları ve giderleri içerir.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>Satıcı iş birliği kullanırken PO'larla çalışma

### <a name="sending-a-po-to-a-vendor"></a>Satıcıya PO gönderme

Satınalma siparişleri Supply Chain Management'ta hazırlanır. Bir PO'nun durumu **Onaylandı** olduğunda, **Satınalma siparişi** sayfasında **Onay için gönder** 'i seçerek PO'yu satıcıya gönderirsiniz. PO durumu **Dış İncelemede** olarak değişir. Satın alma siparişi gönderildikten sonra satıcı bunu satıcı iş birliği arabiriminin **İncelenecek satınalma siparişleri** sayfasında görebilir. Daha sonra satıcı PO'yu kabul edebilir, reddedebilir veya değişiklikler önerebilir. Satıcı, PO'da yapılan değişiklikler gibi bilgileri bildirmek için açıklama da ekleyebilir. Satıcının ilgisini yeni bir PO'ya çekmek istiyorsanız, PO'yu e-postayla göndermek için Yazdırma yönetimi sistemini de kullanabilirsiniz.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>PO'nun satıcı tarafından onaylanması ve kabul edilmesi

Satıcı bir satınalma siparişini kabul ettikten sonra satınalma siparişi otomatik olarak onaylanabilir veya el ile onaylanması gerekebilir. Bu davranış **İş birliğini etkinleştirme** alanının satıcı için **Etkin (PO otomatik olarak onaylanır)** veya **Etkin (PO otomatik olarak ayarlanmaz)** seçeneklerinden hangisine ayarlandığına bağlıdır.

Aşağıdaki tabloda onay için PO gönderdiğinizde satıcının verdiği yanıta bağlı olarak, tipik bilgi alışverişi gösterilmektedir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Satıcı yanıtı</th>
<th>Sonuç</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>Satıcı siparişi <strong>kabul eder</strong> ve Supply Chain Management satıcının kabul ettiği satınalma siparişlerini otomatik olarak onaylamak üzere yapılandırılır.</td>
<td>Siparişin durumu <strong>Onaylandı</strong> olarak güncellenir. Herhangi bir nedenle sipariş güncellenemezse satıcı yanıtı yine de <strong>Kabul Edildi</strong> olarak kaydedilir ancak PO'nun durumu <strong>Dış İncelemede</strong> olarak kalır. 

Satıcıya gönderilen ve <strong>Harici İnceleme</strong> durumunda olan PO satırlardaki onaylanan teslim tarihleriyle güncelleştirilir. Bu güncelleştirme otomatik olarak <strong>Onaylandı</strong> durumuna güncelleştirilen yeni bir sürüm başlatır. Satınalma siparişi teyit edildiğinde, bu satıcının iş birliği arabiriminde görünür.</td>
</tr>
<tr class="odd">
<td>Satıcı siparişi <strong>kabul eder</strong> ancak Supply Chain Management satıcının kabul ettiği satınalma siparişlerini otomatik olarak onaylamak üzere yapılandırılmaz.</td>
<td>Satıcı yanıtı <strong>Kabul Edildi</strong> olarak kaydedilir ancak PO'nun durumu <strong>Dış İncelemede</strong> olarak kalır.

Satıcıya gönderilen ve <strong>Harici İnceleme</strong> durumunda olan PO satırlardaki onaylanan teslim tarihleriyle güncelleştirilir. Bu güncelleştirme otomatik olarak <strong>Dış İncelemede</strong> durumuna güncelleştirilen yeni bir sürüm başlatır. Satınalma siparişini daha sonra el ile onaylayabilirsiniz.</td>
</tr>
<tr class="even">
<td>Satıcı siparişi <strong>reddeder</strong>.</td>
<td>Satıcı yanıtı <strong>Reddedildi</strong> olarak kaydedilir ve PO'nun durumu <strong>Dış İncelemede</strong> olarak kalır. Reddetme yanıtı satıcıların notu ile birlikte alınır.</td>
</tr>
<tr class="odd">
<td>Satıcı siparişi <strong>değişikliklerle</strong> <strong>kabul eder</strong>. Değişiklikler satır düzeyinde önerilir. Satıcı ayrı ayrı satırları kabul edebilir veya reddedebilir. Satıcının önerebileceği diğer değişiklikler şunlardır:
<ul>
<li>Tarihleri veya miktarları değiştirebilirsiniz.</li>
<li>Farklı teslimat tarihleri veya miktarlar için satırları bölebilirsiniz.</li>
<li>Bir maddenin yerine ikame ürün önerebilirsiniz.</li>
</ul>
Satıcı fiyat bilgilerini ve giderleri değiştiremez. Bununla birlikte, satıcı notları kullanarak bu değişiklikleri önerebilir.</td>
<td>Satıcı yanıtı <strong>Değişikliklerle kabul edildi</strong> olarak kaydedilir ve PO'nun durumu <strong>Harici İncelemede</strong> olarak kalır. Durumlar satıcının hangi türde değişiklikler önerdiğini gösterir. Değişikliklerdeki otomatik tüketim hakkında bilgi için, bu konunun ilerleyen bölümündeki &quot;Satıcı değişiklikler önerdiğinde satın alma siparişini güncelleştirme&quot; bölümüne bakın. </td>
</tr>
</tbody>
</table>

Satıcının hangi satınalma siparişlerini yanıtladığını izlemek için **Satınalma siparişi hazırlığı** çalışma alanını kullanabilirsiniz. Bu çalışma alanında, durumu **Dış İncelemede** olan satınalma siparişlerinin yer aldığı iki liste bulunur:

- Harici gözden geçirmede eylem gerektirir
- Harici incelemede satıcı yanıtı bekliyor

### <a name="changing-a-po"></a>PO değiştirme

Satıcının önceden yanıt verdiği bir PO'yu değiştirmek için PO'nın yeni sürümünü satıcıya göndermeniz gerekir. Yeni PO'da önceden gönderilen PO'nun değiştirilmiş bir sürümü olduğunu belirtmek için bir sürüm soneki bulunur. **Satınalma siparişi satıcı onay geçmişi** sayfası sizin ve satıcılarınızın her siparişin geçmişini izlemenize olanak tanır. Yeni PO onaylanana kadar, PO'nun önceden onaylanan sürümü onaylanan PO'lar listesinde kalmaya devam eder.

### <a name="canceling-a-po"></a>Bir satınalma siparişini iptal etme

Bir PO'yu iptal ettiğinizde durum yeniden **Onaylandı** olarak değiştirilir. Satınalma siparişini satıcıya geri göndermelisiniz; böylece satıcı iptali onaylayabilir veya reddedebilir. İptal onaylandıktan sonra, PO satıcının onaylanan PO listesinde **İptal edildi** olarak görünür.

### <a name="adding-attachments-to-a-po"></a>PO'ya ek ekleme

PO'ya dosya, görüntü ve not gibi ekleri belge yönetim sistemini kullanarak ekleyebilirsiniz. **Harici** türündeki ekler PO'yu gönderdiğinizde satıcı için görünür hale gelir.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>Bir satıcı değişiklikler önerdiğinde satınalma siparişini güncelleştirme

Bir satıcı satınalma siparişini yanıtlar ve değişiklikler önerirse, sonraki adım yanıtı işlemek olacaktır.

**Satınalma siparişi hazırlama** çalışma alanında, **Dış incelemede eylem gerektiriyor** listesinde, satıcının değişikliklerle kabul ettiği PO'ları tanımlayabilirsiniz. Bu listeden satıcı yanıtına da gidebilirsiniz.

Yanıtta, satıcı başlıkta aşağıda belirtilen bilgileri değiştirebilir:
 
- Satıcı belge referansı
- Teslimat şekli
- Teslimat koşulları
- Onaylanan teslimat tarihi

Satıcı bir not veya ek de ekleyebilir.

Satırlarda satıcı miktarı ve teslim tarihlerini değiştirebilir, notlar ve ekler ekleyebilir, satırı reddedebilir, satırı metin olarak anahtarlanan başka bir ürün içeren bir satırla değiştirebilir ve bir satırı birden fazla teslimata bölebilir. Satırın durumu satıcının önerdiği değişikliklere bağlı olarak değişir:
    
- **Değişikliklerle kabul edildi**
- **Reddedildi**
- **Değiştirildi** - Bu durumda, **Değiştir** durumuna sahip ekstra bir satır eklenir.
- **Teyit edildi**
- **Plan halinde bölündü** Bu durumda **Zamanlama satırları** durumuna sahip ekstra satırlar eklenecektir.

Bir satırda herhangi bir değişiklik yoksa, satır durumu **Kabul edildi** olur.

Yanıtta, satır durumları satıcının yaptığı değişikliklerinin türlerini size gösterir. Ayrıca, değiştirilen tüm alanlar değişiklikleri tanımlamanıza yardımcı olmak amacıyla koyu renkle gösterilir.

Bir satınalma siparişini yanıttaki veya bir satırdaki **Satın alma siparişi güncelleştirmesi işle** eylemini seçerek güncelleştirebilirsiniz. Başlıktaki ve satırlardaki **PO güncelleştirmesi işlendi mi?** alanı sistemin başlığı veya satırları satınalma siparişini yanıttan kaynaklanan değişikliklerle güncelleştirip güncelleştirmediğini görmenizi sağlar. **PO güncelleştirmesini işle** eylemini başlık veya satır başına yalnızca bir kez çalıştırabilirsiniz.

Bir satınalma siparişinde önerilen tüm değişiklikler güncelleştirilemez. Yalnızca başlıktaki güncelleştirmeler ve satırlardaki tarih ve miktar güncelleştirmeleri satınalma siparişinde otomatik olarak güncelleştirilebilir. Diğer değişiklikler için satınalma siparişini el ile güncelleştirmeniz gerekir. Bu durumda, **Satın alma siparişi güncelleştirmesi işlendi mi?** alanındaki değer **El ile güncelleştirme** olur. Örneğin, bir satıcı bir satırın plan halinde bölünmesini önerirse, bu değişikliğin el ile yapılması gerekir.

**Kabul edildi** durumunda sahip her satırın onaylanmış bir teslim tarihi olacaktır. **PO güncelleştirmesini işle** eylemini çalıştırdığınızda, bu tarih satınalma siparişi üzerinde güncelleştirilir. Notlar ve ekler otomatik olarak geçerli satınalma siparişine aktarılmaz. Ayrıca, geçerli satınalma siparişini **PO güncelleştirmesini işle** eylemiyle güncelleştirdiğinizde, ticari sözleşmeler satınalma siparişi satırlarında yeniden değerlendirilmez.

## <a name="po-statuses-and-versions"></a>Satınalma siparişi durumları ve sürümleri

Bu bölüm, bir satınalma siparişinin teyit edilene kadar sahip olabileceği çeşitli durumları açıklar. Ayrıca, satınalma siparişinin yeni sürümlerinin hangi noktada satıcı için kullanılabilir olacağını da açıklar. Davranışı, satınalma siparişleri için değişiklik yönetimi kullanıp kullanmadığınıza bağlı olarak değişir. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Değişiklik yönetimi kullanmadığınızda sürümler ve durumlar

Aşağıdaki tablo, PO'nun geçebileceği durum ve sürüm değişikliklerine bir örnek gösterir.

| Eylem | Durum ve sürüm |
|--------|--------------------|
| Satınalma siparişinin başlangıç sürümü Supply Chain Management'ta oluşturulur. | Durum **Onaylandı** . |
| PO satıcıya gönderilir. | Satıcı iş birliği arabiriminde bir sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir. |
| Satıcı bir **Değişikliklerle kabul edildi** yanıtı gönderir. | Durum hala **Dış incelemede** olarak görünür. |
| Satıcı tarafından istenen bazı değişiklikleri yaparsınız. | Durum tekrar **Onaylandı** olarak değiştirilir. |
| Satıcıya PO'nun yeni sürümünü gönderirsiniz. | Satıcı iş birliği arabiriminde yeni bir sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir. |
| Satıcı PO'nun yeni sürümünü kabul eder. | Satıcı hesabı satıcı PO'yu kabul ettiğinde durumu **Onaylandı** 'ya otomatik olarak değiştirmek üzere yapılandırılmadıysa, durum hala **Dış İncelemede** olarak kalır. |

Satıcılar PO'yu satıcı iş birliği arabirimini kullanarak onaylamak zorunda değildir. E-posta gönderebilir veya PO'yu kabul ettiklerini başka kanallar aracılığıyla bildirebilirler. Siparişi daha sonra el ile onaylayabilirsiniz. Bu durumda, satıcıdan yanıt olmasa bile siparişin onaylandığını belirten bir uyarı alırsınız. Daha sonra PO onay geçmişinde herhangi bir yanıt alınmamış açık onaylanmış sipariş olarak görünür. Bu noktada, satıcının artık PO'yu onaylama veya reddetme seçeneği yoktur.

> [!NOTE]
> Supply Chain Management'ta diğer işlemler için kullanılabilir durumda olan PO sürümü, bu sürüm satıcı iş birliği arabiriminde kaydedilmemiş olsa bile, daima en son sürümdür.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Değişiklik yönetimi kullandığınızda sürümler ve durumlar

PO'lar için değişiklik yönetimi etkinleştirildiyse, PO **Onaylandı** durumuna gelmek için bir onay iş akışından geçer. Bu işlem satıcı tarafından görülmez.

Aşağıdaki tablo, değişim yönetimi etkinleştirildiğinde PO'nun geçebileceği durum ve sürüm değişikliklerine bir örnek gösterir: Sürüm, PO satıcıya gönderildiği veya doğrulandığı zaman değil, onaylandığı zaman kaydedilir.

| Eylem | Durum ve sürüm |
|--------|--------------------|
| Satınalma siparişinin başlangıç sürümü Supply Chain Management'ta oluşturulur. | Durum **Taslak** 'tır. |
| PO onay işlemine yeniden gönderilir. (Onaylama işlemi, satıcının içinde bulunmadığı dahili bir işlemdir.) | PO onay işlemi sırasında reddedilmediyse, durum **Taslak** yerine **İncelemede** ve **Onay** olarak değiştirilir. Onaylanan PO bir sürüm olarak kaydedilir. | 
| PO satıcıya gönderilir. | Sürüm satıcı iş birliği arabiriminde kaydedilir ve durum **Dış İncelemede** olarak değiştirilir. |
| Satınalma siparişini güncelleştirmek için satıcı tarafından talep edilen bazı değişiklikleri el ile veya yanıttaki **PO güncelleştirmesini işle** eylemini kullanarak yaparsınız. | Durum tekrar **Taslak** olarak değiştirilir. |
| PO yeniden onay işlemine gönderilir. | PO onay işlemi sırasında reddedilmediyse, durum **Taslak** yerine **İncelemede** ve **Onay** olarak değiştirilir. Alternatif olarak, sistem belirli alandaki değişikliklerin yeniden onaylanması gerekmez şeklinde yapılandırılabilir. Bu durumda, durum önce **Taslak** olur ve ardından otomatik olarak **Onaylandı** şeklinde güncellenir. Onaylanan PO yeni bir sürüm olarak kaydedilir. |
| Satıcıya PO'nun yeni sürümünü gönderirsiniz. | Satıcı iş birliği arabiriminde yeni sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir. |
| Satıcı PO'nun yeni sürümünü onaylar. | Durum otomatik olarak veya satıcıdan yanıt alıp PO'yu onayladığınızda **Onaylandı** olarak değişir. |

## <a name="sharing-information-about-consignment-inventory"></a>Konsinye stok hakkındaki bilgileri paylaşma

Konsinye stok kullanıyorsanız, satıcılar aşağıdaki sayfalarda bilgileri görüntülemek için satıcı iş birliği arabirimi kullanabilir:

- **Konsinye stoğu tüketen satınalma siparişleri** - Konsinye stok için yapılan satınalma siparişleri stoğun sahipliği satıcıdan şirketinize geçtiğinde oluşturulur. Aynı anda bir ürün girişi deftere nakledilir. Bu konsinye satınalma siparişleri **Konsinye stoğu tüketen satınalma siparişleri** sayfasında görüntülenir. Bu siparişler, **Satıcı iş birliği** modülündeki **Tüm onaylanan satınalma siparişleri** sayfasına dahil edilmez.
- **Konsinye stoktan alınan ürünler** - Bu sayfa, ürünlerin sahipliğinin satıcıdan şirketinize aktarıldığı tüm hareketleri listeler. Satıcılar bu bilgiyi müşteriye faturalamak için kullanabilir.
- **Eldeki konsinye stok** - Bu sayfa ambarınıza girişi yapılan satıcının sahip olduğu eldeki konsinye stoğu gösterir.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Satıcı iş birliği kullanırken RFQ'larla çalışma

Bu bölüm RFQ işlemi sırasında müşteri ve satıcı arasındaki etkileşimleri açıklar. Ayrıca, bilgilerin satıcılara nasıl iletildiğini de açıklar. RFQ işlemi desteğine temel bir genel bakış için bkz. [Teklif taleplerine (RFQ'lar) genel bakış](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Alternatifler, ekler, düzeltmeler ve iadeler

- **Alternatifler** – Bir RFQ servis talebinin başlığında, katalog dışı madde satırları için alternatiflere izin verildiğini belirtebilirsiniz. Alternatifler etkinleştirildiğinde, satıcılar talep edilen her satır için bir alternatif satırı ekleyebilir.
- **Ekler** – Ekler bir RFQ servis talebine hem başlık düzeyinde hem de satır düzeyinde eklenebilir. Ekleri dahili veya harici olarak sınıflandırılabilir. Dahili ekler yalnızda müşteri tarafında görüntülenebilirken satıcılar gönderildikten sonra harici ekleri görebilir.

    Satıcılar, teklif yanıtına ekler de ekleyebilir. Bu ekler satıcı teklif yanıtını gönderdikten sonra satıcı tarafında görüntülenebilir. Satıcıların eklediği ekler daima harici olarak sınıflandırılır. Bir satıcının teklifle birlikte gönderdiği bir eke ulaşmak için **Teklif ekleri** 'ni veya **Teklif satırı ekleri** 'ni seçin.
    
    RFQ servis talebiyle birlikte gönderilen ekleri açmak için yanıttaki belge işleme ataç simgesini kullanın.

- **Düzeltmeler** – Bir düzeltme sonlandırıldığında, var olan fiyat teklifi yanıtları güncelleştirilmiş değerlerle değiştirilebilmesi için kaldırılır. Satır fiyatı ve miktarı gibi önceki teklifte verilen bilgiler RFQ servis talebindeki günlükler aracılığıyla görüntülenebilir.

    Düzeltmenin işlenmesini zorunlu kılmak için **Talep teklifleri** hızlı sekmesindeki **Tedarik ve kaynak atama parametreleri** sayfasında **RFQ'ları gönderildiğinde kilitle** seçeneğini **Evet** olarak ayarlayın. (Bu seçeneği Kamu sektörü için ayarlanır ve gereklidir.)

- **İadeler** – Bir satıcı teklif gönderdiğinde RFQ servis talebi için daha fazla veya değiştirilmiş bilgilerin gerekli olması durumunda, müşteri teklifi satıcıya geri gönderebilir. Daha önce gönderilen teklifteki veriler tutulur ve satıcı teklif sürecine yeniden başlamak zorunda kalmadan gerekli değişiklikleri yapabilir.

## <a name="public-sector-extensions"></a>Kamu sektörü genişletmeleri

Kamu sektörü için genişletilmiş işlev RFQ servis talebinin satıcılara gönderilmesine ve yayımlanmasına olanak tanır. Bir RFQ yayımladığınızda, bilgi talep eden herhangi bir kişi çoğu kamu sektörü düzenlemesiyle uyumlu olan işi görüntüleyebilir. Sunulan tüm iş **Açık yayımlanan teklif talepleri** liste sayfasında gösterilir ve iptal edilen, beklemede olan veya kabul edilen RFQ'lar **Kapalı yayımlanan teklif talepleri** liste sayfasından görüntülenebilir. Bu belgeler ayrıca Supply Chain Management dışındaki bir sitede aşağıdaki veri varlıklarıyla tümleştirmeler aracılığıyla görüntülenebilir:

- Yayımlanan teklif talepleri
- Yayımlanan teklif talepleri satırı
- Yayımlanan teklif talepleri başlık ekleri

Bu varlıklar Supply Chain Management'ta provizyon sağlanan kullanıcılar olmayan ancak harici siteye anonim erişimleri olan kişilerin mevcut ve kapatılmış işleri görmesine olanak tanır. Ayrıca, **Gönder ve yayımla** 'daki genişletilmiş işlev RFQ işlemi için parametreleri ayarlayan kullanıcının bir e-posta şablonu tanımlamasına da olanak tanır. Daha sonra, tedarik uzmanının RFQ servis talebini oluştururken, gerekli bilgileri RFQ servis talebindeki satıcılara gönderirken e-posta şablonunu seçmesi gerekir. 

RFQ işlemi için parametreleri ayarlayan kullanıcı birden fazla e-posta şablonu oluşturabilir. Bu e-posta şablonları hem statik metin hem de aşağıdaki değiştirme belirteçlerini içerebilir. Bu belirteçler e-posta oluşturulduğunda bağlamsal değerlerle değiştirilir.

- %RFQCase%
- %RFQCaseName%
- %bidType%
- %inviteOnly%
- %expiryDateTime%
- %requester%
- %requestingDepartment%
- %accountnum%
- %todaysdate%
- %createddate%

Bir düzeltme gerekirse ve RFQ gönderildikten sonra gönderilirse, RFQ davet edilen tüm satıcılara yeniden gönderilir. Yayınlanmış belge de **Açık yayımlanan teklif talepleri** sayfasında güncelleştirilir.
