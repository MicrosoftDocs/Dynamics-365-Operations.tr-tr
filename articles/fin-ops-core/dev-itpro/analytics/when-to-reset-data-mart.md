---
title: Veri reyonunu sıfırlamayla ilgili SSS
description: Bu konu, veri reyonu sıfırlama hakkında sık sorulan bazı soruların yanıtlarını sağlar.
author: jinniew
ms.date: 06/09/2021
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
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266621"
---
# <a name="data-mart-resets-faq"></a>Veri reyonunu sıfırlamayla ilgili SSS

Bu konu, veri reyonu sıfırlama hakkında sık sorulan bazı soruların yanıtlarını sağlar. Veri reyonu sıfırlama işlemi zaman alan bir işlem olabilir ve koşullara bağlı olarak gerekli çözüm olmayabilir. Bu nedenle, bu konu bir veri reyonu sıfırlamasının yardımcı olabileceği ve büyük olasılıkla size yardımcı olamayacağı koşullar hakkında bilgi içerir.

## <a name="what-is-a-data-mart-reset"></a>Veri reyonu sıfırlama nedir?

Veri reyonu sıfırlama, tümleştirme görevlerini devre dışı bırakacak, tüm veri reyonu verilerini silecek ve tümleştirmeyi yeniden etkinleştirecektir.

Eski verilerin eklenmemesini sağlamak için veri reyonu sıfırlaması yalnızca mevcut görevler tamamlandıktan sonra başlatılabilir. Tüm görevler tamamlanmadan önce veri reyonunu sıfırlamayı denerseniz şöyle bir ileti görebillirsiniz: "Veri reyonu sıfırlama etkin bir görev nedeniyle işlenemedi. Lütfen daha sonra yeniden deneyin."

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a>Veri reyonu sıfırlama işlemini ne zaman yapmam gerekir?

Aşağıdaki ifadelerden biri veya daha fazlası sizin durumunuza için geçerli ise kuruluşunuz bir veri reyonu sıfırlamadan yararlanabilir:

- Uygulama veritabanı geri yüklendi.
- Bir destek bileti açtınız ve Destek mühendisi sorun giderme adımının bir parçası olarak veri reyonunu sıfırlamanızı istedi.
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a>Veri reyonu sıfırlama ne zaman uygun değildir?

Veri reyonunu sıfırlamayı önermediğimiz bazı durumları aşağıda bulabilirsiniz:

- Veri eşitleme ile ilişkili performans sorunları yaşıyorsunuz.
- Aşağıdakilerden herhangi biri nedeniyle yinelenen bir sıfırlama modeliniz var:

    - **Eksik veri**: Verilerin eksik olduğunu görürseniz, rapor biçiminizi ve veri eşitleme sorunlarını gözden geçirmesi için Microsoft ile bir destek bileti açın.
    - **Tümleştirme durumu takılı kaldı**
    - **Eski kayıtlar**: Yalnızca eski kayıtlar olması tek başına veri reyonunun sıfırlanması için geçerli bir gerekçe değildir. Büyük bir veri kümeniz varsa sıfırlama işleminin çalışması biraz zaman alır ancak bu işlemin iyileştirme sağlama olasılığı düşüktür.

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a>Veri reyonunu sıfırladığımda, önceden tasarlamış olduğum raporları kaybedecek miyim?

Hayır. Raporlarınız veri reyonu sıfırlanmadan etkilenmeyen SQL tablolarında depolanır. Tasarladığınız raporların kaybedilmesiyle ilgili endişeleriniz varsa, kaybetmek istemediğiniz tasarımları yedekleyebilirsiniz. Tasarımları yedeklemek için, Rapor Tasarımcısı'nı açın ve **Şirket \> Şirketler \> Yapı Taşları \> Dışa aktar**'a gidin.
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a>Veri reyonu sıfırlayabilmem için tüm kullanıcıların sistemden çıkması gerekiyor mu?

Hayır. Veri reyonu sıfırlama sırasında kullanıcılar sistemde çalışmaya devam edebilir. Ancak, sıfırlama tamamlanana kadar Financial Reporter ile oluşturulan raporlara erişemezler.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
