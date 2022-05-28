---
title: Satınalma talebine genel bakış
description: Bu konuda, satınalma talebi iş akışı ve satınalma talebinin sahip olabileceği farklı durumlar açıklanmaktadır.
author: GalynaFedorova
ms.date: 11/02/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage, PurchReqConsolidationPartByVendor, PurchReqConsolidationLineDetail, PurchReqConsolidationCreate, PurchReqConsolidationBulkEdit, PurchReqConsolidationAddLine
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2174"
- intro-internal
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6524229800233d1bfdf54a11afc122990eed9d3
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671182"
---
# <a name="purchase-requisition-overview"></a>Satınalma talebine genel bakış

[!include [banner](../includes/banner.md)]

Bu konuda, satınalma talebi iş akışı ve satınalma talebinin sahip olabileceği farklı durumlar açıklanmaktadır.

Organizasyonunuzun kurulumuna bağlı olarak, organizasyonunuzun kullandığı ürünler için satın alma talepleri oluşturabilirsiniz. Bir satın alma talebi, Satın alma departmanına madde veya hizmet satın alma yetkisini veren bir belgedir.  

Bir satın alma talebi onaylandıktan sonra bir satın alma emri oluşturulması için kullanılabilir. Satın alma emirleri, Satın alma departmanının satıcılara gönderdiği bir harici belgedir.

## <a name="creating-purchase-requisitions"></a>Satın alma talepleri oluşturma
**Satın alma taleplerim** sayfasında bir satın alma talebi oluşturabilir ve ihtiyacınız olan maddeleri ve hizmetleri seçebilirsiniz. Organizasyonunuzun oluşturduğu bir tedarik katalogundan maddeleri seçebilirsiniz veya katalogda bulunmayan maddeleri bir tedarik kategorisi seçerek ve ürün ayrıntıları girerek talep edebilirsiniz.  

Bir satınalma talebini gözden geçirmeye göndermeden önce iş akışlarının yapılandırılması gerekir. Satın alma talebini ilk durum olan **Taslak** durumundan son durum olan **Onaylandı** durumuna kadar gözden geçirme sürecinden geçirmek için bir iş akışı kullanabilirsiniz.

### <a name="purchase-requisition-statuses"></a>Satınalma talebi durumları

Bir satın alma talebi oluşturduğunuzda buna bir durumu atanır. Ayrıca, bir satın alma talebine eklediğiniz her satır için de bir durum atanır. Bir iş akışına gözden geçirilmek üzere bir satın alma talebi gönderdiğinizde, satın alma talebinin durumu ve her bir satırın durumu, satırlar iş akışı sürecinden geçtikçe güncelleştirilir.  

Bir satın alma talebini gözden geçirme sürecinden tek bir belge olarak geçirmek için satın alma talebi iş akışı sürecini yapılandırabilirsiniz. Alternatif olarak, satın alma talebindeki satırlar uygun gözden geçiricilere tek tek yönlendirilebilir. Satın alma talep satırları tek tek gözden geçirilirse, her bir satın alma talebi satırı gözden geçirme sürecinde ilerledikçe bu satırın durumu güncelleştirilir. Tüm satırlar gözden geçirme sürecini tamamladığında ve satın alma talebi için gözden geçirme adımı kalmadığında, tüm satın alma talebinin durumu güncelleştirilir.

### <a name="purchase-requisition-workflow"></a>Satın alma talebi iş akışı

Aşağıdaki şemada bir satın alma talebine ve bir satın alma talebi satırına atanan durumlar iş akışı sürecindeki ilerlemesine göre gösterilmiştir.  

