---
title: "Warehousing app içinde App alan adlarını yapılandırın"
description: "Bu konuda nasıl tanımlanacağını ve ambar app alan adları ve öncelikleri Dynamics 365 işlemleri için yapılandırma açıklanmaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>Warehousing app içinde App alan adlarını yapılandırın

Bu konuda nasıl tanımlanacağını ve ambar app alan adları ve öncelikleri Dynamics 365 işlemleri için yapılandırma açıklanmaktadır. 

**Not:** Bu konu için ambar yönetimi özellikleri için geçerlidir. Stok Yönetimi özellikleri için geçerli değildir. Operasyon - 365 Dynamics depolama ambar görevleri gerçekleştirmek için kullanabileceğiniz bir uygulamadır. Siz tanımlamak ve app içinde kullanılan alan adlarını yapılandırın yanı alan adları atanması gereken önceliği yapılandırmak. Bu konuda nasıl tanımlanacağını ve bu ambar app alan adları ve öncelikleri yapılandırmak ve Dynamics 365 içinde depolama işlemleri için - nasıl kullanıldıkları açıklanmıştır. Başvurmak için öğretici Dynamics 365 işlemleri - depolama, bağlantıyı yapılandırma hakkında ayrıntılı bilgi için [yükleme ve yapılandırma işlemleri - depolama için Dynamics 365](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Ambar app alan adlarını yapılandırın
===================================

Dynamics 365 - işlemlerinde kullanmak, mobil aygıtınızda depolama aygıtınızda üzerinde meta verilerin nasıl görüntüleneceğini yapılandırabilirsiniz **ambar app alan adları** sayfa. Dynamics 365 işlemleri için de yeni bir şirkette seçin **varsayılan kurulum oluşturma** ambar mobil aygıt iş akışlarında kullanılan ve sonra tercih edilen giriş modunu ve giriş türü atayabilirsiniz tüm alan adları oluşturmak için. Tüm alan adları oluşturduktan sonra aşağıdaki giriş seçenekleri seçebilirsiniz.

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
<td>Bu seçenek bir tarama alanı olup olmadığını tanımlar veya el ile giriş giriş alanı için seçilen alan adı gösterilecek. Bu alan için barkodlar kullandıysanız alanlara bağlı olarak ayırt etmek kullanışlıdır. <strong>Not:</strong> alan adları ile tercih edilen giriş modunu ayarlamak için <strong>tarama</strong>, barkod okunamaz veya zarar görmüşse, bilgileri el ile girebilirsiniz.</td>
</tr>
<tr class="even">
<td>Giriş türü</td>
<td>Bu seçenek, giriş türü için seçilen alan adı kullanılması gerektiğini tanımlar. Dört seçenek vardır:
<ul>
<li><strong>Seçim</strong> - aralarından seçim yapabileceğiniz seçeneklerin listesini içerir. Bu seçenekle alan adları düzenlenebilir değildir.</li>
<li><strong>Tarih</strong> - alan adları belirtilen bir tarih biçimi etiketli tarih gösterilir. Bu tarihi girmek için hangi biçimde bkz: Ambar çalışanlarına yardımcı olur. Bu seçenekle alan adları düzenlenebilir değildir.</li>
<li><strong>Alfa</strong> - seçtiyseniz, klavye aygıtı el ile app içinde bilgi girerken kullanılacak. Hangi aygıt kullanılan klavye deneyimini değiştirilebilir.</li>
<li><strong>Sayısal</strong> - yalnızca giriş o kullanım sayısal alan adlarına ilişkin bir özel sayısal tuş takımıyla aygıtı klavye yerine giriş alanını görüntülemek için bu seçeneği seçin.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Ambar uygulama alanını önceliğini yapılandırma
======================================

Üzerinde **ambar uygulama alanını öncelik** sayfasında, alan adları farklı öncelik gruplar halinde koyabilirsiniz. Ambar çalışanlarına app kullanarak görevleri gerçekleştirdiğinizde ana görev sayfasında hangi bilgilerin görüntülenmesi gereken karar mümkün kılar. ' İ tıklatırsanız **varsayılan kurulum oluşturma**, varsayılan öncelik grupları kümesi oluşturulur. Gereken sayıda öncelik grubu oluşturmak mümkündür, ancak yalnızca üç öncelik grupları Görev sayfasında gösterilir. Dynamics 365 işlemleri için app için meta veri gönderdiğinde, her alan kendi öncelik grubuna bağlı olarak göreceli bir öncelik atar ve app meta verileri görev sayfasında yer alan ilk üç öncelik grupları görüntüler. Taşan meta verileri geri kalanı İkincil Ayrıntıları sayfasında görüntülenir. Aşağıdaki tablo beş öncelikli Grup örneği gösterir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Grup önceliği</th>
<th>Atanan alanlar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> Öncelik 10</td>
<td><ul>
<li>Madde</li>
<li>Miktar</li>
<li>Ölçü birimi</li>
</ul></td>
</tr>
<tr class="even">
<td> Öncelik 20</td>
<td><ul>
<li>Küme konumu</li>
<li>Küme</li>
</ul></td>
</tr>
<tr class="odd">
<td> Öncelik 30</td>
<td><ul>
<li>Madde açıklaması</li>
</ul></td>
</tr>
<tr class="even">
<td> Öncelik 40</td>
<td><ul>
<li>Yapılandırma</li>
<li>Renk</li>
<li>Ebat</li>
<li>Stil</li>
</ul></td>
</tr>
<tr class="odd">
<td> Priority 50</td>
<td><ul>
<li>Yer</li>
<li>Plaka</li>
</ul></td>
</tr>
</tbody>
</table>

App içinde görüntülenen meta verileri şu alanlardan oluşur, örneğin, ne zaman bir ambar çalışanı görev bir mobil aygıtta gerçekleştiriyor:

-   Madde
-   Miktar
-   Ölçü birimi
-   Madde açıklaması
-   Boyut ve konum

Yukarıdaki tabloda ayarladığınız ambar app alan öncelik bağlı olarak, aşağıdaki 3 satır bilgisi görev sayfasında görüntülenir:

-   Satır 1: Madde, miktar, ölçü birimi
-   2. satır: Madde açıklaması
-   Satır 3: boyut

Örneğin, konum, kalan meta verileri görev sayfasında görüntülenmez, ancak Ayrıntıları sayfasında görüntülenir. Daha fazla bilgi edinmek ve kullanıcı arabirim örnekleri görmek için blog postasının bakın [Dynamics 365 duyuran işlemleri - depolama için](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Ayrıca bkz.
--------

[Yüklemek ve yapılandırmak için depolama işlemleri – Microsoft Dynamics 365](install-configure-warehousing-app.md)


