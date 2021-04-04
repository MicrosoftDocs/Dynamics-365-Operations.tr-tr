---
title: Lifecycle Services'deki (LCS) kaldırılan veya kullanımına son verilen özellikler
description: Bu konu, Microsoft Dynamics Lifecycle Services'ten (LCS) kaldırılmış veya kaldırılması planlanan özellikleri açıklar.
author: AngelMarshall
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b49a6f26b4c2fa895fe0e49f716ce423c3c0057
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559097"
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
<td>Kullanım dışı: BPM içindeki akış grafiği diyagramları bileşeninin 2020 tarihinde ilk olarak kaldırılması beklenir. Aşağıdaki işlevler kullanılamayacak:
<ul>
<li>Tüm akış çizelgeleri salt okunur olacak ve düzenleme için uygun olmayacak. Akış çizelgesi etkinlikleriyle ilişkilendirilmiş şekil özellikleri de kullanılamayacak. Bu akış çizelgeleri, otomatik olarak oluşturulan varsayılan akış çizelgeleri ve varsayılan akış çizelgeleri temel alınarak değiştirilmiş özel akış çizelgeleri içerir.</li>
<li>İşlem adımları salt okunur olacak ve düzenleme için uygun olmayacak.</li>     
<li>Eski sığdırma/boşluk analizi özelliği kullanılamayacak. Bu nedenle, hiçbir Aralık listesi otomatik olarak oluşturulmayacak veya dışa aktarma için kullanılabilir olmayacak.
<p><strong>Not:</strong> Bu özellik daha önce kaldırılmış ve Microsoft Azure DevOps tümleştirmeviyle değiştirildi.</p>
</li>
<li>Akış çizelgesinin sürüm geçmişi kullanılamayacak.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]