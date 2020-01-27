---
title: Lifecycle Services'deki (LCS) kaldırılan veya kullanımına son verilen özellikler
description: Bu konu, Microsoft Dynamics Lifecycle Services'ten (LCS) kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: sericks007
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c792d06e9b0aa42919de924bdcc9118358779b72
ms.sourcegitcommit: 75bbcff474cfb8d2f282be2b9d2d7984d1505fa3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885467"
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
<td>Kullanım dışı: BPM içindeki akış grafiği diyagramları bileşeninin 2020 Şubat tarihinde ilk olarak kaldırılması beklenir. Aşağıdaki işlevler kaldırılacak:
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
