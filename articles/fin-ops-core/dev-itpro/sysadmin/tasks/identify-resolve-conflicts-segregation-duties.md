---
title: Görev ayrımındaki çakışmaları tanımlama ve çözümleme
description: Bu konu görev ayrımındaki çakışmalarının nasıl tanımlandığını ve çözümlendiğini açıklar.
author: peakerbl
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7e25a568b86ce3161e2c52045ff2361c0bc4a0e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681606"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Görev ayrımındaki çakışmaları tanımlama ve çözümleme

[!include [banner](../../includes/banner.md)]

Bu konu görev ayrımındaki çakışmalarının nasıl tanımlandığını ve çözümlendiğini açıklar. Farklı kullanıcılar tarafından gerçekleştirilmesi gereken görevleri ayırmak için kurallar ayarlayabilirsiniz. Bu kavram, görev ayrımı adını taşır. Güvenlik rolü tanımı veya bir kullanıcının rol atamaları kuralları ihlal ederse, çakışma kaydedilir. Tüm çakışmaların yönetici tarafından düzeltilmesi gerekir. Çakışmaları çözmek ve tanımlamak için aşağıdaki yordamı tamamlayın. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Kullanıcı rolü atamalarının yeni görev ayırma kurallarıyla uyumlu olup olmadığını kontrol edin
1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Görev ayrımı > Kullanıcı rolü atalamalarının uygunluğunu doğrula**'ya gidin.
2. **Tamam**'ı seçin. Bir bildirim doğrulamanın sonuçlarını görüntüler. Bir çakışma varsa, **Kullanıcılar** sayfasını açabilir ve kullanıcının rol atamalarını değiştirebilirsiniz. Çakışmalar ayrıca **Görev ayrımı çakışmaları** sayfasında da kaydedilir. Doğrulama işlemini bir toplu iş olarak çalıştırmak için **Toplu iş işleme**'yi seçin ve diğer toplu iş parametrelerini ayarlayın. Toplu iş çalıştırıldıktan sonra çakışmaları **Görev ayrımı çakışmaları** sayfasında gözden geçirebilirsiniz.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Çakışan kullanıcı rolü atamalarını görüntüleyin ve çözümleyin
1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Görev ayrımı > Görev ayrımı çakışmaları**'na gidin. Bir çakışma seçip aşağıdaki düğmelerden birini seçin: **Atama reddetme – ek güvenlik rolüne kullanıcı atama izin verme**. Eğer otomatik rol atamayı reddederseniz, kullanıcı rolden dışarıda olarak işaretlenir. Dışarıda tutulan kullanıcı, rol ile ilişkili olan erişimlere sahip olmaz ve yönetici dışarıda tutulmayı kaldırana kadar role atanamaz. Atamasına izin ver – Çakışmayı **geçersiz kılın** ve kullanıcının her iki güvenlik rolüne de atanmasına izin verin. Bir çakışmayı geçersiz kılarsanız, **Geçersiz kılma nedeni** için bir söz konusu alana bir sebep girmeniz gerekir.  
2. Sayfayı kapatın.
3. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Görev ayrımı > Görev ayrımı çözümlenmemiş çakışmaları**'na gidin. Bir çakışma seçip aşağıdaki düğmelerden birini seçin: **Atama reddetme – ek güvenlik rolüne kullanıcı atama izin verme**. Eğer otomatik rol atamayı reddederseniz, kullanıcı rolden dışarıda olarak işaretlenir. Dışarıda tutulan kullanıcı, rol ile ilişkili olan erişimlere sahip olmaz ve yönetici dışarıda tutulmayı kaldırana kadar role atanamaz. Atamasına izin ver – Çakışmayı **geçersiz kılın** ve kullanıcının her iki güvenlik rolüne de atanmasına izin verin. Bir çakışmayı geçersiz kılarsanız, **Geçersiz kılma nedeni alanı**'na bir sebep girmeniz gerekir.    
4. Sayfayı kapatın.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Mevcut kullanıcı rolü atamalarının yeni görev ayırma kurallarıyla uyumlu olup olmadığını kontrol edin
1. **Gezinti bölmesi > Modüller > Sistem yönetimi > Güvenlik > Görev ayrımı > Görev ayırma kuralları**'na gidin. Bir kural seçin.  
2. **Görevleri ve rolleri doğrula**'yı seçin. Herhangi bir mevcut rol seçilen kuralı ihlal ediyorsa, rolün adını ve çakışan görevlerin adlarını içeren bir ileti görüntülenir. Yönetici güvenlik riski azaltma yöntemini belirtmeli veya rolü, ayrım kurallarını ihlal etmeyecek şekilde değiştirmelidir. Eğer hiçbir rol kuralı ihlal etmiyorsa, tüm kuralların uygun olduğunu belirtir.  

