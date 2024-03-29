---
title: GETLABELTEXT ER işlevi
description: Bu makalede, GETLABELTEXT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: dad87548518b77f2def1cf2383a21607f45170e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285954"
---
# <a name="getlabeltext-er-function"></a>GETLABELTEXT ER işlevi

[!include [banner](../includes/banner.md)]

`GETLABELTEXT` işlevi, belirtilen bir etiketin belirtilen dilde çevirisini temsil eden bir *[Dize](er-formula-supported-data-types-primitive.md#string)* değeri döndürmek için belirli bir etiketi arar.

## <a name="syntax"></a>Sözdizimi

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Bağımsız değişkenler

### <a name="label-id"></a>Etiket kodu

`label id`: *Dize* veya *Etiket Kimliği*

Aşağıdaki etiket türlerinden birinin geçerli kimliği:

- [Elektronik raporlama (ER)](general-electronic-reporting.md) etiketi
- Microsoft Dynamics 365 Finance etiketi

#### <a name="usage-notes"></a>Kullanım notları

Bu bağımsız değişken, aşağıdaki desteklenen desenlerden biri kullanılarak yalnızca sabit olarak tanımlanabilir:

- ER etiketleri için:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Finance etiketleri için:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> Tasarım zamanında, sağlanan etiket kimliği kullanılarak etiket bulunamazsa **[Formül tasarımcısı](er-advanced-formula-editor.md)** sayfasında bir doğrulama hata iletisi gösterilir.

### <a name="language"></a>Dil

`language`: *Dize*

Dil kodunu temsil eden dize.

#### <a name="usage-notes"></a>Kullanım notları

Bu bağımsız değişken metin sabiti olarak veya *Dize* değeri döndüren bir veri kaynağı alanının yolu olarak tanımlanabilir.

> [!NOTE]
> Tasarım zamanında, metin sabiti olarak tanımlandığında sağlanan `language` bağımsız değişkeni kullanılarak dil kodu bulunamazsa doğrulama hata iletisi gösterilir.
>
> Çalışma zamanında, sağlanan `language` bağımsız değişkeni kullanılarak dil kodu bulunamazsa belirtilen bir etiket için `EN-US` sistem dilinin çevirisi döndürülür.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="example-1-system-label"></a><a name=example-1></a>Örnek 1: Sistem etiketi

`GETLABELTEXT (@"SYS70894", "en-us")` ve `GETLABELTEXT ("SYS70894", "en-us")` ifadeleri, `@SYS70894`uygulama etiketi için İngilizce çeviri "Nothing to print" döndürür.

## <a name="example-2-er-label"></a><a name=example-2></a>Örnek 2: ER etiketi

**ISO20022 Kredi transferi (DE)** yapılandırmasından [türetilen](er-quick-start2-customize-report.md#DeriveProvidedFormat) bir ER [yapılandırmasını](general-electronic-reporting.md#Configuration) düzenlemeye başladığınızda, *[Hesaplanan alan](er-calculated-field-ds-performance.md)* türünde yeni bir veri kaynağı girin ve bu veri kaynağının `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` ifadesini yapılandırın. Bu durumda, çalışma zamanında veri kaynağı, başlangıçta temel **ISO20022 Kredi transferi (DE)** ER yapılandırmasında yapılandırılan `@GER_LABEL:VendorName` ER etiketi için Almanca çeviri "Kreditorenname" döndürür.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)

[Elektronik raporlamada çok dilli raporlar tasarlama](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
