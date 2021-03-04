---
title: Müşteri yaşlandırma raporu
description: Müşteri yaşlandırma raporu müşterilerin ödemesi gereken bakiyeleri, tarih aralığına veya yaşlandırma dönemine göre sıralanmış olarak görüntüler.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3a1bba4596c7b645c20a790a6cbe8725ab665d
ms.sourcegitcommit: d77e902b1ab436e5ff3e78c496f5a70ef38e737c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/15/2020
ms.locfileid: "4448981"
---
# <a name="customer-aging-report"></a>Müşteri yaşlandırma raporu 

**Müşteri yaşlandırma** raporu müşterilerin ödemesi gereken bakiyeleri, tarih aralığına veya yaşlandırma dönemine göre sıralanmış olarak görüntüler.

Raporu oluşturduğunuz zaman aşağıdaki varsayılan parametreler görüntülenir. Bu parametreleri, raporda gösterilecek verileri filtrelemek için kullanabilirsiniz. Daha fazla bilgi için bkz. [Koleksiyonlar ayarlama](set-up-collections.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Alan</p></th>
<th><p>Tanım</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Faturalama sınıflandırması</strong></p></td>
<td><p>Rapora dahil edilecek bir veya daha fazla faturalama sınıflandırması seçin.</p>
<div class="alert">

**Not:** Bu denetim yalnızca <STRONG>Kamu Sektörü</STRONG> yapılandırma anahtarı seçildiğinde kullanılabilir.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Faturalama sınıflandırması olmayan hareketleri dahil et</strong></p></td>
<td><p>Bu onay kutusu işaretlenirse, kendilerine atanmış bir faturalama sınıflandırması bulunmayan tüm hareketler raporda görüntülenir.</p>
<div class="alert">

**Not:** Bu denetim yalnızca <STRONG>Kamu sektörü</STRONG> yapılandırma anahtarı seçildiğinde kullanılabilir.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Yaşlandırma başlangıcı</strong></p></td>
<td><p>Geçerli yaşlandırma aralığı üzerinde kullanılan tarihi girin.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bakiye tarihi</strong></p></td>
<td><p>Müşteri bakiyelerinin görüntüleneceği tarihi girin. Bu, hareketler için kesme tarihi olarak da bilinir.</p></td>
</tr>
<tr class="even">
<td><p><strong>Başlangıç tarihi</strong></p></td>
<td><p>Rapora dahil edilecek ilk dönem aralığı veya yaşlandırma döneminde bulunan bir tarih girin.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Ölçütler</strong></p></td>
<td><p>Raporun temel alacağı tarih türünü seçin.</p>
<ul>
<li><p><strong>Hareket tarihi</strong> - Hareketlerin deftere nakil tarihi. Örneğin bu, vade tarihinin hesaplanması için temel oluşturan bir fatura tarihi olabilir.</p></li>
<li><p><strong>Vade tarihi</strong> – Ödeme koşullarınız temel alınarak belirlenen ve hareketlere ait vade tarihi.</p></li>
<li><p><strong>Belge tarihi</strong> – Vade tarihinin hesaplanması için temel olarak alınan ve kullanıcı tarafından tanımlanmış belge tarihi.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Yaşlandırma dönemi tanımı</strong></p></td>
<td><p>Bir yaşlandırma dönemi tanımı seçin. Yaşlandırma aralığı tanımı seçerseniz <strong>aralık</strong> alanı kullanılmaz.</p>
<p>Altı yaşlandırma döneminden daha fazla dönem içeren yaşlandırma dönemi tanımları yazdırılan raporda kullanılamaz.</p>
<div class="alert">

**Not:** <STRONG>Yaşlandırma dönemi tanımları</STRONG> sayfasında yaşlandırma dönemleri ayarlayabilirsiniz.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Yaşlandırma dönemi açıklamasını yazdır</strong></p></td>
<td><p>Yaşlandırma dönemi açıklamalarını rapordaki her yaşlandırma dönemi sütununun üst kısmına dahil etmek için <strong>Evet</strong> seçeneğini belirleyin. Raporu sütun başlıkları olmadan yazdırmak için <strong>Hayır</strong>'ı seçin.</p></td>
</tr>
<tr class="even">
<td><p><strong>Aralık</strong></p></td>
<td><p>Her dönemdeki gün veya ay sayısını girerek, kullanılacak dönemi tanımlayın. Örneğin, yaşlandırma bilgilerini haftalık olarak görüntülemek için bu alana 7 girin ve <strong>Gün/Ay</strong> alanında <strong>Gün</strong> seçeneğini belirleyin.</p>
<div class="alert">

**Not:** Bu alana girdiğiniz bilgiler yalnızca bir yaşlandırma dönemi tanımı seçmemişseniz kullanılabilir. Aksi durumda, yazdırma yönü yaşlandırma dönemi tanımında tanımlanır.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Gün/Ay</strong></p></td>
<td><p><strong>Aralık</strong> alanında dönemi tanımlamak için kullanılan birimi (<strong>Gün</strong> veya <strong>Ay</strong>) olarak seçin.</p></td>
</tr>
<tr class="even">
<td><p><strong>Yazdırma yönü</strong></p></td>
<td><p>Bakiyelerin hesapnaıp hesaplamayacağını ve geçmiş veya gelecekteki dönemler için yaşlandırma raporunu yazdırmayı seçin. Tarihler, <strong>Bakiyesi açık</strong> alanında seçilen tarihe göre değerlendirilir. Geçmiş dönemlerin bilgilerini göstermek için <strong>Geriye dönük</strong> seçeneğini belirleyin. Gelecek dönemlerin bilgilerini göstermek için <strong>İleriye dönük</strong> seçeneğini belirleyin.</p>
<div class="alert">
  
<STRONG>Not:</STRONG> Bu alana girdiğiniz bilgiler yalnızca bir yaşlandırma dönemi tanımı seçmemişseniz kullanılabilir.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Ayrıntılı</strong></p></td>
<td><p>Raporda gösterilen bakiyelere dahil edilen hareketleri listelemek için seçin.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tutarları hareket para birimi cinsinden ekle</strong></p></td>
<td><p>Muhasebe para birimi cinsinden tutarlara ek olarak, tutarları hareket para birimine dahil etmek için seçin. Bu onay kutusu işaretli değilse, rapordaki tutarlar yalnızca muhasebe para biriminde görüntülenir.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Eksi bakiye</strong></p></td>
<td><p>Negatif bakiyeleri olan müşteri hesaplarını dahil etmek için seçin.</p></td>
</tr>
<tr class="even">
<td><p><strong>Sıfır bakiye hesaplarını hariç tut</strong></p></td>
<td><p>Sıfır bakiyesi olan müşteri hesaplarını dışarıda bırakmak için seçin.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Ödeme yerleştirme</strong></p></td>
<td><p>Henüz kapatılmamış ödemeleri görüntülemek için seçin. Bunlar raporun ilk sütununda görüntülenir.</p></td>
</tr>
</tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]