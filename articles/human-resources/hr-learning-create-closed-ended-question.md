---
title: Kapalı uçlu soru oluşturma
description: Kapalı uçlu sorular, yanıtlayan kişinin arasından seçim yapabileceği seçenekler sunmanızı sağlar.
author: twheeloc
ms.date: 08/26/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 18b755675b97e608afccea2e48ea3cfca74c984f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686177"
---
# <a name="create-a-closed-ended-question"></a>Kapalı uçlu soru oluşturma


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Kapalı uçlu sorular, yanıtlayan kişinin arasından seçim yapabileceği seçenekler sunmanızı sağlar. İlk olarak, yanıt grubunu, yanıtları ile birlikte oluşturun, sonra da yanıt grubunu kullanacak soruyu oluşturun. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir.


## <a name="create-an-answer-group"></a>Yanıt grubu oluşturma
1. **Soru Formu** > **Tasarım** > **Yanıt grupları**'na gidin.
2. **Yeni**'ye tıklayın.
3. **Yanıt grubu** alanına bir değer yazın.
4. **Tanım** alanına bir değer girin.
    * Yanıt grubunun bir soru için her kullanılışında, yanıtların farklı bir düzende yerleştirilmesi için **Rastgele seç** işlevini kullanın.  
5. **Yanıt**'a tıklayın.
6. **Yeni**'ye tıklayın.
    * Sıra numarası; **Yanıt grubu** için **Rastgele seç** seçili olmadıkça yanıtların görüntülenme sırasını denetler.  
    * Soru formunu puanlamak için yanıtların puan vermesi sağlanabilir.  
7. **Puanlar** alanına bir sayı girin.
    * Seçilen yanıtın doğru olduğunu belirtmek üzere işaretlenebilir. Bu, soru formunu puanlamak için kullanılabilir.  
8. **Yanıt** alanına bir değer yazın.
    * Yanıt grubu için yanıt seçim seçenekleri oluşturmaya devam edin.  
9. **Yeni**'ye tıklayın.
10. **Puanlar** alanına bir sayı girin.
11. **Yanıt** alanına bir değer yazın.
12. **Yeni**'ye tıklayın.
13. **Puanlar** alanına bir sayı girin.
14. **Yanıt** alanına bir değer yazın.
15. **Yeni**'ye tıklayın.
16. **Puanlar** alanına bir sayı girin.
17. **Yanıt** alanına bir değer yazın.
18. **Yeni**'ye tıklayın.
19. **Puanlar** alanına bir sayı girin.
20. **Yanıt** alanına bir değer yazın.
21. Sayfayı kapatın.
22. Sayfayı kapatın.

## <a name="create-the-question"></a>Soruyu oluşturun.
1. **Soru Formu** > **Tasarım** > **Sorular**'a gidin.
2. **Yeni**'ye tıklayın.
3. **Tür** alanını ilgili soruları birlikte gruplandırmak için kullanın.
    * Kapalı uçlu sorular için **Onay kutusu**, **Alternatif düğmesi** veya **Birleşik giriş kutusu** giriş türlerini kullanabilirsiniz.  
4. **Giriş türü** alanında bir seçenek belirleyin.
5. **Yanıt grubu** alanında bir değer girin veya seçin.
6. **Metin** alanına bir değer yazın.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
