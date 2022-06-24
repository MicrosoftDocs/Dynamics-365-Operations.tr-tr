---
title: Görev ayrımındaki çakışmaları tanımlama ve çözümleme
description: Bu makalede, görev ayrımındaki çakışmalarının nasıl tanımlandığı ve çözümlendiği açıklanmaktadır.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd36db5df2b6871d410bb1feaae825909ec9b3ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883491"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Görev ayrımındaki çakışmaları tanımlama ve çözümleme

[!include [banner](../../includes/banner.md)]

Bu makalede, görev ayrımındaki çakışmalarının nasıl tanımlandığı ve çözümlendiği açıklanmaktadır. Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz. Bu kavram, görev ayrımı adını taşır. Güvenlik rolü tanımı veya bir kullanıcının rol atamaları kuralları ihlal ederse, çakışma kaydedilir. Tüm çakışmaların yönetici tarafından düzeltilmesi gerekir. Çakışmaları çözmek ve tanımlamak için aşağıdaki yordamı tamamlayın.

Kural eklendikten sonra, mevcut tüm rollerin uyumlu olduğunu doğrulayın. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Mevcut rollerin ve görevlerin yeni görev ayırma kurallarıyla uyumlu olduğunu doğrulayın
1. **Sistem yönetimi** > **Güvenlik** > **Görev ayrımı** > **Görev ayrımı kuralları**'na gidin.
3. **Görevleri ve rolleri doğrula**'yı seçin. Herhangi bir rol kuralları ihlal ediyorsa, kuralın ve rolün - adını ve çakışan görevlerin adlarını içeren bir ileti görüntülenir. Çakışan roller **Güvenlik yapılandırması** kullanılarak değiştirilmeli ve çakışan görevleri içermemelidir. Eğer hiçbir rol seçili kuralı ihlal etmiyorsa, tüm kuralların uygun olduğunu belirten bir ileti görüntülenir.   

> [!NOTE]
> Doğrulama yalnızca seçili kural için gerçekleştirilir. Her kural için uyumluluğu doğrulamanız önemlidir.   

Bir rol oluşturduğunuzda veya değiştirdiğinizde, görev ayrımı kuralları otomatik olarak uygulanır. Çakışmaya neden olan görevleri bir role atayamazsınız.

Daha sonra, mevcut tüm rol atamalarının uyumlu olduğunu doğrulayın.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Kullanıcı rolü atamalarının yeni görev ayırma kurallarıyla uyumlu olduğunu doğrulama
1. **Sistem Yönetimi > Güvenlik > Görev ayrımı > Kullanıcı rolü atamalarının uygunluğunu doğrulayın** seçeneğine gidin.
2. **Tamam**'ı seçin. Bir bildirim doğrulamanın sonuçlarını görüntüler. Çakışmalar, **Görev ayırma çözümlenmemiş çakışmaları** sayfasında günlüğe kaydedilir.   

Rollere kullanıcı atadığınızda, görev ayrımı kuralları otomatik olarak uygulanır. Çakışan görevler içeren rollere bir kullanıcı atamayı denerseniz hata iletisi alırsınız. Ek rol atamasını reddederek ya da izin vererek çakışmayı çözmeniz gerekir. Atamaya izin verildiğinde ek rol atanır. 

> [!NOTE]
> Active Directory Etki Alanı gruplarına dayalı olarak rol atanmış kullanıcılar için çakışmalar şu anda doğrulanmaz.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Çakışan kullanıcı rolü atamalarını görüntüleyin ve çözümleyin
1. **Sistem yönetimi** > **Güvenlik** > **Görev ayrımı** > **Görev ayırma çözümlenmemiş çakışmaları** seçeneğine gidin. 
2. Bir çakışma seçin ve daha sonra aşağıdaki eylemlerden birini seçin: 

  - **Atamayı reddet**: Bu eylem, kullanıcının ek güvenlik rolüne atanmasını reddeder. Eğer otomatik rol atamayı reddederseniz, kullanıcı rolden dışarıda olarak işaretlenir. Dışarıda tutulan kullanıcı, rol ile ilişkili olan erişimlere sahip olmaz ve yönetici dışarıda tutulmayı kaldırana kadar role atanamaz. 
-  **Atamaya izin ver**: Bu işlem, çakışmayı geçersiz kılar ve kullanıcının ek güvenlik rolüne atanmasına izin verir. Bir çakışmayı geçersiz kılarsanız, **Geçersiz kılma nedeni** için bir söz konusu alana bir sebep girmeniz gerekir. Geçersiz kılınan tüm rol atamaları, **Görev ayrımı çakışmaları** sayfasında görüntülenebilir.  

> [!NOTE]
> Aynı kullanıcı için birden fazla çakışma listeleniyorsa kullanıcı kaydını seçin ve atanan rolleri **Kullanıcılar** sayfasında değerlendirin. Bu çakışmayı önlemek için, eklendikten veya değiştirildikten sonra her kuralı doğrulayın.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]