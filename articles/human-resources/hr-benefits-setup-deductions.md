---
title: Kesintileri yapılandırma
description: Varsa, her bir avantaj için bir çalışanın maaşından düşmelerini belirlemek için Microsoft Dynamics 365 Human Resources'ta kesintiler kullanın.
author: twheeloc
ms.date: 08/24/2021
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
ms.openlocfilehash: 46a37aebf99751d16952d3d7c07c538713377a67
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324888"
---
# <a name="configure-deductions"></a>Kesintileri yapılandırma


Varsa, her bir avantaj için bir çalışanın maaşından düşmelerini belirlemek için Microsoft Dynamics 365 Human Resources'ta kesintiler kullanın. Kesintilerin geçerlilik tarihi olduğundan, kesinti bilgilerinin geçmiş kaydını tutabilirsiniz. 

1. **Sosyal haklar** yönetimi çalışma alanında, **Kur** altında, **Kesintiler**'i seçin.

2. **Yeni**'yi seçin.

3. Aşağıdaki alanların değerleri belirtin:

   | Alan | Tanım |
   | --- | --- |
   | **Kesinti** | Kazanç kesintiyi tanımlamak için kullanılan benzersiz kod. |
   | **Tanım** | Kesintinin bir açıklaması. |
   | **Yürürlüğe giriş** | Başlangıç tarihi. Geçerli değer varsayılan sistem tarihidir. |
   | **Bitiş tarihi** | Bitiş tarihi. Varsayılan değer 12/31/2154'tir ve hiçbir zaman bunu belirtir. |
   | **Başlık** | Bu kesintinin, bordroya ait kazançların çalışan kısmı için kullanacağı Bordro sistemindeki başlık Kodu. Bu, bir üçüncü taraf bordro sağlayıcı kullanırken kullanılır. |
   | **Personel bordro kesintisi referansı** | Kazançlar bordrolara işlenirken bu kesinti tutarında personel bölümü için kullanılan, bordro sistemindeki kesinti kodu. |
   | **Tutar başlığı** | Bu kesinti miktarının, bordroya ait kazançların çalışan kısmı için kullanacağı Bordro sistemindeki başlık Kodu. Bu, bir üçüncü taraf bordro sağlayıcı kullanırken kullanılır. |
   | **Silinebilir** | Dynamics 365 Finance'tan aktarılan bir değerin Bordro sistemindeki değerin silinmesine neden olmasını belirtir. |
   | **Eşleştirilmiş sütunlar** | Bitişik sütunların eşleştirilmiş olduğu başlık ve kesinti tutarının bordro sistemine verip vermeyeceğini belirtir. |
   | **Yürürlük tarihini değiştir** | Kazanç kesinti değişikliğinin yürürlüğe gireceği tarih. Bu tarihte, **Kesinti değişikliği güncelleştirmesi** işlemini çalıştırdığınız sürece kazanç kesintisi değişiklikleri ve bu kesintiyle ilişkili tüm kazanç planları güncelleştirilir. |
   | **Kesinti değişikliği tamamlandı** | Kazanç kesintisi değişiklikleri kesinti ile yapılan güncelleştirme değişikliği işlemesi ile tamamlandıktan sonra **Kesinti değişikliği tamamlandı** onay kutusu otomatik olarak seçilir. |
   
4. Hazırlık oranı kurulumunda yapılan değişiklikleri izlemek ve sürdürmek için **eylemler**'i seçin ve **sürümleri koru**'yu seçin.

5. **Kaydet**'i seçin. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