[![Satın alma talebi başlık ve satır durumları.](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Satın alma talebi başlık ve satır durumu ilişkileri

Bir satın alma talebinin genel durumu, satın alma talebi satırlarının durumuna göre belirlenir. Bu nedenle, gözden geçirme süreci mutlaka tüm satın alma talebi için gözden geçirme süreci tamamlanmadan önce tüm satın alma talebi satırları için tamamlanmalıdır. Aşağıdaki tabloda satın alma talebi başlığına ve satırlarına atanan durumlar iş akışı sürecindeki ilerlemesine göre gösterilmiştir.

<table>
<thead>
<tr class="header">
<th>Satınalma talebi durumu</th>
<th>Satınalma talebi satırının durumu</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Taslak</td>
<td>Taslak</td>
<td>Satın alma talebi ve satın alma talebi satırı oluşturulmuştur, ancak henüz gözden geçirilmek üzere gönderilmemiştir. <strong>Taslak</strong> durumundaki satın alma talepleri ve satın alma talebi satırlarında değişiklik yapılabilir. Satınalma talebi veya satınalma talebi satırının durumu geri çağrılmış ancak gözden geçirme için yeniden gönderilmemiş olması durumunda da <strong>Taslak</strong> olur. <strong>Not:</strong> Bir satın alma talebini belge düzeyinde gönderebilir veya geri çağırabilirsiniz. Ancak, bir tekli satın alma talebi satırını gönderemez veya geri çağıramazsınız.</td>
</tr>
<tr class="even">
<td>İncelemede</td>
<td><ul>
<li>İncelemede</li>
<li>Reddedildi</li>
</ul></td>
<td>İş akışı, her bir gözden geçiriciye satın alma talebi satırları yönlendirecek şekilde yapılandırılırsa, her bir satırın durumu <strong>Gözden geçiriliyor</strong> veya <strong>Reddedildi</strong> olur. Gözden geçirme süreci tüm satın alma talebi satırları için tamamlandığında ve satın alma talebi için gözden geçirme adımı kalmadığında satın alma talebi durumu güncelleştirilir.
<ul>
<li><strong>Gözden geçiriliyor</strong> – Satın alma talebi satırları gözden geçirilmek üzere gönderilmiştir. İş akışı süreci bir satın alma talebi satırı için tamamlandığında satırın durumu, kalan tüm satın alma talebi satırları gözden geçirilinceye kadar <strong>Gözden geçiriliyor</strong> durumunda kalır.</li>
<li><strong>Reddedildi</strong> – Satınalma talep satırı reddedilmiştir. Reddedilen satın alma talebi satırları değiştirilip yeniden gönderilebilir.</li>
</ul>
Reddedilen bir satın alma talebi satırını yeniden gönderirseniz gözden geçirme süreci, hala gözden geçirilmekte olan satın alma talebindeki tüm satırlar için baştan başlar. </br><strong>Not:</strong> Halihazırda gönderilmiş bir satın alma talebini geri çağırabilirsiniz. Bir satın alma talebini geri çağırdığınızda diğer tüm satın alma talebi satırları da geri çağrılır. Geri çağrılan satın alma talebi satırları silinebilir.</td>
</tr>
<tr class="odd">
<td>Reddedildi</td>
<td>Reddedildi</td>
<td>Satın alma talebi ve tüm satın alma talebi satırları reddedilmiştir. Reddedilen satın alma talepleri ve satın alma talebi satırları yeniden gönderilebilir.</td>
</tr>
<tr class="even">
<td>Onaylandı</td>
<td><ul>
<li>Onaylandı</li>
<li>İptal edildi</li>
<li>Kapalı</li>
</ul></td>
<td>Tüm satın alma talebi satırları gözden geçirme sürecini tamamlamıştır ve satın alma talebi için gözden geçirme adımı kalmamıştır.
<ul>
<li><strong>Onaylandı</strong> – Bir satın alma talebi satırı için gözden geçirme süreci tamamlanmış ve satır onaylanmıştır.</li>
<li><strong>İptal edildi</strong> – Satın alma talebi satırı daha önce onaylanmıştır, ancak artık gerekli olmadığından iptal edilmiştir. Sadece onaylanan satın alma talebi satırları iptal edilebilir.</li>
<li><strong>Kapatıldı</strong> – Satın alma talebi satırı onaylanmıştır ve belgeler, talep amacına uygun olarak oluşturulmuştur.
<ul>
<li>Talep amacı tüketim ise, satın alma talebi satırı için bir satın alma siparişi oluşturulmuştur.</li>
<li>Talep amacı stok yenileme ise, bir veya daha fazla sayıda karşılama belgesi üretilmiştir.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>İptal edildi</td>
<td>İptal edildi</td>
<td>Satınalma talebi ve tüm satınalma talebi satırları iptal edilmiştir.</br> <strong>Not:</strong> Bir satın alma talebi satırındaki bir maddeye artık ihtiyaç duymuyorsanız, halihazırda onaylanmışsa satın alma talebi satırını mutlaka iptal etmelisiniz. Sadece onaylanan satın alma talebi satırları iptal edilebilir. Satın alma talep satırları gözden geçiriliyor ise, satın alma talebi <strong>Gözden geçiriliyor</strong> durumunda olacaktır. Bu durumda satın alma talebini geri çağırabilir ve uygun satın alma talep satırını silebilirsiniz.</td>
</tr>
<tr class="even">
<td>Kapalı</td>
<td><ul>
<li>Kapalı</li>
<li>İptal edildi</li>
</ul></td>
<td>Satın alma talebi kapalıdır ve bir veya daha fazla sayıda karşılama belgesi üretilmiştir.
<ul>
<li><strong>Kapatıldı</strong> – Satın alma talebi satırı onaylanmıştır ve belgeler, talep amacına uygun olarak oluşturulmuştur.
<ul>
<li>Talep amacı tüketim ise, satın alma talebi satırı için bir satın alma siparişi oluşturulmuştur.</li>
<li>Talep amacı stok yenileme ise, bir veya daha fazla sayıda karşılama belgesi üretilmiştir.</li>
</ul></li>
<li><strong>İptal edildi</strong> – Satın alma talebi satırı daha önce onaylanmıştır, ancak artık gerekli olmadığından iptal edilmiştir. Sadece onaylanan satın alma talebi satırları iptal edilebilir.</li>
</ul>
<strong>Not:</strong> Kapatılmış bir satın alma talebi satırındaki bir maddeye artık gereksinim duymuyorsanız, satın alma talebi satırı için oluşturulan karşılama belgesindeki satırı mutlaka iptal etmeniz gerekir.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Birden fazla mali hesaba dağıtım maliyetleri
Bir satın alma talebinde yer alan bir ürünün maliyetini birden fazla mali hesaba dağıtabilirsiniz. Organizasyonunuz maliyet merkezleri ve departmanlar gibi boyutlar kullanıyorsa bir ürünün maliyetini mali hesaplar için boyutlara dağıtabilirsiniz.

## <a name="requisition-purposes"></a>Talep amaçları
Talep amaçları, talep amacının yerine getirilmesi sürecini daha esnek hale getirmektedir. Bir talep oluşturduğunuzda, buna iki amaçtan birini atayabilirsiniz: tüketim veya stok yenileme. Talebin amacına ve organizasyonunuzun kurulumuna bağlı olarak, talep isteği bir satınalma siparişi, transfer emri, üretim emri veya kanban ile karşılanabilir.  

Tedarik politikalarında, organizasyonunuz için bir talep oluşturulduğunda kullanılabilecek talep amaçlarını kontrol edebilirsiniz.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Tüketim amacına sahip olan talepler

Tüketim amacına sahip olan bir talep, organizasyonunuz tarafından dahili olarak kullanılacak maddeler veya hizmetler için talebi temsil eder. Bu talep türü tarafından oluşturulan talep daima bir satın alma emri tarafından karşılanır. Supply Chain Management, satın alma taleplerini otomatik olarak üretecek şekilde yapılandırılmışsa satın alma emirleri satın alma talebi onaylandıktan sonra oluşturulur.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Bir stok yenileme amacına sahip olan talepler

Stok yenileme amacına sahip bir talep, stokun yenilenmesi talebini temsil eder. Örneğin, maddeleri belirli bir tarihte ve belirli bir perakende konumunda satılacak şekilde yenilemek üzere bir talep oluşturabilirsiniz. Bu tür bir talep türünde oluşturulan talep bir satın alma emri, transfer emri, üretim emri veya kanban tarafından karşılanabilir.  

Talep amacı, stok yenileme ise talep, parasal değer yerine miktar olarak ifade edilir. Bu nedenle, yükümlülük muhasebesi, bütçe kontrolü, sabit kıymet belirleme için ticaret kuralları (BRAD), proje muhasebesi ve bunlarla bağlantılı kurallar geçerli değildir. Sadece stokta bulunan ve belirtilen tüzel kişilik için serbest bırakılan ürünlerimiz stok yenileme talep isteğini karşılayabilir. Talep amacı stok yenileme olduğunda kullanılabilecek ürünleri tanımlamak için **Stok yenileme kategorisi erişim politikası kuralı** sayfasını kullanın.  

Bir stok yenileme amacına sahip olan satın alma taleplerini kullanabilmek için talep isteğini dahil edecek master planlama kurmanız gerekir. Bu türde bir talep tarafından oluşturulan talep için karşılama yöntemi, organizasyonunuzdaki maddeler için kurulmuş ve master planlama kullanılarak planlanmış tedarik politikalarına göre otomatik olarak belirlenir.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Satın alma talepleri ve teklif talepleri
Bazı durumlarda bir satın alma talebinde talep edilen ürünlerin satıcısını ve fiyatını tanımlamak için bir teklif talebi (RFQ) süreci başlatmanız gerekir. Satın alma talebi gözden geçirme aşamasındayken bir RFQ oluşturulabilir. Bir teklifi kabul ettiğinizde satıcı, fiyat vb. hakkındaki bilgiler talebe aktarılır.  

Bir satınalma talebini **Satınalma talebi ayrıntıları** sayfasında **Beklemede** onay kutusunu seçerek beklemeye alabilirsiniz. Satınalma talebinin işlenmesine yalnızca beklemede onay kutusu seçimini kaldırdıktan sonra devam edebilirsiniz.  

> [!NOTE]
> e-procurement altında satın alma talebiniz için RFQ, satıcıların ilave satırlar eklemesine izin verebilir. Bu durumda satın alma talebiniz onaylanan alternatifleri yansıtır.

## <a name="demand-consolidation"></a>Talep konsolidasyonu
Birden fazla satın alma talebindeki satın alma talebi satırlarını birleştirerek, daha iyi fiyatlar, daha düşük nakliye ve taşıma maliyetleri ve daha düşük işletme maliyetleri elde etmek üzere satıcılarınızla pazarlık gücünüzü artırabilirsiniz.  

Satın alma talebi satırları talep birleştirilmesi için sadece aşağıdaki ifadelerin doğru olması durumunda uygun olacaktır:

-   Satın alma talebi onaylanmış olmalıdır.
-   Satın alma talebi, manuel işleme ve talep birleştirme için satın alma politikası kural kriterlerini karşılamalıdır.

Manuel işleme kriterlerini karşılayan, onaylanmış satın alma talep satırları **Onaylanan satın alma taleplerini serbest bırak** sayfasında listelenir. Bir satın alma talebi satırı ayrıca talep birleştirme kriterlerini karşılıyorsa satır bir birleştirme fırsatına eklenebilir.  

Bir birleştirme fırsatı, gruplandırılan bir satın alma talebi satırı kümesidir, böylece satın alma profesyonelleri satıcılarla en iyi anlaşmaları yapabilirler. Bir birleştirme fırsatı için seçtiğiniz satın alma talebi satırları **Satın alma talebi birleştirme** sayfasında görüntülenir. Değişiklikler gerekiyorsa bu sayfadaki satırları değiştirebilirsiniz. Ayrıca, birleştirme fırsatına yeni satırlar ekleyebilir veya mevcut satırları kaldırabilirsiniz.  

Bir birleştirme fırsatına satın alma satırları ekledikten ve gerekli değişiklikleri gerçekleştirdikten sonra birleştirilen satın alma talebi satırları için bir satın alma emri oluşturabilirsiniz.  

> [!NOTE]
> **Satın alma talebi birleştirme** sayfasında bir satın alma talebi için yaptığınız değişiklikler, oluşturduğunuz satın alma emrine yansıtılacaktır. Ancak, satır, satın alma talebinde değişmeden kalır, böylece tarihi korunur.  

Talep birleştirme için uygun olmayan veya bir birleştirme talebi için seçilmemiş satın alma talebi satırları için bir satın alma emri oluşturmak için satırları manuel olarak işlemeniz gerekir.

### <a name="consolidating-purchase-requisition-lines"></a>Satın alma talebi satırlarının birleştirilmesi

Talep birleştirme süreci bir iş akışında bir satın alma talebi onaylandığında ve organizasyonunuz için bütçe kontrolü yapılandırılmışsa bütçe rezervasyonları ve ön yükümlülükler kaydedildiğinde başlar. Aşağıdaki şemada talep birleştirme süreç akışı gösterilmiştir.  

[![İsteğe bağlı konsolidasyon için işlem akışı.](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Onaylanan satınalma talep satırlarını birleştirmek için şu adımları izleyin:

1.  Manuel işleme için tutulan ve talep birleştirme için uygun olan onaylanmış talep satırlarını gözden geçirin.
2.  Bir birleştirme fırsatına eklenecek satırları seçin.
3.  Yeni bir birleştirme fırsatı oluşturun veya mevcut bir birleştirme fırsatına talep satırları ekleyin.
4.  Talep satırlarında gerekli değişiklikleri gerçekleştirin ve birleştirme fırsatına artık dahil etmek istemediğiniz talep satırı maddelerini kaldırın.
5.  Birleştirilmiş talep satırları veya bir birleştirme fırsatındaki satın alma talebi satırları için satın alma emirleri oluşturun.


## <a name="additional-resources"></a>Ek kaynaklar

[Tüketim talebi oluşturma](tasks/create-requisition-consumption.md)

[Satınalma talebi iş akışı](purchase-requisitions-workflow.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]