---
title: Ömür olaylarını işle
description: Microsoft Dynamics 365 Human Resources'un çalışan yaşam döngüsü sırasında, her çalışan çeşitli ömür etkinliği değişiklikleriyle karşılaşabilir.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef160af483f81b8c1e60a274029b77c3cd34f924
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324803"
---
# <a name="process-life-events"></a>Ömür olaylarını işle

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources'un çalışan yaşam döngüsü sırasında, her çalışan çeşitli ömür etkinliği değişiklikleriyle karşılaşabilir. Örneğin, evlilik, istihdam değişikliği veya bağımlı/lehdarlık değişikliği gibi. Yaşam olaylarını kullanmak için **Kazanç parametreleri** sayfasında yaşam olaylarını etkinleştirmeniz, yaşam olayı türlerini ayarlamanız ve plan türleri için yaşam olayı seçeneklerini ayarlamanız gerekir.

Ömür olaylarını işleyebilmeniz için, işe alma zaman dilimi sırasında açık kaydı en az bir kere çalıştırmanız gerekir. Amerika Birleşik Devletleri, her yıl için kayıt açma işlemi genellikle bir kez yapılır. Amerika Birleşik Devletleri dışında, açık kayıt işe alma sırasında çalıştırılabilir. Bir çalışanın ömür olaylarının işlenmesi için bir avantaj planı seçmesini, ancak açık kayıt işleme içinde yer almış olmaları gerekmez. 

Gelecekteki bir tarihte gerçekleşen ömür olayları olan çalışanlarınız varsa, ömür olayı işlemeyi kullanın. Bu olay, gelecekteki ömür olayları veya bir çalışana özgü olmayan, eklenen ömür olayları (yeni bir örnektir) gibi işlenmediği tüm ömür olaylarını işler. Gerçek zamanlı yaşam olayları gizlenir.

Örneğin, bugün 1 Şubat ise ve 14 Şubat'ta Joe Smith'in bir yasal varlıkları değiştirmek için planlandıysa, 15 Şubat tarihinde ömür olayı işlemeyi çalıştırırsanız, sistem 15 Şubat tarihine kadar tüm olayları işler. 

1. **Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, **Ömür olayı işlemini** seçin.

2. **Ömür olayı işlemini çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Kayıt dönemi** | Ömür olayları işleyecek kayıt dönemi. |
   | **Tüzel kişilik** | Ömür olayları işleyecek yasal varlık. |
   | **Yaşam olayı tarihi** | Sistem, kayıt süresi boyunca bu tarihe kadar olan tüm olayları işler. |
   | **Çalışan** | Ömür olayları işleyecek çalışan. Bu alanı boş bırakırsanız, ömür olayları tüm çalışanlar için işlem görür. |

3. İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:

   1. İşlem bilgilerini girin.

   2. Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.

   3. İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.

   4. **Tamam**'ı seçin. İşlem, ayarladığınız parametrelerle çalışacaktır.

4. **Tamam**'ı seçin.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
