---
title: Kişisel iletişim uygunluk seçeneklerini yapılandırma
description: Bu makalede, Microsoft Dynamics 365 Human Resources'da kişisel ilgili kişiler için uygunluk seçeneklerinin nasıl yapılandırılacağı açıklanmaktadır.
author: twheeloc
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e3e393002901f31c035a54bd8036ed20ecdf9e00
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803897"
---
# <a name="configure-personal-contact-eligibility-options"></a>Kişisel iletişim uygunluk seçeneklerini yapılandırma


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu makalede, Microsoft Dynamics 365 Human Resources'daki kazançlarda kullanılabilecek kişisel ilgili kişi türlerinin nasıl yapılandırılacağı açıklanmaktadır. Kişisel ilgili kişiler, planlarınız kapsamında yer alacak (bakmakla yükümlü oldukları) veya planlarınızdan yararlanacak kişilerdir (yararlananlar). Bakmakla yükümlü olunan kişiler genellikle eşler veya çocuklardır. Yararlananlar eş, çocuk, sorumlu veya ebeveyn olabilir.

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
   | **Yaş** |Kazanç planı için uygun ilgili kişinin yaş üst sınırını belirtir. Bu alan yalnızca bir ilişki seçerseniz etkindir. Bu yaş, kişisel ilgili kişinin hesaplanan geçerlilik süresi ile karşılaştırılır. Hesaplanan Yaş: (tedarik tarihi – kişisel ilgili kişi Doğum tarihi/365). Bu sayı her zaman bir tamsayıdır.
**Bakmakla yükümlü olunan yaşı büyük kişi** ilgili kişi uygunluk seçeneği için bu alandaki yaş minimum yaştır. Örnek: **Bakmakla yükümlü olunan yaşı büyük kişi** seçeneği için yaş 18 olarak ayarlanmışsa, bakmakla yükümlü olunan yaşı büyük kişi olarak işaretlenen ve 18 ya da üzeri yaşta olan kişiler uygunluk seçeneği kapsamına girer.  |

4. **Kaydet**'i seçin. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
