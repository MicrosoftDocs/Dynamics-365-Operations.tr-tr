--- 
title: "Görev ayrımındaki çakışmaları tanımlayın ve çözümleyin"
description: "Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c3a366ea4b558ba4e4af7336992dbb091b0b1414
ms.contentlocale: tr-tr
ms.lasthandoff: 09/29/2017

---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Görev ayrımındaki çakışmaları tanımlayın ve çözümleyin

[!include[task guide banner](../../includes/task-guide-banner.md)]

Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz. Bu kavram, görev ayrımı adını taşır. Güvenlik rolü tanımı veya bir kullanıcının rol atamaları kuralları ihlal ederse, çakışma kaydedilir. Tüm çakışmaların yönetici tarafından düzeltilmesi gerekir. Çakışmaları çözmek ve tanımlamak için aşağıdaki yordamı tamamlayın. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Kullanıcı rolü atamalarının yeni görev ayırma kurallarıyla uyumlu olup olmadığını kontrol edin
1. Sistem Yönetimi > Güvenlik > Görev ayrımı > Kullanıcı rolü atamalarının uygunluğunu doğrulayın seçeneğine gidin.
2. Tamam'a tıklayın.
    * Bir bildirim doğrulamanın sonuçlarını görüntüler.     Bir çakışma varsa, Kullanıcılar sayfasını açabilir ve kullanıcının rol atamalarını değiştirebilirsiniz. Çakışmalar ayrıca Görev ayrımı çakışmaları sayfasında da kaydedilir.     Doğrulama işlemini bir toplu iş olarak çalıştırmak için Toplu iş işleme'yi seçin ve diğer toplu iş parametrelerini ayarlayın. Toplu iş çalıştırıldıktan sonra çakışmaları Görev ayrımı çakışmaları sayfasında gözden geçirebilirsiniz.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Çakışan kullanıcı rolü atamalarını görüntüleyin ve çözümleyin
1. Sistem Yönetimi > Güvenlik > Görev ayrımı > Görev ayrımı çakışmaları seçeneğine gidin.
    * Bir çakışma seçip aşağıdaki düğmelerden birini tıklatın:      atama reddetme – ek güvenlik rolüne kullanıcı atama izin verme. Eğer otomatik rol atamayı reddederseniz, kullanıcı rolden dışarıda olarak işaretlenir. Dışarıda tutulan kullanıcı, rol ile ilişkili olan erişimlere sahip olmaz ve yönetici dışarıda tutulmayı kaldırana kadar role atanamaz.     Atamasına izin ver – Çakışmayı geçersiz kılın ve kullanıcının her iki güvenlik rolüne de atanmasına izin verin. Bir çakışmayı geçersiz kılarsanız, geçersiz kılma nedeni için bir söz konusu alana bir Sebep girmeniz gerekir.  
2. Sayfayı kapatın.
3. Sistem Yönetimi > Güvenlik > Görev ayrımı > Çözülmemiş görev ayrımı çakışmaları seçeneğine gidin.
    * Bir çakışma seçip aşağıdaki düğmelerden birini tıklatın:      atama reddetme – ek güvenlik rolüne kullanıcı atama izin verme. Eğer otomatik rol atamayı reddederseniz, kullanıcı rolden dışarıda olarak işaretlenir. Dışarıda tutulan kullanıcı, rol ile ilişkili olan erişimlere sahip olmaz ve yönetici dışarıda tutulmayı kaldırana kadar role atanamaz.     Atamasına izin ver – Çakışmayı geçersiz kılın ve kullanıcının her iki güvenlik rolüne de atanmasına izin verin. Bir çakışmayı geçersiz kılarsanız, geçersiz kılma nedeni için bir söz konusu alana bir Sebep girmeniz gerekir.    
4. Sayfayı kapatın.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Mevcut kullanıcı rolü atamalarının yeni görev ayırma kurallarıyla uyumlu olup olmadığını kontrol edin
1. Sistem Yönetimi > Güvenlik > Görev ayrımı > Görev ayrımı kuralları seçeneğine gidin.
    * Bir kural seçin.  
2. Görevleri ve rolleri doğrulaya tıklayın.
    * Herhangi bir mevcut rol seçilen kuralı ihlal ediyorsa, rolün adını ve çakışan görevlerin adlarını içeren bir ileti görüntülenir. Yönetici güvenlik riski azaltma yöntemini belirtmeli veya rolü, ayrım kurallarını ihlal etmeyecek şekilde değiştirmelidir.     Eğer hiçbir rol kuralı ihlal etmiyorsa, tüm kuralların uygun olduğunu belirtir.  


