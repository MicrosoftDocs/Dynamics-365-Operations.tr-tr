---
title: Kapalı uçlu soru oluşturma
description: Kapalı uçlu sorular, yanıtlayan kişinin arasından seçim yapabileceği seçenekler sunmanızı sağlar.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09bf57b26111be0e3de358a6c955b3df7bf50668
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467903"
---
# <a name="create-a-closed-ended-question"></a>Kapalı uçlu soru oluşturma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Kapalı uçlu sorular, yanıtlayan kişinin arasından seçim yapabileceği seçenekler sunmanızı sağlar. İlk olarak, yanıt grubunu, yanıtları ile birlikte oluşturun, sonra da yanıt grubunu kullanacak soruyu oluşturun. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-an-answer-group"></a>Yanıt grubu oluşturma
1. Sırasıyla Anket > Tasarım > Yanıt grupları seçimlerini yapın.
2. Yeni'ye tıklayın.
3. Yanıt grubu alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
    * Yanıt grubunun bir soru için her kullanılışında, yanıtların farklı bir düzende yerleştirilmesi için rastgele seç özelliğini kullanın.  
5. Yanıtla'yı tıklatın.
6. Yeni'ye tıklayın.
    * Sıra numarası rastgele seç, yanıt grubu için seçili olmadıkça yanıtların görüntülenme sırasını denetler.  
    * Soru formunu puanlamak için yanıtların puan vermesi sağlanabilir.  
7. Puanlar alanına bir sayı girin.
    * Seçilen yanıtın doğru olduğunu belirtmek üzere işaretlenebilir. Bu, soru formunu puanlamak için kullanılabilir.  
8. Yanıt alanına bir değer yazın.
    * Yanıt grubu için yanıt seçim seçenekleri oluşturmaya devam edin.  
9. Yeni'ye tıklayın.
10. Puanlar alanına bir sayı girin.
11. Yanıt alanına bir değer yazın.
12. Yeni'yi tıklatın.
13. Puanlar alanına bir sayı girin.
14. Yanıt alanına bir değer yazın.
15. Yeni'yi tıklatın.
16. Puanlar alanına bir sayı girin.
17. Yanıt alanına bir değer yazın.
18. Yeni'yi tıklatın.
19. Puanlar alanına bir sayı girin.
20. Yanıt alanına bir değer yazın.
21. Sayfayı kapatın.
22. Sayfayı kapatın.

## <a name="create-the-question"></a>Soruyu oluşturun.
1. Soru formu > Tasarım > Sorular'a gidin.
2. Yeni'ye tıklayın.
3. Tür alanını ilgili soruları birlikte gruplandırmak için kullanın.
    * Kapalı uçlu sorular için onay kutusu, alternatif düğmesi veya birleşik giriş kutusu giriş türlerini kullanabilirsiniz.  
4. Giriş türü alanında bir seçenek seçin.
5. Yanıt grubu alanında bir değer girin veya seçin.
6. Metin alanına bir değer yazın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]