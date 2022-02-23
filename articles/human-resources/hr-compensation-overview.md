---
title: Ücret planları
description: Ücret ve Kazanç Yöneticileri, kuruluşun çalışanları için sabit veya değişken ücret planlarını korumak ve işlemek için Ücret yönetimi kullanabilirler.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b6dd163b0e956624eb57fa031b918a94609f9cfa
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420896"
---
# <a name="compensation-plans"></a>Ücret planları

Ücret ve Kazanç Yöneticileri, kuruluşun çalışanları için sabit veya değişken ücret planlarını korumak ve işlemek için Ücret yönetimi kullanabilirler.

### <a name="introduction"></a>Giriş

Ücret yönetimi, temel maaş ve ikramiyelerin teslimatının denetimi için kullanılır. Bir personelin sabit temel maaşı ve başarı artışı, sabit ücret planları aracılığıyla denetlenir. İkramiyelerin ödemesi, örneğin prim ödemeleri, performans ödülleri, hisseler, hibeler ve ayrıca da tek seferlik ödüller, değişken ücret planları tarafından denetlenir. 

Çalışanlar her iki tipteki bir veya daha çok plana kayıtlı olabilir. Bir çalışanın ücret planındaki kayıt için uygun olması için aşağıdaki gereksinimleri karşılaması gerekir:
-   Çalışanın aktif bir pozisyon atamasının olması gerekir.
-   Çalışanın maaş planı uygunluk kuralları tarafından tanımlanan ölçütlere uyması gerekir.

## <a name="compensation-setup"></a> Ücret ayarla
Aşağıdaki tablo, Şirketinizin ücretlendirme planını ayarlarken ücretlendirme işleminin bütünleyici olabilecek bileşenlerini listelemektedir.

