---
title: Perakende mağazasına yönelik ekstreler oluşturma, hesaplama ve deftere nakletme
description: Bu konuda bir mağaza için el ile ekstre oluşturma, hesaplama ve deftere nakletme adımları açıklanmaktadır.
author: jashanno
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a3d82daed16c1b37d10653f04c1dc473cd5c5abc3a6443972da6e8ecf9820f1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719884"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Perakende mağazasına yönelik ekstreler oluşturma, hesaplama ve deftere nakletme

[!include [banner](../includes/banner.md)]

Bu konuda bir mağaza için el ile ekstre oluşturma, hesaplama ve deftere nakletme adımları açıklanmaktadır. Aynı görevler için yapılandırılabilecek toplu işler de vardır. Toplu işleri yapılandırma ve çalıştırmayla ilgili adımlar diğer konularda bulunabilir. Bu yordamı tamamlamak için POS'ta tamamlanan ve ardından Dynamics 365 Commerce uygulamasına çekilen hareketleriniz olmalıdır. Bu kayıt USRT demo veri şirketini kullanır.

1. Giriş sayfasından **Mağaza mali öğeleri**'ni seçin.
2. **Yeni ekstre**'yi seçin.
3. **Mağaza numarası** alanında, açılır menüden bir seçenek belirleyin.
4. **Tamam**'ı seçin.
5. **Kurulum** grubunda, ekstreye hangi hareketlerin dahil edileceğini ve bunların ekstre satırlarında nasıl gruplandırılacağını denetleyen ayarlar bulunur. **Kurulum** grubunu açarak bu ayarları değiştirebilir veya varsayılanları kullanabilirsiniz.  
    - **Ekstre yöntemi** alanı ekstre satırlarının nasıl gruplandırılacağını belirtir.  
    - Personel üyesi seçin veya ekstreyi yalnızca belirli bir personel için hesaplamak veya kaydetmek isterseniz **personel/kayıt** alanından kayıt yapın.  
6. **Kapanış yöntemi** alanında bir seçenek belirleyin.
7. Eylem bölmesinden **Ekstre hesapla**'yı seçin.
8. **Evet**'i seçin.
    - Ekstreyi hesaplandıktan sonra, kullanılan her ödeme ve ekstre yöntemi için toplam tutarları içeren satırlar oluşturulmalıdır.  
    - Girilmesi veya güncelleştirilmesi gerekiyorsa her satıra sayılmış bir tutar girin. Sayılan alanı POS'ta yapılan kasa sayımlarından alınan tutarlarla doldurulur.  
9. Eylem bölmesinden **Ekstreyi deftere naklet**'i seçin.
10. **Kapat**'ı seçin.
11. Bölmeyi kapatın.
12. Giriş sayfasında **Mağaza mali öğeleri**'ni seçin.
13. **Deftere nakledilen ekstreler** sekmesini seçin.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]