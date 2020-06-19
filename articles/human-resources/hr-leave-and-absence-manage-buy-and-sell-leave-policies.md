---
title: İzin satın alma ve satma ilkelerini yönetme
description: Dynamics 365 Human Resources'ta çalışanların izin satın alma ve satma olanağı sağlayabilirsiniz.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 859445f2b6e980b5960e512e69129f6a8fc6df2b
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429025"
---
# <a name="manage-buy-and-sell-leave-policies"></a>İzin satın alma ve satma ilkelerini yönetme

[!include [banner](includes/preview-feature.md)]

Çalışanların bir izin satınalma ilkesi oluşturarak izin satın alması için bunu etkinleştirebilirsiniz.  

## <a name="enable-employees-to-buy-and-sell-leave"></a>Çalışanların izin satın alma ve satma olanağını etkinleştirin

1. **İzin ve devamsızlık parametreleri** sayfasında, **çalışanların izin satın almasına izin vermek** için **Evet** 'i seçin . 

## <a name="create-a-buy-leave-policy"></a>İzin satınalma İlkesi Oluştur

1. **İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin. 

2. **İzin satın alma ve satma ilkesi** seçin.

3. **Yeni**'yi seçin.

4. İlke için**İzin Satınalma ve satma ilkesi** altındaki bir **ad** ve **açıklama** girin . 

5. Bir **İlke türü** seçin. 

   Kullanılabilir ilke türleri haftalık **tutar** ve **saat sayısı**. Çalışanların satın alabileceği ve satılabilecek maksimum tutarlar için **sabit bir tutar** girmek üzere **tutar** 'ı seçin. **Haftalık saatleri** seçerseniz , çalışanın atadığı çalışma tarihi takviminde tanımlanan çalışma zamanı, ilkenin maksimum tutarını belirlemek için kullanılır. 

6. İlke için **başlangıç tarihi** ve **Bitiş tarihi** seçin. İzin satın alma veya satma istekleri yalnızca bu zaman dilimi boyunca gönderme için kullanılabilir olacak. 

7. **İlke satın alma** altında , çalışanın pozisyonunda tanımlanan fmaya bağlı olarak maksimum tutarı aktarmak için **tam zaman eşdeğerliliği** (FTE) öğesini seçin. İlke türü **tutar** ise **Maksimum sabit bir tutar** girin. 

8. İzin satın almak üzere çalışanlar için izin tiplerini eklemek için **Ekle**'yi seçin. İlkeye birden fazla izin türü ekleyebilirsiniz. 

9. Bir çalışanın satın alabileceği maksimum tutarı belirlemek için, farklı servis ayları etkinleştirmek üzere izin türüne ait **servis ayları** girin. 

10. İzin türü için **maksimum tutarı** girin. 

11. Çalışanın izin verilecek **oranı** girin. 

12. İsteğe bağlı olarak alma için kullanılacak **kazanç kodunu** girin. 

13. İsteğe bağlı olarak, izin türü için maksimum tutarı belirlemek üzere FTE'nin kullanılması gerekip belirlenir. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Bir izin ve devamsızlık planına izin satınalma ve satış ilkesini ekleyin

1. **İzin ve devamsızlık** sayfasında, bir izin ve devamsızlık planı seçin.

2. **Kurallar** altında **İzin satın alma ve satma ilkesi** seçin.

## <a name="see-also"></a>Ayrıca bkz.

[İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)</br>
[İzin ve devamsızlık türlerini yapılandırma](hr-leave-and-absence-types.md)</br>
[İzin ve devamsızlık planları tahakkuk ettirme](hr-leave-and-absence-accrue.md)</br>
[İzin satın alma ve satma](hr-employee-self-service-buy-sell-leave.md)

