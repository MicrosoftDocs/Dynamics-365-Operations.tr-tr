---
title: Pozisyon bütçeleme için sorun giderme
description: Bu makalede pozisyon bütçelemeyi yapılandırdığınızda karşılaşabileceğiniz sorulara yanıtlar verilmiştir. Bütçe maliyet öğelerinin, ücret gruplarının ve ücret ızgaralarının nasıl oluşturulacağı hakkında sıkça sorulan soruların yanıtlarını içerir.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: kfend
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d09aa8528eeccb214aea02b333ebd6353314984
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722981"
---
# <a name="position-budgeting-troubleshooting"></a>Pozisyon bütçeleme için sorun giderme

[!include [banner](../includes/banner.md)]

Bu makalede pozisyon bütçelemeyi yapılandırdığınızda karşılaşabileceğiniz sorulara yanıtlar verilmiştir. Bütçe maliyet öğelerinin, ücret gruplarının ve ücret ızgaralarının nasıl oluşturulacağı hakkında sıkça sorulan soruların yanıtlarını içerir. 

## <a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>İnsan Kaynaklarında tahmin pozisyonu sayfasını neden bulamıyorum?

Tahmin pozisyonları, Bütçelemeye taşınmıştır.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Bir bütçe maliyet öğesini neden silemiyorum?
Bir tahmin pozisyonuna atanmış bir bütçe maliyet öğesini silemezsiniz. Bir bütçe maliyeti öğesini silmeden önce bunu tüm tahmin pozisyonlarından kaldırmanız gerekir. **İpucu:** Bir bütçe maliyeti öğesinin atandığı tüm pozisyonları bulmak için, maliyet öğesini **Bütçe maliyeti öğeleri** sayfasında seçin ve ardından **Pozisyonları güncelle** düğmesini tıklayın. Maliyet öğesini kullanan pozisyonlar üst ızgarada listelenir.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Bir maliyet öğesini her biri açmadan birden fazla tahmin pozisyonundan nasıl kaldırabilirim?
Bir maliyet öğesini kaldıramazsınız. Ancak, başlangıç ve bitiş tarihlerini bütçe planlama döngüsü tarihlerinin dışında kalacak şekilde değiştirirseniz maliyet öğesinin, bu bütçe planlama döngüsündeki tahmin pozisyonlarıyla bağlantısı kesilir. Bu değişikliği yapmak için, bütçe maliyeti öğesini açın ve ardından **Maliyet hesaplama** FastTab'inde **Tarihleri değiştir** düğmesini tıklayın ve geçerlilik tarihini veya bitiş tarihini değiştirin. Maliyet öğesinin atandığı tüm tahmin pozisyonlarını otomatik olarak güncellemek için **Tamam** düğmesini tıklayın. **İpucu:** Bu yöntemi kullanırsanız, bütçe maliyeti öğesini başlangıç ve bitiş tarihlerinin artık uygun aralıkta olmadığı **tüm** tahmin pozisyonlarından kaldırmanız gerektiğine dikkat edin. Bu etkiyi istemiyorsanız, bütçe maliyeti öğesini kaldırmak istediğiniz her bir tahmin pozisyonunu açmanız ve değişikliği el ile gerçekleştirmeniz gerekir.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Bütçe maliyeti öğesi için Maliyet hesaplaması FastTab'ine neden bir yıllık tutar giremiyorum?
**Hesaplama temeli** FastTab'inde bütçe maliyeti öğeleri varsa, sistemin değeri hesaplaması için bir yüzdeye ihtiyaç duyması nedeniyle bir yıllık tutar giremezsiniz. Değeri değiştirmek için, **Hesaplama temeli** FastTab'inden tüm bütçe maliyeti öğelerini kaldırın.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Bütçe maliyeti türünü neden kazançtan başka bir bütçe maliyeti türü değiştiremiyorum?
Bazı bütçe maliyeti öğeleri, hesaplama temeli olarak kazanç maliyet öğesini kullanır. **Bütçe maliyet türünü** değiştirmek için, kazanç maliyet öğesini tüm bütçe maliyeti öğelerinin **Hesaplama temeli** FastTab'inden kaldırın.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Bir bütçe maliyeti öğesi için bütçe maliyeti öğesi satırlarındaki tarihi neden değiştiremiyorum?
Bir bütçe maliyeti öğesi bir tahmin pozisyonu tarafından kullanılıyorsa o bütçe maliyeti öğesindeki tarihi değiştiremezsiniz. Bu sınırlama, tahmin pozisyonların her zaman bütçe maliyeti öğesinin kuralları dahilinde kalmasının garanti edilmesine yardımcı olur. Tarihi değiştirmek için **Maliyet hesaplaması** FastTab'inde **Tarihleri değiştir** düğmesini tıklayın ve yeni tarihleri girin. Ardından, maliyet öğesinin atandığı pozisyonları güncellemek için **Tamam** düğmesini tıklayın.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Ücret grubu sayfasındaki bir bütçe maliyeti öğesi için maliyetleri neden değiştiremiyorum?
Bütçe maliyet öğelerini sadece **Bütçe maliyet öğeleri** sayfasında oluşturabilir ve değiştirebilirsiniz.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Bir tahmin pozisyonundaki bir maliyet öğesi için tarihleri değiştirdiğimde neden bir hata mesajı alıyorum?
Tahmin pozisyonu maliyet öğesi satırındaki tarihler şu aralıklarda olmalıdır:

-   Pozisyonun etkinleştirme ve bitiş tarihleri.
-   Bütçe maliyet öğesinin etkinleştirme ve bitiş tarihleri.
-   Tahmin pozisyonunun bütçe planlama süreciyle bağlantılı bütçe döngüsünün başlangıç ve bitiş tarihleri.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
