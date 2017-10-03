---
title: "Harici satıcılarla satıcı iş birliği"
description: "Bu konu, satınalma aracılarının satınalma siparişleri ve konsinye stok hakkında bilgileri paylaşmak için harici satıcılarla nasıl iş birliği yapabileceğini açıklar."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: cbd099403f48b502ca74bcb38ae12decedb8f2da
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="vendor-collaboration-with-external-vendors"></a>Harici satıcılarla satıcı iş birliği

[!include[banner](../includes/banner.md)]


Bu konu, satınalma aracılarının satınalma siparişleri ve konsinye stok hakkında bilgileri paylaşmak için harici satıcılarla nasıl iş birliği yapabileceğini açıklar.

**Satıcı iş birliği** modülü Microsoft Dynamics 365 for Finance and Operations ile elektronik veri alış verişi (EDI) tümleştirmesi olmayan satıcılar için tasarlanmıştır. Satıcıların satınalma siparişi, fatura ve konsinye stoğu bilgileriyle çalışmasına olanak tanır. Bu konuda SS'ler ve konsinye stokla çalışmak için satıcı iş birliği arabirimini kullanan harici satıcılarla nasıl iş birliği yapabileceğiniz açıklanmaktadır. Ayrıca belirli bir satıcının satıcı iş birliğini kullanmak üzere nasıl etkinleştirileceği ve tüm satıcıların bir SS'ye yanıt verdiklerinde görecekleri bilgilerin nasıl tanımlanacağı da açıklanır. Satıcıların harici satıcı iş birliği arabiriminde yapabilecekleri hakkında daha fazla bilgi için bkz. [Müşterilerle satıcı iş birliği](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Satıcıların faturalama işlemlerinde satıcı iş birliğini nasıl kullanacakları hakkında daha fazla bilgi için bkz. [Satıcı iş birliği faturalama çalışma alanı](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). Yeni satıcı iş birliği kullanıcılarını hazırlama hakkında daha fazla bilgi için bkz. [Satıcı iş birliği kullanıcılarını yönetme](manage-vendor-collaboration-users.md).

Satıcıların faturalama işlemlerinde satıcı iş birliğini nasıl kullanacakları hakkında daha fazla bilgi için bkz. [Satıcı iş birliği faturalama çalışma alanı](/dynamics365/unified-operations/financials/accounts-payable/vendor-portal-invoicing-workspace). 

Yeni satıcı iş birliği kullanıcılarını hazırlama hakkında daha fazla bilgi için bkz. [Satıcı iş birliği kullanıcılarını yönetme](manage-vendor-collaboration-users.md).

## <a name="define-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Satıcılara SS'lere yanıt verdiklerinde gösterilen bilgileri tanımlama
Satıcılar onlara gönderdiğiniz bir SS'yi yanıtladıklarında SS'yi kabul etme, reddetme veya değişikliklerle kabul etme onayı vermeleri gereken bir ileti kutusu görürler. Bu noktada satıcıya gösterilmesi gereken bilgiler işletmenize özel olabileceğinden, her üç onay iletisinde görüntülenen metni belirleyebilirsiniz. Örneğin, metin satıcıya işlemin sonraki adımları veya hüküm ve koşullar hakkında bilgilendirebilir.  

SS yanıtında görüntülenen metni tanımlamak için:

1.  **SAS'lara yanıt veren satıcılar için bilgiler** sayfasını açın.
2.  Yanıt türlerinden birini seçin.
3.  **Düzenle**'yi tıklatın.
4.  Satıcıların **Bilgi iletisi** kutusunda görmesini istediğiniz bilgileri girin.

İletileri birden fazla dilde eklemeniz gerekirse ayrı iletiler oluşturun ve her biri için uygun dil kodunu belirtin. İleti satıcının kullandığı dilde gösterilir.

## <a name="set-the-vendor-collaboration-options-for-a-specific-vendor"></a>Belirli bir satıcı için satıcı iş birliği seçeneklerini ayarlama
Finace and Operations uygulamasında satıcı iş birliğinin genel ayarları bir yönetici tarafından yapılandırılır. Örneğin, yönetici iş birliği yaptığınız tüm satıcılar için kullanılabilen güvenlik rollerini belirler. Ayrıca her satıcı hesabı için farklı olabilen ayarlar da bulunmaktadır. Bunları şu şekilde ayarlamanız gerekir:
-   Satıcı iş birliğini etkinleştirin.
-   Satıcının fiyat bilgilerini görmesini isteyip istemediğinize karar verin.

### <a name="enable-vendor-collaboration"></a>Satıcı iş birliğini etkinleştirme

Harici bir satıcı için kullanıcı hesaplarının oluşturulabilmesi için, satıcı hesabını bu satıcının satıcı iş birliğini kullanmasına izin verecek şekilde yapılandırmanız gerekir. Bunu yapmak için, **Satıcılar** sayfasında bulunan **Genel** sekmesinden **İş birliğini etkinleştirme** alanını etkin olarak ayarlayın. Seçebileceğiniz iki seçenek bulunmaktadır:

-   **Etkin (SS otomatik olarak onaylanır)**- Satınalma siparişleri satıcılar değişiklik olmadan kabul ettiğinde otomatik olarak onaylanır.
-   **Etkin (SS otomatik olarak onaylanmaz)**- Satınalma siparişlerinin satıcı kabul ettikten sonra kuruluşunuz tarafından onaylanması gerekir.

### <a name="decide-whether-you-want-the-vendor-to-see-price-information"></a>Satıcının fiyat bilgilerini görmesini isteyip istemediğinize karar verme

Birim fiyatı, iskontolar ve masraflar gibi fiyat bilgilerini paylaşmak isterseniz satıcı hesabından **Satınalma siparişi fiyatları/tutarı** seçeneğini **Evet** olarak ayarlamanız gerekir. Bu seçenek **Satınalma siparişi varsayılanları** sekmesinde bulunmaktadır.

## <a name="work-with-pos-when-using-vendor-collaboration"></a>Satıcı iş birliği kullanırken SS'lerle çalışma
### <a name="sending-a-po-to-the-vendor"></a>Satıcıya SS gönderme

Satınalma siparişleri Finace and Operations içinde hazırlanır. SS **Onaylandı** durumuna sahip olduğunda, **Satınalma siparişi** sayfasındaki **Onay için gönder** eylemini kullanarak satıcıya gönderirsiniz. SS durumu **Dış İncelemede** olarak değişir. Satın alma siparişi gönderildikten sonra satıcı bunu satıcı işbirliği arabiriminin **İncelenecek satınalma siparişleri** sayfasında görebilir. Daha sonra satıcı siparişi kabul edebilir, reddedebilir veya değişiklikler önerebilir. Satıcı, PO'da yapılan değişiklikler gibi bilgileri bildirmek için açıklama da ekleyebilir. Satıcının ilgisini yeni bir PO'ya çekmek istiyorsanız, PO'yu e-postayla göndermek için yazdırma yönetimi sistemini de kullanabilirsiniz.

### <a name="confirmation-and-acceptance-of-the-po-by-the-vendor"></a>SS'nin satıcı tarafından onaylanması ve kabul edilmesi

Satıcı bir satınalma siparişini kabul ettiğinde, SS otomatik olarak onaylanabilir veya el ile onaylanması gerekebilir. Bu durum **Satıcı etkinleştirme** alanının satıcı için **Etkin (SS otomatik olarak onaylanır)** veya **Etkin (SS otomatik olarak ayarlanmaz)** seçeneklerinden hangisine ayarlandığına bağlıdır.  

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
<td>Satıcı siparişi <strong>kabul eder</strong>. Finace and Operations, satıcı kabul ettiğinde SS'leri otomatik olarak onaylayacak şekilde yapılandırılmıştır.</td>

<td>Siparişin durumu <strong>Onaylandı</strong> olarak güncellenir. Herhangi bir nedenle sipariş güncellenemezse satıcı yanıtı yine de <strong>Kabul Edildi</strong> olarak kaydedilir ancak SS'nin durumu <strong>Dış İncelemede</strong> olarak kalır. 

Satıcıya gönderilen ve **Harici İnceleme** durumunda olan SS satırlardaki onaylanan teslim tarihleriyle güncelleştirilir. Güncelleştirme otomatik olarak **Onaylandı** durumuna güncelleştirilen yeni bir sürüm başlatır. Satınalma siparişi teyit edildiğinde, bu satıcının işbirliği arabiriminde görünür.</td>
</tr>
<tr class="odd">
<td>Satıcı siparişi <strong>kabul eder</strong>. Finace and Operations, satıcı kabul ettiğinde SS'leri otomatik olarak onaylayacak şekilde yapılandırılmamıştır.</td>
<td>Satıcı yanıtı <strong>Kabul Edildi</strong> olarak kaydedilir ancak SS'nin durumu <strong>Dış İncelemede</strong> olarak kalır.

Satıcıya gönderilen ve **Harici İnceleme** durumunda olan SS satırlardaki onaylanan teslim tarihleriyle güncelleştirilir. Güncelleştirme **Harici İncelemede** durumuna ayarlanacak yeni bir sürüm başlatır. Daha sonra satınalma siparişini el ile onaylayabilirsiniz.</td>

</tr>
<tr class="even">
<td>Satıcı siparişi <strong>reddeder</strong>.</td>
<td>Satıcı yanıtı <strong>Reddedildi</strong> olarak kaydedilir ve PO'nun durumu <strong>Dış İncelemede</strong> olarak kalır. Reddetme yanıtı satıcının notu ile birlikte alınır.</td>
</tr>
<tr class="odd">
<td>Satıcı siparişi <strong>değişikliklerle kabul eder</strong>. Değişiklikler satır düzeyinde önerilir. Satırları tek tek kabul etmek veya reddetmek mümkündür. Diğer olası değişiklikler şunları içerir:
<ul>
<li>Tarihleri veya miktarları değiştirebilirsiniz.</li>
<li>Farklı teslimat tarihleri veya miktarlar için satırları bölebilirsiniz.</li>
<li>Madde değiştirebilirsiniz.</li>
</ul>
Fiyat bilgileri ve masraflar satıcı tarafından değiştirilemez. Bunlar için yapılan değişiklik önerilerinde notlar kullanılabilir.</td>
<td>Satıcı yanıtı <strong>Değişikliklerle kabul edildi</strong> olarak kaydedilir ve SS'nin durumu <strong>Harici İncelemede</strong> olarak kalır. Durumlar satıcının hangi türde değişiklikler önerdiğini gösterir. Değişikliklerdeki otomatik tüketim hakkında bilgi için, satıcı değişiklikler önerdiğinde satın alma siparişini güncelleştirme konusunda aşağıdaki bölümüne bakın. </td>
</tr>
</tbody>
</table>

Satıcının hangi satınalma siparişlerini yanıtladığını izlemek için **Satınalma siparişi** **hazırlığı** çalışma alanını kullanabilirsiniz. Bu çalışma alanında, durumu **Dış İncelemede** olan satınalma siparişlerinin yer aldığı iki liste bulunur:

-   Dış incelemede eylem gerektirir.
-   Dış incelemede satıcı yanıtı bekliyor.

### <a name="changing-a-po"></a>SS değiştirme

Önceden yanıt verilmiş bir SS'yi değiştirmek için SS'nin yeni sürümünü satıcıya göndermeniz gerekir. Yeni SS'de önceden gönderilen SS'nin değiştirilmiş bir sürümü olduğunu belirtmek için bir sürüm soneki bulunur. **Satınalma siparişi satıcı onay geçmişi** sayfası sizin ve satıcılarınızın her siparişin geçmişini izlemenize olanak tanır. Yeni SS onaylanana kadar, SS'nin önceden onaylanan sürümü onaylanan SS'ler listesinde kalmaya devam eder.

### <a name="cancelling-a-po"></a>SS'yi iptal etme

Bir SS'yi iptal ettiğinizde durum yeniden **Onaylandı** olarak değiştirilir. Satıcının iptali onaylayabilmesi veya reddedebilmesi için PO'yu Satıcı portalı üzerinden satıcıya tekrar göndermeniz gerekir. İptal onaylandıktan sonra, SS satıcının onaylanan SS listesinde **İptal edildi** olarak görünür.

### <a name="adding-attachments-to-a-po"></a>SS'ye ek ekleme

SS'ye dosya, görüntü ve not gibi ekleri belge yönetim sistemini kullanarak ekleyebilirsiniz. **Harici** türündeki ekler SS'yi gönderdiğinizde satıcı için görünür hale gelir.

## <a name="update-the-po-when-a-vendor-suggests-changes"></a>Bir satıcı değişiklikler önerdiğinde satınalma siparişini güncelleştirme
Bir satıcı satınalma siparişini yanıtladığında ve değişiklikler önerdiğinde, sonraki adım yanıtı işlemek olacaktır.
**Satınalma siparişi hazırlama çalışma alanında**, Harici inceleme eylem gerektiriyor listesinde, satıcının yanıtladığı satınalma siparişini değişikliklerle kabul edildi olarak tanımlayabilirsiniz. Harici inceleme eylem gerektiriyor listesinde, satıcı yanıtına da gidebilirsiniz. Yanıtta, satıcı başlıkta aşağıda belirtilen bilgileri değiştirebilir.
 
-   Satıcı belge referansı
-   Teslimat şekli
-   Teslimat koşulları
-   Onaylanan teslimat tarihi

Satıcı bir not veya ek de ekleyebilir

Satırlarda satıcı miktarı ve teslim tarihlerini değiştirebilir, notlar ve ekler ekleyebilir, satırı reddedebilir, satırı metin olarak anahtarlanan başka bir ürün içeren bir satırla değiştirebilir ve bir satırı birden fazla teslimata bölebilir. Satıcı tarafından önerilen değişikliklere bağlı olarak satır durumunda farklı satır durumları olacaktır:
    
-   **Değişikliklerle kabul edildi**
-   **Reddedildi**
-   **Değiştirildi** Bu durumda, **Değiştir** durumuna sahip ekstra bir satır eklenir.
-   **Onaylandı** Plan halinde bölündü Bu durumda **Zamanlama satırları** durumuna sahip ekstra satırlar eklenecektir.

Bir satırda herhangi bir değişiklik yoksa, satır durumu **Kabul edildi** olur.

Yanıtta, satıcının yaptığı değişikliklerinin türlerini gösteren daha önce sözü edilen satır durumlarını görebilirsiniz. Ayrıca, değiştirilen tüm alanlar değişiklikleri tanımlamanıza yardımcı olmak amacıyla koyu renkle gösterilir.

Bir satınalma siparişini yanıttaki veya bir satırdaki **Satın alma siparişi güncelleştirmesi işle** eylemine tıklayarak güncelleştirebilirsiniz. Başlıktaki ve satırlardaki **SS güncelleştirmesi işlendi mi?** göstergesi sistemin başlığı veya satırları satınalma siparişini yanıttan kaynaklanan olası değişikliklerle güncelleştirip güncelleştirmediğini görmenizi sağlar. **SS güncelleştirmesini işle** işlemini başlık veya satır başına yalnızca bir kez çalıştırabilirsiniz.

Bir satınalma siparişinde önerilen tüm değişiklikler güncelleştirilemez. Yalnızca başlıktaki güncelleştirmeler ve satırlardaki tarih ve miktar güncelleştirmeleri satınalma siparişinde otomatik olarak güncelleştirilebilir. Diğer değişiklikler için satınalma siparişini el ile güncelleştirmeniz gerekir. Bu durumda, **Satın alma siparişi güncelleştirmesi işlendi mi?** göstergesi **El ile güncelleştirme**'yi gösterir. Bir örnek olarak, el ile işlenmesi gereken bir değişiklik, satıcının satırı bir plana göre bölmeyi önermesi olabilir.

**Kabul edildi** durumuna sahip bir satırda **SS güncelleştirmesini işle** işlemini yürüttüğünüzde satınalma siparişinde güncelleştirilecek onaylanan bir teslim tarihi olacaktır. Notlar ve ekler otomatik olarak geçerli satınalma siparişine aktarılmaz. Geçerli satınalma siparişini **SS güncelleştirmesini işle** eylemiyle güncelleştirdiğinizde, ticari sözleşmeler satınalma siparişi satırlarında yeniden değerlendirilmez.


## <a name="po-statuses-and-versions"></a>Satınalma siparişi durumları ve sürümleri
Bu bölüm, bir satınalma siparişinin teyit edilene kadar sahip olabileceği çeşitli durumları açıklar. Ayrıca, satınalma siparişinin yeni sürümlerinin hangi noktada satıcı için kullanılabilir olacağını da açıklar. Davranışı, satınalma siparişleri için değişiklik yönetimi kullanıp kullanmadığınıza bağlı olarak değişir. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Değişiklik yönetimi kullanmadığınızda sürümler ve durumlar

Aşağıdaki tablo, PO'nun geçebileceği durum ve sürüm değişikliklerine bir örnek gösterir.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eylem**                                                               | **Durum ve sürüm**                                                                                                                                       |
| SS başlangıç sürümü Finance and Operations uygulamasında oluşturulur. | Durum **Onaylandı** .                                                                                                                                  |
| SS satıcıya gönderilir.                                            | Satıcı iş birliği arabiriminde bir sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir.                                          |
| Satıcı bir **Değişikliklerle kabul edildi** yanıtı gönderir.                  | Durum hala **Dış incelemede** olarak görünür.                                                                                                                  |
| Satıcı tarafından istenen bazı değişiklikler yaparsınız.                  | Durum tekrar **Onaylandı** olarak değiştirilir.                                                                                                                        |
| Satıcıya SS'nin yeni sürümünü gönderirsiniz.                        | Satıcı iş birliği arabiriminde yeni bir sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir.                                      |
| Satıcı SS'nin yeni sürümünü kabul eder.                            | Satıcı hesabı SS'yi kabul ettiğinde durumu **Onaylandı**'ya otomatik olarak değiştirmek üzere yapılandırılmadıysa, durum hala **Dış İncelemede** kalır. |


Satıcılar SS'yi satıcı iş birliği arabirimini kullanarak onaylamak zorunda değildir. E-posta iletisi gönderebilir veya PO'yu kabul ettiklerini başka kanallar aracılığıyla bildirebilirler. Bundan sonra, Finance and Operations uygulamasında siparişi el ile onaylayabilirsiniz. Bu durumda, satıcıdan yanıt olmasa bile siparişin onaylandığını belirten bir uyarı alırsınız. Daha sonra SS onay geçmişinde herhangi bir yanıt alınmamış açık onaylanmış sipariş olarak görünür. Satıcının artık SS'yi onaylama veya reddetme seçeneği yoktur.  


>[!NOTE]
>Dynamics 365 for Finance and Operations uygulamasında diğer işlemler için kullanılabilir durumda olan SS sürümü, bu sürüm satıcı iş birliği arabiriminde kaydedilmemiş olsa bile, daima en son sürümdür.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Değişiklik yönetimi kullandığınızda sürümler ve durumlar

SS'ler için değişiklik yönetimi etkinleştirildiyse, SS **Onaylandı** durumuna gelmek için bir onay iş akışından geçer. Bu işlem satıcı tarafından görülmez.  

Aşağıdaki tablo, değişim yönetimi etkinleştirildiğinde PO'nun geçebileceği durum ve sürüm değişikliklerine bir örnek gösterir: Sürüm, SS satıcıya gönderildiği veya doğrulandığı zaman değil, onaylandığı zaman kaydedilir.

|                                                                          |                                                                                                                                                              |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Eylem**                                                               | **Durum ve sürüm**                                                                                                                                       |
| SS başlangıç sürümü Finance and Operations uygulamasında oluşturulur.      | Durum **Taslak**'tır.  |
| PO onay işlemine yeniden gönderilir. (Onaylama işlemi, satıcının içinde bulunmadığı dahili bir işlemdir.)                                                           | SS onay işlemi sırasında reddedilmediyse, durum **Taslak** yerine **İncelemede** ve **Onay** olarak değiştirilir. Onaylanan PO bir sürüm olarak kaydedilir.           | 
| SS satıcıya gönderilir                                                            | Sürüm satıcı iş birliği arabiriminde kaydedilir ve durum **Dış İncelemede** olarak değiştirilir.      |
| Satınalma siparişini güncelleştirmek için satıcı tarafından talep edilen bazı değişiklikleri el ile veya yanıttaki eylemi kullanarak yaparsınız.                                                            | Durum tekrar **Taslak** olarak değiştirilir.     |
|PO yeniden onay işlemine gönderilir.                                                |  SS onay işlemi sırasında reddedilmediyse, durum **Taslak** yerine **İncelemede** ve **Onay** olarak değiştirilir. Alternatif olarak, sistem belirli alandaki değişikliklerin yeniden onaylanması gerekmez şeklinde yapılandırılabilir. Bu durumda, durum önce **Taslak** olur ve ardından otomatik olarak **Onaylandı** şeklinde güncellenir. Onaylanan PO yeni bir sürüm olarak kaydedilir.                                         |
|Satıcıya SS'nin yeni sürümünü gönderirsiniz.                                                |  Satıcı iş birliği arabiriminde yeni sürüm kaydedilir ve durum **Dış İncelemede** olarak değiştirilir.                                         |
|Satıcı PO'nun yeni sürümünü onaylar.                                                |  Durum otomatik olarak veya satıcıdan yanıt alıp PO'yu onayladığınızda **Onaylandı** olarak değişir. |

## <a name="share-information-about-consignment-inventory"></a>Konsinye stok hakkında bilgileri paylaşma
Konsinye stok kullanıyorsanız, satıcılar aşağıdaki sayfalarda bilgileri görüntülemek için satıcı iş birliği arabirimi kullanabilir:

-   **Konsinye stoğu tüketen satınalma siparişleri** - Konsinye stok için yapılan satınalma siparişleri stoğun sahipliği satıcıdan şirketinize geçtiğinde oluşturulur. Aynı anda bir ürün girişi deftere nakledilir. Bu konsinye satınalma siparişleri yalnızca **Konsinye stoğu tüketen satınalma siparişleri** sayfasında görüntülenir. Bu siparişler, **Satıcı iş birliği** modülündeki **Tüm onaylanan satınalma siparişleri** sayfasına dahil edilmez.
-   **Konsinye stoktan alınan ürünler** - Bu sayfa, ürünlerin sahipliğinin satıcıdan şirketinize aktarıldığı tüm hareketleri listeler. Satıcılar bu bilgiyi müşteriye faturalamak için kullanabilir.
-   **Eldeki konsinye stok** - Bu sayfa ambarınıza girişi yapılan müşterinin sahip olduğu eldeki konsinye stoğu gösterir.





