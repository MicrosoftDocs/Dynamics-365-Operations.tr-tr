--- 
title: " Perakende ekstreleri için mağaza yapılandırmaları"
description: "Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende mağazasına ilişkin yapılandırmaları gösterir."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 441ba692f559f9966f3e2512c7760ad2f732b768
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="store-configurations-for-retail-statements"></a> Perakende ekstreleri için mağaza yapılandırmaları

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

Bu yordam, Perakende ekstrelerinin oluşturulması ve nakledilmesini etkileyen Perakende mağazasına ilişkin yapılandırmaları gösterir. Perakende mağazalardaki mali boyutlar başka bir yordamda anlatılacaktır. Bu yordam, USRT demo şirketini kullanır.

1. Retail and commerce > Channels > Retail stores > All retail stores (Perakende ve ticaret > Kanallar > Perakende mağazaları > Tüm perakende mağazaları) menüsüne gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
    * Ekstre/kapanış bölümündeki ayarlar mağaza için ekstre oluşturma, doğrulama ve deftere nakil işlemlerini etkiler.  Ekstre/kapanış bölümünü açın.  
    * Ekstre satırlarını gruplandırmak için kullanmak istediğiniz yöntemi seçin.  
    * Ekstreleri ekstre oluşturma toplu işinden oluştururken her gün için yalnızca bir ekstre oluşturulması gerekiyorsa "Evet"i seçin.  
    * Kasa sayımı hesaplaması alanı, ödeme beyanlarının birlikte mi ekleneceğini yoksa son eklenen beyanın mı kullanılacağını belirler.  
    * Yuvarlama farklarının nakledileceği genel muhasebe hesabını seçin.  
    * Maksimum yuvarlama farkı alanına izin verilen maksimum yuvarlama farkını girebilirsiniz.  
    * Deftere nakil alanına, bir ekstre için izin verilen maksimum toplam deftere nakil farkını girebilirsiniz.  
    * Vardiya alanına, ekstrede yer alan bir vardiyadaki maksimum toplam farkı girebilirsiniz.  
    * Hareket alanına, ekstre satırındaki maksimum toplam farkı girebilirsiniz.  
    * Kapanış yöntemi alanında, bir ekstreye dahil edilen hareketlerin kapatılan bir vardiyanın bir parçası mı olacağını yoksa belirlenen tarih/saat aralığındaki herhangi bir hareketin kullanılmasının mümkün olup olmayacağını belirleyebilirsiniz.  
    * İş günü sonu alanına, gece yarısından sonra gerçekleştirilen hareketlerin önceki gün için deftere kaydedilmesi gerekiyorsa bir saat girebilirsiniz.  
    * Gece yarısından sonra gerçekleşen hareketlerin deftere önceki günün bir parçası olarak nakledilmesi gerekiyorsa "Evet"i seçin.  
    * Tanımlanan her ekstre yöntemi için oluşturulan ekstreleri almak için "Evet"i seçin. Bu, aynı ayna işlenebilecek çok sayıda küçük ekstre oluşturacağından, deftere nakil performansının yüksek hareket hacmine sahip mağazalar için geliştirilmesi gerektiğinde yararlı olabilir.  
    * Varsayılan müşteri alanında, bağımsız müşterilere satış için kullanılacak müşteri hesabını seçebilirsiniz.  


