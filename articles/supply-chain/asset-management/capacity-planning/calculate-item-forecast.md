---
title: Madde tahminini hesapla
description: Bu konuda Varlık Yönetiminde madde tahmininin nasıl hesaplandığını açıklanmaktadır.
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
ms.openlocfilehash: 9091ff7a394cd08b68e78c8f668d7cd962003e6d
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886782"
---
# <a name="calculate-item-forecast"></a>Madde tahminini hesapla

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Önceki bölümde anlatılan Kapasite yükü hesaplamaları yapabileceğiniz gibi, madde tahmini hesaplamaları da yapabilirsiniz.

- Bakım zamanlaması satırları  
- Henüz zamanlanmamış olan iş emirleri  
- Planlanan iş emirleri

Bu, belirli bir döneme ait beklenen madde tüketiminin (iş emirlerini tamamlamak için gerekli diğer maddelerin yanı sıra yedek parçaların) genel görünümünü almak istediğinizde yararlıdır. Madde tahmini hesaplaması tüm varlıklar veya seçilen varlıklar üzerinde yapılabilir. Ayrıca bir bakım kesinti süresi faaliyetinde (**Tüm bakım kesinti süresi faaliyetleri** veya **Etkin bakım kesinti süresi faaliyetleri**) veya iş emri havuzunda (**Tüm iş emri havuzları** veya **Etkin iş emri havuzları**) da hesaplama yapabilirsiniz.

1. **Varlık yönetimi** > **Sorgular** > **Madde tahmini** veya **Varlık yönetimi** > **Genel** > **İş emri havuzları** > **Tüm iş emri havuzları** / **Etkin iş emri havuzları** > listeden iş emri havuzu seçin > **Madde tahmini** düğmesine veya **Varlık yönetimi** > **Genel** > **Bakım kesinti süresi faaliyetleri** > **Tüm bakım kesinti süresi faaliyetleri** / **Etkin bakım kesinti süresi faaliyetleri** > listeden bakım kesinti süresi faaliyeti seçin > **Madde tahmini** düğmesine tıklayın.

2. **Madde tahminini hesapla** iletişim kutusunda, **Başlangıç tarihi/saati** ve **Bitiş tarihi/saati** alanlarında hesaplama için bir dönem seçin.

3. Bakım zamanlaması satırlarını tahmin hesaplamasına dahil etmek istiyorsanız **Bakım zamanlamasını dahil et** düğmesini "Evet" seçeneğine getirin.

4. İş emri işlerini tahmin hesaplamasına dahil etmek istiyorsanız **İş emrini dahil et** düğmesini "Evet" seçeneğine getirin.

5. İşlem yapılacak yerleşimlerle ilişkilendirmek istediğiniz madde tahmini satırlarının ayrıntılarını göstermek için **Düzey** alanını kullanabilirsiniz. Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım zamanlaması satırlarıve iş emirleri üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. **Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm bakım zamanlaması satırlarını ve tüm iş emirlerini gösteren ayrıntılı bir sonuç görürsünüz.

6. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

7. **Gruplandırma ölçütü...** eylem bölmesi gruplarında, hesaplamanın gerekli ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın. Seçilen eylem bölmesi grubu düğmeleri mavi renkte vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

8. Maddelerle ilgili ürün, depolama alanı veya izleme boyutlarını görmek istiyorsanız, **Boyutları görüntüle** düğmesine tıklayın. İlgili onay kutularını seçin ve **Tamam**'a tıklayın.

Aşağıdaki şekilde bir arabirim ekran görüntüsü gösterilmektedir.

![Şekil 1](media/02-capacity-planning.png)