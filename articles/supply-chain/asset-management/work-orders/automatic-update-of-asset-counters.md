---
title: Kıymet sayaçlarını otomatik olarak güncelleştirme
description: Bu konuda, Varlık Yönetiminde varlık sayaçlarının otomatik olarak güncelleştirilmesi açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fcc46fad8d57b7d4d57edfa4f2ae06de923d1c14
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209194"
---
# <a name="automatic-update-of-asset-counters"></a>Kıymet sayaçlarını otomatik olarak güncelleştirme

[!include [banner](../../includes/banner.md)]

Varlık sayaçlarının el ile kaydı hakkında bilgi edinmek için bkz. [Varlık sayaçlarının el ile güncelleştirilmesi](../work-orders/manual-update-of-asset-counters.md). Varlık sayaçlarının nasıl ayarlanacağı konusunda bilgi için bkz. [Sayaçlar](../setup-for-objects/counters.md).

Sayaç değerleri, üretim saetleri veya üretim miktarına (bu üretilen miktardır) göre üretim kayıtlarından da otomatik olarak güncelleştirilebilir. Bu güncelleştirme, **Varlık sayaçlarını güncelleştir** sayfasında gerçekleştirilir. Bir veya daha fazla varlığı bir **Başlangıç tarihi** parametresi ayarlayarak güncelleştirebilirsiniz. Bu parametre, üretim kayıtları (üretim saatleri veya üretim miktarları) için başlangıç tarihini belirtir. Başka bir deyişle, sayaç değerlerinin güncelleştirilmesi gereken tarihi belirtir.

Bir kaynakla ilişkili olan *ve* üretim saatlerine veya üretim miktarına göre güncelleştirilmek üzere ayarlanan varlık sayaçları bulunan tüm varlıklar otomatik güncelleştirmeye dahil edilir. Yeni sayaç değerleri oluşturulur.

Üretim miktarına dayalı sayaçlar için sayım, hem sağlam miktarı hem de kaydedilen hata miktarını içerir. Üretim miktaır kaydı için kullanılan birim sayaçta kullanılan birimden farklıysa miktar sayaç birimine karşılık gelecek şekilde dönüştürülür.

Yukarıda belirtildiği gibi, otomatik sayaçlar üretim kayıtlarından güncelleştirilebilir. Bu nedenle, sayaçlarını otomatik olarak güncelleştirmek istediğiniz varlık bir kaynakla (makine) ilişkili olmalıdır. Üretilen miktarlar veya üretim saatleri kaynağa kaydedildiğinde, ilgili varlık sayaçlarını güncelleştirebilirsiniz.

1. **Varlık yönetimi** > **Periyodik** > **Varlıklar** > **Varlık sayaçlarını güncelleştir**'i seçin.

2. **Başlangıç tarihi** alanında otomatik güncelleştirmenin başlangıç tarihini seçin.

    >[!NOTE]
    >Bu alandaki tarih, **Rota hareketlerinden** gelen "süren iş" tarihidir (**Üretim denetimi** > **Sorgular ve raporlar** > **Üretim** > **Rota hareketleri** > **Fiziksel tarih** alanı).

3. **Dahil edilecek kayıtlar** hızlı sekmesinde, otomatik güncelleştirme için belirli varlıkları, varlık türlerini veya kaynakları seçebilirsiniz. **Filtre**'yi seçin ve ilgili seçimleri yapın.

4. **Arka planda çalıştır** hızlı sekmesinde gerektiğinde otomatik güncelleştirmeyi toplu iş olarak ayarlayabilirsiniz.

    Aşağıdaki örnekte **Varlık sayaçlarını güncelleştir** iletişim kutusunun bir örneği gösterilmektedir.

    ![Şekil 1](media/12-work-orders.png)

5. **Tamam**'ı seçin. 

Otomatik varlık sayacı güncelleştirmesi yapıldıktan sonra, **Varlık sayaçları** sayfasında bulunan varlıkla ilgili sayaç kayıtlarını görüntüleyebilirsiniz. **Varlık yönetimi** > **Ortak** > **Varlıklar** > **Tüm varlıklar**'ı seçin, varlığı seçin ve ardından Eylem Bölmesinde **Varlık** sekmesine gidip **Önleyici** grubundan **Sayaçlar**'ı seçin.

**Varlık toplam değeri** sayfasında tüm varlıklardaki tüm sayaç türlerinde yapılmış en son kaydın genel görünümünü alabilirsiniz. **Varlık Yönetimi** > **Sorgular** > **Varlıklar** > **Varlık toplam değeri**'ni seçin. Bu sayfa, **Varlık sayaçları** sayfasına benzer, ancak kayıt ekleyemez veya düzenleyemezsiniz. Yalnızca genel bakış içindir.

Aşağıdaki örnekte **Varlık toplam değeri** sayfasının bir örneği gösterilmektedir.

![Şekil 2](media/13-work-orders.png)

Aaşağıdaki noktaları unutmayın:

- Otomatik olarak güncelleştirilen sayaç türleri için el ile sayaç değeri kayıtları da oluşturabilirsiniz. Daha fazla bilgi için bkz. [Varlık sayaçlarını el ile güncelleştirme](../work-orders/manual-update-of-asset-counters.md).

- Başka bir sayaca ilişkin sayaçlar ayarlayabilirsiniz. Bu durumda, bir sayaç güncelleştirildiğinde, ilgili sayaçlar aynı anda otomatik olarak güncelleştirilir. İlgili sayaçların nasıl ayarlanacağı konusunda daha fazla bilgi için bkz. [Sayaçlar](../setup-for-objects/counters.md).