<table>
<thead>
<tr class="header">
<th>Bileşen</th>
<th>Daha fazla bilgi...</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sabit maaş eylemleri</td>
<td>Sabit ücret eylemleri iki amacı gerçekleştirir:
<ul>
<li>Eylemler, bir çalışanın ücreti değiştiğinde kayıt edilmesi gereken bilgileri belirleyebilir. Örneğin, promosyon veya indirme gibi bir değişim için bir sebebin kaydedilmesini gerektirebilirsiniz.</li>
<li>Eylemler, bir hesaplamanın bir sabit ücret planı işlendiğinde uygulandığından emin olunması sağlayabilir.  Örneğin, öz varlık türündeki eylemler, çalışanın ücretini, çalışanın seviyesinin en düşük referans noktasıyla kıyaslar ve çalışanın en az minimum miktar kadar ücret aldığından emin olunmasını sağlar.</li>
</ul></td>
</tr>
<tr class="even">
<td>Düzeyler</td>
<td>Düzeyler işlerle ve bir işle ilgili olan tüm pozisyonlarla ilişkilidir. Üç ücret planı tipi için de farklı düzeyler oluşturabilirsiniz: Derece, Bant ve Adım.</td>
</tr>
<tr class="odd">
<td>Ücret kademesi kullanım oranı matrisi</td>
<td>Kademesi kullanım oranı matrisi, çalışanları işlerinin denetim noktalarına geçiş yaptırmanıza yardımcı olur. Ayrıca, bireysel bir çalışanın performansına veya şirketin genel performansına bakmaksızın, şirket içindeki ödeme oranı eşitliğini kontrol etmek için aralık kullanımını kullanabilirsiniz. Örneğin, kendi aralıklarında daha düşük ödeme alan çalışanlar, aralıkta daha yüksek ücret alan çalışanlara göre daha yüksek oranlı artışlar alır. Bu şekilde, öz varlıklar arasındaki farkları sistematik olarak mahsup edebilirsiniz. Kademesi kullanımı aşağıdaki gibi hesaplanır: (Sabit ödeme oranı - Aralik minimumu) ÷ (Aralık maksimumu - Aralık minimumu).</td>
</tr>
<tr class="even">
<td>Referans noktası ayarları</td>
<td>Bir referans noktası ayarlamasına, matris içindeki aralığı temsil eden bir dizi referans noktası dahildir. Her aralık bir ödeme oranı ile ilişkili olabilir. Örneğin, kademe planları genellikle; en az, orta nokta ve en sık referans noktalarına sahip olacaktır.</td>
</tr>
<tr class="odd">
<td>Ücret matrisi</td>
<td>Ücret matrisi, bir ücretlendirme yapısı oluşturmak için kullanabileceğiniz referans noktaları ve düzeyleri kümesidir.</td>
</tr>
<tr class="even">
<td>Maaş yapısı</td>
<td>Bir ücret yapısı, ödeme oranlarının her bir düzey için referans noktalarıyla ilişkilendirildiği bir ödeme matrisidir.</td>
</tr>
<tr class="odd">
<td>Uygunluk kuralları</td>
<td>Uygunluk kuralları, çalışanların dahil olduğu belirli işler, iş işlevler, iş türler, departmanlar, işçi sendikaları veya belirli maaş planları tarafından kapsanan maaş bölgeleri tanımlamak için kullanılır. Çalışanları plana kaydetmek için hem değişken hem de sabit maaş planları için uygunluk kuralları oluşturmanız gerekir. Bir tazminat planına ilişkin uygunluk kurallarını belirttikten sonra, plandan, plan tarafından kapsanan işlere uygulanacak düzey kümelerini tanımlayabilirsiniz.</td>
</tr>
<tr class="even">
<td>Ödeme sıklıkları</td>
<td>Ödeme sıklıkları, ücretin belirtildiği zaman aralığını belirtmek için kullanılır.  Örneğin, ödeme sıklığı, saatlik ödeme oranına karşılık, yıllık bir maaş olarak mı belirtilmiş olduğunu anlamanıza yardımcı olur. Ödeme sıklıkları ayrıca dönüşüm faktörlerini, aylık, haftalık, iki haftalık ve saatlik ödeme sıklıklarını, yıllık ödeme sıklığına dönüştürmek için dönüşüm faktörlerini ayarlamak için kullanılır.</td>
</tr>
<tr class="odd">
<td>Tazminat bölgeleri</td>
<td>Ücret bölgeleri, çalışma alanı konumu esas alınarak çalışanın maaşını belirtmek için kullanılır.</td>
</tr>
<tr class="even">
<td>Kontrol noktası</td>
<td>Kontrol noktası tüm çalışanlar için tazminat düzeyinin ne olduğunu düşündüğünüzü belirleyen ödeme oranını tanımlar. Kademeli plan yapılarında kontrol noktaları genellikle aralığın orta noktasıdır. Bant yapıları nadiren kontrol noktaları kullanır. Sabit maaş planı için denetim noktasını, Sabit maaş planları formunda belirtebilirsiniz.</td>
</tr>
<tr class="odd">
<td>İş işlevleri</td>
<td>İş işlevleri, belirli işler için maaş planlarını sınıflandırmada ve filtre uygulamada kullanılır.</td>
</tr>
<tr class="even">
<td>İş tipleri</td>
<td>İş türleri, belirli işler için maaş planlarını sınıflandırmada ve filtre uygulamada kullanılır.</td>
</tr>
<tr class="odd">
<td>Değişken maaş tipleri</td>
<td>Stok ödülleri veya nakit ödül primleri gibi değişken tazminat tipleri değişken tazminat planlarında ayarlanır.</td>
</tr>
<tr class="even">
<td>Maaş kılavuzları</td>
<td>Ücret yapısını içeren ücret kılavuzları.  Ücret kılavuzları, bir veya birden fazla ücret planları tarafından kullanılabilir.</td>
</tr>
<tr class="odd">
<td>Performans planları</td>
<td>Performans planları bir performans için ödeme stratejisinde kullanmak için planı bir dağıtım matrisiyle ilişkilendirmede kullanılabilir.</td>
</tr>
<tr class="even">
<td>Performans değerlendirmeleri</td>
<td>Performans notları, performans planlarında bir hak edilen ödül tutarını veya performans ödülünü belirlemek üzere kullanılır.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a> İşleme olayları
Bir işleme olayı, bir veya daha fazla sabit ya da değişken tazminat planına kayıtlı tüm çalışanlar için belirli bir döneme ait tazminat bilgilerini hesaplayan ücret iş akışlarıdır. Bir işleme olayını, ücretlendirme sonuçlarını test etmek veya güncelleştirmek için tekrar tekrar çalıştırabilirsiniz.

<a name="compensation-events"></a>Maaş olayları
-------------------

İşlem etkinliği her çalıştırıldığında bir ücret etkinliği oluşturulur.  Ücret etkinlikleri, bu işlem etkinliğine dahil edilmiş her personel ücret işleminin sonucunu içerirler.  Hesaplamalar doğru olduğunda, işlem etkinliklerinden etkilenen personellerin ücret kayıtlarını güncelleştirmek için ücret etkinliğini yükleyebilirsiniz.

## <a name="recommendations"></a> Öneriler
İşlem olayını çalıştırdıktan sonra, bir çalışanın başarı artış veya ikramiye tutarına, işleme olayında hesaplanan yönergelere göre ayarlamalar yapılması önerilir. Çalışanlar için öneriler yapmak için ücret planlarını veya işlem olayını ayarladığınızda, önerileri etkinleştirmeniz gerekir.



