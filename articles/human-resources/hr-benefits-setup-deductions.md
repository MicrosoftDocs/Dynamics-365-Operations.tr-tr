---
title: Kesintileri yapılandırma
description: Varsa, her bir avantaj için bir çalışanın maaşından düşmelerini belirlemek için Microsoft Dynamics 365 Human Resources'ta kesintiler kullanın.
author: andreabichsel
ms.date: 04/06/2020
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
ms.openlocfilehash: 4fac1624ce3a88b9fb4adcf303860e82f9d9165b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055568"
---
# <a name="configure-deductions"></a>Kesintileri yapılandırma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Varsa, her bir avantaj için bir çalışanın maaşından düşmelerini belirlemek için Microsoft Dynamics 365 Human Resources'ta kesintiler kullanın. Kesintilerin geçerlilik tarihi olduğundan, kesinti bilgilerinin geçmiş kaydını tutabilirsiniz. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Kesintiler**'i seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Kesinti** | Kazanç kesintiyi tanımlamak için kullanılan benzersiz kod. |
   | **Tanım** | Kesintinin bir açıklaması. |
   | **Yürürlüğe giriş** | Başlangıç tarihi. Geçerli değer varsayılan sistem tarihidir. |
   | **Bitiş tarihi** | Bitiş tarihi. Varsayılan değer 12/31/2154'dir ve hiçbir zaman bunu belirtir. |
   | **Başlık** | Bu kesintinin, bordroya ait kazançların çalışan kısmı için kullanacağı Bordro sistemindeki başlık Kodu. Bu, bir üçüncü taraf bordro sağlayıcı kullanırken kullanılır. |
   | **Personel bordro kesintisi referansı** | Kazançlar bordrolara işlenirken bu kesinti tutarında personel bölümü için kullanılan, bordro sistemindeki kesinti kodu. |
   | **Tutar başlığı** | Bu kesinti miktarının, bordroya ait kazançların çalışan kısmı için kullanacağı Bordro sistemindeki başlık Kodu. Bu, bir üçüncü taraf bordro sağlayıcı kullanırken kullanılır. |
   | **Silinebilir** | Dynamics 365 for Finance and Operations'tan aktarılan bir değerin Bordro sistemindeki değerin silinmesine neden olmasını belirtir. |
   | **Eşleştirilmiş sütunlar** | Bitişik sütunların eşleştirilmiş olduğu başlık ve kesinti tutarının bordro sistemine verip vermeyeceğini belirtir. |
   | **Yürürlük tarihini değiştir** | Kazanç kesinti değişikliğinin yürürlüğe gireceği tarih. Bu tarihte, sistem, kazanç indirimini otomatik olarak değiştirir ve **Kesinti değişikliği güncelleştirmesi** işlemini çalıştırdığınız sürece, bu kesinti ile ilişkili tüm kazanç planlarını güncelleştirir. |
   | **Kesinti değişikliği tamamlandı** | Kazanç kesintisi değişiklikleri kesinti ile yapılan güncelleştirme değişikliği işlemesi ile tamamlandıktan sonra **Kesinti değişikliği tamamlandı** onay kutusu otomatik olarak seçilir. |
   
4. Hazırlık oranı kurulumunda yapılan değişiklikleri izlemek ve sürdürmek için **eylemler**'i seçin ve **sürümleri koru**'yu seçin.

5. **Kaydet**'i seçin. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]