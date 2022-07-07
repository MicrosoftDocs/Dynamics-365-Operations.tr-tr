---
title: Madde tahminini hesapla
description: Bu makalede Varlık Yönetiminde madde tahmininin nasıl hesaplandığını açıklanmaktadır.
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetItemForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 25e9b00533fb183b27c1bbe616cf6f414b44b5e7
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016115"
---
# <a name="calculate-item-forecast"></a>Madde tahminini hesapla

[!include [banner](../../includes/banner.md)]

 

Önceki bölümde anlatılan Kapasite yükü hesaplamaları yapabileceğiniz gibi, madde tahmini hesaplamaları da yapabilirsiniz:

- bakım zamanlaması satırları  
- henüz zamanlanmamış olan iş emirleri  
- planlanmış iş emirleri

Bu, belirli bir döneme ait beklenen madde tüketiminin (iş emirlerini tamamlamak için gerekli diğer maddelerin yanı sıra yedek parçaların) genel görünümünü almak istediğinizde yararlıdır. Madde tahmini hesaplaması tüm varlıklar veya seçilen varlıklar üzerinde yapılabilir. Ayrıca bir bakım kesinti süresi faaliyetinde (**Tüm bakım kesinti süresi faaliyetleri** veya **Etkin bakım kesinti süresi faaliyetleri**) veya iş emri havuzunda (**Tüm iş emri havuzları** veya **Etkin iş emri havuzları**) da hesaplama yapabilirsiniz.

1. **Varlık yönetimi** > **Sorgular** > **Madde tahmini** veya **Varlık yönetimi** > **İş emri havuzları** > **Tüm iş emri havuzları** / **Etkin iş emri havuzları**'na tıklayın > listeden iş emri havuzu seçin > **Madde tahmini** düğmesine veya **Varlık yönetimi** > **Bakım kesinti süresi faaliyetleri** > **Tüm bakım kesinti süresi faaliyetleri** / **Etkin bakım kesinti süresi faaliyetleri**'ne tıklayın > listeden bakım kesinti süresi faaliyeti seçin > **Madde tahmini** düğmesine tıklayın.

2. **Madde tahminini hesapla** iletişim kutusunda, **Başlangıç tarihi/saati** ve **Bitiş tarihi/saati** alanlarında hesaplama için bir dönem seçin.

3. Bakım zamanlaması satırlarını tahmin hesaplamasına dahil etmek istiyorsanız **Bakım zamanlamasını dahil et** düğmesini "Evet" seçeneğine getirin.

4. İş emri işlerini tahmin hesaplamasına dahil etmek istiyorsanız **İş emrini dahil et** düğmesini "Evet" seçeneğine getirin.

5. İşlem yapılacak yerleşimlerle ilişkilendirmek istediğiniz madde tahmini satırlarının ayrıntılarını göstermek için **Düzey** alanını kullanabilirsiniz. 

      Örneğin alana "1" değerini girerseniz ve çok düzeyli bir işlem yapılacak yerleşim yapınız varsa, işlem yapılacak yerleşim için tüm bakım zamanlaması satırlarıve iş emirleri üst düzeyde gösterilir ve dolayısıyla bir satırdaki saatler, alt düzeyde bulunan işlem yapılacak yerleşimden eklenebilir. 
  
      **Düzey** alanına "0" değerini girerseniz ilişkili oldukları tüm işlem yapılacak yerleşim düzeyinde bulunan tüm bakım zamanlaması satırlarını ve tüm iş emirlerini gösteren ayrıntılı bir sonuç görürsünüz.

6. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

7. **Gruplandırma ölçütü...** gruplarında, hesaplamanın gerekli ayrıntı düzeyini göstermek için ilgili düğmelere tıklayın. Aşağıdaki ekran görüntüsünde, seçilen **Gruplama ölçütü** düğmeleri mavi renkle vurgulanır. Etkinleştirmek veya devre dışı bırakmak için bir düğmeye tıklayın.

8. Maddelerle ilgili ürün, depolama alanı veya izleme boyutlarını görmek istiyorsanız, **Boyutları görüntüle** düğmesine tıklayın. İlgili onay kutularını seçin ve **Tamam**'a tıklayın.

![Şekil 1.](media/02-capacity-planning.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]