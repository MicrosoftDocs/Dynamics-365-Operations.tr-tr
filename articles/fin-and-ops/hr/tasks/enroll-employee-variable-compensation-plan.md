---
title: Çalışanı bir değişken tazminat planına kaydetme
description: Tazminat ve Kazançlar yöneticisi, nakit ve nakit olmayan personel ikramiyelerini hesaplamak için personeli değişken ücret planlarına kaydedebilir.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d120f8bb52252956d75178d2ffac6ab632385e00
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "856405"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>Çalışanı bir değişken tazminat planına kaydetme

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tazminat ve Kazançlar yöneticisi, nakit ve nakit olmayan personel ikramiyelerini hesaplamak için personeli değişken ücret planlarına kaydedebilir. Bu prosedürde, bir değişken ücret planının oluşturulduğu ve planda Kaydı etkinleştirin alanı ayarının Evet yapıldığı, söz konusu değişken ücret planı için uygunluk kuralları oluşturulduğu varsayılmaktadır. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu prosedüre başlamak için İnsan Kaynakları > Çalışanlar > Personel > Ücret > Değişken plan kaydı'na gidin

1. Yeni'ye tıklayın.
2. Plan alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Plan arama, yalnızca, Uygunluk kurallarına göre personelin uygun olduğu değişken ücret planlarını gösterecek biçimde filtre edilir.  
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. Genel bölümünün genişletilmiş görünümüne geçin.
5. Yürürlük tarihi alanına bir tarih girin.
6. Kaydet'e tıklayın.
7. Geçersiz Kılmalar bölümünün genişletilmiş görünümüne geçin.
    * İsteğe bağlı olarak, seçili değişken plan için belirtilen işe alma kuralı Yüzde olduğu zaman personelin işe alınma tarihini geçersiz kılmak üzere bir işe alma kuralı tarihi ayarlanabilir.  
    * Değişken plan bir temel yüzdesi planıysa, personel için ikramiye yüzdesi geçersiz kılınabilir. Değişken ücret planı bir birim sayısı planıysa, personel için birim sayısı geçersiz kılınabilir.  
    * Personele ikramiye olarak sabit bir tutar verilecekse, tutar burada ayarlanabilir.  
8. Kuruluş geçersiz kılmaları bölümünün genişletilmiş görünümüne geçin.
    * Personelin performansı, farklı departmanların performansı veya çalışanın pozisyonuna atanmış olandan farklı bir departmanın performansı göz önünde bulundurulacaksa, departman geçersiz kılınabilir. Yüzde sütununun toplamı 100 olmalıdır.  

