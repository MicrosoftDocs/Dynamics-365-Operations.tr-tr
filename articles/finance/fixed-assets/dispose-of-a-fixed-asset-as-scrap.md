---
title: Sabit kıymeti hurda olarak elden çıkarma
description: Bu konu, hurda olarak elden çıkarılan bir sabit kıymet için hareketleri eleme sürecini açıklar.
author: moaamer
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 4dee4468079a9ad500f513900cec090acf6026ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969140"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Sabit kıymeti hurda olarak elden çıkarma

[!include [banner](../includes/banner.md)]

Bu konu, hurda olarak elden çıkarılan bir sabit kıymet için hareketleri eleme sürecini açıklar. Elenebilecek hareket tipleri bir kıymetin alımını ve birikmiş amortisman hareketlerini ve diğer sabit kıymet hareketlerini içerir. Bu hareketlerin elenmesi alım düzeltmesi, amortisman ayarlaması, yeniden değerleme, değer artırma ve değer azaltma hesapları gibi bilanço hesaplarını etkiler.

| Hareket                                         | Borç (Br.) | Alacak (Al.) |
|-----------------------------------------------------|-------------|--------------|
| Br. Birikmiş amortisman                        | X           |              |
| Al. sabit kıymet kazancı/zararı                          |             | X            |
| Br. Sabit kıymet kazancı/zararı                          | X           |              |
| Al. Sabit kıymet alımı hesabı                 |             | X            |
| Br. Sabit kıymet kazanç/kayıp (net defter değeri \[NDD\]) | X           |              |
| Al. Sabit kıymet kazancı/zararı (NDD)                    |             | X            |

> [!NOTE]
> Her hareket türü için kullanılacak doğru hesapları tanımlamak ve ayrıca elden çıkarma işleminin ve oluşturduğu hareketlerin doğrulanması için şirketinizin mali müdürü (CFO) veya denetleyicinizle yakından çalışmanızı öneririz.

Sabit bir kıymeti hurda olarak elden çıkarmadan önce kıymetin alım değeri, geçerli yıla ait amortisman, önceki yıla ait amortisman ve kıymetin NDD'si ile ilişkili genel muhasebe sehapları oluştırmanız gerekir. Sabit kıymet hareket türleri **Sabit kıymetler deftere nakil profili** sayfasında listelenmiştir. **Sabit kıymetler \> Kurulum \> Sabit kıymet deftere nakil profilleri**'ne gidin ve **Elden çıkarma** hızlı sekmesinde, kılavuzun üstündeki alanda bulunan **Hurda**'yı seçin. Aşağıdaki şekil, **Sabit kıymet deftere nakil profilleri** sayfasındaki sabit kıymet hareket türlerinin listesini gösterir.


[![Bir kıymetin hurda olarak elden çıkarılması, Şek. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

Aşağıdaki örnekte, sabit kıymet 1 Ocak 2018 tarihinde elde edildi ve 31 Mart 2019 tarihinde hurdaya çıkarılacak.

- **Alım fiyatı:** 24.000,00 ABD Doları (USD)
- **Servis ömrü:** İki yıl
- **Amortisman yöntemi:** Sabit servis ömrü
- **Amortisman tutarı:** ayda 1.000,00 USD

Sabit kıymetin NDD'si aşağıdaki formül kullanılarak hesaplanır:

Net defter değeri = Alım fiyatı – Amortisman

Bu örnekte, sabit kıymet elde edildi ve Ocak 2018 ile Mart 2019 arasında 15 ay için amortisman uygulandı. Bu nedenle kıymetin NDD'si 9.000,00 USD (24.000,00 USD – 15.000,00 USD).

[![Sabit kıymet amortisman örneği](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Elden çıkarma günlüğü oluşturmak için **Sabit kıymetler \> Günlük girişleri \> Sabit kıymetler günlüğü**'ne gidin ve Eylem bölmesinde **Satırlar**'ı seçin. **Elden çıkarma – hurda**'yı ve ardından sabit kıymet kodunu seçin. Kıymetin tamamen elden çıkarılması için **Borç** alanına veya **Alacak** alanına değer girmeyin.

[![Sabit kıymet günlüğü](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Sabit kıymet elden çıkarma hurda hareketi, sabit kıymet defterinin alan değerlerini aşağıdaki yollarla değiştirir:

- **Bakiye** bölümünde, **Durum** alanı **Hurdaya çıkarıldı** şeklinde güncelleştirilir.
- **Çıkış** bölümünde, **Elden çıkarma tarihi** alanı kıymetin hurdaya çıkarıldığı tarihe ayarlanır.

[![Sabit kıymetler günlüğü ayrıntısı](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

Aşağıdaki şekil sabit kıymet bakiyesini gösterir.

[![Sabit kıyme bakiyesi](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

Aşağıdaki şekil deftere nakledilen fişi gösterir.

[![Net defter değeri](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)
