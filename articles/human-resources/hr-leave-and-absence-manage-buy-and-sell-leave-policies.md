---
title: İzin satın alma ve satma ilkelerini yönetme
description: Dynamics 365 Human Resources'ta çalışanların izin satın alma ve satma olanağı sağlayabilirsiniz.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveBuySellPolicy, LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 491d1654bd219b487f95a1eb328e574114ec1f9f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051389"
---
# <a name="manage-buy-and-sell-leave-policies"></a>İzin satın alma ve satma ilkelerini yönetme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

İzin satın alma ve satma ilkesi oluşturarak personelin izin satın almasını ve satmasını etkinleştirebilirsiniz. Onaylar için iş akışını kullanmak, maksimum tutar ve ücret belirlemek ve satın alma ile satma için ücret ayarlamak için bu ilkeleri yapılandırabilirsiniz. 

## <a name="enable-employees-to-buy-and-sell-leave"></a>Çalışanların izin satın alma ve satma olanağını etkinleştirin

1. **İzin ve devamsızlık parametreleri** sayfasında, **Personelin izin satın almasına izin ver** ve **Personelin izin satmasına izin ver** için **Evet**'i seçebilirsiniz.

## <a name="create-a-buy-and-sell-leave-policy"></a>İzin satın alma ve satma ilkesi oluşturma

1. **İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin. 

2. **İzin satın alma ve satma ilkesi** seçin.

3. **Yeni**'yi seçin.

4. İlke için **İzin Satınalma ve satma ilkesi** altındaki bir **ad** ve **açıklama** girin . 

5. Bir **İlke türü** seçin. 

   Kullanılabilir ilke türleri haftalık **tutar** ve **saat sayısı**. Çalışanların satın alabileceği ve satılabilecek maksimum tutarlar için **sabit bir tutar** girmek üzere **tutar** 'ı seçin. **Haftalık saatleri** seçerseniz , çalışanın atadığı çalışma tarihi takviminde tanımlanan çalışma zamanı, ilkenin maksimum tutarını belirlemek için kullanılır. 

6. İlke için **başlangıç tarihi** ve **Bitiş tarihi** seçin. İzin satın alma veya satma istekleri yalnızca bu zaman dilimi boyunca gönderme için kullanılabilir olacak. 

7. İlke için **İş Akışı Kimliği** seçin. Tüm satın alma ve satma istekleri, inceleme ve onay için bu iş akışını kullanır. 

8. **İlke satın alma** altında , çalışanın pozisyonunda tanımlanan fmaya bağlı olarak maksimum tutarı aktarmak için **tam zaman eşdeğerliliği** (FTE) öğesini seçin. İlke türü **tutar** ise **Maksimum sabit bir tutar** girin. 

9. İzin satın almak üzere çalışanlar için izin tiplerini eklemek için **Ekle**'yi seçin. İlkeye birden fazla izin türü ekleyebilirsiniz. 

10. Bir çalışanın satın alabileceği maksimum tutarı belirlemek için, farklı servis ayları etkinleştirmek üzere izin türüne ait **servis ayları** girin. 

11. İzin türü için **maksimum tutarı** girin. 

12. Çalışanın izin verilecek **oranı** girin. 

13. İsteğe bağlı olarak alma için kullanılacak **kazanç kodunu** girin. 

14. İsteğe bağlı olarak, izin türü için maksimum tutarı belirlemek üzere FTE'nin kullanılması gerekip belirlenir. 

15. Bir satış ilkesi oluşturmak için **Satış ilkesi** bölümündeki 8 ile 14. adımlar arasındaki işlemleri uygulayın. 

## <a name="add-the-buy-and-sell-leave-policy-to-a-leave-and-absence-plan"></a>Bir izin ve devamsızlık planına izin satınalma ve satış ilkesini ekleyin

1. **İzin ve devamsızlık** sayfasında, bir izin ve devamsızlık planı seçin.

2. **Kurallar** altında **İzin satın alma ve satma ilkesi** seçin.

## <a name="see-also"></a>Ayrıca bkz.

[İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)</br>
[İzin ve devamsızlık türlerini yapılandırma](hr-leave-and-absence-types.md)</br>
[İzin ve devamsızlık planları tahakkuk ettirme](hr-leave-and-absence-accrue.md)</br>
[İzin satın alma ve satma](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]