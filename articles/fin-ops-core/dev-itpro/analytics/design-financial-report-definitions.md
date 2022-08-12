---
title: Finansal rapor tasarımcısında rapor tanımları
description: Bu makalede rapor tanımları hakkında bilgi verilmektedir.
author: aprilolson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom:
- "59131"
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.form: FinancialReports
ms.openlocfilehash: 0c581637b9c122f4cf34279f7f0b030041c0ac48
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206147"
---
# <a name="report-definitions-in-financial-report-designer"></a>Finansal rapor tasarımcısında rapor tanımları

[!include [banner](../includes/banner.md)]

Bu makalede rapor tanımları hakkında bilgi verilmektedir. Bir rapor tanımı, bir satır tanımı, bir sütun tanımı ve rapor oluşturmak için isteğe bağlı bir raporlama ağacı tanımı kullanılan bir rapor bileşenidir (veya yapı taşıdır). Bir rapor tanımı ayrıca bir raporu özelleştirmek için kullanılan seçenek ve ayarlar sunar. 

Bir rapor tanımı bir rapor oluşturmak üzere bir satır tanımı, bir sütun tanımı ve bir opsiyonel raporlama ağacı tanımı kullanan bir rapor bileşenidir (veya yapı taşıdır). Ayrıca bir rapor tanımı, bir raporu özelleştirmek için kullanabileceğiniz seçenekler ve ayarlar sağlar. Satır tanımları ile sütun tanımlarını belirlemenizin ardından, bunları bir rapor tanımında birleştirmeniz gerekir. Bu noktada, ayrıntı düzeyi ve rapor tarihi gibi diğer tanım yönlerini de tanımlarsınız. Ardından kaydedebilir ve rapor oluşturabilirsiniz. Mali raporlama aşağıdaki ayrıntı düzeylerini sunar:

- Mali
- Finans ve Hesap
- Mali, Hesap ve Hareket

Ancak, verilerin Microsoft Dynamics ERP sisteminde nasıl saklandığına bağlı olarak, hareket ayrıntıları raporlarda kullanılamayabilir.

## <a name="create-a-report-definition"></a>Rapor tanımı oluşturma
1. Rapor Tasarımcısı'ndaki **Dosya** menüsünde, **Yeni**'ye tıklayın ve ardından **Rapor Tanımı**'nı seçin.
2. **Rapor**, **Çıkış ve Dağıtım**, **Üst Bilgiler ve Alt Bilgiler** ve **Ayarlar** sekmelerinde ilgili bilgileri belirtin.

## <a name="contents-of-a-report-definition"></a>Bir rapor tanımının içerikleri
Aşağıdaki tabloda bir rapor tanımındaki sekmeler ve bilgilerin nasıl kullanıldığı açıklanmaktadır.

<table>
<thead>
<tr>
<th>Sekme</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr>
<td>Rapor</td>
<td>Rapor oluşturun, rapor yapılandırın veya var olan bir raporu değiştirin.</td>
</tr>
<tr>
<td>Çıkış ve Dağıtım</td>
<td>Raporun çıkış türünü ve hedefini değiştirin.</td>
</tr>
<tr>
<td>Üst Bilgiler ve Alt Bilgiler</td>
<td>Raporun üst bilgilerini ve alt bilgilerini tanımlayıp biçimlendirin. Örneğin, üstbilgiye veya altbilgiye metin veya resim ekleyebilirsiniz. Mali raporlama görüntülerde .bmp, .jpg ve .png dosyalarını destekler. Şirket adı, rapor adı veya sayfa numarası gibi diğer bilgileri eklemek için otomatik metin kodlarını da ekleyebilirsiniz.</td>
</tr>
<tr>
<td>Ayarlar</td>
<td>Aşağıdaki ayarlar gibi rapor tanımı ayarlarını belirtin:
<ul>
<li>Tutarları biçimlendirme ve yuvarlama</li>
<li>Ayrıntı raporlarını biçimlendirme</li>
<li>Raporlama ağaçlarını biçimlendirme</li>
<li>Özel durum raporu oluşturma</li>
<li>Para birimi dönüşümü belirtme</li>
<li>Alt toplam ve filtre hesabı ayrıntıları</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Ek kaynaklar

[Mali raporlama](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
