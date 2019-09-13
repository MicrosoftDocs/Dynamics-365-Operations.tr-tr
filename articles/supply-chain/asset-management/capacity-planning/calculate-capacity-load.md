---
title: Kapasite yükünü hesapla
description: Bu konuda Varlık Yönetiminde kapasite yükünün nasıl hesaplandığını açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: c6d15861492a46ddb1222db2210f8c751ed38cb3
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886805"
---
# <a name="calculate-capacity-load"></a>Kapasite yükünü hesapla

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Varlık Yönetiminde, kapasite yükünü şunlar üzerinde hesaplayabilirsiniz:

- bakım zamanlaması satırları  
- henüz zamanlanmamış olan iş emirleri  
- planlanmış iş emirleri

Bu, belirli bir döneme ait beklenen kapasite yükünün genel görünümünü almak istediğinizde yararlıdır. Kapasite yükü hesaplanması tüm varlıklar veya seçilen varlıklar üzerinde yapılabilir. Ayrıca, bakım kesinti süresi faaliyetleri veya iş emri havuzlarında da hesaplama yapabilirsiniz.

1. **Varlık yönetimi** > **Sorgular** > **Kapasite yükü** veya **Varlık yönetimi** > **Genel** > **İş emri havuzları** > **Tüm iş emri havuzları** / **Etkin iş emri havuzları** > listeden iş emri havuzu seçin > **Kapasite yükü** düğmesine veya **Varlık yönetimi** > **Genel** > **Bakım kesinti süresi faaliyetleri** > **Tüm bakım kesinti süresi faaliyetleri** / **Etkin bakımkesinti süresi faaliyetleri** > listeden bakım faaliyeti seçin > **Kapasite yükü** düğmesine tıklayın.

2. **Kapasite yükünü hesapla** iletişim kutusunda, **Başlangıç tarihi/saati** ve **Bitiş tarihi/saati** alanlarında hesaplama için bir dönem seçin.

3. Bakım zamanlaması satırlarını hesaplamaya dahil etmek istiyorsanız **Bakım zamanlamasını dahil et** düğmesini "Evet" seçeneğine getirin.

4. İş emri işlerini hesaplamaya dahil etmek istiyorsanız **İş emrini dahil et** düğmesini "Evet" seçeneğine getirin.

5. İşlem yapılacak yerleşimlerle ilişkilendirmek istediğiniz kapasite yükü satırlarının ayrıntılarını göstermek için **Düzey** alanını kullanabilirsiniz. Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım zamanlaması satırlarıve iş emirleri üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. **Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeylerinde bulunan tüm bakım zamanlaması satırlarını ve tüm iş emirlerini gösteren ayrıntılı bir sonuç görürsünüz.

6. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

7. **Gruplandırma ölçütü...** eylem bölmesi gruplarında, hesaplamanın gerekli ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın. Seçilen eylem bölmesi grubu düğmeleri mavi renkte vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

Aşağıdaki şekilde bir arabirim örneği gösterilmektedir.

![Şekil 1](media/01-capacity-planning.png)

>[!NOTE]
>Yalnızca planlanan iş emirleriyle ilgili kapasite planlamasına odaklanmak istiyorsanız bkz. [Planlanan iş emirlerinde kapasite yükünü hesaplama](../work-order-scheduling/calculate-capacity-load-on-scheduled-work-orders.md).

