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
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11f86bfa4bfcece164755bb5d86944e0bed0fff2
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692296"
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
