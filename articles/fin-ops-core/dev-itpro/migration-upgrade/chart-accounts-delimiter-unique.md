---
title: Hesap planı ayırıcısını benzersiz yapma
description: Bu konu nasıl hesap planı ve boyut için aynı sınırlayıcıya sahip olamayacağınızı açıklar. Yükseltmeden sonra sınırlayıcı değerlerini değiştirmeniz gerekir.
author: panolte
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 6081a62077f1fc6b6920991ed6faae667c25a47c
ms.sourcegitcommit: e8a2a1e34fa48a42afac9724828f4ec72b6d7085
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/13/2022
ms.locfileid: "8573632"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Hesap planı ayırıcısını benzersiz yapma

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012'de, hesap planı ve boyut değerleri için aynı sınırlayıcı kullanabilirsiniz. Finans ve Operasyon uygulamalarının geçerli sürümlerinde hesap planı ve boyut adları veya değerleri için aynı sınırlayıcıya sahip olamazsınız. Yinelenen bir sınırlayıcı varsa, yükseltme işleminden sonra değiştirebilirsiniz. 

## <a name="update-delimiter"></a>Sınırlayıcıyı güncelleştirme
Hesap planıyla bir çakışma varsa, hesap planı sınırlayıcısı ve proje/alt proje kodu biçimi değiştirilemez. Diğer boyut sınırlayıcılar değiştirilemez. 
- Yükseltme yaptıktan sonra hesap planı sınırlayıcısını **Genel muhasebe parametreleri** > **Hesap planı ve boyutlar** > **Sınırlayıcıyı değiştir** altından değiştirebilirsiniz. 
- Tek çakışma proje/alt proje kodu biçimiyle olduğunda, bu değeri **Proje yönetimi ve muhasebe parametreleri** > **Genel** > **Alt proje biçimini değiştir** altından değiştirebilirsiniz. 

### <a name="other-considerations"></a>Dikkat edilecek diğer noktalar
Proje/alt proje kimliğine benzer şekilde satıcılar veya müşteriler gibi mali boyutlar olarak kullanılan diğer ana veri kayıtları, hesap planı sınırlayıcısıyla aynı karakteri kullanan hesap kimliği değerlerine sahip olmamalıdır. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Güncelleştirilen sınırlayıcıların ortamınız için gerekip gerekmediğini belirleme 
Yükseltilen ortamınızdaki sınırlayıcılarda çakışma varsa, bölümlenmiş giriş denetimi veya boyut giriş denetimine değer girerken tutarsızlıkla karşılaşabilirsiniz. Bunun anlamı, hesap ve boyut birleşimleri girerken, daima aramaları veya bir açılır menüyü kullanmanız gerekeceğidir.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
