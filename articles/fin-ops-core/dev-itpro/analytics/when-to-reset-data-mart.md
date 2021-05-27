---
title: Veri reyonunu sıfırlama zamanı
description: Bu konuda, veri reyonu sıfırlayarak iyileştirilebilecek durumlar ile veri reyonunu sıfırlamanın fayda sağlamayacağı durumlar listelenmektedir.
author: jinniew
ms.date: 05/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: bc2c4ee490f3bebd6e7c91609a06f8dfedfcb628
ms.sourcegitcommit: 5916ea2a94ab9af7aac21f0fc44e194d5ce82917
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2021
ms.locfileid: "5989004"
---
# <a name="when-to-reset-a-data-mart"></a>Veri reyonunu sıfırlama zamanı

Veri reyonu sıfırlamak zaman alabilir. Koşullara bağlı olarak, bu eylem gerekli çözüm olmayabilir. Bu konuda, veri reyonu sıfırlayarak iyileştirilebilecek durumların yanı sıra veri reyonunu sıfırlamanın fayda sağlamayacağı durumlar listelenmektedir.  

## <a name="when-do-i-need-to-do-a-data-mart-reset"></a>Veri reyonu sıfırlama işlemini ne zaman yapmam gerekir?
Veri reyonunu sıfırlamadan önce aşağıdaki soruları göz önünde bulundurun. Bir veya daha fazla sorunun yanıtı evet ise veri reyonu sıfırlamak kuruluşunuz için faydalı olabilir.

- Uygulama veritabanı geri yüklendi mi?
- Bir destek olayı açtınız mı ve destek mühendisi sorun giderme adımının bir parçası olarak veri reyonunu sıfırlamanızı istedi mi?
 
## <a name="when-is-it-not-appropriate-to-reset-a-data-mart"></a>Veri reyonu sıfırlamak hangi durumlarda uygun değildir?
Veri reyonunu sıfırlamayı önermediğimiz durumlar bulunur. Bunlara aşağıdakiler dahildir. 

- Veri eşitleme ile ilişkili performans sorunları yaşıyorsunuz. 
- Aşağıdakilerden herhangi biri nedeniyle yinelenen bir sıfırlama modeliniz varsa: 
  - **Eksik veri** 
  - **Tümleştirme durumu takılı kaldı** 
  - **Eski kayıtlar**: Yalnızca eski kayıtlar olması tek başına veri reyonunun sıfırlanması için geçerli bir gerekçe değildir. Büyük bir veri kümeniz varsa sıfırlama işleminin çalışması biraz zaman alır ancak bu işlemin iyileştirme sağlama olasılığı düşüktür.
 
## <a name="what-is-a-data-mart-reset"></a>Veri reyonu sıfırlama nedir?
- Sıfırlama, yalnızca mevcut görevler tamamlandığında başlar. Bu, eski verilerin eklenmemesini sağlar. Bu aşamada, "Veri reyonu sıfırlama işlemi, etkin bir görev nedeniyle işlenemedi. Lütfen daha sonra yeniden deneyin."
- Sıfırlama, tümleştirme görevlerini devre dışı bırakır ve tüm veri reyonu verilerini siler. Tümleştirme yeniden etkinleştirilir.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Veri reyonunu sıfırladığımda, önceden tasarlamış olduğum raporları kaybedecek miyim? 
Hayır, raporlarınız veri reyonu sıfırlanmadan etkilenmeyen SQL tablolarında depolanır. Tasarladığınız raporların kaybedilmesiyle ilgili endişeleriniz varsa, kaybetmek istemediğiniz tasarımları yedekleyebilirsiniz. Bunları yedeklemek için, Rapor Tasarımcısı'nı açın ve **Şirket > Şirketler > Yapı Taşları > Dışa aktar**'a gidin.
 
## <a name="is-it-necessary-for-all-users-to-exit-the-system-to-reset-the-data-mart"></a>Tüm kullanıcıların veri reyonu sıfırlamak için sistemden çıkması gerekiyor mu?
Hayır, veri reyonu sıfırlama sırasında kullanıcılar sistemde çalışmaya devam edebilir. Ancak, sıfırlama tamamlanana kadar Mali Raporlayıcı ile oluşturulan raporlara erişemezler. 

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
