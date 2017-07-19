---
title: "Muhasebe veya raporlama para birimlerini dönüştürme"
description: 
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 728af2fff6317c17e47d48ea07dbeb57068fbf3f
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017

---

# <a name="convert-accounting-or-reporting-currencies"></a>Muhasebe veya raporlama para birimlerini dönüştürme

[!include[banner](../includes/banner.md)]




Muhasebe para birimini ya da raporlama para birimini değiştirmesi gereken bir şirketin iki seçeneği vardır. İlk seçenek, yeni bir şirket oluşturmak ve taze bir başlangıç yapmaktır. İkinci seçenek ise, muhasebe ve raporlama para birimi dönüştürme işlemini çalıştırmaktır. Bu, sistemdeki her hareketi değiştiren ve çok uzun süren bir işlemdir. İşlemin çalıştırılması için bazı ayarlar da yapılması gerekir.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>Para birimi dönüştürme işlemi için tüzel kişiliği hazırlama
Tüzel kişiliğin para birimini dönüştürebilmek için müşteri ve satıcı hesaplarına ilişkin tüm yabancı para birimi yeniden değerleme tutarlarını eski haline döndürmeniz ve önceki mali yılları kapatmanız gerekir. Ayrıca, dönüştürme için veritabanını hazırlamanız ve sonra para birimi dönüştürme işleminin gerçekleştirileceği tüzel kişiliğin hesabında gerekli değişiklikleri yapmanız gerekir. Para birimi dönüştürme işlemini tamamladıktan sonra bazı ek yordamları da tamamlamalısınız. Dönüştürülen tutarlardaki farkları yuvarlayarak mutabakat sağlamanız, iş istatistiklerini yeniden hesaplamanız, genel muhasebe hareketlerini günlüğü aktarmanız, erişimi dönüşüm aracıyla sınırlamanız ve müşteri ve satıcı hesaplarının yabancı para birimi tutarlarını yeniden değerlemeniz gerekir.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Otomatik hareketlere ilişkin hesapları ayarlama
Para birimi dönüştürme işlemi sırasında, kazançlar veya zararlar ya da kuruş farkları **Otomatik hareketler için hesaplar** sayfasında tanımlanan hesaplara nakledilir. Dönüştürme işleminin çalıştırılabilmesi için ana hesapların aşağıdaki hareket türlerine atanması gerekir:

-   Muhasebe para birimi dönüştürme karı
-   Muhasebe para birimi dönüştürme zararı
-   Muhasebe para birimi cinsinden kuruş farkı
-   Raporlama para birimi cinsinden kuruş farkı
-   Yıl sonu sonucu

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Yuvarlanan farkları ve toplam yeniden hesaplamaları deftere nakletme
Aşağıdaki bilgiler yuvarlamadaki farkların nerede oluşabileceğini açıklar:

-   Ürün fiyatları 0 (sıfır) olarak dönüştürülmüşse ürün numarasını, modül türünü, dönüştürme öncesi fiyatı ve birimi gösteren bir rapor oluşturulurken.
-   Satış vergisi ve genel muhasebe arasında oluşan yuvarlama farkları genel muhasebe günlüğüne nakledilirken.
-   Yabancı para birimi yeniden değerleme tutarları ve müşteri ile satıcı hareketinin tutarları yeniden hesaplanırken.
-   Her bir müşteri ve satıcının yuvarlama farkları için müşteri ve satıcı kapatma kayıtları oluşturulurken.
-   Müşteriler ve satıcılar için yuvarlama farkları genel muhasebe günlüğüne nakledilirken.
-   Kapatılan maliyet tutarları ve kapatılan stok hareketlerindeki maliyet düzeltme tutarları yeniden hesaplanırken.
-   Stok yönetimindeki yuvarlama farkları genel muhasebe günlüğüne nakledilirken.
-   Eldeki stok yeniden hesaplanırken.
-   Genel muhasebe günlüklerindeki toplam tutarlar yeniden hesaplanırken.
-   Genel muhasebe kapanış tabloları yeniden hesaplanırken.
-   Genel muhasebe bakiyeleri yeniden hesaplanırken.
-   Genel muhasebedeki yuvarlama farkları genel muhasebe günlüğüne nakledilirken.
-   Açılış genel muhasebe hareketleri yeniden hesaplanırken.
-   Genel muhasebe bakiyelerindeki nihai tutar yeniden hesaplanırken.

Yeni bir genel muhasebe hesabı para birimine dönüştürme yapıyorsanız ve toplam tutarların yeniden hesaplanması veya yuvarlama farklarının deftere nakli sırasında bir hata oluşursa **Genel muhasebe hesabı para birimi dönüşümü** sayfasını kapatmanız gerekir. Toplam tutarlar sonra yeniden hesaplanır ve yuvarlama farkları deftere nakledilir.

## <a name="processing-the-currency-conversion"></a>Para birimi dönüştürmeyi işleme alma
Para birimi dönüştürme işlemini başlattığınızda, tüm kullanıcıların sistemden çıkış yapması gerekir. Yeni genel muhasebe defteri veya raporlama para birimi ve döviz kurları tanımlamanız gerekir. **Tamam**'ı tıklattığınızda, işlem çalıştırılır ve sistemdeki her bir hareketi günceller. Para birimi dönüştürme çok uzun bir işlemdir. Tamamlandığında, muhasebe veya raporlama para biriminin **Muhasebe defteri** sayfasında güncellendiğini görürsünüz.

## <a name="completing-the-currency-conversion"></a>Para birimi dönüştürmeyi tamamlama
Para birimi dönüştürmesinin ardından dönüştürülen tüm tutarların doğru olduğundan emin olmak için tüm mutabakat raporlarını tekrar oluşturmalısınız.

-   Genel muhasebe para biriminin dönüşümü sonucunda yuvarlama farkları ortaya çıkarsa, bu farklar yuvarlama farkının oluştuğu fiş kullanılarak deftere nakledilmez. Bunun yerine, dönüştürme nakilleri için girilen fiş kullanılarak nakledilir. Dönüştürme işleminden sonra fişe ve tarihe göre denetleme gerçekleştirilen tüm raporlarda bu yuvarlama farkları eklenir. Bu doğru bir yöntemdir ve yok sayılabilir.
-   Müşteri ve satıcı mutabakat raporları toplam satırında farklı bir tutar görüntülerse ve dönüştürme öncesi tutarla bir farkı yoksa, bu fark tutarının deftere nakledilmesi gerekir. Hesap, müşteri ve satıcılar için özet hesaptır. Mahsup hesap, dönüşüm zararının veya dönüşüm kârının genel muhasebe defteridir.

Tüm genel muhasebe hareketi günlükleri silinmiş olduğundan, genel muhasebe hareketlerini günlüğe aktarabilirsiniz. **Genel muhasebe** &gt; **Dönemsel** &gt; **Günlükler** &gt; **Günlüğe aktarma**'yı tıklatın. Para birimi dönüştürme işleminden sonra yeniden değerleme gerekiyorsa yabancı para birimi tutarlarını yeniden değerleyebilirsiniz. Yeniden değerleme işlem için **Yöntem** alanında **Standart** seçeneğini belirleyerek yabancı para birimi tutarlarını yeniden değerleyebilirsiniz.




