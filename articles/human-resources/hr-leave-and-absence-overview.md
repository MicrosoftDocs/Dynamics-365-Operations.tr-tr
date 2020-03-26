---
title: Özet
description: Dynamics 365 Human Resources'ta **İzin ve devamsızlık** çalışma alanı, yeni izin planları oluşturmak için esnek bir çerçeve, isteklerin yönetilmesi için iş akışları ve çalışanların zaman istebilmesi için sezgisel bir self servis sayfası sağlar.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 493bc3abe82103541125914896252b2eae596b38
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091760"
---
# <a name="overview"></a>Özet

Dynamics 365 Human Resources, çalışanlarınız için harika yararlar sağlamanıza yardımcı olur. **İzin ve devamsızlık** çalışma alanı, yeni izin planları oluşturmak için esnek bir çerçeve, isteklerin yönetilmesi için iş akışları ve çalışanların zaman istebilmesi için sezgisel bir self servis sayfası sağlar. Analitik yardım kuruluşunuz, izin planlarınızın bakiyelerini ve kullanımını ölçmenize ve izlemesine yardımcı olur.

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

- [İzin süresi iste](hr-employee-self-service-request-time-off.md)
- [İzin ve devamsızlığı yönetme talepleri](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-preview-features"></a>İzin ve devamsızlık Önizleme özellikleri

Bir **korumalı alan** ortamında yeni izin ve devamsızlık Önizleme özelliklerini deneyebilirsiniz. Bilgi Önizleme özelliklerini açmak için bkz. [Özellikleri yönet](hr-admin-manage-features.md). Önizleme özellikleri şunları içerir:

- **İzin ve devamsızlık takvimi** -İzin ve devamsızlık parametreleri, **İnsan kaynakları parametreleri**'nden, **İzin ve devamsızlık parametreleri** adlı yeni bir ekrana geçecek. Yeni ekranda yeni bir **Takvim** sekmesi var. Bu önizleme yalnızca parametrelerin bir alt kümesini sağlıyor. Yeni ekrana **İzin ve devamsızlık** çalışma alanının **Bağlantılar** sekmesinden erişebilirsiniz. Takvimler şunları içerir:
  - **Şirket takvimi** -Tüm çalışan izin isteklerini gösterir. **İnsan kaynakları** rolündeki kişiler bu takvime **İzin ve devamsızlık** çalışma alanının **Bağlantılar** sekmesinden erişebilirler.
  - **Yönetici ekibi takvimi** - Tüm bağlı çalışanların izin isteklerini gösterir. Yöneticiler takvime **İzin ve devamsızlık** altındaki Çalışan self servisi'ndeki **Ekibim** sekmesinden erişebilirler. 

- **İzin ve devamsızlık tatil takvimleri** - İzin türleri, çalışma zamanı takvimiyle birlikte kullanılan yeni bir **Tatil** seçeneği içeriyor. Tatiller ve kapanışlar ile tanımlanan günler artık çalışma günleri oluşturulurken **Tatil** olarak belirleniyor. Tahakkuklar işlenirken, çalışma gününe denk gelen tatilleri hesaba katmak için, takvime atanan çalışanlarda ayarlamalar yapılıyor.

- **İzin tahakkuku denetimi** - Yeni bir ekran, hem toplu olarak hem de tek tek çalışanların tahakkukları ne zaman işlediğini ve sildiğini incelemenizi sağlıyor. Bu yeni ekrana **İzin ve devamsızlık** çalışma alanının **Bağlantılar** sekmesinden erişebilirsiniz.

- **İzin tahakkuku silme** - Artık belirli izin planları için tahakkuk kayıtlarını silebilirsiniz. Bu yeni seçeneğe **İzin ve devamsızlık** çalışma alanının **Bağlantılar** sekmesinden erişebilirsiniz. Tek tek çalışanlar için bu seçenek, çalışan profilindeki **İzin ve devamsızlık** gruplandırmasında görüntülenir. 

- **İzin tahakkuku yuvarlama** - **İzin türü** için yeni seçenekler tahakkukta hangi tür yuvarlama kullanılacağını ve tahakkuk işlemi sırasında yuvarlamanın ondalık duyarlığını tanımlıyor. Tahakkuklar işlenirken, tahakkuk kayıtlarına yuvarlama ve duyarlık uygulanır. 

- **Tek bir izin planında birden fazla izin türü yapılandır** - İzin türleri için izin tahakkuku zaman çizelgesindeki yeni bir sütun, farklı tahakkuk zamanlamalarıyla bir izin ve devamsızlık planı üzerinde birden fazla izin türü tanımlamanıza olanak sağlıyor. Önceki **İzin türü** alanı kaldırıldı. Çalışan kaydında, izin türlerinin bakiyeleri şimdi ekranın üst bölümünde değil, bir tabloda görüntüleniyor.

  > [!IMPORTANT]
  > Bu özelliği etkinleştirildikten sonra kapatabilirsiniz.

- **Tahakkuk için bir çalışanın tam zamanlı eşdeğerliliğini (FTE) kullanımı** - İzin tahakkuku zaman çizelgesindeki yeni bir sütun, tahakkuk için FTE kullanmaya izin veriyor. Tahakkuklar işlenirken, uygulama, çalışanın birincil pozisyonunu ve orantılı tahakkuk tutarını belirlemek için tanımlanan FTE'yi kullanıyor.

  > [!NOTE]
  > Bu özellik ancak **Tek bir izin planında birden fazla izin türü yapılandır**'ı etkinleştirirseniz kullanılabilir. 
