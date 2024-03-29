---
title: Denetim ilkesi kuralları
description: Gider raporlarını, satıcı faturalarını ve satınalma siparişlerini değerlendirerek, oluşturduğunuz ilke kurallarına uygun olup olmadıklarından emin olmak için denetim ilkelerini kullanabilirsiniz. Bir denetim ilkesiyle ilişkili kuralların tümü, belirlediğiniz bir zaman planına göre top iş modunda çalıştırılır.  Her ilke kuralı, ilke kuralı türünün bir örneğidir. Her ilke kuralı türü için aynı anda yalnızca bir ilke kuralı etkin olabilir.
author: panolte
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: kfend
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8272cd516f1b31f20ded7c2fdb8bfc4c4d984d42
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710515"
---
# <a name="audit-policy-rules"></a>Denetim ilkesi kuralları

[!include [banner](../includes/banner.md)]

Gider raporlarını, satıcı faturalarını ve satınalma siparişlerini değerlendirerek, oluşturduğunuz ilke kurallarına uygun olup olmadıklarından emin olmak için denetim ilkelerini kullanabilirsiniz. Bir denetim ilkesiyle ilişkili kuralların tümü, belirlediğiniz bir zaman planına göre top iş modunda çalıştırılır.  Her ilke kuralı, ilke kuralı türünün bir örneğidir. Her ilke kuralı türü için aynı anda yalnızca bir ilke kuralı etkin olabilir. 

## <a name="queries-and-query-types"></a>Sorgular ve sorgu türleri

Bir denetim ilkesi kuralı oluşturduğunuzda öncelikle bir ilke kuralı türü seçersiniz. İlke kuralı türü, ilke kuralının oluşturulmasında başlangıç noktası olarak kullanılmak üzere Uygulama Nesne Ağacı (AOT) sorgusunu belirler. Ayrıca, ilke kuralı için kullanmak üzere sorgu türünü belirtir. Sorgu, İlke kuralının değerlendirdiği kaynak belgeyi belirler. Ayrıca, kaynak belgesinde hem tüzel kişiliği hem belgeler denetim için seçildiğinde kullanılacak tarihi tanımlayan alanları belirler. Sorgu türü, sorgu sayfasındaki ve Denetim ilkesi kuralı sayfadaki varsayılan alanları kontrol eder. Aşağıdaki tabloda denetim ilkesi kuralları için mevcut sorgu türleri gösterilmiştir.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Sorgu tipi</th>
<th>Amaç</th>
<th>Daha fazla bilgi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Koşullu</td>
<td>Kaynak belge öznitelikleri belirtilen değerlerle karşılaştırarak değerlendirin.</td>
<td></td>
</tr>
<tr class="even">
<td>Topla</td>
<td>Nümerik değerleri toplayarak birden fazla kaynak belgesini veya kaynak belge satırlarını bir ilke kuralıyla karşılaştırarak değerlendirin.</td>
<td></td>
</tr>
<tr class="odd">
<td>Örnekleme</td>
<td>Politika ihlalleri için değerlendirmek üzere kaynak belgelerin belirli bir oranını rastgele seçin.</td>
<td>Bu seçimi yaptığınızda, denetim için rastgele seçilecek belge yüzdesini belirlemek için Denetim ilkesi kuralı sayfasını kullanın.</td>
</tr>
<tr class="even">
<td>Çoğalt</td>
<td>Belirtilen alanlarda tekrarlanan girdileri içerip içermediğini belirlemek için kaynak belgeleri değerlendirin.</td>
<td>Bu seçimi yaptığınızda, belgeler tekrarlanan girdiler için değerlendirildiğinde belge seçim tarihi aralığının başlangıcı olarak eklenecek gün sayısını belirlemek için Denetim İlkesi kuralı sayfasını kullanın.</td>
</tr>
<tr class="odd">
<td>Liste araması</td>
<td>Belirli varlıklar için kaynak belgeleri değerlendirin.</td>
<td>Sorgu kök belgesi, denetlenen belgeyi tanımlar. Sorgu mutlaka dirpartytable tablosuna bir referans içeren bir liste sorgusu olmalıdır. Bu seçenek sadece aşağıdaki AOT sorgularıyla kullanılabilir:
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (Gider raporu izlenen personel)</li>
<li><span class="ui">AuditPolicyPurchList</span> (Satın alma emri izlenen satıcılar)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (Satıcı faturası izlenen satıcılar)</li>
</ul>
Bu seçimi yaptığınızda, Denetim İlkesi kuralı sayfasında izlenen varlıkları belirtin.</td>
</tr>
<tr class="even">
<td>Anahtar sözcük araması</td>
<td>Belirli sözcükleri içerip içermediklerini belirlemek için kaynak belgeleri değerlendirin.</td>
<td>Bu seçimi yaptığınızda, Denetim İlkesi kuralı sayfasına aradığınız kelimeleri girin. Denetim İlkesi kural sayfası ayrıca girdiğiniz sözcükler için değerlendirilecek tabloları ve alanları belirlemenizi sağlayan seçenekler de içerir.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Genel parametreler
Belirli bir denetim ilkesi için ilke kurallarının tümü aynı toplu iş parametrelerini ve aynı belge seçimin tarihi aralığını paylaşır. Bu parametreler, ilke için İlave seçenekler sayfasında belirlenir.



## <a name="additional-resources"></a>Ek kaynaklar

[İlke ihlali ve olaylarını denetleme](audit-policy-violations-cases.md)
[Kaynak belgeler için denetleme ilkeleri tanımla](tasks/define-audit-policies-source-documents.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
