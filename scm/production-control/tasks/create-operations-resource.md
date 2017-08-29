--- 
title: "Operasyon kaynağı oluşturma"
description: "Operasyon kaynağı, bir projenin veya bir üretim işleminin etkinliklerini gerçekleştirir."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 12e4a93f908c348a848e056df00115bf2dc50635
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-an-operations-resource"></a>Operasyon kaynağı oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Operasyon kaynağı, bir projenin veya bir üretim işleminin etkinliklerini gerçekleştirir. Bu prosedürler, size bir operasyon kaynağının nasıl tanımlanacağını gösterir. Bu yordamı, USMF demo veri şirketini veya kendi verilerinizi kullanarak uygulayabilirsiniz.

1. Kaynaklar'a gidin.
2. Yeni'ye tıklayın.
3. Kaynak alanına bir değer yazın.
4. Açıklama alanına bir değer girin.

## <a name="define-capacity-and-consumption-parameters"></a>Kapasite ve tüketim parametrelerini tanımlayın
1. Operasyon bölümünü genişletin.
2. Hurda yüzdesi alanına bir sayı girin.
3. Kurulum kategorisi alanında bir değer girin veya seçin.
    * Kurulum maliyetinin nasıl açıklanacağını tanımlayan maliyet kategorisini belirtin.  
4. Çalışma süresi kategorisi alanına bir değer girin veya buradan bir değer seçin.
    * Çalışma zamanının nasıl açıklanacağını tanımlayan maliyet kategorisini belirtin.  
5. Miktar kategorisi alanında bir değer girin veya seçin.
    * Çıkış miktarına göre kaynak maliyetinin nasıl açıklanacağını tanımlayan maliyet kategorisini belirtin.  
6. Kapasite birimi alanında bir seçenek belirtin.
    * Operasyon kaynağının kapasitesinin ifade edileceği birimi belirtin.  
7. Kapasite alanına bir sayı girin.
8. Verimlilik yüzdesi alanında bir sayı girin.
    * Operasyon kaynağından beklediğiniz verimliliği belirtin. Verimlilik yüzdesi, operasyon kaynağının iş çıkarma yeteneğini ayarlar ve kaynağa ayrılan zamanı etkiler.  
9. Operasyon planlama yüzdesi alanında bir sayı girin.
    * Operasyon planlamasında kullanmak istediğiniz operasyon kaynağı kapasitesinin maksimum yüzdesini belirtin.  
10. Sınırlı kapasite alanında Evet'i seçin.
    * Operasyon kaynağı, mevcut kullanılabilir kapasiteye göre planlanacaksa ve mevcut kapasite rezervasyonları değerlendirilecekse bu seçeneği Evet yapın. Bu seçenek Hayır yapılırsa, operasyon kaynağının sonsuz kapasiteye sahip olduğu varsayılır ve kaynak, kapasitesinin üzerinde rezerve edilebilir.  
11. Darboğazdaki kaynak alanında Evet'i seçin.

## <a name="define-working-times"></a>Çalışma zamanlarını tanımlayın
1. Takvimler bölümünü genişletin.
2. Ekle öğesini tıklatın.
3. Takvim alanına bir değer girin veya buradan bir değer seçin.
    * Kaynak kapasitesini (saat cinsinden) tanımlayan çalışma zamanı takvimini belirtin.  
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="define-resource-capabilities"></a>Kaynak yeteneklerini tanımlama
1. Yetenekler bölümünü genişletin.
2. Ekle öğesini tıklatın.
    * Yetenek, bir operasyon kaynağının belirli bir etkinliği gerçekleştirebilme becerisidir. Zamanlama altyapısı, kaynakları ayırmak için, her bir etkinliğin kaynak gereksinimlerini, kullanılabilecek operasyon kaynaklarının yetenekleriyle eşleştirir.  
3. Yetenekler alanında bir değer girin veya seçin.
4. Düzey alanına bir sayı girin.
    * Kaynağın yeteneğini sergilemede kullanacağı yeterlilik düzeyini belirtin.  
5. Öncelik alanına bir sayı girin.
    * Yeteneğe göre operasyon kaynağı önceliğini belirleyin. Önceliğe göre planlama yaparken, ilk olarak en yüksek önceliği (en düşük sayısal değerle temsil edilir) olan operasyon kaynağı seçilir.  

## <a name="assign-resource-to-resource-group"></a>Kaynak grubuna kaynak atayın
1. Kaynak grupları bölümünü genişletin.
2. Ekle öğesini tıklatın.
    * Kaynak grubu, operasyon kaynaklarının tesis, üretim birimi ve ambar koşullarını tanımlar. Kaynak grubu planlaması ancak bir kaynak grubuna atandığı zaman yapılabilir ve yalnızca kaynak grubunun bulunduğu tesiste olabilir.  
3. Kaynak grubu alanında bir değer girin veya seçin.
4. Giriş konumu alanında bir değer girin veya seçin.
    * Operasyon kaynağının malzemeleri alacağı ambar konumu belirtin.  


