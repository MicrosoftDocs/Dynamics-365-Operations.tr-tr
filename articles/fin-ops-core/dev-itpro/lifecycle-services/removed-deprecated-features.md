---
title: Lifecycle Services'deki (LCS) kaldırılan veya kullanımına son verilen özellikler
description: Bu konu, Microsoft Dynamics Lifecycle Services'ten (LCS) kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: AngelMarshall
manager: AnnBe
ms.date: 02/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 96ecd040ef8661765c0a3861d8e07fee3c241161
ms.sourcegitcommit: fb7d0efd97754f1ae0b5aa765d0eeb3f57b8078f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027992"
---
# <a name="removed-or-deprecated-features-in-lifecycle-services-lcs"></a>Lifecycle Services'deki (LCS) kaldırılan veya kullanımına son verilen özellikler

[!include[banner](../includes/banner.md)]

Bu konu, Microsoft Dynamics Lifecycle Services (LCS) için kaldırılmış veya artık kullanılmayan özellikleri açıklar.

- *Kaldırılan* özellik artık hizmette bulunmaz.
- *Kullanımına son verilen* özellik etkin geliştirmede değildir ve sonraki güncellemede kaldırılabilir.

Bu liste, kaldırılan veya kullanımına son verilen özellikleri kendi planlamanız için göz önünde bulundurmanız amacıyla hazırlanmıştır.

## <a name="october-2019-announcements"></a>Ekim 2019 duyuruları

### <a name="flowchart-diagrams-in-business-process-modeler"></a>İş süreci modelleyicideki akış tabloları

<table>
<tbody>
<tr>
<td><strong>Kullanımı sonlandırma/kaldırma nedeni</strong></td>
<td>Eski tasarım düşük kullanıma neden olduğundan, İş süreci modelleyici (BPM) içindeki akış çizelgesi diyagramları bileşenini yeniden modelliyoruz.</td>
</tr>
<tr>
<td><strong>Başka bir özellik ile değiştirildi?</strong></td>
<td>Hayır</td>
</tr>
<tr>
<td><strong>Etkilenen alanlar</strong></td>
<td>İş süreci modelleyici</td>
</tr>
<tr>
<td><strong>Durum</strong></td>
<td>Kullanım dışı: BPM içindeki akış grafiği diyagramları bileşeninin 2020 tarihinde ilk olarak kaldırılması beklenir. Aşağıdaki işlevler kaldırılacak:
<ul>
<li>Varolan akış çizelgeleri görüntülemek veya düzenlemek için kullanılamayacak. Akış çizelgesi etkinlikleriyle ilişkilendirilmiş şekil özellikleri de kullanılamayacak, çünkü <strong>akış grafiği</strong> sekmesinin tamamı kaldırılacak. Bu akış çizelgeleri, otomatik olarak oluşturulan varsayılan akış çizelgeleri ve varsayılan akış çizelgeleri temel alınarak değiştirilmiş özel akış çizelgeleri içerir.</li>
<li>Eski sığdırma/boşluk analizi özelliği kullanılamayacak. Bu nedenle, hiçbir Aralık listesi otomatik olarak oluşturulmayacak veya dışa aktarma için kullanılabilir olmayacak.
<p><strong>Not:</strong> Bu özellik daha önce kaldırılmış ve Microsoft Azure DevOps tümleştirmeviyle değiştirildi.</p>
</li>
<li>Akış çizelgesinin sürüm geçmişi kullanılamayacak.</li>
</ul>
</td>
</tr>
</tbody>
</table>
