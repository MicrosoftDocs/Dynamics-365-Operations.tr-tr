---
title: Commerce fiyatlandırma API'leri
description: Bu makalede, Microsoft Dynamics 365 Commerce fiyatlandırma altyapısı tarafından sağlanan çeşitli fiyatlandırma API'leri açıklanmaktadır.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2022
ms.locfileid: "9294135"
---
# <a name="commerce-pricing-apis"></a>Commerce fiyatlandırma API'leri

[!include [banner](../includes/banner.md)]

Bu makalede, Microsoft Dynamics 365 Commerce fiyatlandırma altyapısı tarafından sağlanan çeşitli fiyatlandırma API'leri açıklanmaktadır.

Dynamics 365 Commerce fiyatlandırma altyapısı, çeşitli fiyatlandırma senaryolarını desteklemek için harici uygulamalar tarafından kullanılabilen aşağıdaki Retail Server API'lerini sağlar:

- **GetActivePrices** – Bu API, ürünün basit iskontolarıyla birlikte hesaplanan fiyatını alır.
- **CalculateSalesDocument** – Bu API, ürünler birlikte satın alınmışsa belirli miktarlardaki ürünlerin fiyatlarını ve iskontolarını hesaplar.
- **GetAvailablePromotions** – Bu API, sepetteki ürünlerde geçerli iskontoları alır. 
- **AddCoupons** – Bu API bir sepete kuponlar ekler.
- **RemoveCoupons** – Bu API, bir sepetteki kuponları kaldırır.

Dış uygulamalarda Retail Server API'lerinin nasıl kullanıldığı hakkında daha fazla bilgi için bkz. [Dış uygulamalarda Retail Server API'lerini kullanma](dev-itpro/consume-retail-server-api.md).

## <a name="getactiveprices"></a>GetActivePrices

*GetActivePrices* API'si Commerce 10.0.4 sürümünde kullanılmaya başlandı. Bu API, ürünün basit iskontolarıyla birlikte hesaplanan fiyatını alır. Çok satırlı iskontoları hesaplamaz ve bir API isteğindeki her ürünün miktarının 1 olduğunu varsaymaktadır. Bu API ayrıca, giriş olarak ürünlerin bir listesini alabilir ve bireysel ürünlerin fiyatını toplu olarak sorgulayabilir.

*GetActivePrices* API'si, **Çalışan**, **Müşteri**, **Anonim** ve **Uygulama** Commerce rollerini destekler.

*GetActivePrices* API'si için ana kullanım örneği, perakendecilerin geçerli indirimler dahil olmak üzere bir ürünün en iyi fiyatını göstermek istediği ürün ayrıntıları sayfasıdır (PDP).

Aşağıdaki tablo, *GetActivePrices* API'sinin giriş parametrelerini gösterir.

| Adı                                    | Alt ad | Türü | Gerekli/İsteğe bağlı | Açıklama |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | Gerekli | |
|                                         | ChannelId | uzun | Gerekli | |
|                                         | CatalogId | uzun | Gerekli | |
| productIds                              | | IEnumerable\<long\> | Gerekli | Fiyatların hesaplanacağı ürünlerin listesi. |
| activeDate                              | | DateTimeOffset | Gerekli | Fiyatların hesaplandığı tarih. |
| customerId                              | | dize | İsteğe bağlı | Müşteri hesap numarası. |
| affiliationLoyaltyTiers                 | | IEnumerable\<AffiliationLoyaltyTier\> | İsteğe bağlı | İlişki ve bağlılık programı katmanları. |
|                                         | AffiliationId | uzun | Gerekli | İlişki kimliği. |
|                                         | LoyaltyTierId | uzun | İsteğe bağlı | Bağlılık programı katman kimliği. |
| includeSimpleDiscountsInContextualPrice | | bool | İsteğe bağlı | Fiyatlandırma hesaplamasına basit iskontolar eklemek için bu parametreyi **true** olarak ayarlayın. Varsayılan değer **yanlış** değeridir. |
| includeVariantPriceRange                | | bool | İsteğe bağlı | Bir ana ürünün tüm türevleri arasında minimum ve maksimum fiyatları elde etmek için bu parametreyi **true** olarak ayarlayın. Varsayılan değer **yanlış** değeridir. |
| includeAttainablePricesAndDiscounts     | | bool | İsteğe bağlı | Mümkün olan fiyat ve indirimleri elde etmek için bu parametreyi **true** olarak ayarlayın. Varsayılan değer **yanlış** değeridir. |

**Örnek istek gövdesi**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Örnek yanıt gövdesi**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>CalculateSalesDocument

*CalculateSalesDocument* API'si Commerce 10.0.25 sürümünde kullanılmaya başlandı. Bu API, ürünler bir siparişte birlikte satın alınmışsa belirli miktarlardaki ürünlerin fiyatlarını ve iskontolarını hesaplar. *CalculateSalesDocument* API'sinin arkasındaki fiyatlandırma hesaplaması, tek satırlı iskontoları ve çoklu satır iskontolarını dikkate alır.

