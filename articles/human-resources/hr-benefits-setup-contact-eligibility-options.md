---
title: Kişisel ilgili kişi uygunluk seçeneklerini yapılandır
description: Microsoft Dynamics 365 Human Resources'un kişisel kişileri için uygunluk seçeneklerini yapılandırın. Özel kişiler lehçileri veya bağımlı olabilir.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 071523e2a1e9de6f0ed2b77e4ad6802efb0073f7
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558261"
---
# <a name="configure-personal-contact-eligibility-options"></a>Kişisel iletişim uygunluk seçeneklerini yapılandırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, Microsoft Dynamics 365 Human Resources'daki yan haklarda kullanılabilecek kişisel kişi türlerinin nasıl yapılandırılacağı açıklanmaktadır. Kişisel ilgili kişiler, planlarınız kapsamında yer alacak (bakmakla yükümlü oldukları) veya planlarınızdan yararlanacak kişilerdir (yararlananlar). Bakmakla yükümlü olunan kişiler genellikle eşler veya çocuklardır. Yararlananlar eş, çocuk, sorumlu veya ebeveyn olabilir.

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Kişisel iletişim kişisi uygunluk seçenekleri** seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Uygunluk seçeneği** | Uygunluk seçeneğini tanımlamak için benzersiz uygunluk seçeneği adı veya kodu. |
   | **Açıklama** | Uygunluk seçeneğinin kısa bir açıklaması |
   | **İlgili kişi uygunluk kodu** | Kişisel uygunluk seçeneğini en iyi açıklayan sistem kodu. Aşağıdaki seçeneklerden birini belirleyebilirsiniz: <ul><li>İlişki</li><li>Öğrenci</li><li>Bakmakla yükümlü olunan kişinin yaşı çok büyük</li><li>Çok yaşlı engelli bakmakla yükümlü olunan kişi</li></ul> |
   | **Durum** | Uygunluk seçeneği durumu. Uygunluk seçeneğinin durumu etkin değil olarak ayarlanmışsa kişisel ilgili kişiler için o kişisel ilgili kişi uygunluk seçeneğini seçemezsiniz. |
   | **İlişki** | Kişisel ilgili kişi ve çalışan arasındaki ilişkiyi belirtir. Bu alan yalnızca, ilgili kişi uygunluğu kodu ilişki olarak ayarlandığında etkindir. |
   | **Yaş** | Kazanç planı için uygun bir kişisel ilgili kişinin yaş üst sınırı. Bu alan yalnızca bir ilişki seçerseniz etkindir. Bu yaş, kişisel ilgili kişinin hesaplanan geçerlilik süresi ile karşılaştırılır. Hesaplanan Yaş: (tedarik tarihi – kişisel ilgili kişi Doğum tarihi/365). Bu sayı her zaman bir tamsayıdır. |

4. **Kaydet**'i seçin. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
