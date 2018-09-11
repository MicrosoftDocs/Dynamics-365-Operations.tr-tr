--- 
title: "Madde varışı genel bakış profili ayarlama"
description: "Bu görev bir varış genel bakış profili kurulumu üzerinde odaklanır."
author: ShylaThompson
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 5ddc491d73bbb6ac02e37a9c9b9d93545f6f9556
ms.contentlocale: tr-tr
ms.lasthandoff: 02/07/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a>Madde varışı genel bakış profili ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev bir varış genel bakış profili kurulumu üzerinde odaklanır. Varış genel bakış profili, varış genel bakışı kullanıcı tarafından açıldığında uygulanacak kurallar topluluğudur. Bu prosedürü USMF demo veri şirketinde kullanabilirsiniz. Bu yordam genel olarak bir teslim alma memuru tarafından yerine getirilir.





1. Stok yönetimi > Kurulum > Dağıtım > Varış genel bakış profilleri öğesine gidin.
2. Yeni'ye tıklayın.
    * Neredeyse her zaman aynı ambarda tam kamyon yükleri boşaltmakla uğraşacağınız için, alınan maddelerin kayıt işlemini basitleştirmek için bir varış genel bakış profilini oluşturmalısınız  
3. Varış genel bakış profili alanına bir değer yazın.
4. Satırları göster alanında, bir seçenek seçin.
    * Makbuzlar için hangi satırların gösterileceğini seçin:   Tümü – durumu ne olursa olsun tüm satırları göster.   İşlemde - İlerlemenin Tamamlandı veya Kısmen olduğu girişlerin satırlarını gösterin. Bu, her satır için miktarın tamamının ya da miktarın bir kısmının bir varış günlüğüne kaydedildiği anlamına gelir.   Tamamlanmış değil - İlerlemenin Hiçbiri veya Kısmen olduğu girişlerin satırlarını gösterin. Bu, her satır için bir varış günlüğüne miktarın hiçbir kısmının kaydedilmediği ya da yalnızca bir kısmının kaydedildiği anlamına gelir.  
5. Varış seçenekleri bölümünü genişletin veya daraltın.
6. İleriye doğru gün alanına bir değer yazın.
    * Bu, sonraki birkaç gün içinde (ayarladığınız sayıya bağlı olarak) alınması beklenen alış irsaliyesi satırlarını göstermek için bir filtre ayarlar.  
7. Geriye doğru gün alanına bir değer yazın.
    * Bu, bugünden belir bir sayıdaki gün önce alınmış olması beklenen ürün girişi satırlarını gösteren bir filtre ayarlar.  
8. Ambarlar alanına bir değer yazın.
    * Bir ya da birden fazla fazla ambarı filtreleyin.  
9. Teslimat şekli alanında bir değer seçin.
    * Bu, yalnızca bu teslimat şekli ile alış irsaliyesi satırlarını gösterecek bir filtre ayarlar.  
10. Ad alanında WHS'yi seçin.
11. Ambar alanında ambar 24'ü seçin.
    * Bu, bu profili kullan kayıtlı alış irsaliyesi satırları için kullanılacak varsayılan ambardır.  
12. Konum alanında Baydoor'u seçin.
    * Bu, bu profildeki kayıtlı giriş irsaliyesi satırları için kullanılacak varsayılan konumdur.  
13. Varış sorgusu ayrıntıları bölümünü genişletin veya daraltın.
14. Tesisle kısıtla alanında konum 2'yi seçin.
    * Bu, yalnızca bu tesis ile alış irsaliyesi satırlarını gösterecek bir filtre ayarlar.  
15. Satın alma siparişleri seçeneğini Evet olarak ayarlayın.
    * Satınalma siparişlerinden alış irsaliyesi satırlarını seçin.  
16. Transfer emirleri seçeneğini Evet olarak ayarlayın.
    * Transfer emirlerinden alış irsaliyesi satırlarını seçin.  
17. Kaydet'e tıklayın.
18. Sayfayı kapatın.


