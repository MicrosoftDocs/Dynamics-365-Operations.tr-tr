---
title: Kişisel ilgili kişi uygunluk seçeneklerini yapılandır
description: Microsoft Dynamics 365 Human Resources'un kişisel kişileri için uygunluk seçeneklerini yapılandırın. Özel kişiler lehçileri veya bağımlı olabilir.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 137416477928fd4d6b4438f25df5afea93972027
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2021
ms.locfileid: "5114604"
---
# <a name="configure-personal-contact-eligibility-options"></a>Kişisel ilgili kişi uygunluk seçeneklerini yapılandır

Bu makalede, Microsoft Dynamics 365 Human Resources'un Yararlarında kullanılacak kişisel ilgili kişi türlerinin nasıl yapılandırılacağı gösterilmektedir. Özel kişiler lehçileri veya bağımlı olabilir. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Kurulum** altında, **Kişisel iletişim kişisi uygunluk seçenekleri** seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Uygunluk seçeneği** | Uygunluk seçeneğini tanımlamak için benzersiz uygunluk seçeneği adı veya kodu. |
   | **Açıklama** | Uygunluk seçeneğinin kısa bir açıklaması |
   | **İlgili kişi uygunluk kodu** | Kişisel uygunluk seçeneğini en iyi açıklayan sistem kodu. Aşağıdaki seçeneklerden birini belirleyebilirsiniz: <ul><li>İlişki</li><li>Öğrenci</li><li>Bakmakla yükümlü olunan kişinin yaşı çok büyük</li><li>Çok yaşlı engelli bakmakla yükümlü olunan kişi</li></ul> |
   | **Durum** | Uygunluk seçeneği durumu. Uygunluk seçeneğinin durumu etkin değil olarak ayarlanmışsa, kişisel kişiler için o kişisel ilgili kişi uygunluk seçeneğini seçemezsiniz. |
   | **İlişki** | Kişisel ilgili kişi ve çalışan arasındaki ilişkiyi belirtir. Bu alan yalnızca, ilgili kişi uygunluğu kodu ilişki olarak ayarlandığında etkindir. |
   | **Yaş** | Kazanç planı için uygun bir kişisel ilgili kişinin yaş üst sınırı. Bu alan yalnızca bir ilişki seçerseniz etkindir. Bu yaş, kişisel ilgili kişinin hesaplanan geçerlilik süresi ile karşılaştırılır. Hesaplanan Yaş: (tedarik tarihi – kişisel ilgili kişi Doğum tarihi/365). Bu sayı her zaman bir tamsayıdır. |

4. **Kaydet**'i seçin. 
