---
title: Kıymet sayaçlarını el ile güncelleme
description: Bu makalede, Varlık Yönetiminde varlık sayaçlarının el ile güncelleştirilmesi açıklanmaktadır.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 30c672286c16a4353556a507019960edb93f8b1b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016608"
---
# <a name="manual-update-of-asset-counters"></a>Kıymet sayaçlarını el ile güncelleştirme

[!include [banner](../../includes/banner.md)]



Sayaçlar, bir varlık üzerinde varlığın işlemde olduğu saat sayısı veya üretilmiş miktar gibi kayıtlar için kayıt oluşturmak amacıyla kullanılır.

Bir sayaç için seçilen sayaç türü, sayaç değerlerini devralmak üzere ayarlanabilir. Başka bir deyişle, **VArlık sayacı değerlerini devral** seçeneği **Sayaçlar** sayfasının **Genel** hızlı sekmesinde **Evet** olarak ayarlanır (**Varlık yönetimi** > **Kurulum** > **Varlık türleri** > **Sayaçlar**). Bu durumda, bu türde yeni bir sayaç satırı oluşturduğunuzda, aynı sayaç türünü kullanan her alt varlık otomatik olarak güncelleştirilir.

**Tüm varlıklar** sayfasında, varlık üzerinde yaptığınız okumaları temel alarak, varlıkta saatler veya miktar sayacı kayıtları oluşturursunuz.

1. **Varlık yönetimi** > **Varlıklar** > **Tüm varlıklar**'ı seçin.

2. Varlığı seçin ve ardından Eylem bölmesinde **Varlık** sekmesinde, **Önleyici** grubunda **Sayaçlar**'ı seçin. **Varlık sayaçları** sayfası, seçilen varlıkta yapılmış olan önceki tüm sayaç kayıtlarının listesini gösterir.

3. Kayıt oluşturmak için **Yeni**'yi seçin. Varlık kodu **Varlık** alanına otomatik olarak girilir.

4. **Sayaç** alanında, ilgili sayacı seçin. Yalnızca, varlıkta seçilen varlık türüyle ilgili sayaçlar seçilebilir. İlgili birim otomatik olarak **Birim** alanına girilir.

5. **Kayıtlı** alanında, sayaç kaydının tarih ve saatini seçin.

6. **Değer** alanına, son sayac kaydından sonra gelen numarayı girin. Alternatif olarak, **Toplu değer** alanına toplam sayım numarasını girin.

Aaşağıdaki noktaları unutmayın:

- Bir varlığa fiziksel olarak yeni bir sayaç yüklerseniz, değişikliği **Varlık sayaçları** sayfasında varlığa kaydetmeniz gerekir. Daha sonra, aynı zaman damgalarına sahip iki kayıt satırı oluşturmanız gerekir. İlk satırın değiştirdiğiniz sayaç için olması gerekir. Yeni sayaçla ilgili satırda, **Sayaç sıfırla** onay kutusunu seçin. **Toplamlar** alanında toplam sayı numarası, bu sayaç türündeki tüm kayıtlı değerlerin toplam sayaç toplamıdır.

- **Sayaç sıfırlama** onay kutusu "İtibaren bir kez..." veya "Ulaşıldığında..." aralık türüne sahip bir bakım planı kullanan bir varlıkta işaretlendiğinde, ayrı bir sayaç satırı oluşturduğunuz ve yeni bir sayaçla baştan başladığınızdan sayaç yeni sayaç satırında etkin olmaya devam eder.

Aşağıdaki örnekte **Varlık sayaçları** sayfasının bir örneği gösterilmektedir.

![Şekil 1.](media/11-work-orders.png)

**Varlık sayaçları** sayfasında (**Varlık yönetimi** > **Sorgular** > **Varlıklar** > **Varlık sayaçları**), gereksinim duyduğunuz gibi, aynı anda birden fazla varlıkta sayaç kaydı yapabilirsiniz.

>[!NOTE]
>El ile gerçekleştirilen sayaç kayıtlarında sapmaları tanımlamak için bir aralık ayarlayabilirsiniz. Kayıtlar tanımlanan aralığın dışında olduğunda gösterilecek ileti türünü de belirleyebilirsiniz. Sayaçların nasıl ayarlanacağı konusunda daha fazla bilgi için bkz. [Sayaçlar](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]