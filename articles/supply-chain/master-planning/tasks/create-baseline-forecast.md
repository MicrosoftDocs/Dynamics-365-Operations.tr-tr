---
title: 'Kılavuz: Temel tahmin oluşturma'
description: Üretim planlayıcısı, zaman serisi tahmin modellerini kullanarak veya geçmiş talebi kopyalayarak bir taban tahmini oluşturabilir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a20b30827c9096dd8d8f67d149305cf594ff05
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/10/2021
ms.locfileid: "6223974"
---
# <a name="guide-create-a-baseline-forecast"></a>Kılavuz: Temel tahmin oluşturma

[!include [banner](../../includes/banner.md)]

Üretim planlayıcısı, zaman serisi tahmin modellerini kullanarak veya geçmiş talebi kopyalayarak bir taban tahmini oluşturabilir. Bu yordam, tüm ürünler için, bir madde tahsisatı anahtarı kullanarak bir temel tahmini oluşturup geçmiş talebi kopyalamayı gösterir.

## <a name="set-up-an-item-allocation-key"></a>Madde tahsisat anahtarı ayarlama

1. **Master planlama > Kurulum > Şirketlerarası planlama grupları**'na gidin.
2. Kayıtları bulmak için Hızlı Filtre'yi kullanın. Örneğin, *İsim* alanı üzerinde *10* değerini girerek filtreleme yapın.
    * Talep tahmini tüzel kişilikler arasında çalışır. Bu nedenle tahminler oluşturmak istediğiniz tüm şirketleri bir şirketlerarası planlama grubuna dahil etmeniz gerekir.  
3. Listede, istenen kaydı bulun ve seçin.
4. **Madde tahsisat anahtarları**'nı seçin.
    * Tahminleri oluşturmak istediğiniz tüm madde tahsisat anahtarlarını seçin.  
5. Listede, seçili satırı işaretleyin.
    * D_Aloc madde tahsisat anahtarını seçin.  
6. **>** öğesini seçin.
7. Sayfayı kapatın.
8. Sayfayı kapatın.

## <a name="set-up-the-demand-forecasting-parameters"></a>Talep tahmini parametrelerini ayarlama

1. **Master planlama > Kurulum > Talep tahmini > Talep tahmini parametreleri**'ne gidin.
2. **Tahmin algoritma parametreleri** bölümünü genişletin.
3. **Tahmin oluşturma stratejisi** alanında **Geçmiş talep üzerine kopyala** öğesini seçin.
4. **Kaydet**'i seçin.

## <a name="create-a-baseline-forecast"></a>Temel tahmin oluşturma

1. **Master planlama > Tahmin > Talep tahmini > İstatistik temel tahmini oluştur** seçeneğine gidin.
2. **Başlangıç tarihi** alanına bir tarih girin.
    * 1 Ocak 2015'den sonra satış emirleriniz varsa, bu tarihi girin. Bunu yapmazsanız, satış siparişlerinizin en erken tarihini girin.  
3. **Bitiş tarihi** alanına bir tarih girin.
    * Satış emirlerinin son tarihini (örneğin *2015-03-31*) girin.  
4. **Başlangıç tarihi** alanına bir tarih girin.
    * *2015-04-01* girin. Bu tarih bir sonraki tahmin kovasının başlangıç tarihi olarak otomatik hesaplanır.  
5. **Eklenecek kayıtlar** bölümünü genişletin.
6. **Filtre**'yi seç.
7. Listede, seçili satırı işaretleyin.
    * **Alan**  =  *Şirketlerarası planlama grubu* olan satırı seçin.  
8. **Ölçütler** alanına bir değer yazın.
    * İlk görevde kullandığınız, şirketlerarası planlama grubunu (örneğin *10*) yazın.  
9. Listede, istenen kaydı bulun ve seçin.
    * **Alan** =  *Madde tahsisatı anahtarı* olan satırı seçin.  
10. **Ölçütler** alanına bir değer yazın.
11. **Tamam**'ı seçin.
12. **Gelişmiş parametreler** bölümünü genişletin.
13. **Tahmin aralığı** alanında, *Ay* öğesini seçin.
14. **Tahmin dönemi** alanında, *3* girin.
15. **Dondurulmuş zaman dilimi** alanında *1* girin.
16. **Tamam**'ı seçin.

## <a name="visualize-the-demand-forecast"></a>Talep tahminini görselleştirin

1. **Master planlama > Tahmin > Talep tahmini > Düzeltilmiş talep tahmini** seçeneğine gidin.
2. Toplanmış görünüm tablosunda, sıra 1 sütun 2 konumundaki hücreyi seçin. Bu tahmin oluşturduğunuz ikinci aydır.
3. **QtyCell**'i *400*'e ayarlayın.
    * Hücrede, ilk olarak tahminde bulunduğunuzdan farklı bir sayı girin, örneğin 400.  
4. Tahminde el ile bir düzeltme uyguladınız. Sonraki adımdaki grafik göstergeye dikkat edin.
5. **Tahmin satırı ayrıntıları**'nı seçin.
    * Bu sayfada, doğruluk değerleri, geçmiş talep, ve tahminleri görebilirsiniz. Bu tahminde değişiklikler de yapabilirsiniz.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]