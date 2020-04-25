---
title: Özet
description: Dynamics 365 Human Resources'ta İzin ve devamsızlık çalışma alanı, yeni izin planları oluşturmak için esnek bir çerçeve, isteklerin yönetilmesi için iş akışları ve çalışanların zaman istebilmesi için sezgisel bir self servis sayfası sağlar.
author: andreabichsel
manager: AnnBe
ms.date: 04/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5f7ba32b31a67d81ee5be568b0e64842f343f96b
ms.sourcegitcommit: 9940ca772807d3c4e1ff3bf47f45b7251c4469ac
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/04/2020
ms.locfileid: "3226242"
---
# <a name="overview"></a>Özet

Dynamics 365 Human Resources, çalışanlarınız için harika yararlar sağlamanıza yardımcı olur. **İzin ve devamsızlık** çalışma alanı, yeni izin planları oluşturmak için esnek bir çerçeve, isteklerin yönetilmesi için iş akışları ve çalışanların zaman istebilmesi için sezgisel bir self servis sayfası sağlar. Analiz kuruluşunuzun izin planlarınızın bakiyelerini ve kullanımını ölçmesine ve izlemesine yardımcı olur.

## <a name="set-up-leave-and-absence"></a>İzin ve devamsızlık ayarla

Çalışanlarınız için izin planları oluşturabilmeniz için, önce birkaç Kurulum adımı yapmanız gerekir:

- [Bırakma ve devamsızlık parametrelerini konfigüre et](hr-leave-and-absence-parameters.md)
- [Çalışma süresi takvimleri oluşturma](hr-leave-and-absence-working-time-calendar.md)
- [Bir izin isteğini iş akışı oluşturma](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>İzin planları oluşturmak ve yönetmek

Çalışanlarınız için izin planları oluşturmadan önce, bırakma ve devamsızlık tipleri oluşturmanız gerekir. Bir izin planı oluşturduktan sonra, çalışanların plana kaydolmalarını sağlayabilirsiniz. Ayrıca, tahakkuk sürecini çalıştırabilir, uyarılar oluşturabilir ve planlarınız için Analizi görüntüleyebilirsiniz.

- [İzin ve devamsızlık türleri yapılandır](hr-leave-and-absence-types.md)
- [İzin ve devamsızlık planı oluştur](hr-leave-and-absence-plans.md)
- [Çalışanları bir izin planına atama](hr-leave-and-absence-enroll.md)
- [İzin ve devamsızlık planları tahakkuk etme](hr-leave-and-absence-accrue.md)
- [Bırakma ve devamsızlık için Analizi görüntüle](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>İsteği kapatma ve istekleri yönetme

Çalışanlarınız talep dışı bırakma saatleri gönderebilir ve bunları, **çalışan self servis** çalışma alanında yönetebilirsiniz.

- [İzin iste](hr-employee-self-service-request-time-off.md)
- [İzin ve devamsızlık isteklerini yönetme](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Bilinen izin ve devamsızlık sorunları

### <a name="rounding-precision"></a>Yuvarlama hassasiyeti

**Yuvarlama türünü** ayarlarken **Yuvarlama hassasiyeti**'ni ayarlayamazsınız. **Yuvarlama hassasiyeti**'ni yalnızca **İzin ve devamsızlık türü** varlığını kullanarak ayarlayabilirsiniz. 

1. **İzin ve devamsızlık türleri**'nden **İzin ve devamsızlık türü** varlığını açmak için **Excel'de Aç**'ı seçin.

2. Dosya açılıp etkinleştirildikten sonra **Tasarla**'yı seçin.

3. **İzin ve devamsızlık türü** tablosunda, düzenlemek için kalem seçeneğini belirleyin.

4. **RoundingPrecision** ve **RoundingType** değerini seçip alanlar listesine eklemek için **Ekle**'yi seçin.

5. **Güncelleştir**'i ve ardından **Bitti**'yi seçin.

6. Önceden ayarlanmamışsa, her bir izin türü için **Yuvarlama türü**'nü girin veya seçin. 

7. Uygun türler için **Yuvarlama hassasiyeti**'ni girin.

8. Değişiklikleri Human Resources'a göndermek için **Yayımla**'yı seçin.

## <a name="leave-and-absence-preview-features"></a>İzin ve devamsızlık Önizleme özellikleri

Bir **korumalı alan** ortamında yeni izin ve devamsızlık Önizleme özelliklerini deneyebilirsiniz. Önizleme özelliklerini açma hakkında bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md). Önizleme özellikleri şunları içerir:

- **İzin askıya alma** - Human Resources'ta bir çalışan için izin ve devamsızlığı askıya alabilirsiniz. İzni askıya alma, seçili izin türleri için izin tahakkuklarını durdurur. Askıya alma bir tahakkuk işleminden sonra gerçekleştiğinde, askıya alınan izin çalışanın izin bakiyesinde eşit dağıtılmış bir ayarlama oluşturur. 

- **Devretme kuralları** - Devretme ayarlamalarının transfer edildiği devir bakiyeleri için bir devretme izin türü belirtebilirsiniz. Örneğin, bir çalışan 10 günü ileri taşıyorsa, bu 10 gün için farklı bir izin türü seçebilirsiniz. 