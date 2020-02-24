---
title: Ömür olaylarını işle
description: Microsoft Dynamics 365 Human Resources'un çalışan yaşam döngüsü sırasında, her çalışan çeşitli ömür etkinliği değişiklikleriyle karşılaşabilir.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 91812432ead4b0afccfba30f8023f014e216236a
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010874"
---
# <a name="process-life-events"></a>Ömür olaylarını işle

[!include [banner](includes/preview-feature.md)]

Microsoft Dynamics 365 Human Resources'un çalışan yaşam döngüsü sırasında, her çalışan çeşitli ömür etkinliği değişiklikleriyle karşılaşabilir. Örneğin, evlilik, istihdam değişikliği veya bağımlı/lehdarlık değişikliği gibi. Ömür olaylarını kullanmak için, sosyal haklar parametreleri formunda ömür olaylarını etkinleştirmeniz, ömür olay tiplerini ayarlamanız ve plan tipleri için ömür olayı seçeneklerini ayarlamanız gerekir.

Ömür olaylarını işleyebilmeniz için, işe alma zaman dilimi sırasında açık kaydı en az bir kere çalıştırmanız gerekir. Amerika Birleşik Devletleri, her yıl için kayıt açma işlemi genellikle bir kez yapılır. Amerika Birleşik Devletleri dışında, açık kayıt işe alma sırasında çalıştırılabilir. Bir çalışanın ömür olaylarının işlenmesi için bir avantaj planı seçmesini, ancak açık kayıt işleme içinde yer almış olmaları gerekmez. 

Gelecekteki bir tarihte gerçekleşen ömür olayları olan çalışanlarınız varsa, ömür olayı işlemeyi kullanın. Bu olay, gelecekteki ömür olayları veya bir çalışana özgü olmayan, eklenen ömür olayları (yeni bir örnektir) gibi işlenmediği tüm ömür olaylarını işler. Gerçek zamanlı ömür olayları gizli.

Örneğin, bugün 1 Şubat ise ve 14 Şubat'ta Joe Smith'in bir yasal varlıkları değiştirmek için planlandıysa, 15 Şubat tarihinde ömür olayı işlemeyi çalıştırırsanız, sistem 15 Şubat tarihine kadar tüm olayları işler. 

1. **Sosyal haklar** yönetimi çalışma alanında, **işlem** altında, **Ömür olayı işlemini** seçin.

2. **Ömür olayı işlemini çalıştır** iletişim kutusunda, aşağıdaki alanlar için değer belirtin:

   | Alan | Tanım |
   | --- | --- |
   | Kayıt dönemi | Ömür olayları işleyecek kayıt dönemi. |
   | Tüzel kişilik | Ömür olayları işleyecek yasal varlık. |
   | Yaşam olayı tarihi | Sistem, kayıt süresi boyunca bu tarihe kadar olan tüm olayları işler. |
   | Çalışan | Ömür olayları işleyecek çalışan. Bu alanı boş bırakırsanız, ömür olayları tüm çalışanlar için işlem görür. |

3. İşlemi arka planda çalıştırmak istiyorsanız, **arka planda Çalıştır** 'ı seçin ve aşağıdaki görevleri gerçekleştirin:

   1. İşlem bilgilerini girin.

   2. Tekrarlayan iş ayarlamak için **tekrarlama**'yı seçin, yinelenme bilgilerini girin ve **Tamam**'ı seçin.

   3. İş uyarısı ayarlamak için, **uyarılar**'ı seçin, alınacak uyarıları seçin ve **Tamam**'ı seçin.

   4. **Tamam**'ı seçin. İşlem, ayarladığınız parametrelerle çalışacaktır.

4. **Tamam**'ı seçin.