*CalculateSalesDocument* API'si için ana kullanım örneği, tam alışveriş sepeti bağlamının kalıcı olmadığı senaryolardaki (örneğin satış teklifleri) fiyatlandırma hesaplamasıdır. Satış noktası (POS) ve Commerce e-ticaretteki senaryolar da bu kullanım durumundan yararlanabilir. Sepet öğeleri bir küme olarak hesaplandığında (örneğin, ayrı paketler, bağlantılı veya önerilen ürünler veya sepete eklenmiş olan ürünler için), daha düşük bir toplam fiyat müşterileri alışveriş sepetine ürün eklemeye ikna edebilir.

*CalculateSalesDocument* API'sinin hem isteği hem de yanıtı için veri modeli **Alışveriş Sepeti**'dir. Ancak, bu API'nin bağlamında veri modeli, **SalesDocument** olarak adlandırılır. Özelliklerin çoğu isteğe bağlı olduğundan ve yalnızca birkaçı fiyatlandırma hesaplamasını etkiliyorsa, aşağıdaki tabloda yalnızca fiyatlandırma ile ilgili alanlar gösterilir. Diğer alanların API isteğinde yer almasını önermeyiz.

*CalculateSalesDocument* API'sinin kapsamı yalnızca fiyat ve iskontoların hesaplanmasında kullanılır. Vergiler ve ücretler dahil edilmez.

Aşağıdaki tablo, **SalesDocument** adlı nesne içindeki giriş parametrelerini gösterir.

| Adı             | Alt ad | Türü | Gerekli/İsteğe bağlı | Açıklama |
|------------------|----------|------|-------------------|-------------|
| Kimlik               | | dize | Gerekli | Satış belgesinin tanımlayıcısı. |
| CartLines        | | IList\<CartLine\> | İsteğe bağlı | Fiyatların ve iskontoların hesaplanacağı satırların listesi. |
|                  | Ürün Kimliği | uzun | CartLine'ın kapsamında gereklidir | Ürün kayıt kodu. |
|                  | ItemId | dize | İsteğe bağlı | Öğe tanımlayıcısı. Bir değer sağlanmışsa, bu değerin **ProductID** parametresi ile eşleşmesi gerekir. |
|                  | InventoryDimensionId | dize | İsteğe bağlı | Stok boyutu tanımlayıcısı. Bir değer sağlanmışsa, **ItemId** ve **InventoryDimensionId** değerleri birleşimi **ProductId** parametresinin değeriyle eşleşmelidir. |
|                  | Miktar | ondalık | CartLine'ın kapsamında gereklidir | Ürünün miktarı. |
|                  | UnitOfMeasureSymbol | dize | İsteğe bağlı | Ürünün birimi. Varsayılan olarak, bir değer sağlanmamışsa API, ürünün satış birimini kullanır. |
| CustomerId       | | dize | İsteğe bağlı | Müşteri hesap numarası. |
| LoyaltyCardId    | | dize | İsteğe bağlı | Bağlılık programı kartı tanımlayıcısı. Bağlılık programı kartıyla ilişkilendirilmiş herhangi bir müşteri hesabının, **CustomerID** parametresi değeriyle (sağlanmışsa) eşleşmesi gerekir. Bağlılık programı kartı bulunamazsa veya durumu **Engellendi** ise dikkate alınmayacaktır. |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | İsteğe bağlı | İlişki bağlılık programı katman satırları. **CustomerId** ve/veya **LoyaltyCardId** değerleri sağlanmışsa, karşılık gelen ilişki bağlılık programı katman satırları **AffiliationLines** değerinde sağlanan satırlarla birleştirilir. |
|                  | AffiliationId | uzun | AffiliationLoyaltyTier'ın kapsamında gereklidir | İlişki kayıt kimliği. |
|                  | LoyaltyTierId | uzun | AffiliationLoyaltyTier'ın kapsamında gereklidir | Bağlılık programı katman kayıt kimliği. |
|                  | AffiliationTypeValue | int | AffiliationLoyaltyTier'ın kapsamında gereklidir | İlişki satırının **Genel** türü (**0**) veya **Bağlılık programı** türünde (**1**) olduğunu belirten bir değer. Bu parametre **0** olarak ayarlanırsa API, tanımlayıcı olarak **AffiliationId** değerini alır ve **LoyaltyTierId** değerini yoksayar. **1** olarak ayarlanırsa API, tanımlayıcı olarak **LoyaltyTierId** değerini alır ve **AffiliationId** değerini yoksayar. |
|                  | ReasonCodeLines | Koleksiyon\<ReasonCodeLine\> | AffiliationLoyaltyTier'ın kapsamında gereklidir | Neden kodu satırları. Bu parametrenin fiyatlandırma hesaplaması üzerinde etkisi yoktur, ancak **AffiliationLoyaltyTier** nesnesinin bir parçası olarak gereklidir. |
|                  | CustomerId | dize | AffiliationLoyaltyTier'ın kapsamında gereklidir | Müşteri hesap numarası. |
| Kuponlar          | | IList\<Coupon\> | İsteğe bağlı | Uygulanamaz (etkin değil, süresi dolmuş veya bulunamadı) olan kuponlar, fiyatlandırma hesaplamasında dikkate alınmayacak. |
|                  | Kod | dize | Kupon kapsamında gereklidir | Kupon kodu. |
|                  | CodeId | dize | İsteğe bağlı | Kupon kodu tanımlayıcısı. Bir değer sağlanmışsa, bu değerin **Code** parametresi ile eşleşmesi gerekir. |
|                  | DiscountOfferId | dize | İsteğe bağlı | İskonto tanımlayıcısı. Bir değer sağlanmışsa, bu değerin **Code** parametresi ile eşleşmesi gerekir. |

