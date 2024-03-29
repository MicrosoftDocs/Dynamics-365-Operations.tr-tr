---
title: Ters işlemli amortismanın etkileri
description: Bu makalede, sabit kıymet hareketini ters kaydetmenin olası etkileri ele alınmaktadır.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: kfend
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f0eeaafe7538b6aeeadfc804096ecee11e714da
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714215"
---
# <a name="depreciation-effects-with-reversals"></a>Ters işlemli amortismanın etkileri

[!include [banner](../includes/banner.md)]

Bu makalede, sabit kıymet hareketini ters kaydetmenin olası etkileri ele alınmaktadır. 

Sabit kıymet hareketlerine ve sabit kıymetle ilişkili hareketlere ters işlem uygulayabilirsiniz. Ayrıca tersine çevrilmiş bir hareketi de iptal edebilirsiniz. 

Kıymet için deftere nakledilen en son hareket olmayan bir hareketi tersine çevirebilir veya iptal edebilirsiniz. Öncelikle, tersine çevireceğiniz hareketten sonra herhangi bir amortisman hareketinin deftere nakledilip edilmediğini belirleyin. Bu adımın sebebi bir hareketi ters kaydettiğinizde amortismanın yeniden hesaplanmayacak olmasıdır. Bu nedenle, amortisman ters işlem örneklerde gösterildiği gibi genellikle olduğundan daha fazla veya daha az belirtilir. 

Bir hareketi tersine çevirdiğinizde amortismanın doğru olduğundan emin olmak için amortismanın yeniden hesaplanmayacağını belirten bir ileti alırsanız, iptal işlemiyle devam etmeyin. Bunun yerine, önce tersine çevirmeye çalıştığınız hareketten sonra nakledilen amortisman hareketini tersine çevirin ve sonra iptal işlemiyle devam edin. Amortismanın yeniden hesaplanmasıyla ilgili uyarılmazsınız ve iptal işlemiyle devam edebilirsiniz. 

Aşağıdaki örneklerde, uyarı iletisinden sonra, öncelikle amortisman hareketlerini tersine çevirmeden devam ederseniz oluşacak hesaplamalar gösterilir.

## <a name="example-1-depreciation-is-overstated"></a> Örnek 1: Amortisman olduğundan daha fazla belirtilir
Bir kıymet beş yıllık kullanım süresi ve sabit amortisman (60 amortisman dönemi) ile ayarlanmıştır. Bu örnekte, amortisman olduğundan daha fazla belirtilmiştir.
#### <a name="asset-transaction-history"></a>Kıymet hareket geçmişi

| Tarih       | Hareket tipi                                                          | Tutar                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| 1 Ocak  | Alım                                                               | 59.000,00                                 |
| 1 Ocak  | Alım düzeltmeleri                                                    | 1.000,00                                  |
| 31 Ocak | Amortisman (bir amortisman dönemine yönelik teklifin kullanılmasıyla oluşturulan) | 1.000,00Hesaplaması: Defter değeri (59.000 + 1.000 amortisman) / kalan amortisman dönemi sayısı (60) |

#### <a name="reversal-action"></a>Tersine çevirme eylemi

| Tarih      | Hareket türü                | Tutar    |
|-----------|---------------------------------|-----------|
| 1 Ocak | Alım ayarlaması iptali | -1.000,00 |

#### <a name="depreciation-effect"></a>Amortisman etkisi

| Tarih        | Hareket türü        | Tutar                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| 28 Şubat | Amortisman (teklif) | 983,05Hesaplaması: Defter değeri (59.000 - 1.000 amortisman) / kalan amortisman dönemi sayısı (59) |

Amortisman 16,95 değeri kadar daha fazla belirtilir (1000 - 983,05).

## <a name="example-2-depreciation-is-understated"></a> Örnek 2: Amortisman olduğundan daha az belirtilir
Bir kıymet beş yıllık kullanım süresi ve sabit amortisman (60 amortisman dönemi) ile ayarlanmıştır. Bu örnekte, amortisman olduğundan daha az belirtilmiştir.
#### <a name="asset-transaction-history"></a>Kıymet hareket geçmişi

| Tarih       | Hareket türü                                                          | Tutar                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| 1 Ocak  | Alım                                                               | 59.000,00                                   |
| 1 Ocak  | Değer azaltma düzeltmesi                                                     | 1.000,00                                    |
| 31 Ocak | Amortisman (bir amortisman dönemine yönelik teklifin kullanılmasıyla oluşturulan) | 966,67Hesaplaması: Defter değeri (59.000 - 1.000 amortisman) / kalan amortisman dönemi sayısı (60) |

#### <a name="reversal-action"></a>Tersine çevirme eylemi

| Tarih      | Hareket türü               | Tutar    |
|-----------|--------------------------------|-----------|
| 1 Ocak | Değer azaltma düzeltmesi iptali | -1.000,00 |

#### <a name="depreciation-effect"></a>Amortisman etkisi

| Tarih        | Hareket türü        | Tutar                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| 28 Şubat | Amortisman (teklif) | 983,62Hesaplaması: Defter değeri (59.000 - 966,67 amortisman) / kalan amortisman dönemi sayısı (59) |

Amortisman 16,95 değeri kadar daha az belirtilir (983,62 - 966,67).



## <a name="additional-resources"></a>Ek kaynaklar

[Sabit kıymet amortismanı](fixed-asset-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
