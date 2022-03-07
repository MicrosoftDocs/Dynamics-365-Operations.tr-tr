---
title: Çalışanı bir değişken tazminat planına kaydetme
description: Tazminat ve Kazançlar yöneticisi, nakit ve nakit olmayan personel ikramiyelerini hesaplamak için personeli değişken ücret planlarına kaydedebilir.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49a64407778fba5669ad13f239363bffd4b0c7d6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/31/2022
ms.locfileid: "8071575"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>Çalışanı bir değişken tazminat planına kaydetme


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tazminat ve Kazançlar yöneticisi, nakit ve nakit olmayan personel ikramiyelerini hesaplamak için personeli değişken ücret planlarına kaydedebilir. Bu yordamda, bir değişken ücret planının oluşturulduğu ve planda **Kaydı etkinleştir** alanının **Evet** olarak ayarlandığı, söz konusu değişken ücret planı için uygunluk kuralları oluşturulduğu varsayılmaktadır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordamı başlatmak için **İnsan kaynakları** > **Çalışanlar** > **Personel** > **Ücret** > **Değişken plan kaydı**'na gidin.

1. **Yeni**'yi tıklatın.
2. **Plan** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Plan arama, yalnızca, Uygunluk kurallarına göre personelin uygun olduğu değişken ücret planlarını gösterecek biçimde filtre edilir.  
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. **Genel** bölümünün genişletilmiş görünümüne geçin.
5. **Yürürlük tarihi** alanına bir tarih girin.
6. **Kaydet**'e tıklayın.
7. **Geçersiz Kılmalar** bölümünün genişletilmiş görünümüne geçin.
    * İsteğe bağlı olarak, seçili değişken plan için belirtilen işe alma kuralı Yüzde olduğu zaman personelin işe alınma tarihini geçersiz kılmak üzere bir işe alma kuralı tarihi ayarlanabilir.  
    * Değişken plan bir temel yüzdesi planıysa, personel için ikramiye yüzdesi geçersiz kılınabilir. Değişken ücret planı bir birim sayısı planıysa, personel için birim sayısı geçersiz kılınabilir.  
    * Personele ikramiye olarak sabit bir tutar verilecekse, tutar burada ayarlanabilir.  
8. **Kuruluş geçersiz kılmaları** bölümünün genişletilmiş görünümüne geçin.
    * Personelin performansı, farklı departmanların performansı veya çalışanın pozisyonuna atanmış olandan farklı bir departmanın performansı göz önünde bulundurulacaksa, departman geçersiz kılınabilir. **Yüzde** sütununun toplamı 100 olmalıdır.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
