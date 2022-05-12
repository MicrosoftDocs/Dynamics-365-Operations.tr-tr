---
title: Vergi kodu belirlenemiyor
description: Bu konu, Vergi Hesaplama hizmetinin "Vergi kodu belirlenemedi" hatasının nasıl düzeltileceğini açıklamaktadır.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 3c0914f0013ad2de61cd5a59e3092fef149742e4
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2022
ms.locfileid: "8645438"
---
# <a name="tax-code-cannot-be-determined"></a>Vergi kodu belirlenemiyor

[!include [banner](../includes/banner.md)]

Bu konu, Vergi Hesaplama hizmetinde "Vergi kodu belirlenemedi" hatasını aldığınızda atacağınız adımları açıklamaktadır.

## <a name="symptom"></a>Belirti

Aşağıdaki hata iletisini alırsınız: "Başlık/Satırlar - 1, vergi kodu belirlenemiyor." Alternatif olarak, aşağıdaki örnekte gösterildiği gibi, hata giderme dosyasında bulabilirsiniz. Daha fazla bilgi için bkz. [Sorun giderme için hata ayıklama modunu etkinleştirme](tcs-troubleshooting-enable-debug-mode.md).

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Nedeni

Bu sorun büyük olasılıkla vergi grubu ve madde vergi grubu kesişmediği için ortaya kaynaklanmaktadır.

## <a name="troubleshoot"></a>Sorun giderme

Sorunu düzeltmek için şu adımları izleyin.

1. Sorun giderme dosyasında, vergi grubunun ve madde vergi grubunun belirlendiğini doğrulayın. **Vergi Grubu** ve **Madde Vergi Grubu** değerleri boşsa, vergi grubu ve madde vergi grubu belirlenmemiştir. Belirlendikleri takdirde, sonuçlar yanlış olabilir.

    Sorun giderme dosyası örneği burada verilmiştir.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
                            "Adjustment": null
                        }
                    ],
                    "Measures": {
                        ...
                    },
                    ...
                }
            ]
        },
        ...
    }
    ```

2. Satış siparişi satırı ayrıntılarının **Kurulum** sekmesindeki **Satış vergisini geçersiz kıl** seçeneğinin etkinleştirildiğini doğrulayın.

    - Vergi kodları etkinleştirildiğinde, hareket satırına girdiğiniz **Vergi grubu** ve **Madde vergi grubu** değerlerine göre belirlenir. Bu değerlerin doğru girildiğini doğrulayın.
    - Etkin değilse, **Vergi grubu uygulanabilirlik** ve **Madde vergi grubu uygulanabilirlik** alanları için doğru değerlerin ayarlandığını doğrulayın. Daha fazla bilgi için, bkz. [Eşleşen sonuç bulunamadı](tcs-troubleshooting-no-matching-result.md).

3. Vergi grubu ve madde vergi grubu doğru olarak belirlenirse, kesişimin olup olmadığını belirleyin.

    1. RCS'de; **Vergi özellikleri** \> **Vergi kodları ve grupları** \> **Vergi grubu**'na gidin.

        | Line.Tax Grubu | Vergi Kodları |
        |----------------|-----------|
        | Grup A        | A         |

    2. **Vergi özellikleri** \> **Vergi kodları ve grupları** \> **Madde vergi grubu**'na gidin.

        | Line.Item Vergi Grubu | Vergi Kodları |
        |---------------------|-----------|
        | Grup B             | B:         |

    Vergi grubu ve madde vergi grubu için bir kesişim yoksa, vergi kodu belirlenmeyecektir.

## <a name="mitigation"></a>Risk azaltma

1. Bu konunun [Sorun giderme](#troubleshoot) bölümündeki her adımı izleyin ve kurulumu gerektiği gibi düzeltin. Vergi grubu ve madde vergisi grubu doğru saptanmadı ise bkz. [Eşleşen sonuç bulunamadı](tcs-troubleshooting-no-matching-result.md).
2. Vergi grubu ve madde vergi grubu için kesişim yoksa, RCS'de yeni bir özellik sürümü oluşturun ve kurulumu düzeltin.

    - **Vergi özellikleri** \> **Vergi kodları ve grupları** >  **Madde vergi grubu**'na gidin.

        | Line.Item Vergi Grubu | Vergi kodları |
        |---------------------|-----------|
        | Grup B             | A;B       |

    Vergi kodu **A** belirlenecek.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
