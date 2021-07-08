---
title: İzin satın alma ve satma isteği iş akışı oluşturma
description: Dynamics 365 Human Resources'ta izin satın alma ve satma isteklerini tutarlı bir şekilde yönetmek için izin satın alma ve satma isteği iş akışı oluşturun.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9ec21cda4779fea8c28b73d25842219da900da9d
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271506"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a>İzin satın alma ve satma isteği iş akışı oluşturma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources'ta izin satın alma ve satma isteklerinizi tutarlı bir şekilde yönetmek için bir iş akışı oluşturabilirsiniz. **İzin satın alma ve satma** iş akışı şunları yapmanızı sağlar:

- Görevleri tanımla
- Görevleri kimin tamamlayagerektiğini belirleyin
- İstekleri kimlerin onaylayabilir veya reddedilebileceği belirtin

## <a name="create-a-buy-and-sell-leave-request-workflow"></a>İzin satın alma ve satma isteği iş akışı oluşturma

1. **İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.

2. **Kurulum**'un altında, **İnsan kaynakları iş akışlarını** seçin.

3. **Yeni**'yi, ardından **İzin satın alma ve satma isteği**'ni seçin. 

4. **Bu dosya açılsın mı?** ileti kutusu görüntülenirse, **aç**'ı seçin ve şirket kimlik bilgilerinizle oturum açın.

5. İzin talepleriniz için iş akışı oluşturmak üzere iş akışı düzenleyicisini kullanın. İş akışlarıyla çalışma hakkında daha fazla bilgi için bkz. [İş akışları genel bakışı oluştur](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Bir izin ve devamsızlık isteği iş akışı veri öğeleri

İzin satın alma ve satma istekleri iş akışlarında koşullu veya otomatik onaylar oluşturmak için aşağıdaki veri öğelerini kullanabilirsiniz:

- **Tutar**
- **İzin satın alma ve satma ilkesi**
- **Şirket**
- **Oluşturan**
- **Oluşturulma tarihi ve saati**
- **Bitiş tarihi**
- **İzin türü**
- **Değiştiren**
- **Değiştirilme tarihi ve saati**
- **İstek kodu**
- **Başlangıç tarihi**
- **Durum** 
- **Gönderme tarihi**
- **Gönderen:**
- **İnsan kaynakları tarafından gönderildi**
- **Yönetici tarafından gönderildi**
- **Adına gönderildi**
- **Çalışan**

## <a name="workflow-examples"></a>İş akışı örnekleri

Bu örnekler, şu veri öğelerini kullanarak nasıl farklı iş akışı koşulları oluşturabileceğinizi göstermektedir:

- Bu rollerin personel adına gönderdiği izin satın alma ve satma isteklerini otomatik olarak onaylamak için otomatik eylemdeki **İnsan kaynakları tarafından gönderildi** ve **Yönetici tarafından gönderildi** seçeneğini kullanın. Otomatik eylemler hakkında daha fazla bilgi için bkz. [İş akışında onay süreçlerini yapılandırma](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- İş akışının belirli izin türlerine sahip istekleri nasıl yönlendireceğini kontrol etmek için koşullu deyimde veya otomatik eylemde **İzin türü** kullanın.

## <a name="see-also"></a>Ayrıca bkz.

[İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)<br>
[İzin satın alma ve satma ilkelerini yönetme](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)<br>
[İzin satın alma ve satma](hr-employee-self-service-buy-sell-leave.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
