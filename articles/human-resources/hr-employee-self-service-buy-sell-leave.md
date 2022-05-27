---
title: İzin satın alma ve satma
description: Bu konuda, Dynamics 365 Human Resources uygulamasında izin satın alma ve satma isteklerinin nasıl gönderileceği açıklanmaktadır.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ESSLeaveBuyRequestEntry, EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 695840516849dcfeb69895f6808d828d5878c59b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688190"
---
# <a name="buy-and-sell-leave"></a>İzin satın alma ve satma


>[!Important]
>Bu konuda belirtilen işlevler şu anda bağımsız Dynamics 365 Human Resources uygulamasını kullanan müşteriler için kullanıma sunulmaktadır. İşlevlerin bazıları veya tümü, Finance 10.0.26 sürümünden sonra Finance altyapısında ileride yayınlanacak bir sürümünün parçası olarak kullanılabilir.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources'ta, şirketiniz tarafından ayarlanan izin satın alma ve satma ilkelerine göre izin satın alma ve satma istekleri gönderebilirsiniz.  

## <a name="request-to-buy-leave"></a>İzin satın alma talebi

1. **Çalışan Self servis** çalışma alanında, **izin satın alma talebi** döşemesinin dışında **izin isteyi** seçin. 

2. **İzin türü** ekleyin ve satın almak istediğiniz bırakma tutarı için bir **tutar** girin. 

3. İsteğinizi göndermeye hazır olduğunuzda **Gönder**'i seçin. 

Bakiyeleriniz otomatik olarak güncelleştirilir veya güncelleştirmeden önce onay işleminden geçer. Bu, satın alma ilkesinin nasıl yapılandırıldığına bağlıdır.

## <a name="request-to-sell-leave"></a>İzin satma isteği

1. **Personel self servisi** çalışma alanında **Kalan İzinler** kutucuğunda **İzin satma isteği**'ni seçin. 

2. **İzin türü** ekleyin ve satmak istediğiniz izin tutarı için bir **Tutar** girin. 

3. İsteğinizi göndermeye hazır olduğunuzda **Gönder**'i seçin.

Bakiyeleriniz otomatik olarak güncelleştirilir veya güncelleştirmeden önce onay işleminden geçer. Bu, satın alma ilkesinin nasıl yapılandırıldığına bağlıdır.


## <a name="troubleshooting"></a>Sorun Giderme 

Bir izin satın alma veya satma talebi iş akışı başarısız olursa, **EssLeaveBuySellRequestApprover** ayrıcalığına sahip kullanıcılar, tüm izin satınalma ve satma taleplerini gözden geçirebilir. Bunu yapmak için **İzin ve devamsızlık > Bağlantılar > İzin satın alma ve satma istekleri > İleti günlüğü**'ne gidin (sol üstte). **İleti günlüğü** kullanıcılara hareketlerin nasıl işlendiğini ve ilişkili iş akışı geçmişini gösterir.


## <a name="see-also"></a>Ayrıca bkz.

[İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)</br>
[İzin satın alma ve satma ilkelerini yönetme](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
