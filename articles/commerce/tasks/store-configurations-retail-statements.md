---
title: " Perakende ekstreleri için mağaza yapılandırmaları"
description: Bu yordam, Commerce ekstrelerinin oluşturulması ve nakledilmesini etkileyen mağazasına ilişkin yapılandırmaları gösterir.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57081b9e737373641cd9d884919d03dcf62a2ffe
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140667"
---
# <a name="store-configurations-for-retail-statements"></a> Perakende ekstreleri için mağaza yapılandırmaları

[!include [banner](../includes/banner.md)]

Bu yordam, Commerce ekstrelerinin oluşturulması ve nakledilmesini etkileyen mağazasına ilişkin yapılandırmaları gösterir. Mağazalardaki mali boyutlar başka bir yordamda anlatılacaktır. Bu yordam, USRT demo şirketini kullanır.

1. **Gezinme paneli**'nde, **Modüller > Perakende ve Ticaret > Kanallar > Mağazaları > Tüm mağazaları**'na gidin.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. **Düzenle**'yi tıklatın.
5. **Ekstre/kapanış** hızlı sekmesindeki ayarlar mağaza için ekstre oluşturma, doğrulama ve deftere nakil işlemlerini etkiler. **Ekstre/Kapanış** hızlı sekmesini genişletin.  
6. **Ekstre yöntemi** alanında, ekstre satırlarını gruplandırmak için kullanmak istediğiniz yöntemi seçin.  
7. Ekstreleri ekstre oluşturma toplu işinden oluştururken her gün için yalnızca bir ekstre oluşturulması gerekiyorsa **Her gün bir ekstre**'ye "Evet"i seçin.  
8. **Kasa sayımı hesaplaması** alanı, ödeme beyanlarının birlikte mi ekleneceğini yoksa son eklenen beyanın mı kullanılacağını belirler.  
9. **Yuvarlama** alanında yuvarlama farklarının nakledileceği genel muhasebe hesabını seçin.  
10. **Maksimum yuvarlama farkı** alanına izin verilen maksimum yuvarlama farkını girebilirsiniz.
11. **Deftere nakil** alanına, bir ekstre için izin verilen maksimum toplam deftere nakil farkını girebilirsiniz.
12. **Vardiya** alanına, ekstrede yer alan bir vardiyadaki maksimum toplam farkı girebilirsiniz.  
13. **Hareket** alanına, ekstre satırındaki maksimum toplam farkı girebilirsiniz.  
14. **Kapanış yöntemi** alanında, bir ekstreye dahil edilen hareketlerin kapatılan bir vardiyanın bir parçası mı olacağını yoksa belirlenen tarih/saat aralığındaki herhangi bir hareketin kullanılmasının mümkün olup olmayacağını belirleyebilirsiniz.  
15. **İş günü sonu** alanına, gece yarısından sonra gerçekleştirilen hareketlerin önceki gün için deftere kaydedilmesi gerekiyorsa bir saat girebilirsiniz.  
16. Gece yarısından sonra gerçekleşen hareketlerin deftere önceki günün bir parçası olarak nakledilmesi gerekiyorsa **İş günü olarak naklet**'i "Evet"i seçin.  
17. Tanımlanan her ekstre yöntemi için oluşturulan ekstreleri almak için **Ekstre yöntemine göre böl**'e "Evet"i seçin. Bu, aynı ayna işlenebilecek çok sayıda küçük ekstre oluşturacağından, deftere nakil performansının yüksek hareket hacmine sahip mağazalar için geliştirilmesi gerektiğinde yararlı olabilir.  
18. **Genel** hızlı sekmesinde **Varsayılan müşteri** alanında, bağımsız müşterilere satış için kullanılacak müşteri hesabını seçebilirsiniz.  

