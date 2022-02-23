---
title: Hesap planı ayırıcısını benzersiz yapma
description: Bu konu nasıl hesap planı ve boyut için aynı sınırlayıcıya sahip olamayacağınızı açıklar. Yükseltmeden sonra sınırlayıcı değerlerini değiştirmeniz gerekir.
author: panolte
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 72965e9c6182bdac123feb1bc5cc4b82d91cd588
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020116"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Hesap planı ayırıcısını benzersiz yapma

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012'de, hesap planı ve boyut değerleri için aynı sınırlayıcı kullanabilirsiniz. Finance and Operations'ın geçerli sürümlerinde hesap planı ve boyut değerleri için aynı sınırlayıcıya sahip olamazsınız. Yinelenen bir sınırlayıcı varsa, yükseltme işleminden sonra değiştirebilirsiniz. 

Bu özellik aşağıdaki sürümlerde kullanılabilir:
- Finance and Operations sürüm 8.0
- Finance and Operations sürüm 7.1, KB 4094701 Boyut değerleri hesap planı sınırlayıcısını içerdiğinde mali boyutlar girilemez
- Finance and Operations sürüm 7.2, KB 4092967 Alt proje biçimi boyut sınırlayıcıyı içerdiğinde alt proje boyut olarak seçilemez

## <a name="update-delimiter"></a>Sınırlayıcıyı güncelleştirme
Hesap planıyla bir çakışma varsa, hesap planı sınırlayıcısı ve proje/alt proje kodu biçimi değiştirilemez. Diğer boyut sınırlayıcılar değiştirilemez. 
- Yükseltme yaptıktan sonra hesap planı sınırlayıcısını **Genel muhasebe parametreleri** > **Hesap planı ve boyutlar** > **Sınırlayıcıyı değiştir** altından değiştirebilirsiniz. 
- Tek çakışma proje/alt proje kodu biçimiyle olduğunda, bu değeri **Proje yönetimi ve muhasebe parametreleri** > **Genel** > **Alt proje biçimini değiştir** altından değiştirebilirsiniz. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Güncelleştirilen sınırlayıcıların ortamınız için gerekip gerekmediğini belirleme 
Yükseltilen ortamınızdaki sınırlayıcılarda çakışma varsa, bölümlenmiş giriş denetimi veya boyut giriş denetimine değer girerken tutarsızlıkla karşılaşabilirsiniz. Bunun anlamı, hesap ve boyut birleşimleri girerken, daima aramaları veya bir açılır menüyü kullanmanız gerekeceğidir.
