---
title: Madde varışı genel bakış profili ayarlama
description: Bu konu bir varış genel bakış profili kurulumu üzerinde odaklanır.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69389dd3a53ffec11116e16512bd038b45eda4d4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439556"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Madde varışı genel bakış profili ayarlama

[!include [banner](../../includes/banner.md)]]

Bu konu bir varış genel bakış profili kurulumu üzerinde odaklanır. Varış genel bakış profili, varış genel bakışı kullanıcı tarafından açıldığında uygulanacak kurallar topluluğudur. Bu prosedürü USMF demo veri şirketinde kullanabilirsiniz. Bu yordam genel olarak bir teslim alma memuru tarafından yerine getirilir.

1. Gezinme bölmesinde **Modüller > Stok yönetimi > Kurulum > Dağıtım > Varış genel bakış profilleri**'ne gidin.
2. **Yeni**'yi seçin. Neredeyse her zaman aynı ambarda tam kamyon yükleri boşaltmakla uğraşacağınız için, alınan maddelerin kayıt işlemini basitleştirmek için bir varış genel bakış profilini oluşturmalısınız  
3. **Varış genel bakış profili** alanına bir değer yazın.
4. **Satırları göster** alanında, bir seçenek seçin. Girişler için gösterilecek satırları seçin:  

    - **Tümü** – Durumuna bakmaksızın tüm satırları gösterin.   
    - **İşlemde** - İlerlemenin Tamamlandı veya Kısmen olduğu girişlerin satırlarını gösterin. Bu, her satır için miktarın tamamının ya da miktarın bir kısmının bir varış günlüğüne kaydedildiği anlamına gelir.   
    - **Tamamlanmış değil** - İlerlemenin Hiçbiri veya Kısmen olduğu girişlerin satırlarını gösterin. Bu, her satır için bir varış günlüğüne miktarın hiçbir kısmının kaydedilmediği ya da yalnızca bir kısmının kaydedildiği anlamına gelir.  

5. **Varış seçenekleri** bölümünü genişletin veya daraltın.
6. **İleriye doğru gün** alanına bir değer yazın. Bu, sonraki birkaç gün içinde (ayarladığınız sayıya bağlı olarak) alınması beklenen alış irsaliyesi satırlarını göstermek için bir filtre ayarlar.  
7. **Geriye doğru gün** alanına bir değer yazın. Bu, bugünden belir bir sayıdaki gün önce alınmış olması beklenen ürün girişi satırlarını gösteren bir filtre ayarlar.  
8. **Ambarlar** alanına bir değer yazın. Bir ya da birden fazla fazla ambarı filtreleyin.  
9. **Teslimat şekli** alanında bir değer seçin. Bu, yalnızca bu teslimat şekli ile alış irsaliyesi satırlarını gösterecek bir filtre ayarlar.  
10. **Ad** alanında WHS'yi seçin.
11. **Ambar** alanında ambar 24'ü seçin. Bu, bu profili kullan kayıtlı alış irsaliyesi satırları için kullanılacak varsayılan ambardır.  
12. **Konum** alanında **Baydoor**'u seçin. Bu, bu profildeki kayıtlı giriş irsaliyesi satırları için kullanılacak varsayılan konumdur.  
13. **Varış sorgusu ayrıntıları** bölümünü genişletin veya daraltın.
14. **Tesisle kısıtla** alanında konum 2'yi seçin. Bu, yalnızca bu tesis ile alış irsaliyesi satırlarını gösterecek bir filtre ayarlar.  
15. **Satın alma siparişleri** seçeneğini **Evet** olarak ayarlayın. Satınalma siparişlerinden alış irsaliyesi satırlarını seçin.  
16. **Transfer** emirleri seçeneğini **Evet** olarak ayarlayın. Transfer emirlerinden alış irsaliyesi satırlarını seçin.  
17. **Kaydet**'i seçin.
18. Sayfayı kapatın.

