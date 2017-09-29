--- 
title: "Temel tahmin oluşturma"
description: "Üretim planlayıcısı, zaman serisi tahmin modellerini kullanarak veya geçmiş talebi kopyalayarak bir taban tahmini oluşturabilir."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c94a9766319531bd8285cca04003225709ce2113
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-baseline-forecast"></a>Temel tahmin oluşturma

[!include[task guide banner](../../includes/task-guide-banner.md)]

Üretim planlayıcısı, zaman serisi tahmin modellerini kullanarak veya geçmiş talebi kopyalayarak bir taban tahmini oluşturabilir. Bu yordam, tüm ürünler için, bir madde tahsisatı anahtarı kullanarak bir temel tahmini oluşturup geçmiş talebi kopyalamayı gösterir. 


## <a name="set-up-an-item-allocation-key"></a>Madde tahsisat anahtarı ayarlama
1. Master planlama > Kurulum > Şirketlerarası planlama grupları'na gidin.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, İsim alanı üzerinde '10' değerini girerek filtreleme yapın.
    * Talep tahmini tüzel kişilikler arasında çalışır. Bu nedenle tahminler oluşturmak istediğiniz tüm şirketleri bir şirketlerarası planlama grubuna dahil etmeniz gerekir.  
3. Listede, istenen kaydı bulun ve seçin.
4. Madde tahsisat anahtarlarına tıkla.
    * Tahminleri oluşturmak istediğiniz tüm madde tahsisat anahtarlarını seçin.  
5. Listede, seçili satırı işaretleyin.
    * D_Aloc madde tahsisat anahtarını seçin.  
6. > öğesini tıklayın.
7. Sayfayı kapatın.
8. Sayfayı kapatın.

## <a name="set-up-the-demand-forecasting-paramters"></a>Talep tahmini için parametreleri ayarlayın
1. Master planlama > Kurulum > Talep tahmini > Talep tahmini parametreleri'ne gidin.
2. Tahmin algoritma parametreleri bölümünü genişletin.
3. Tahmin oluşturma strateji alanında 'Geçmiş talep üzerine kopyala' seçin.
4. Kaydet'e tıklayın.

## <a name="create-a-baseline-forecast"></a>Temel tahmin oluşturma
1. Master planlama > Tahmin > Talep tahmini > İstatistik temel tahmini oluştur seçeneğine gidin.
2. Başlangıç tarihi alanına bir tarih girin.
    * 1 Ocak 2015'den sonra satış emirleriniz varsa, bu tarihi girin. Bunu yapmazsanız, satış siparişlerinizin en erken tarihini girin.  
3. Bitiş tarihi alanına bir tarih girin.
    * Satış emirlerinin son tarihini (örneğin '2015-03-31') girin.  
4. Başlangıç tarihi alanına bir tarih girin.
    * '2015-04-01' girin. Bu tarih bir sonraki tahmin kovasının başlangıç tarihi olarak otomatik hesaplanır.  
5. Eklenecek kayıtlar bölümünü genişletin.
6. Filtre'ye tıklayın.
7. Listede, seçili satırı işaretleyin.
    * Alan = Şirketlerarası planlama grubu olan satırı seçin.  
8. Ölçütler alanına bir değer yazın.
    * Şirketlerarası planlama grubu, örneğin, ilk görevinde kullandığınız, 10'u yazın.  
9. Listede, istenen kaydı bulun ve seçin.
    * Alan = Madde tahsisatı anahtarı olanı seçin.  
10. Ölçütler alanına bir değer yazın.
11. Tamam'a tıklayın.
12. Gelişmiş parametreler bölümünü genişletin.
13. Tahmin aralığı alanında, 'Ay' seçin.
14. Tahmin dönemi alanında, '3' girin.
15. Dondurulmuş zaman dilimi alanında '1' girin.
16. Tamam'a tıklayın.

## <a name="visualize-the-demand-forecast"></a>Talep tahminini görselleştirin
1. Master planlama > Tahmin > Talep tahmini > Düzeltilmiş talep tahmini seçeneğine gidin.
2. Toplanmış görünüm tablosunda, sıra 1 sütun 2 konumundaki hücreyi seçin. Bu tahmin oluşturduğunuz ikinci aydır.
3. QtyCell 'i 400'e ayarlayın.
    * Hücrede, ilk olarak tahminde bulunduğunuzdan farklı bir sayı girin, örneğin 400.  
4. Tahminde el ile bir düzeltme uyguladınız. Sonraki adımdaki grafik göstergeye dikkat edin.
5. Tahmin satırı ayrıntıları'na tıklayın.
    * Bu sayfada, doğruluk değerleri, geçmiş talep, ve tahminleri görebilirsiniz. Bu tahminde değişiklikler de yapabilirsiniz.  

