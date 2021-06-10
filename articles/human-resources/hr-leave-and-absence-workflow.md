---
title: Bir izin isteğini iş akışı oluşturma
description: Dynamics 365 Human Resources'ta izin isteklerini sürekli olarak yönetmek Için bir izin ve devamsızlık isteği iş akışı oluşturun.
author: andreabichsel
ms.date: 05/08/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5580b4b07b2d335ad9444a064c726bc4aca1db6a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056552"
---
# <a name="create-a-leave-request-workflow"></a>Bir izin isteğini iş akışı oluşturma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources'ta izin isteklerini sürekli olarak yönetmek Için bir izin ve devamsızlık isteği iş akışı oluşturun. **İzin ve devamsızlık** iş akışı şunları yapmanızı sağlar:

- Görevleri tanımla
- Görevleri kimin tamamlayagerektiğini belirleyin
- İstekleri kimlerin onaylayabilir veya reddedilebileceği belirtin

## <a name="create-a-leave-and-absence-request-workflow"></a>Bir izin ve devamsızlık isteğini iş akışı oluşturma

1. **İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.

2. **Kurulum**'un altında, **İnsan kaynakları iş akışlarını** seçin.

3. **Yeni**'ı seçin ve sonra **İzin ve devamsızlık isteği**'ni seçin. 

4. **Bu dosya açılsın mı?** ileti kutusu görüntülenirse, **aç**'ı seçin ve şirket kimlik bilgilerinizle oturum açın.

5. İzin talepleriniz için iş akışı oluşturmak üzere iş akışı düzenleyicisini kullanın. İş akışlarıyla çalışma hakkında daha fazla bilgi için bkz. [İş akışları genel bakışı oluştur](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)

## <a name="leave-and-absence-request-workflow-data-elements"></a>Bir izin ve devamsızlık isteği iş akışı veri öğeleri

İzin ve devamsızlık istekleri iş akışlarında koşullu veya otomatik onaylar oluşturmak için aşağıdaki veri öğelerini kullanabilirsiniz:

- **Tutar**
- **Açıklama**
- **Şirket**
- **Oluşturan**
- **Oluşturma tarihi ve saati**
- **Bitiş tarihi**
- **İzin türü**
- **Değiştiren**
- **Değiştirilme tarihi ve saati**
- **Neden kodu**
- **İstek kodu**
- **Başlangıç tarihi**
- **Durum** 
- **Gönderme tarihi**
- **Gönderen:**
- **İnsan kaynakları tarafından gönderildi**
- **Yönetici tarafından gönderildi**
- **Adına gönderildi**
- **Çalışan**
- **Çalışan türü**

Bu örnekler, şu veri öğelerini kullanarak nasıl farklı iş akışı koşulları oluşturabileceğinizi göstermektedir:

- Hastalık izni isteklerini onay için İK'ya **Cerrahi** neden koduyla yönlendirmek için **Neden kodu**'nu koşullu ifadede kullanın ve diğer tüm neden kodlarını yöneticiye yönlendirin. Koşullu ifadeler hakkında daha fazla bilgi için, bkz. [İş akışında koşullu kararları yapılandırma](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md). 

- Bu rollerin personel adına gönderdiği izin isteklerini otomatik olarak onaylamak için otomatik eylemdeki **İnsan kaynakları tarafından gönderildi** ve **Yönetici tarafından gönderildi** seçeneğini kullanın. Otomatik eylemler hakkında daha fazla bilgi için bkz. [İş akışında onay süreçlerini yapılandırma](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).

- İş akışının belirli izin türlerine sahip istekleri nasıl yönlendireceğini kontrol etmek için koşullu deyimde veya otomatik eylemde **İzin türü** kullanın.

## <a name="see-also"></a>Ayrıca bkz.

- [İzin ve devamsızlığa genel bakış](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]