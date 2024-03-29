---
title: Sabit kalan ömür amortismanı
description: Bu makale, amortismanın Sabit kalan ömür yöntemi hakkında genel bir bakış sağlar.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 185e1c101ffb6dfbd47348952d6dfc47ab137ffa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853452"
---
# <a name="straight-line-life-remaining-depreciation"></a>Sabit kalan ömür amortismanı

[!include [banner](../includes/banner.md)]

Bu makale, amortismanın Sabit kalan ömür yöntemi hakkında genel bir bakış sağlar.

Bir sabit kıymek amortisman profili ayarladığınızda ve **Amortisman profilleri** sayfasındaki **Yöntem** alanından **Kalan düz çizgi yaşamı** öğesini seçtiğinizde amortisman profiline atanan sabit kıymetlerin amortismanı kıymetin kalan hizmet ömrüne dayalı olacaktır. Amortisman tutarı genellikle her amortisman döneminde aynı olur. Düz çizgi kalan ömür amortismanı ayarlamak için, **Amortisman profilleri** sayfasında **Amortisman yılı** alanı ve **Dönem sıklığı** alanındaki seçenekleri de belirlemeniz gerekir. **Dönem sıklığı** alanındaki kullanılabilir seçenekler, **Amortisman yılı** alanında seçili değere bağlı olarak değişir.

## <a name="select-a-depreciation-year"></a>Bir amortisman yılı seçin
**Amortisman profilleri** sayasındaki **Amortisman yılı** alanından **Takvim** Yılı veya **Mali** Yıl seçimi yapabilirsiniz. Varsayılan değer **Takvim** seçeneğidir. Seçiminiz, **Dönem sıklığı** alanında bulunan seçenekleri belirler. Bu alan, amortisman tahakkuk deftere nakil tarihlerini ve tutarlarını takvim yılı boyunca tanımlar.

### <a name="calendar"></a>Takvim

**_Amortisman yılı_*alanında **Takvim**'i seçerseniz, mali takvimi farklı tanımlamış olsanız bile, 1 Ocak-31 Aralık arası bir yıl varsayılır. _* Takvim** seçeneği, amortisman tabanını her yıl 1 Ocak 'ta güncelleştirilir. Tipik olarak, amortisman tabanı, net defter değeri eksi hurda değeridir. Bu makalenin devamındaki örnekte, amortisman tabanı hesaplamalar sütununda yer alan ilk ifadedeki pay olur. Amortisman yılı olarak **Takvim** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir :

- **Yıllık** 31 Aralık'ta bir tutarı nakleder.
- **Aylık** seçeneği her takvim ayının sonunda bir aylık tutarı nakleder.
- **Üç aylık** seçeneği, üç aylık takvim döneminin sonunda (31 Mart, 30 Haziran, 30 Eylül ve 31 Aralık) bir üç aylık tutar nakleder.
- **Altı Aylık** seçeneği, altı aylık takvim döneminde ( 30 Haziran ve 31 Aralık) bir altı aylık tutar nakleder.
- **Günlük** seçeneği her gün için bir işlem kullanarak günlük amortisman yöntemi için amortisman tutarını nakleder.

Örneğin, **Yıllık** seçeneğini belirlerseniz yıllık amortisman her yılın 31 Aralık tarihinde yalnızca bir defa nakledilir. **Aylık** seçeneğini belirlerseniz aylık amortisman her ayı, yıllık amortisman tutarının on ikide biri oranında nakleder

### <a name="fiscal"></a>Mali

**Amortisman yılı** alanından **Mali Yıl** seçimini yaparsanız düz çizgi kalan yaşam amortismanı kullanılır Amortisman, kalan mali yıllar temel alınarak hesaplanır. Örneğin, 1 Temmuz 2015 ile 30 Haziran 2016 arasındaki mali yıl için amortisman hesaplaması 1 Temmuz'da başlar. Mali yıl 12 aydan daha uzun veya daha kısa olabilir. Amortisman her mali dönem için ayarlanır. Bir sonraki mali yılın uzunluğu, **Mali takvimler** sayfasında ayarlanan mali dönemler tarafından belirlenir. Amortisman yılı olarak **Mali** seçerseniz, **Dönem sıklığı** alanında şu seçenekler kullanılabilir:

- **Yıllık**, mali yıl için hesaplanan toplam amortisman tutarını tek tutar olarak, mali yılın son gününde nakleder.
- **Mali dönem** seçeneği, mali yılın amortismanının toplam tutarını hesaplar. Bu tutar daha sonra, defter için belirtilen mali takvim için **Mali takvimler** sayfasında tanımlanan mali dönemlere aktarılır.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Değişmeyen bir sabit kıymet için düz çizgi amortisman örneği
Bir sabit kıymet aşağıdaki özelliklere sahiptir.

| Alan               | Değer  |
|:---------------------|--------:|
| Alım maliyeti    | 11,000 |
| Hurda değeri       | 1,000  |
| Amortisman tabanı   | 10.000 |
| Servis ömrü yıl sayısı  | 5      |
| Yıllık amortisman | 2.000  |

Amortisman tutarı her yıl aynıdır: (Edinme maliyeti – Hurda değeri) ÷ Servis ömrü yıl

| Dönem | Yıllık amortisman miktarının hesaplaması | Yıl sonunda net defter değeri |
|:--------:|:-----------------------------------------------|---------------------------------------:|
| Yıl 1 | (11.000 – 1.000) ÷ 5 = 2.000                  | 9.000                                 |
| 2. yıl | (9.000 – 1.000) ÷ 4 = 2.000                   | 7.000                                 |
| 3. yıl | (7.000 – 1.000) ÷ 3 = 2.000                   | 5.000                                 |
| Yıl 4 | (5.000 – 1.000) ÷ 2 = 2.000                   | 3.000                                 |
| Yıl 5 | (3.000 – 1.000) ÷ 1 = 2.000                   | 1.000                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
