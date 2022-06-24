---
title: Çalışma zamanı takvimi oluşturma
description: Dynamics 365 Human Resources'ta Çalışma zamanı takvimi, tatiller ve çalışma dışı zamanları tanımlayın .
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 35fcb7c4068ff2f68970d9c0127491e4a63dab4c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861087"
---
# <a name="create-a-working-time-calendar"></a>Çalışma zamanı takvimi oluşturma


> [!Important]
> Bu makalede belirtilen işlevler şu anda tek başına Dynamics 365 Human Resources uygulamasını kullanan müşteriler için kullanıma sunulmaktadır. İşlevlerin bazıları veya tümü, Finance 10.0.26 sürümünden sonra Finance altyapısında ileride yayınlanacak bir sürümünün parçası olarak kullanılabilir.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources'deki bir çalışma zamanı takvimi, çalışanların kuruluşunuzda çalıştığı günleri ve saatleri gösterir. Bir çalışan zaman aşımı isteği gönderdiğinde, tatiller ve kapanışlar hakkında endişelenmenize gerek yoktur.

Zaman aşımı isteklerini kolaylaştırmak için, bu öğeleri kuruluşunuz için konfigüre edin:

- çalışma takvimi
- Tatiller ve kapanışlar
- Çalışmama süresi

Çalışma zamanı takvimi ayarlarken son iki öğeyi ekleyebilirsiniz. Ayrıca, bunları ayrı olarak yapılandırabilir veya güncelleştirebilirsiniz.

## <a name="set-up-a-working-time-calendar"></a>Bir çalışma zamanı takvimi ayarlama

Günlerinizi ve operasyon saatlerinizi gösteren en az bir çalışma zamanı takvimi ayarlayın. Birden fazla ülkede ve bölgede konumlarınız varsa, her alan için bir çalışma zamanı takvimi ayarlamak isteyebilirsiniz.

1. **Kuruluş yönetimi** sayfasında **Takvimler** üzerine tıklayın.

2. **Yeni**'yi seçin ve takviminiz için bir ad ve açıklama girin.

3. **Oluşturma seçenekleri** altında, organizasyonunuzun iş günlerini seçin ve çalışma sürelerini girin. 
   - Tatil veya kapanış eklemek için, **tatiller ve kapanışlar** yanında **Ekle** düğmesini seçin.
   - Yarım ve daha fazla mola gibi çalışma dışı zamanı eklemek için **çalışma dışı süresi** altında **Ekle**'yi seçin ve ad ve zaman aralığını girin.

4. **Günler** altında, takviminizde günleri oluşturmak için **Oluştur** üzerine tıklayın. Takviminizin tarih aralığını girin ve **gün oluştur** seçeneğini belirleyin.

5. Çalışma zamanlamaları eklemek için, **çalışma zamanlaması** altında, **Ekle**'yi seçin ve her iş çizelgesi için saatleri girin.

## <a name="configure-holidays-and-closures"></a>Tatiller ve kapanışları yapılandırın

Tatilleri ve kapanışları, çalışma zamanı takviminden ayrı olarak ekleyebilir veya değiştirebilirsiniz.

1. **Kuruluş yönetimi** sayfasında **Tatiller ve kapanışlar** üzerine tıklayın.

2. **Yeni**'yi seçin ve tatil veya kapanış için bir ad ve tarih girin.

## <a name="configure-non-work-time"></a>Çalışmama süresi yapılandırın

Çalışmama süreleri çalışma zamanı takviminden ayrı olarak ekleyebilir veya değiştirebilirsiniz.

1. **Kuruluş yönetimi** sayfasında **İŞ DIŞI ZAMAN** üzerine tıklayın.

2. **Yeni**'yi seçin ve çalışmama süresi ad ve zaman aralığı girin.

İzin ve devamsızlığı Banka tatili düzeltmeleri önizlemesi özelliğini etkinleştirdiyseniz, İnsan Kaynakları takvimde kayıtlı olan çalışanlara göre ayarlanacak gün sayısını belirlemek için tatiller ve kapatma tarihleri kullanır.

## <a name="see-also"></a>Ayrıca bkz.

- [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)
- [İzin ve devamsızlık türleri yapılandır](hr-leave-and-absence-types.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
