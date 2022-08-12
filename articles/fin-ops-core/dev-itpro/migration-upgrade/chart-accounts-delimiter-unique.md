---
title: Hesap planı ayırıcısını benzersiz yapma
description: Bu makalede, hesap planı ve boyut için aynı sınırlayıcıya sahip olamamanızın nedeni açıklanmaktadır. Yükseltmeden sonra sınırlayıcı değerlerini değiştirmeniz gerekir.
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
ms.openlocfilehash: 2fd29d747c7141b051e6c7c68db94abfd849f947
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123511"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Hesap planı ayırıcısını benzersiz yapma

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012'de, hesap planı ve boyut değerleri için aynı sınırlayıcı kullanabilirsiniz. Finans ve operasyon uygulamalarının geçerli sürümlerinde hesap planı ve boyut adları veya değerleri için aynı sınırlayıcıya sahip olamazsınız. Yinelenen bir sınırlayıcı varsa, yükseltme işleminden sonra değiştirebilirsiniz. 

## <a name="update-delimiter"></a>Sınırlayıcıyı güncelleştirme
Hesap planıyla bir çakışma varsa, hesap planı sınırlayıcısı ve proje/alt proje kodu biçimi değiştirilemez. Diğer boyut sınırlayıcılar değiştirilemez. 
- Yükseltme yaptıktan sonra hesap planı sınırlayıcısını **Genel muhasebe parametreleri** > **Hesap planı ve boyutlar** > **Sınırlayıcıyı değiştir** altından değiştirebilirsiniz. 
- Tek çakışma proje/alt proje kodu biçimiyle olduğunda, bu değeri **Proje yönetimi ve muhasebe parametreleri** > **Genel** > **Alt proje biçimini değiştir** altından değiştirebilirsiniz. 

### <a name="other-considerations"></a>Dikkat edilecek diğer noktalar
Proje/alt proje kimliğine benzer şekilde satıcılar veya müşteriler gibi mali boyutlar olarak kullanılan diğer ana veri kayıtları, hesap planı sınırlayıcısıyla aynı karakteri kullanan hesap kimliği değerlerine sahip olmamalıdır. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Güncelleştirilen sınırlayıcıların ortamınız için gerekip gerekmediğini belirleme 
Yükseltilen ortamınızdaki sınırlayıcılarda çakışma varsa, bölümlenmiş giriş denetimi veya boyut giriş denetimine değer girerken tutarsızlıkla karşılaşabilirsiniz. Bunun anlamı, hesap ve boyut birleşimleri girerken, daima aramaları veya bir açılır menüyü kullanmanız gerekeceğidir.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

