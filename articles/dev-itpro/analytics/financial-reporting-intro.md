---
title: Mali raporlama
description: Finance and Operations için mali raporlama, finans ve şirket profesyonellerinin mali tabloları oluşturmasını, güncelleştirmesini, dağıtmasını ve görüntülemesini sağlar. Farklı türlerde raporlar tasarlamanıza yardımcı olmak için geleneksel raporlama kısıtlamalarının ötesine geçer.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ae2087cf142fc2670bda3c542b336f12978178a6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2019
ms.locfileid: "323790"
---
# <a name="financial-reporting"></a>Mali raporlama

[!include [banner](../includes/banner.md)]

Finance and Operations için mali raporlama, finans ve şirket profesyonellerinin mali tabloları oluşturmasını, güncelleştirmesini, dağıtmasını ve görüntülemesini sağlar. Geleneksel raporlama kısıtlamalarının ötesine geçerek çeşitli rapor türlerini etkin şekilde oluşturmanıza yardımcı olur.

Mali raporlama boyut desteği içerir. Bu nedenle, hesap segmentleri veya boyutları derhal kullanılabilir hale gelir Ek araçlar veya yapılandırma adımları gerekli değildir.

## <a name="financial-reporting-setup"></a>Mali raporlama ayarı
**Mali raporlama kurulumu** sayfası sistemdeki tüm finansal boyutların listesini içerir. **Genel muhasebe** \> **Genel muhasebe ayarı** \> **Mali raporlama ayarı**.

**Mali raporlama kurulumu** sayfası, Mali raporda bildirdiğiniz verileri belirleyen iki bölüm içerir:

- **Boyutlar sekmesi**: Farklı şirketler farklı boyutlar ve hesap yapıları kullandığından, kullanıcıların raporlarda tüm mali boyutları görüntülemek istediği sırayı belirlemenin bir yolu yoktur. Bu sayfa, Mali raporlamada bir rapor oluşturduğunuzda ve görüntülediğinizde mali boyutların görünmesini istediğiniz sırayı ayarlamanıza olanak tanır.
- **Öznitelikler sekmesi**, **Satıcılar** ve **Müşteriler**'i filtreleme ve rapor tasarımı için öznitelik olarak kullanmayı isteyip istemediğinizi seçebileceğiniz alandır. Satıcı ve Müşteri üzerinde raporlama yapmak ancak hareketleri deftere naklederken birden çok müşteri veya satıcıyı tek bir fişe girmiyor olmanız durumunda değerlidir. Müşteri ve/veya Satıcı seçme tümleştirmeye ek süre ekler.

## <a name="financial-reporting-components"></a>Mali raporlama bileşenleri
Mali raporlamanın aşağıdaki bileşenleri raporların oluşturulmasını, görüntülenmesini ve programlanmasını kolaylaştırır.

| Bileşen        | İşlevler | Ek bilgiler |
|------------------|-----------|------------------------|
| Rapor Tasarımcısı  | Bir rapor tanımlamak ve oluşturmak için birleştirilebilecek rapor yapı taşları oluşturun. Rapor sihirbazı daha az deneyimli kullanıcılara tasarım süreci boyunca rehberlik eder. İleri düzey kullanıcılar, yeni rapor yapı taşları oluşturabilir veya mevcut yapı taşlarını gereksinimlerini karşılayacak şekilde değiştirebilirler. | |
| Rapor programları | Düzenli aralıklarla oluşturulması için tek bir raporu veya bir raporlar grubu planlayın. | [Mali rapor oluşturma](generate-financial-report.md) |

## <a name="features"></a>Özellikler
<table>
<thead>
<tr>
<th>Özellik</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr>
<td>Rapor tasarım esnekliği</td>
<td>Rapor Tasarımcısı, bir rapor tasarlarken size şu raporlama seçeneklerini sağlar:
<ul>
<li>Boyut birleşimlerini kaydedin ve boyutları birden fazla rapor için yeniden kullanın.</li>
<li>Boyut açıklamalarının nasıl biçimlendirilip görüntülendiğini kontrol edin.</li>
<li>Rapor yapı taşlarında atlanan hesapları veya boyutları belirleyin.</li>
<li>Toplanan tahminler için başlıkları biçimlendirin.</li>
</ul>
</td>
</tr>
<tr>
<td>Mali rapor işbirliği</td>
<td>Aşağıdaki özellikler raporların oluşturulmasını ve dağıtılmasını yönetmenize yardımcı olur:
<ul>
<li>Raporları günlük, haftalık, aylık veya yıllık olarak otomatik şekilde oluşturulmaları için planlayın.</li>
<li>Dijital imzalarla daha iyi belge güvenliği sunan salt okunur XPS biçiminde dışa aktarın.</li>
<li>Bir Microsoft Excel çalışma sayfasına aktarın.</li>
<li>Raporları paylaşmak için, raporlara ait bağlantılar içeren e-posta iletileri oluşturabilirsiniz.</li>
</ul>
</td>
</tr>
<tr>
<td>Etkileşimli rapor görüntüleme</td>
<td>Etkileşimli özellikler aşağıdaki görevleri yerine getirmenizi sağlar:
<ul>
<li>Görüntülediğiniz raporun rapor tarihini değiştirin.</li>
<li>Görüntülediğiniz raporun para birimini değiştirin.</li>
<li>Raporu özet veya ayrıntılı görünümde görüntüleyin.</li>
<li>Rapor içeriğini belirli bir boyutla veya boyut birleşimiyle sınırlandırmak için boyut filtreleri ekleyin.</li>
<li>Rapor içeriğini belirli bir öznitelikle veya öznitelik birleşimiyle sınırlandırmak için öznitelik filtreleri ekleyin.</li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a>Ek kaynaklar
[Mali rapor oluşturma](generate-financial-report.md)
