---
title: İş emirleri oluşturma
description: Bu konuda Varlık Yönetimi'nde iş emirleri oluşturma işlemi açıklanmaktadır.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 876aef9f3f470490bb385e1861c837dcfa82db69
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131805"
---
# <a name="creating-work-orders"></a>İş emirleri oluşturma

[!include [banner](../../includes/banner.md)]

Önleyici bakım işlerini planladıktan sonra, bir sonraki adım bunlar için iş emirleri oluşturmaktır. Bu adımı bakım zamanlamalarından birini kullanarak tamamlayabilirsiniz. Bakım zamanlamasındaki zamanlanmış işler, aşağıdaki tabloda açıklanan şekilde farklı başvuru türlerine sahip olabilir:

| Referans türü | Tanım |
|---|---|
| Bakım planları | *Süre* veya *Sayaç* bakım planı türüne bağlı olan önleyici bakım işleri. |
| Bakım sıraları | Benzer bir bakım türü gerektiren birkaç kıymeti içeren önleyici bakım işleri. |
| Bakım talebi | Bir kıymetin bakımı veya onarımı için el ile oluşturulmuş bir istek. Bu istek bir iş emrine dönüştürülebilir. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Bakım zamanlamanıza göre iş emirleri oluşturma

Bakım zamanlamanızı temel alan iş emirleri oluşturmak için aşağıdaki adımları izleyin.

1. İş emirlerinizden zamanlama öğelerini nasıl seçmek istediğinize bağlı olarak, aşağıdaki sayfalardan birini açın:

    - Tüm bakım zamanlamaları (**Kıymet yönetimi \> Yönetim zamanlaması \> Tüm bakım zamanlamaları**)
    - Bakım zamanlaması satırlarını aç (**Kıymet yönetimi \> Yönetim zamanlaması \> Bakım zamanlaması satırlarını aç**)
    - Bakım zamanlaması havuzlarını aç (**Kıymet yönetimi \> Yönetim zamanlaması \> Bakım zamanlaması havuzlarını aç**)

1. Izgarada, iş emri oluşturmak istediğiniz her zamanlanmış bakım işi için onay kutusunu seçin. Ardından, Eylem Bölmesi'nde **İş emri**'ni seçin.

    **İş emri oluşturun** iletişim kutusu görüntülenir. **Bakım tahmini saatleri** alanında, seçili satırlar için tahmini saatlerin toplam sayısı gösterilir.

    ![İş emri oluşturun iletişim kutusu](media/18-preventive-maintenance.png)

1. **Parametreler** bölümünde, oluşturulması gereken iş emirlerinin sayısını belirtin. Aşağıdaki seçeneklerden birini belirleyin:

    - **Satır başına bir iş emri**: Her bakım zamanlaması satırı için bir iş emri oluşturun.
    - **Şuna göre bir iş emri**: Bu seçeneği belirlediğinizde sunulan diğer seçeneklerin ayarlarına göre gruplandırılmış iş emirleri oluşturun.

1. **İş emri türü** alanında, oluşturduğunuz tüm iş emirleri için kullanılacak iş emri türünü seçin.
1. Ayarlarınıza göre iş emirlerini oluşturmak için **Tamam**'ı seçin.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Bakım planı çalışırken otomatik olarak oluşturulan iş emri satırlarını gruplandırma

> [!IMPORTANT]
> Bu bölümde açıklanan işlev, özel bir önizleme sürümünün bir parçası olarak sunulur. İçerik ve işlevde değişiklik yapılabilir. Önizleme sürümleri hakkında daha fazla bilgi için bkz. [One Version hizmeti güncelleştirmeleriyle ilgili SSS](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).

Bu özellik, sistem bir bakım planına göre otomatik olarak iş emirleri oluşturmak üzere ayarlandığında, iş emri satırlarını tek bir iş emri altında gruplandırmak için kurallar tanımlamanıza olanak sağlar. Daha önce otomatik olarak oluşturulan iş emirleri yalnızca tek bir satır içerebiliyordu. Ancak, şu anda iş emirlerini kıymet, kıymet türü veya işlem yapılacak yerleşim gibi ölçütlere göre gruplandırabilirsiniz. (Elle oluşturulan iş emirleri bu konunun önceki bölümünde açıklandığı gibi zaten bu şekilde gruplandırılabilir.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Otomatik oluşturulan iş emirleri için gruplandırmayı etkinleştirme

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Kıymet Yönetimi*
- **Özellik adı:** *(Önizleme) Bakım planı çalıştırırken iş emirlerini gruplandırmak için kural uygulama*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Otomatik oluşturulan iş emirleri için gruplandırmayı ayarlama

Otomatik oluşturulan iş emirleri için gruplandırmayı ayarlamak üzere şu adımları izleyin:

1. **Kıymet yönetimi \> Kurulum \> Önleyici bakım \> Bakım planları**'na gidin.
1. Gruplandırılmış iş emirleri oluşturmak istediğiniz her plan için şu adımları izleyin:

    1. Liste bölmesinde planı seçin.
    1. **Satırlar** hızlı sekmesinde, her satırda **Otomatik oluştur** onay kutusunun seçili olduğundan emin olun.

1. **Kıymet yönetimi \> Dönemsel \> Önleyici bakım \> Bakım planlarını zamanla** öğesine gidin.
1. **Bakım planlarını zamanlayın** iletişim kutusundaki **Dönem** bölümünde, plan için değerlendirme tarihini (iş oluşturulacak zamanlanmış bakım işlerini bulmak için ne kadar süre sonraya bakılması gerektiğini) belirtin.
1. **Zamanlamayı kullanarak iş emrini otomatik olarak oluştur** seçeneğini *Evet* olarak ayarlayın.
1. **İş emri** bölümünde aşağıdaki seçeneklerden birini belirleyin:

    - **Satır başına bir iş emri**: Her bakım zamanlaması satırı için bir iş emri oluşturun. (Bu seçenek, *Bakım planı çalıştırırken iş emirlerini gruplandırmak için kural uygula* özelliği kapalıyken kullanılabilen işlevle aynı işlevi sağlar.)
    - **Şuna göre bir iş emri**: Bu seçeneği belirlediğinizde sunulan diğer seçeneklerin ayarlarına göre gruplandırılmış iş emirleri oluşturun.

1. Seçeneklerin yalnızca bakım planlarınızın bazılarını çalıştırırken geçerli olmasını istiyorsanız **Eklenecek kayıtlar** hızlı sekmesinde, Microsoft Dynamics 365 Supply Chain Management'taki diğer toplu işlerde yapacağınız gibi gerekli filtreleri ekleyin.
1. **Arka planda çalıştır** hızlı sekmesinde, Supply Chain Management'taki diğer toplu işler için yapacağınız şekilde, ihtiyaç duyduğunuz toplu iş ve zamanlama seçeneklerini ayarlayın.
1. Seçili bakım planlarını çalıştırmak ve/veya zamanlamak için **Tamam**'ı seçin.
