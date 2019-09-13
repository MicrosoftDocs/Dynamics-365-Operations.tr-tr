---
title: Varlık sayaçlarını el ile güncelleştirme
description: Bu konuda, Varlık Yönetiminde varlık sayaçlarının el ile güncelleştirilmesi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875947"
---
# <a name="manual-update-of-asset-counters"></a>Varlık sayaçlarını el ile güncelleştirme

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Sayaçlar, varlıkta örneğin operasyondaki saat sayısı veya üretilen miktar sayısı gibi kayıtları oluşturmak için kullanılır.

Bir sayaç için seçilen sayaç türü sayaç değerlerini devralmak üzere ayarlanırsa (**Varlık yönetimi** > **Kurulum** > **Varlık türleri** > **Sayaçlar** > **Genel** hızlı sekmesi > **Varlık sayaç değerlerini devral** düğmesi "Evet" olarak ayarlanır) bu tür için yeni bir sayaç satırı oluşturduğunuzda, aynı sayaç türünü kullanan alt varlıklar otomatik olarak güncelleştirilir.

**Tüm varlıklar**'da, varlık üzerinde yaptığınız okumaları temel alarak, varlıkta saatler veya miktar sayacı kayıtları oluşturursunuz.

1. **Varlık yönetimi** > **Ortak** > **Varlıklar** > **Tüm varlıklar** öğesini seçin.

2. Listeden varlığı seçin ve **Sayaçlar**'a tıklayın. **Varlık sayaçları** formunda, seçilen varlıktaki önceki tüm sayaç kayıtlarının listesini görürsünüz.

3. Yeni bir kayıt oluşturmak için **Yeni**'ye tıklayın. Varlık kodu otomatik olarak eklenir.

4. **Sayaç** alanında, ilgili sayacı seçin. Yalnızca, varlıkta seçilen varlık türüyle ilgili sayaçlar kullanılabilir. İlgili birim otomatik olarak **Birim** alanına eklenir.

5. Sayaç kaydı için tarih ve saat seçin.

6. **Değer** alanına, en son sayaç kaydından itibaren numarayı ekleyin veya **Toplam değer** alanına toplam sayı numarasını ekleyin.

- Bir varlığa fiziksel olarak yeni bir sayaç yüklerseniz, değişikliği **Varlık sayaçlarında** varlığa kaydetmeniz gerekir. Daha sonra, aynı zaman damgalarına sahip iki kayıt satırı oluşturmanız ve yeni sayaca ilişkin satırda, **Sayaç sıfırlama** onay kutusunu seçmeniz gerekir. İki kayıt satırını oluşturduğunuzda, ilk satır değiştirdiğiniz sayaca ait olmalıdır. **Toplamlar** alanında toplam sayı numarası, bu sayaç türündeki tüm kayıtlı değerlerin toplam sayaç toplamıdır.  
- **Sayaç sıfırlama** onay kutusu "İtibaren bir kez..." veya "Ulaşıldığında..." aralık türüne sahip bir bakım planı kullanan bir varlıkta işaretlendiğinde, ayrı bir sayaç satırı oluşturduğunuz ve yeni bir sayaçla baştan başladığınızdan sayaç yeni sayaç satırında etkin olmaya devam eder.

![Şekil 1](media/11-work-orders.png)


Birden fazla varlıkta sayaç kayıtları yapmanız gerekiyorsa, bunu **Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Varlık sayaçları** altından yapabilirsiniz.

>[!NOTE]
>El ile sayaç kayıtlarında sapmaları tanımlamak için bir aralık ve kayıtlar tanımlanan aralığın dışında olduğunda görüntülenecek olan ileti türü ayarlayabilirsiniz. Sayaçların kurulumuyla ilgili olarak [Sayaçlar](../setup-for-objects/counters.md) konusuna bakın.
