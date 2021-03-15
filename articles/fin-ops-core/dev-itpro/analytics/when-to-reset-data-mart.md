---
title: Veri reyonunu sıfırlama zamanı
description: Bu konuda, veri reyonu sıfırlayarak iyileştirilebilecek durumlar ile veri reyonunu sıfırlamanın fayda sağlamayacağı durumlar listelenmektedir.
author: jinniew
manager: AnnBe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1c1524c7a1a3fbe71c51b23571996d87641cdf7e
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093224"
---
# <a name="when-to-reset-a-data-mart"></a>Veri reyonunu sıfırlama zamanı

Veri reyonu sıfırlamak zaman alabilir. Koşullara bağlı olarak, bu eylem gerekli çözüm olmayabilir. Bu konuda, veri reyonu sıfırlayarak iyileştirilebilecek durumların yanı sıra veri reyonunu sıfırlamanın fayda sağlamayacağı durumlar listelenmektedir.  

## <a name="when-do-you-need-to-do-a-data-mart-reset"></a>Veri reyonu sıfırlama işlemini ne zaman yapmanız gerekir?
Veri reyonunu sıfırlamadan önce aşağıdaki soruları göz önünde bulundurun. Bir veya daha fazla sorunun yanıtı evet ise veri reyonu sıfırlamak kuruluşunuz için faydalı olabilir.

- Uygulama veri tabanı geri yüklendi ancak veri reyonu veri tabanı geri yüklenmedi.
- Bir muhasebe dönemi için rapor tasarımıyla ilgili bir sorundan kaynaklanmayan hatalı veriler görüyorsunuz.
- Bir hesap dönemiyle ilgili hatalı veriler görüyorsunuz ve Rapor Tasarımcısındaki **Tümleştirme durumu** sayfasında yer alan Tümleştirme denemeleri bölümünde kayıtlar listeleniyor (Rapor Tasarımcısını başlatın ve  **Araçlar > Tümleştirme durumu**'nu seçin).
- Bir destek olayı açtınız ve destek mühendisi sorun giderme adımının bir parçası olarak veri reyonunu sıfırlamanızı istedi.
 
## <a name="when-its-not-appropriate-to-reset-a-data-mart"></a>Veri reyonu sıfırlamak hangi durumlarda uygun değildir?
Veri reyonunu sıfırlamayı önermediğimiz durumlar bulunur. Bunlara aşağıdakiler dahildir. 

- Nedenin bu konuda listelenmediği durumlar.
- Veri eşitlemeyle ilişkili performans sorunları yaşıyorsunuz. Bu durumda, veri reyonunu sıfırlamak faydalı olmaz.
- Aşağıdakilerden herhangi biri nedeniyle yinelenen bir sıfırlama modeliniz varsa: 
  - **Eksik veriler**: Önce, rapor tasarım sorunlarını ve veri eşitleme zamanlaması sorunlarını (ör. eksik verilerin deftere nakledilmesinden itibaren olgu eşlemesinin çalıştırılmadığını görüyorsanız) ortadan kaldırın.
  - **Takılı kalan tümleştirme durumu**: Tümleştirme yavaşsa veya takılı kalmışsa veri reyonunu sıfırlamak büyük ihtimalle sorunu çözmeyecektir.
  - **Sıfırlama denemelerinin başarısız olması**: Sıfırlama işlemini tamamlamak için birkaç deneme yapılmışsa ve eksik veriler nedeniyle başarısız olunmuşsa, bir destek olayı açmanızı ve veri reyonunu yeniden sıfırlamaya çalışmadan önce durumunuzu analiz etmek için bir destek mühendisinden yardım almanızı öneririz.
  - **Eski kayıtlar**: Yalnızca eski kayıtlar olması tek başına veri reyonunun sıfırlanması için geçerli bir gerekçe değildir. Büyük bir veri kümeniz varsa sıfırlama işleminin çalışması biraz zaman alır ancak bu işlemin iyileştirme sağlama olasılığı düşüktür.
 
## <a name="what-a-data-mart-reset-does-not-do"></a>Veri reyonu sıfırlamasının gerçekleştiremeyeceği işlemler  
- Sıfırlama, yalnızca mevcut görevler tamamlandığında başlar. Bu, eski verilerin eklenmemesini sağlar. Bu aşamada, "Veri reyonu sıfırlama işlemi, etkin bir görev nedeniyle işlenemedi. Lütfen daha sonra yeniden deneyin."
- Sıfırlama, tümleştirme görevlerini devre dışı bırakır ve tüm veri reyonu verilerini siler. Tümleştirme yeniden etkinleştirilir.

> [!NOTE]
> Aşağıdaki noktalar, veri reyonu sıfırlamanın *gerçekleştirmeyeceği* iki işlemi belirtir. <br>
> - Sıfırlama işlemleri rapor tasarımlarını temizlemez. <br>
> - Sıfırlama işlemleri, seçili olmadıkça şirket verilerini veya kullanıcı verilerini temizlemez.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]