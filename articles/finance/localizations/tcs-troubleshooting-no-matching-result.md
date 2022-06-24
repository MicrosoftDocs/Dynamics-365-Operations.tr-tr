---
title: Eşleşen sonuç bulunamadı
description: Bu makale, Vergi Hesaplama hizmetinin "Eşleşen sonuç bulunamadı" hatasının nasıl düzeltileceğini açıklamaktadır.
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
ms.openlocfilehash: d3bbc76741fdd018d1b2987538b8de7f6d92ee53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845158"
---
# <a name="no-matching-result-could-be-found"></a>Eşleşen sonuç bulunamadı

[!include [banner](../includes/banner.md)]

Bu makale, Vergi Hesaplama hizmetinde "Eşleşen sonuç bulunamadı" hatasını aldığınızda atacağınız adımları açıklamaktadır.

## <a name="symptom"></a>Belirti

Şu hata iletisini alırsınız: "Başlık/Satırlar - 1, Veri grubu, eşleşen sonuç bulunamadı."

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
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
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

Sorun, Regulatory Configuration Service'deki (RCS) özellik kurulumu yanlış olduğunda oluşur.

## <a name="troubleshoot"></a>Sorun giderme

1. Sorun giderme dosyasını karşıdan yükleyin. Daha fazla bilgi için bkz. [Sorun giderme için hata ayıklama modunu etkinleştirme](tcs-troubleshooting-enable-debug-mode.md).
2. Kurulum sorununu gidermek için Vergi servis hesaplama girişini Özellik kurulumuyla karşılaştırın.

    Aşağıdaki örnek Vergi servis hesaplama girişini gösterir.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    Aşağıdaki tablo, RCS'deki vergi grubu uygulanabilirliğini listeler.

    | Header.Business işlemi | Lines.Business Birimi | Header.Ship Kaynak Posta Kodu | Vergi Grubu |
    |-------------------------|---------------------|---------------------------|-----------|
    | Günlük                 |                     |                           | Grup A   |
    | Satış                   |                     | 30160                     | Grup B   |

    Vergi servis hesaplama girişine göre, başlıktaki **İş Süreci** değeri **Satışlar** ve başlıktaki **Sevk Yeri Posta Kodu** değeri **30159**'dur. Bu giriş, RCS'deki uygulanabilirlik kurallarının kurulumuna dayanır. Eşleşen bir satır olmadığından, hata oluşur.

    > [!NOTE]
    > Uygulanabilirlik kuralındaki değer boşsa, kural her bir değere uygulanabilir.

## <a name="mitigation"></a>Risk azaltma

Hatayı azaltmak için aşağıdaki adımları izleyin.

1. RCS'de, **Genelleştirme özellikleri** \> **Vergi hesaplama**'ya gidin.
2. Özelliğin yeni bir sürümünü oluşturun.
3. İlgili bilgiler için bir satır ekleyin.

    | Header.Business işlemi | Lines.Business Birimi | Header.Ship Kaynak Posta Kodu| Vergi Grubu |
    |-------------------------|---------------------|--------------------------|-----------|
    | Günlük                 |                     |                          | Grup A   |
    | Satış                   |                     | 30160                    | Grup B   |
    | Satış                   |                     | 30159                    | Grup B   |

4. Özellik kurulum sürümünü yayımlayın.
5. Microsoft Dynamics 365 Finance'te, **Vergi** \> **Kurulum** \> **Vergi yapılandırması** \> **Vergi hesaplama parametreleri**'ne gidin ve yeni sürümü seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
