---
title: Bakım durumu
description: Bu konuda Kıymet Yönetimi'nde bakım durumu hesaplama işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918361"
---
# <a name="maintenance-status"></a>Bakım durumu

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Belirli bir döneme ait yeni, etkin ve tamamlanmış bakım isteklerinin, iş emirlerinin ve bakım kesinti faaliyetlerinin genel görünümünü görmek için, kıymet yönetiminde hesaplama yapabilirsiniz. Aynı dönem için tamamlanan koşul değerlendirmelerinin sayısını da görebilirsiniz. Gelen ve tamamlanan bakım istekleriyle ve iş siparişleriyle ilgili iş yükünün özetini almak için bu hesaplamayı kullanın.

## <a name="make-a-maintenance-status-calculation"></a>Bakım durumu hesaplaması yap

1. **Varlık Yönetimi** > **Sorgular** > **Bakım durumu**' nu tıklatın.

2. **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında hesaplamayı yapmak istediğiniz **Durumu hesapla** iletişim kutusunda, girin.

3. İşlem yapılacak yerleşimlerle ilgili olarak bakım satırlarının ne kadar ayrıntılı olmasını istediğinizi belirtmek için **Düzey** alanını kullanabilirsiniz. Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım satırları üst düzeyde gösterilir ve dolayısıyla bir satırdaki durum, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. **Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm bakım satırlarını gösteren ayrıntılı bir sonuç görürsünüz.

4. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

5. **Gruplandırma ölçütü...** eylem bölmesi gruplarında, hesaplamanın gerekli ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın. Seçilen eylem bölmesi düğmeleri vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

6. **Grupla...** düğmelerini etkinleştirerek veya devre dışı bırakarak her değişiklik yaptığınızda hesaplamayı güncelleştirmek için **Güncelleştir** düğmesine basmayı unutmayın.

7. Yeni bir bakım durumu hesaplaması oluşturmak istiyorsanız **durum**'ı tıklatın.

>[!NOTE]
>**Bakım durumunda** gösterilen sonuçlar yalnızca gerçek başlangıç tarihi ve saatine sahip bakım isteklerini ve çalışma emirlerini içerir. Bitiş tarihi ve saati boş olabilir.

*Örnek 1:*

Aşağıdaki şekilde, **Yıl** ve **Ay** düğmeleri etkinleştirilmiştir. Burada, bakım istekleriyle ve iş emirleriyle ilgili iş yükü ve iş emirleri hakkında genel bakış elde edebilirsiniz. 

![Şekil 1](media/13-controlling-and-reporting.png)

*Örnek 2:*

Aşağıdaki çizimde, işlem yapılacak yerleşim bilgileri eklendi. Şimdi, coğrafi konumları, fabrikaları veya çalışma alanlarını temsil eden işlem yapılacak konumlar arasında iş yükü ve iş yükünü karşılaştırmak mümkündür. 

![Şekil 2](media/14-controlling-and-reporting.png)

