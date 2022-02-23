---
title: Ambarlama uygulaması içerisinde alan adlarını yapılandırma
description: Bu konu, Dynamics 365 Supply Chain Management için ambar uygulaması alan adlarını ve önceliklerini tanımlamayı ve yapılandırmayı açıklamaktadır.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: ac31b3d2b3b1d9ca51919fe75e06f0de1cda0c63
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963447"
---
# <a name="configure-app-field-names-in-the-warehouse-app"></a>Ambarlama uygulaması içerisinde alan adlarını yapılandırma

[!include [banner](../includes/banner.md)]

Bu konu, Dynamics 365 Supply Chain Management için ambar uygulaması alan adlarını ve önceliklerini tanımlamayı ve yapılandırmayı açıklamaktadır. 

> [!NOTE]
> Bu konu, Ambar yönetimindeki özellikler için geçerlidir. Stok yönetimindeki özellikler için geçerli değildir. Ambarlama, ambar görevlerini gerçekleştirmek için kullanabileceğiniz bir uygulamadır. Uygulama içerisinde kullanılan alan adlarını tanımlayabilir ve yapılandırabilirsiniz ve ayrıca alan adlarının atanacağı önceliği de yapılandırabilirsiniz. Bu konu, bu ambar uygulamaların alan adlarını ve önceliklerini nasıl tanımlayacağını ve yapılandıracağını ve bunların Ambarlama içerisinde nasıl kullanıldıklarını açıklar. Ambarlama'ya bağlantıyı yapılandırma hakkında ayrıntılı bilgi için [Ambarlama uygulamasını yükleme ve yapılandırmaya genel bakış](install-configure-warehousing-app.md) eğitimine bakın.

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

<a name="additional-resources"></a>Ek kaynaklar
--------

[Ambarlama uygulamasını yükleme ve yapılandırmaya genel bakış](install-configure-warehousing-app.md)
