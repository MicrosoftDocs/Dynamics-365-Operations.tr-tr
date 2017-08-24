--- 
title: "Faiz işleme"
description: "Bu prosedürde, vade farkı dekontlarının nasıl oluşturulacağı, yazdırılacağı ve deftere nakledileceği gösterilmektedir."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8a53c4deb146d336fdd8ca88a081e6a5af71465a
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="process-interest"></a>Faiz işleme

[!include[task guide banner](../../includes/task-guide-banner.md)]

Bu prosedürde, vade farkı dekontlarının nasıl oluşturulacağı, yazdırılacağı ve deftere nakledileceği gösterilmektedir. Bu görevde USMF demo şirketi kullanılmaktadır.


## <a name="set-up-interest-on-the-posting-profile"></a>Deftere nakil profilinde faiz ayarlayın
1. Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri'ne gidin.
2. Düzenle öğesine tıklayın.
    * Açılır listeden bir faiz kodu seçin. Bu deftere nakil profilini kullanarak hareketler için faiz hesaplanmasını istemiyorsanız alanı boş bırakın.  
    * Tablo kısıtlaması sekmesi, faiz işleme biçimini değiştirmenize olanak sağlar. Bu alan Evet olarak ayarlanırsa, bu deftere nakil profili için faiz hesaplanır.  

## <a name="calculate-interest"></a>Vade farkını hesapla
1. Alacak ve tahsilatlar > Faiz > Vade farkı dekontları oluştur'a gidin.
    * Faizini hesaplayacağınız hareket türlerini seçmeniz gerekir. Bu türlerdeki açık hareketlerin tümü hesaplamaya dahil edilir.  
    * Faiz'i seçerseniz, faizin faizini hesaplarsınız. Bu hareketleri dahil etmeden önce faizin faizini hesaplamayı kontrol eden yasaları incelemek isteyebilirsiniz.  
    * Faiz, bu tarihten "Bitiş tarihi"ne kadar olan dönem üzerinden hesaplanır. Bir "Başlangıç tarihi" belirtmezseniz, deftere nakledilmemiş tüm vade farkı dekontları iptal edilir ve faiz hareket tarihinden yeniden hesaplanır.  
2. Vade farkı dekontunun tarihini girin.
    * Üç deftere nakil profili seçeneği vardır:   Hesap – Her bir vade farkı dekontunun müşteri hesabına atanan deftere nakil profilini kullanın.   Seçim – Deftere nakil profili alanında seçtiğiniz deftere nakil profilini kullanın.   Hareket – Her bir vade farkı dekontu için faizin hesaplandığı hareketlerdeki bağımsız deftere nakil profilini kullanın. Atanmış deftere nakil profili olmayan hareketlerde, Alacak hesapları parametreleri formundaki Genel muhasebe ve satış vergisi alanında belirtilen deftere nakil profili kullanılır.  
    * "Kullanılacak deftere nakil profili" ayarını "Seç" olarak değiştirdiyseniz, burada bir deftere nakil profili seçin.  
3. Eklenecek kayıtlar bölümünü genişletin veya daraltın.
4. Filtre'ye tıklayın.
5. Ölçütler alanına bir Müşteri kodu girin. Örneğin, TR-001 girin.
6. Tamam'a tıklayın.
7. Tamam'a tıklayın.

## <a name="print-interest-notes"></a>Vade farkı dekontlarını yazdır
1. Alacak ve tahsilatlar > Faiz > Vade farkı dekontlarını gözden geçir ve işle'ye gidin.
2. Durum alanında, "Oluşturuldu"yu seçin.
3. Yazdırıldı alanında, "Yazdırılmadı"yı seçin.
4. Yazdır'ı tıklatın.
5. Eklenecek kayıtlar bölümünü genişletin veya daraltın.
6. Tamam'a tıklayın.
7. Sayfayı kapatın.

## <a name="post-the-interest-note"></a>Vade farkı dekontunu deftere nakledin
1. Deftere nakil için hazır bir vade farkı dekontu seçin (durumu Oluşturuldu'dur).
2. Deftere Naklet öğesine tıklayın.
3. Vade farkı dekontu için deftere nakil tarihini girin.
    * Her bir vade farkı dekontu için bir genel muhasebe hareketi oluşturmak üzere Evet'i seçin.     Evet'i seçmezseniz, müşteriye gidecek tüm vade farkı dekontlarındaki faizler toplanır ve tek harekette genel muhasebeye nakledilir.  
4. Eklenecek kayıtlar bölümünü genişletin veya daraltın.
5. Tamam'a tıklayın.
6. Durum alanında, "Deftere nakledildi"yi seçin.


