---
title: "Madde varışı genel bakış profili ayarlama"
description: "Bu görev bir varış genel bakış profili kurulumu üzerinde odaklanır."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: ca70b6afbbadf1122f57285eff58125f8e10346b
ms.contentlocale: tr-tr
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-an-item-arrival-overview-profile"></a>Madde varışı genel bakış profili ayarlama

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

