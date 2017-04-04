---
title: "Harici satıcılarla satıcı iş birliği"
description: "Bu konu, satınalma aracılarının satınalma siparişleri ve konsinye stok hakkında bilgileri paylaşmak için harici satıcılarla nasıl iş birliği yapabileceğini açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: d585ae0716a4bd9c3531e8639cd7c6b3cab780ac
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-collaboration-with-external-vendors"></a>Harici satıcılarla satıcı iş birliği

Bu konu, satınalma aracılarının satınalma siparişleri ve konsinye stok hakkında bilgileri paylaşmak için harici satıcılarla nasıl iş birliği yapabileceğini açıklar.

**Satıcı iş birliği** modülü Microsoft Dynamics 365 for Operations ile elektronik veri alış verişi (EDI) tümleştirmesi olmayan satıcılar için tasarlanmıştır. Satıcıların satınalma siparişi, fatura ve konsinye stoğu bilgileriyle çalışmasına olanak tanır. Bu konuda SS'ler ve konsinye stokla çalışmak için satıcı iş birliği arabirimini kullanan harici satıcılarla nasıl iş birliği yapabileceğiniz açıklanmaktadır. Ayrıca belirli bir satıcının satıcı iş birliğini kullanmak üzere nasıl etkinleştirileceği ve tüm satıcıların bir SS'ye yanıt verdiklerinde görecekleri bilgilerin nasıl tanımlanacağı da açıklanır. Satıcıların harici satıcı iş birliği arabiriminde yapabilecekleri hakkında daha fazla bilgi için bkz. [Müşterilerle satıcı iş birliği](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Satıcıların faturalama işlemlerinde satıcı iş birliğini nasıl kullanacakları hakkında daha fazla bilgi için bkz. [Satıcı iş birliği faturalama çalışma alanı](/dynamics365/operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Yeni satıcı iş birliği kullanıcılarını hazırlama hakkında daha fazla bilgi için bkz. [Satıcı iş birliği kullanıcılarını yönetme](manage-vendor-collaboration-users.md).

## <a name="define-the-information-shown-to-vendors-when-they-respond-to-pos"></a>Satıcılara SS'lere yanıt verdiklerinde gösterilen bilgileri tanımlama
Satıcılar onlara gönderdiğiniz bir SS'yi yanıtladıklarında SS'yi kabul etme, reddetme veya değişikliklerle kabul etme onayı vermeleri gereken bir iletişim kutusu görürler. Bu noktada satıcıya gösterilmesi gereken bilgiler işletmenize özel olabilir ve üç onay iletisinde görüntülenen metni belirleyebilirsiniz. Örneğin, metin satıcıya işlemin sonraki adımları veya hüküm ve koşullar hakkında bilgilendirebilir.  

SS yanıtında görüntülenen metni tanımlamak için:

1.  **SAS'lara yanıt veren satıcılar için bilgiler** sayfasını açın.
2.  Yanıt türlerinden birini seçin.
3.  **Düzenle**'ye tıklayın.
4.  Satıcıların **Bilgi iletisi** kutusunda görmesini istediğiniz bilgileri girin.

İletileri birden fazla dilde eklemeniz gerekirse uygun dil kodlarıyla ayrı iletiler oluşturun. İleti satıcının kullandığı dilde gösterilir.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Belirli bir satıcı için satıcı iş birliği seçeneklerini ayarlama
Dynamics 365 for Operations uygulamasında satıcı iş birliğinin genel ayarları bir yönetici tarafından yapılandırılır. Örneğin, yönetici iş birliği yaptığınız tüm satıcılar için kullanılabilen güvenlik rollerini belirler. Ayrıca her satıcı hesabı için farklı olabilen bazı ayarlar da bulunmaktadır. Bunları şu şekilde ayarlamanız gerekir:

-   Satıcı iş birliğini etkinleştirin.
-   Satıcının fiyat bilgilerini görmesini isteyip istemediğinize karar verin.

### <a name="enable-vendor-collaboration"></a>Satıcı iş birliğini etkinleştirme

Harici bir satıcı için kullanıcı hesaplarının oluşturulabilmesi için, satıcı hesabını bu satıcının satıcı iş birliğini kullanmasına izin verecek şekilde yapılandırmanız gerekir. Bunu yapmak için, **Satıcılar** sayfasında bulunan **Genel** sekmesinden **İş birliğini etkinleştirme** alanını etkin olarak ayarlayın. Seçebileceğiniz iki seçenek bulunmaktadır:

-   **Etkin (SS otomatik olarak onaylanır) **- Satınalma siparişleri satıcılar değişiklik olmadan kabul ettiğinde otomatik olarak onaylanır.
-   **Etkin (SS otomatik olarak onaylanmaz) **- Satınalma siparişlerinin satıcı kabul ettikten sonra kuruluşunuz tarafından onaylanması gerekir.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Satıcının fiyat bilgilerini görmesini isteyip istemediğinize karar verme

Birim fiyatı, iskontolar ve masraflar gibi fiyat bilgilerini paylaşmak isterseniz satıcı hesabından **Satınalma siparişi fiyatları/tutarı** seçeneğini **Evet** olarak ayarlamanız gerekir. Bu seçenek **Satınalma siparişi varsayılanları** sekmesinde bulunmaktadır.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Satıcı iş birliği kullanırken SS'lerle çalışma
### <a name="sending-a-po-to-the-vendor"></a>Satıcıya SS gönderme

Satınalma siparişleri Dynamics 365 for Operations içinde hazırlanır. Durumu olduğunda PO **Onaylandı**, kullanarak satıcıya göndermek ** onay için gönderme ** eylem **satınalma siparişi** sayfa. SS durumu **Dış İncelemede** olarak değişir. SS gönderildikten sonra satıcı bu siparişi satıcı iş birliği arabiriminde siparişi kabul edebileceği, reddedebileceği veya değişiklik önerebileceği **İncelenecek satınalma siparişleri** sayfasında görebilir. Satıcı, PO'da yapılan değişiklikler gibi bilgileri bildirmek için açıklama da ekleyebilir. Satıcının ilgisini yeni bir PO'ya çekmek istiyorsanız, PO'yu e-postayla göndermek için yazdırma yönetimi sistemini de kullanabilirsiniz.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>SS'nin satıcı tarafından onaylanması ve kabul edilmesi

Satıcı bir satınalma siparişini kabul ettiğinde, SS otomatik olarak onaylanabilir veya el ile onaylanması gerekebilir. Bu bağlıdır ** satıcı etkinleştirme ** ayarlanırsa **etkin (PO otomatik teyit)** satıcısının veya çok **etkin (PO değil otomatik teyit)**.  

Aşağıdaki tabloda onay için SS gönderdiğinizde satıcının verdiği yanıta bağlı olarak, tipik bilgi alışverişi gösterilmektedir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Satıcı yanıtı</strong></td>
<td><strong>Sonuç</strong></td>
</tr>
<tr class="even">
<td>Satıcı siparişi <strong>kabul eder</strong>. Dynamics 365 for Operations, satıcı kabul ettiğinde SS'leri otomatik olarak onaylayacak şekilde yapılandırılmıştır.</td>
<td>Siparişin durumu <strong>Onaylandı</strong> olarak güncellenir. Herhangi bir nedenle sipariş güncellenemezse satıcı yanıtı yine de <strong>Kabul Edildi</strong> olarak kaydedilir ancak SS'nin durumu <strong>Dış İncelemede</strong> olarak kalır.</td>
</tr>
<tr class="odd">
<td>Satıcı siparişi <strong>kabul eder</strong>. Dynamics 365 for Operations, satıcı kabul ettiğinde SS'leri otomatik olarak onaylayacak şekilde yapılandırılmamıştır.</td>
<td>Satıcı yanıtı <strong>Kabul Edildi</strong> olarak kaydedilir ancak SS'nin durumu <strong>Dış İncelemede</strong> olarak kalır.</td>
</tr>
<tr class="even">
<td>Satıcı siparişi <strong>reddeder</strong>.</td>
<td>Satıcı yanıtı <strong>Reddedildi</strong> olarak kaydedilir ve PO'nun durumu <strong>Dış İncelemede</strong> olarak kalır. Reddetme yanıtı satıcıların notu ile birlikte alınır.</td>
</tr>
<tr class="odd">
<td>Satıcı <strong>değişikliklerle sipariş kabul</strong>. Değişiklikleri satır düzeyinde önerilir. Satırları tek tek kabul etmek veya reddetmek mümkündür. Diğer olası değişiklikler şunları içerir:
<ul>
<li>Tarihleri veya miktarları değiştirebilirsiniz.</li>
<li>Farklı teslimat tarihleri veya miktarlar için satırları bölebilirsiniz.</li>
<li>Madde değiştirebilirsiniz.</li>
</ul>
Fiyat bilgileri ve masraflar satıcı tarafından değiştirilemez. Bunlar için yapılan değişiklik önerilerinde notlar kullanılabilir.</td>
<td>Satıcı yanıt olarak kayıtlı <strong>değişikliklerle kabul</strong>, <strong></strong>ve SS durumu kalır <strong>içinde dış İnceleme</strong>.</td>
</tr>
</tbody>
</table>

Kullanabileceğiniz **satınalma siparişi****hazırlık** satıcı yanıt için hangi POs izlemek için çalışma alanı. Bu çalışma durumundaki satınalma siparişleri içeren iki listeleri içeren **içinde dış İnceleme**:

-   Dış incelemede eylem gerektirir.
-   Dış incelemede satıcı yanıtı bekliyor.

### <a name="changing-a-po"></a>SS değiştirme

Önceden yanıt verilmiş bir SS'yi değiştirmeniz gerektiğinde, SS'nin yeni sürümünü satıcıya gönderirsiniz. Yeni SS'de önceden gönderilen SS'nin değiştirilmiş bir sürümü olduğunu belirtmek için bir sürüm soneki bulunur. **Satınalma siparişi satıcı onay geçmişi** sayfası sizin ve satıcılarınızın her siparişin geçmişini izlemenize olanak tanır. Yeni SS onaylanana kadar, SS'nin önceden onaylanan sürümü onaylanan SS'ler listesinde kalmaya devam eder.

### <a name="cancelling-a-po"></a>SS'yi iptal etme

Bir SS'yi iptal ettiğinizde durum yeniden **Onaylandı** olarak değiştirilir. Satıcının iptali onaylayabilmesi veya reddedebilmesi için PO'yu Satıcı portalı üzerinden satıcıya tekrar göndermeniz gerekir. İptal onaylandıktan sonra, SS satıcının onaylanan SS listesinde **İptal edildi** olarak görünür.

### <a name="adding-attachments-to-a-po"></a>SS'ye ek ekleme

SS'ye dosya, görüntü ve not gibi ekleri belge yönetim sistemini kullanarak ekleyebilirsiniz. **Dış** kısıtlama türüyle eklenen ekler SS'yi gönderdiğinizde satıcı için görünür hale gelir.

## <a name="purchase-order-statuses-and-versions"></a>Satınalma siparişi durumları ve sürümleri
Bu bölümde, bir SS'nin onaylandığı ana kadar alabileceği farklı durumlar ve SS'nin yeni sürümlerinin satıcı için görünür hale getirildiği noktalar açıklanmaktadır. Bu, satınalma siparişleri için değişiklik Yönetimi kullanıp bağlı olarak farklılıklar vardır. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Değişiklik yönetimi kullanmadığınızda sürümler ve durumlar

Aşağıdaki tablo, PO'nun geçebileceği durum ve sürüm değişikliklerine bir örnek gösterir.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eylem**                                                               | **Durum ve sürüm**                                                                                                                                       |
| SS başlangıç sürümü Dynamics 365 for Operations uygulamasında oluşturulur. | Durum **Onaylandı** .                                                                                                                                  |
| SS satıcıya gönderilir.                                            | Satıcı iş birliği arabiriminde bir sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir.                                          |
| Satıcı bir **Değişikliklerle kabul edildi** yanıtı gönderir.                  | Durum hala **Dış incelemede** olarak görünür.                                                                                                                  |
| Satıcı tarafından istenen bazı değişiklikler yaparsınız.                  | Durum tekrar **Onaylandı** olarak değiştirilir.                                                                                                                        |
| Satıcıya SS'nin yeni sürümünü gönderirsiniz.                        | Satıcı iş birliği arabiriminde yeni bir sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir.                                      |
| Satıcı SS'nin yeni sürümünü kabul eder.                            | Satıcı hesabı SS'yi kabul ettiğinde durumu **Onaylandı**'ya otomatik olarak değiştirmek üzere yapılandırılmadıysa, durum hala **Dış İncelemede **kalır. |

Satıcılar SS'yi satıcı iş birliği arabirimini kullanarak onaylamak zorunda değildir. E-posta iletisi gönderebilir veya PO'yu kabul ettiklerini başka kanallar aracılığıyla bildirebilirler. Bundan sonra, Dynamics 365 for Operations uygulamasında siparişi el ile onaylayabilirsiniz. Bunu yaparsanız satıcıdan yanıt olmasa bile siparişin onaylandığını belirten bir uyarı alırsınız. Daha sonra SS onay geçmişinde herhangi bir yanıt alınmamış açık onaylanmış sipariş olarak görünür. Satıcının artık SS'yi onaylama veya reddetme seçeneği yoktur.  

**Not:** Dynamics 365 for Operations uygulamasında diğer işlemler için kullanılabilir durumda olan SS sürümü, bu sürüm satıcı iş birliği arabiriminde kaydedilmemiş olsa bile, daima en son sürümdür.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Değişiklik yönetimi kullandığınızda sürümler ve durumlar

SS'ler için değişiklik yönetimi etkinleştirildiyse, SS **Onaylandı** durumuna gelmek için bir onay iş akışından geçer. Bu işlem satıcı tarafından görülmez.  

Aşağıdaki tablo, değişim yönetimi etkinleştirildiğinde PO'nun geçebileceği durum ve sürüm değişikliklerine bir örnek gösterir: Sürüm, SS satıcıya gönderildiği veya doğrulandığı zaman değil, onaylandığı zaman kaydedilir.

|                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eylem**                                                                                                    | **Durum ve sürüm**                                                                                                                                                                                                                                                                                                                                                                      |
| SS başlangıç sürümü Dynamics 365 for Operations uygulamasında oluşturulur.                                      | Durum **Taslak**'tır.                                                                                                                                                                                                                                                                                                                                                                    |
| PO onay işlemine yeniden gönderilir. (Bu satıcının içinde bulunmadığı dahili bir işlemdir.) | SS onay işlemi sırasında reddedilmediyse, durum **Taslak** yerine **İncelemede** ve **Onay** olarak değiştirilir. Onaylanan PO bir sürüm olarak kaydedilir.                                                                                                                                                                                                                     |
| SS satıcıya gönderilir                                                                                  | Sürüm satıcı iş birliği arabiriminde kaydedilir ve durum **Dış İncelemede** olarak değiştirilir.                                                                                                                                                                                                                                                                       |
| Satıcı tarafından istenen bazı değişiklikler yaparsınız.                                                       | Durum tekrar **Taslak** olarak değiştirilir.                                                                                                                                                                                                                                                                                                                                                    |
| PO yeniden onay işlemine gönderilir.                                                            | SS onay işlemi sırasında reddedilmediyse, durum **Taslak** yerine **İncelemede** ve **Onay** olarak değiştirilir. Alternatif olarak, sistem belirli alandaki değişikliklerin yeniden onaylanması gerekmez şeklinde yapılandırılabilir. Bu durumda, durum önce **Taslak** olur ve ardından otomatik olarak **Onaylandı** şeklinde güncellenir. Onaylanan PO yeni bir sürüm olarak kaydedilir. |
| Satıcıya SS'nin yeni sürümünü gönderirsiniz.                                                             | Satıcı iş birliği arabiriminde yeni sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir.                                                                                                                                                                                                                                                                   |
| Satıcı PO'nun yeni sürümünü onaylar.                                                                | Durum otomatik olarak veya satıcıdan yanıt alıp PO'yu onayladığınızda **Onaylandı** olarak değişir.                                                                                                                                                                                                                                                     |

## <a name="share-information-about-consignment-inventory"></a>Konsinye stok hakkında bilgileri paylaşma
Konsinye stok kullanıyorsanız, satıcılar aşağıdaki sayfalarda bilgileri görüntülemek için satıcı iş birliği arabirimi kullanabilir:

-   **Konsinye stoğu tüketen satınalma siparişleri** - Konsinye stok için yapılan satınalma siparişleri stoğun sahipliği satıcıdan şirketinize geçtiğinde oluşturulur. Aynı anda bir ürün girişi deftere nakledilir. Bu konsinye satınalma siparişleri yalnızca **Konsinye stoğu tüketen satınalma siparişleri** sayfasında görüntülenir. Bu siparişler, **Satıcı iş birliği** modülündeki **Tüm onaylanan satınalma siparişleri** sayfasına dahil edilmez.
-   **Konsinye stoktan alınan ürünler** - Bu sayfa, ürünlerin sahipliğinin satıcıdan şirketinize aktarıldığı tüm hareketleri listeler. Satıcılar bu bilgiyi müşteriye faturalamak için kullanabilir.
-   **Eldeki konsinye stok** - Bu sayfa ambarınıza girişi yapılan müşterinin sahip olduğu eldeki konsinye stoğu gösterir.



