---
title: Faiz işleme
description: Bu prosedürde, vade farkı dekontlarının nasıl oluşturulacağı, yazdırılacağı ve deftere nakledileceği gösterilmektedir.
author: ShivamPandey-msft
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3b97515e29d04866172216fc29af9a8d992568276c5e01acd67ad9d0028ea0c5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764371"
---
# <a name="process-interest"></a>Faiz işleme

[!include [banner](../../includes/banner.md)]

Bu prosedürde, vade farkı dekontlarının nasıl oluşturulacağı, yazdırılacağı ve deftere nakledileceği gösterilmektedir. Bu görevde USMF demo şirketi kullanılmaktadır.


## <a name="set-up-interest-on-the-posting-profile"></a>Deftere nakil profilinde faiz ayarlayın
1. **Gezinti bölmesinde** **Modüller > Alacak ve tahsilatlar > Kurulum > Müşteri deftere nakil profilleri**'ne gidin.
2. **Düzenle**'yi tıklatın.
3. **Kurulum hızlı sekmesinde**, **Faiz kodu** alanında, açılan listeden bir faiz kodu seçin. Bu deftere nakil profilini kullanarak hareketler için faiz hesaplanmasını istemiyorsanız alanı boş bırakın. **Tablo kısıtlaması** hızlı sekmesi, faiz işleme biçimini değiştirmenize olanak sağlar. Bu alan Evet olarak ayarlanırsa, bu deftere nakil profili için faiz hesaplanır.  

## <a name="calculate-interest"></a>Vade farkını hesapla
1. **Gezinti bölmesinde** **Modüller > Alacak ve tahsilatlar > Faiz > Vade farkı dekontları oluştur**'a gidin.
2. Faizini hesaplayacağınız hareket türlerini seçmeniz gerekir. Bu türlerdeki açık hareketlerin tümü hesaplamaya dahil edilir.  
3. **Faiz**'i 'Evet' olarak ayarlarsanız faizin faizini hesaplarsınız. Bu hareketleri dahil etmeden önce faizin faizini hesaplamayı kontrol eden yasaları incelemek isteyebilirsiniz.  
4. **Başlangıç tarihi** alanına bu faiz hesaplamasının başlayacağı tarihi girin. Bir **Başlangıç tarihi** belirtmezseniz, deftere nakledilmemiş tüm vade farkı dekontları iptal edilir ve faiz hareket tarihinden yeniden hesaplanır.
5. **Bitiş tarihi** alanına bu faiz hesaplamasının biteceği tarihi girin.
6. **Şuradan alınan değerleri kullan** alanında bir seçenek belirtin. Üç deftere nakil profili seçeneği vardır:
    - Hesap – Her vade farkı dekontu için müşteri hesabına atanmış deftere nakil profilini kullan. 
    - Seçim – Deftere nakil profili alanında seçtiğiniz deftere nakil profilini kullanın.
    - Hareket – Her bir vade farkı dekontu için faizin hesaplandığı hareketlerdeki bağımsız deftere nakil profilini kullanın. Atanmış deftere nakil profili olmayan hareketlerde, Alacak hesapları parametreleri formundaki Genel muhasebe ve satış vergisi alanında belirtilen deftere nakil profili kullanılır.  
7. **Eklenecek kayıtlar** hızlı sekmesini genişletin.
8. **Filtrele** öğesine tıklayın.
9. **Ölçütler** alanına bir Müşteri kodu girin. Örneğin, 'TR-001' girin.
6. **Tamam**'a tıklayın.
7. **Tamam**'a tıklayın.

## <a name="print-interest-notes"></a>Vade farkı dekontlarını yazdır
1. **Gezinti bölmesinde** **Modüller > Alacak ve tahsilatlar > Faiz > Vade farkı dekontlarını incele ve işle**'ye gidin.
2. **Durum** alanında, "Oluşturuldu"yu seçin.
3. **Yazdırıldı** alanında, "Yazdırılmadı"yı seçin.
4. **Yazdır**'ı tıklatın.
5. **Eklenecek kayıtlar** hızlı sekmesini genişletin.
6. **Tamam**'a tıklayın.
7. Sayfayı kapatın.

## <a name="post-the-interest-note"></a>Vade farkı dekontunu deftere nakledin
1. Deftere nakil için hazır bir vade farkı dekontu seçin (durumu Oluşturuldu'dur).
2. **Naklet**'e tıklayın.
3. Vade farkı dekontu için deftere nakil tarihini girin. Her bir vade farkı dekontu için bir genel muhasebe hareketi oluşturmak üzere Evet'i seçin. Evet'i seçmezseniz, müşteriye gidecek tüm vade farkı dekontlarındaki faizler toplanır ve tek harekette genel muhasebeye nakledilir.  
4. **Eklenecek kayıtlar** hızlı sekmesini genişletin.
5. **Tamam**'a tıklayın.
6. **Durum** alanında, "Deftere nakledildi"yi seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]