**Örnek istek gövdesi**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Tüm alışveriş sepeti nesnesi, yanıt gövdesi olarak döndürülür. Fiyatları ve iskontoları denetlemek için, aşağıdaki tabloda yer alan alanlara odaklanmanız gerekir.

| Adı           | Alt ad | Türü | Açıklama |
|----------------|----------|------|--------------|
| NetPrice       | | ondalık | İndirimler uygulanmadan önceki tüm satış belgesi net fiyatı. |
| DiscountAmount | | ondalık | Tüm satış belgesinin toplam iskonto tutarı. |
| TotalAmount    | | ondalık | Tüm satış belgesinin toplam tutarı. |
| CartLines      | | IList\<CartLine\> | Fiyat ve iskonto ayrıntılarını içeren hesaplanmış satırlar. |
|                | Fiyat | ondalık | Ürünün birim fiyatı. |
|                | NetPrice | ondalık | İndirimler uygulanmadan önce satırın net fiyatı (= *Fiyat* &times; *Tutar*). |
|                | DiscountAmount | ondalık | İndirim tutarı. |
|                | TotalAmount | ondalık | Satırın nihai toplam fiyatlandırma sonucu. |
|                | PriceLines | IList\<PriceLine\> | Fiyat kaynağı (temel fiyat, fiyat ayarlaması veya ticari anlaşma) ve tutar dahil olmak üzere fiyat detayları. |
|                | DiscountLines | IList\<DiscountLine\> | İskonto ayrıntıları. |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

Birçok sepet satırı bulunan bir sepet verildiğinde, *GetAvailablePromotions* API'si sepet satırlarının tüm geçerli iskontolarını döndürür. 

*GetAvailablePromotions* API'si için ana kullanım örneği, perakendecilerin geçerli alışveriş sepetine yönelik uygulanan indirimleri veya kullanılabilir kuponları sergiledikleri bir alışveriş sepeti sayfasıdır.

Aşağıdaki tablo, *GetAvailablePromotions* API'sinin giriş parametrelerini gösterir.

| Adı        | Türü | Gerekli/İsteğe bağlı | Açıklama |
|-------------|------|-------------------|-------------|
| anahtar         | dize | Gerekli | Alışveriş sepeti kodu. |
| cartLineIds | IEnumerable\<string\> | İsteğe bağlı | Bu parametreyi yalnızca seçili sepet satırları için iskontoları iade etmek üzere ayarlayın. |

**Örnek yanıt gövdesi**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

*AddCoupons* API'si bir sepete bir kupon listesi eklemeyi destekler. Bu, kuponlar eklendikten sonra sepet nesnesini döndürür.

Aşağıdaki tablo, *AddCoupons* API'sinin giriş parametrelerini gösterir.

| Adı                 | Türü | Gerekli/İsteğe bağlı | Açıklama |
|----------------------|------|-------------------|-------------|
| anahtar                  | dize | Gerekli | Alışveriş sepeti kodu. |
| couponCodes          | IEnumerable\<string\> | Gerekli | Alışveriş sepetine eklenecek kupon kodları. |
| isLegacyDiscountCode | bool | İsteğe bağlı | Kuponun eski bir iskonto kodu olduğunu belirtmek için bu parametreyi **true** olarak ayarlayın. Varsayılan değer **yanlış** değeridir. |

## <a name="removecoupons"></a>RemoveCoupons

*RemoveCoupons* API'si bir sepetten bir kupon listesini kaldırmayı destekler. Bu, kuponlar kaldırıldıktan sonra sepet nesnesini döndürür.

Aşağıdaki tablo, *RemoveCoupons* API'sinin giriş parametrelerini gösterir.

| Adı        | Türü | Gerekli/İsteğe bağlı | Açıklama |
|-------------|------|-------------------|-------------|
| anahtar         | dize | Gerekli | Alışveriş sepeti kodu. |
| couponCodes | IEnumerable\<string\> | Gerekli | Alışveriş sepetinden kaldırılacak kupon kodları. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
