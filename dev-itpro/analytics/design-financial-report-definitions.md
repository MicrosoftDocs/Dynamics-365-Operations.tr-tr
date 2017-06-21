---
title: "Finansal rapor tasarımcısında rapor tanımları"
description: "Bu makalede rapor tanımları hakkında bilgi verilmektedir. Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanan bir rapor bileşenidir (veya yapı taşıdır). Bir rapor tanımı ayrıca bir raporu özelleştirmek için kullanılan seçenek ve ayarlar sunar."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: ShylaThompson
ms.search.scope: Management Reporter, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 86b527b72ef0c9af71e70fe280bcdfe3992a36b1
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="report-definitions-in-financial-report-designer"></a>Finansal rapor tasarımcısında rapor tanımları

[!include[banner](../includes/banner.md)]


Bu makalede rapor tanımları hakkında bilgi verilmektedir. Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanan bir rapor bileşenidir (veya yapı taşıdır). Bir rapor tanımı ayrıca bir raporu özelleştirmek için kullanılan seçenek ve ayarlar sunar. 

Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanan bir rapor bileşenidir (veya yapı taşıdır). Bir rapor tanımı, ayrıca raporun özelleştirilmesi için kullanabileceğiniz ilave seçenekler ve ayarlar da sağlar. Satır tanımlarını ve sütun tanımları tanımladıktan sonra rapor tanımında birleştirmeniz gerekir. Bu noktada, ayrıntı düzeyi ve rapor tarihi gibi diğer tanım yönlerini de tanımlarsınız. Ardından kaydedebilir ve rapor oluşturabilirsiniz. Mali raporlama aşağıdaki ayrıntı düzeylerini sunar:

-   Mali
-   Finans ve Hesap
-   Finans, Hesap ve İşlem

Ancak, verilerin Microsoft Dynamics ERP sisteminde nasıl depolandığına bağlı olarak, işlem ayrıntıları raporlarda mevcut olmayabilir.

## <a name="create-a-report-definition"></a>Rapor tanımı oluşturma
1.  Rapor Tasarımcısı'nda **Dosya** menüsünde **Yeni** seçeneğini tıklatın ve sonra **Rapor Tanımı** seçeneğini seçin.
2.  **Rapor**, **Çıktı ve Dağıtım**, **Üstbilgiler ve Altbilgiler** ve **Ayarlar** sekmelerinde uygun bilgileri belirtin.

## <a name="contents-of-a-report-definition"></a>Bir rapor tanımı içeriği
Aşağıdaki tablo, rapor tanımı sekmeleirni ve bilgilerin nasıl kullanıldığını açıklanmaktadır.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sekme</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Rapor</td>
<td>Rapor oluşturma, rapor yapılandırma veya varolan bir raporu değiştirme.</td>
</tr>
<tr class="even">
<td>Çıktı ve Dağıtım</td>
<td>Çıktı türünü ve rapor hedefini değiştirin.</td>
</tr>
<tr class="odd">
<td>Üst Bilgiler ve Alt bilgiler</td>
<td>Rapor için üst bilgileri ve alt bilgileri tanımlayın ve biçimlendirin. Örneğin, üstbilgiye veya altbilgiye metin veya resim ekleyebilirsiniz. Mali raporlama görüntülerde .bmp, .jpg ve .png dosyalarını destekler. Şirket adı, rapor adı veya sayfa numarası gibi diğer bilgileri eklemek için otomatik metin kodlarını da ekleyebilirsiniz.</td>
</tr>
<tr class="even">
<td>Ayarlar</td>
<td>Aşağıdaki ayarları gibi rapor tanımı ayarlarını belirtin:
<ul>
<li>Biçimlendirme ve tutarların yuvarlanması</li>
<li>Ayrıntı raporlarını biçimlendirme</li>
<li>Raporlama ağaçlarını biçimlendirme</li>
<li>Özel durum raporu oluşturma</li>
<li>Para birimi dönüştürme belirtme</li>
<li>Alt toplam ve filtre hesap ayrıntıları</li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Ayrıca bkz.
--------

[Mali raporlama](financial-reporting-intro.md)




