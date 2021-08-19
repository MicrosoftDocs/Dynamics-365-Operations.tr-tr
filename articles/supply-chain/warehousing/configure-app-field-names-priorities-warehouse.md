---
title: Ambar Yönetimi mobil uygulaması için alanları yapılandırma
description: Bu konu, Ambar Yönetimi mobil uygulamasında gösterilen alan adlarını ve önceliklerini tanımlamayı ve yapılandırmayı açıklamaktadır.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 31b1d9e26a5c21a6be5fd89992316e1d6e657c183a71d5155d8d76e83362c845
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721163"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a>Ambar Yönetimi mobil uygulaması için alanları yapılandırma

[!include [banner](../includes/banner.md)]

Bu konu, Ambar Yönetimi mobil uygulamasında gösterilen alan adlarını ve önceliklerini tanımlamayı ve yapılandırmayı açıklamaktadır.

> [!NOTE]
> Bu konu, Ambar yönetimindeki özellikler için geçerlidir. Stok yönetimindeki özellikler için geçerli değildir. Ambar Yönetimi mobil uygulaması ambar görevlerini gerçekleştirmek için kullanabileceğiniz bir uygulamadır. Uygulama içerisinde kullanılan alan adlarını tanımlayabilir ve yapılandırabilirsiniz ve ayrıca alan adlarının atanacağı önceliği de yapılandırabilirsiniz. Bu konu, bu Ambar Yönetimi mobil uygulamalarının alan adlarını ve önceliklerini nasıl tanımlayacağını ve yapılandıracağını ve bunların nasıl kullanıldıklarını açıklar.

## <a name="configure-warehouse-app-field-names"></a>Ambar uygulaması alan adlarını yapılandırın

Ambarlama'yı mobil cihazınızda kullandığınızda, meta verini cihazınızda nasıl görüntüleceğini **Ambar uygulaması alan adları** sayfasından ayarlayabilirsiniz. Yeni bir şirkette ambar mobil cihaz iş akışlarında kullanılacak tüm alan adlarını oluşturmak için **Varsayılan kurulum oluşturma**'yı seçin ve daha sonra tercih edilen giriş modunu ve giriş türünü bunlara atayın. Tüm alan adlarını oluşturduktan sonra, aşağıdaki giriş seçeneklerini seçebilirsiniz.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Seçenek</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tercih edilen giriş modu</td>
<td>Bu seçenek, seçilen alan adı için bir tarama alanının mı yoksa elle girdi girişi alanının mı gösterileceğini belirler. Bu, barkodlar alanda kullanılıyorsa alanların ayırt edilmesi için kullanışlıdır. <strong>Not:</strong> Tercih edilen giriş modu <strong>Tarama</strong> olarak ayarlanmış alanlar için, barkod okunamaz veya zarar görmüşse, bilgileri el ile girebilirsiniz.</td>
</tr>
<tr class="even">
<td>Giriş türü</td>
<td>Bu seçenek, seçilen alan adı için hangi giriş türünün kullanılacağını tanımlar. Dört seçenek kullanılabilir:
<ul>
<li><strong>Seçim</strong> - Aralarından seçim yapabileceğiniz seçeneklerin listesini içerir. Bu seçenekle alan adları düzenlenebilir değildir.</li>
<li><strong>Tarih</strong> - Tarih olarak belirtilen alan adları etiket ile bir tarih biçimi gösterir. Bu, ambar çalışanlarının tarihi hangi biçimde gireceklerini görmelerine yardımcı olur. Bu seçenekle alan adları düzenlenebilir değildir.</li>
<li><strong>Alfa</strong> - Seçiliyse, cihazın klavyesi bilgiyi uygulamaya el ile girmek için kullanılır. Klavye deneyimi, hangi cihazın kullanıldığına göre değiştirilebilir.</li>
<li><strong>Sayısal</strong> - Yalnızca sayısal giriş kullanan alan adları için giriş alanında cihaz klavyesi yerine özel bir sayısal klavye görüntülemek için bu seçeneği kullanabilirsiniz.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>Ambar uygulaması alan önceliğini yapılandırma

**Ambar uygulaması alan önceliği** sayfasında, alan adlarını farklı öncelik gruplarına yerleştirebilirsiniz. Ambar çalışanları uygulamayı kullanırlarken ana görev sayfasında hangi bilginin gösterileceğini belirlemeyi mümkün kılar. **Varsayılan kurulum oluştur** üzerine tıklarsanız, öncelik gruplarının varsayılan bir kümesi oluşturulur. İhtiyaç duyulduğu kadar öncelik grubu oluşturmak mümkündür, ancak görev sayfasında sadece üç öncelik grubu gösterilir. Sistem uygulamaya meta veri gönderdiğinde her alanın öncelik grubuna göre bir göreceli öncelik atar ve uygulama, görev sayfası içerisindeki meta veride içerilen ilk üç öncelik grubunu görüntüler. Taşan meta verinin geri kalanı, ikincil ayrıntılar sayfasında görüntülenir. Aşağıdaki tablo beş öncelik grubu örneğini gösterir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Önceli grubu</th>
<th>Atanan alanlar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Ölçüt 10</td>
<td><ul>
<li>Madde</li>
<li>Miktar</li>
<li>Ölçü birimi</li>
</ul></td>
</tr>
<tr class="even">
<td> Ölçüt 20</td>
<td><ul>
<li>Küme konumu</li>
<li>Küme</li>
</ul></td>
</tr>
<tr class="odd">
<td> Ölçüt 30</td>
<td><ul>
<li>Madde açıklaması</li>
</ul></td>
</tr>
<tr class="even">
<td> Ölçüt 40</td>
<td><ul>
<li>Yapılandırma</li>
<li>Renk</li>
<li>Ebat</li>
<li>Stil</li>
</ul></td>
</tr>
<tr class="odd">
<td> Ölçüt 50</td>
<td><ul>
<li>Yer</li>
<li>Plaka</li>
</ul></td>
</tr>
</tbody>
</table>

Örneğin bir ambar çalışanı mobil cihaz üzerinde bir görev yerine getirdiğinde, uygulamada görüntülenen meta veri aşağıdaki alanlardan oluşuyorsa:

-   Madde
-   Miktar
-   Ölçü birimi
-   Madde açıklaması
-   Boyut ve Konum

Yukarıdaki tabloda ayarlanmış olan ambar uygulaması alan öncelik kümesine dayanarak, aşağıdaki 3 bilgi satırı görev sayfasında görüntülenir.

-   Satır 1: Madde, Miktar ve Ölçü Birimi
-   Satır 2: Madde açıklaması
-   Satır 3: Boyut

Kalan meta veri, örneğin Konum, görev sayfasında görüntülenmeyecektir, ancak bir ayrıntılar sayfasında görüntülenir. Kullanıcı arabirimi hakkında daha fazla bilgi almak ve örnekler görmek için şu blog gönderisine bakın [Finance and Operations - Ambarlama](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

## <a name="additional-resources"></a>Ek kaynaklar

[Ambar Yönetimi mobil uygulamasını yükleme ve bağlama](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]