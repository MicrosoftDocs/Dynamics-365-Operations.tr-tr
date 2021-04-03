---
title: GETENUMVALUEBYNAME işlevi
description: Bu konu, GETENUMVALUEBYNAME Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bfc173130a9fc57385826f77443ec28946ef68fd
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570602"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME işlevi

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME` işlevi, belirtilen numaralandırma veri kaynağındaki belirli bir *Enum* değerini *dize* değeri olarak belirtilen numaralandırma adını kullanarak arar. *Numaralama* değeri bulunursa, işlev bunu döndürür. Aksi durumda, işlev **boş** numaralandırma değerini döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`enumeration data source path`: *numaralandırması*

Aşağıdaki sabit listesi tiplerinden birinin veri kaynağının geçerli yolu:

- Elektronik raporlama (ER) model numaralandırması
- ER biçim numaralandırma
- Microsoft Dynamics 365 Finance numaralandırması

`enumeration value text`: *Dize*

Tek bir numaralandırma değerinin adını gösteren bir dize değeri.

## <a name="return-values"></a>Dönüş değerleri

Boş giriş yapılabilir *Enum*

Sonuç numaralandırma değeri.

## <a name="usage-notes"></a>Kullanım notları

Bir *dize* değeri olarak belirtilen numaralandırma değerinin adı kullanılarak bir *Enum* değeri bulunamazsa, hiçbir özel durum atılır.

## <a name="example-1"></a>Örnek 1

Aşağıdaki örnekte, bir veri modelinde oluşturulan **ReportDirection** numaralandırması gösterilmektedir. Etiketlerin numaralandırma değerleri ile tanımlandığını unutmayın.

![Veri modeli numaralandırması için kullanılabilir değerler](./media/ER-data-model-enumeration-values.PNG)

Aşağıdaki örnek ayrıntıları göstermektedir:

- **$Direction** veri kaynağı bir er raporu içinde konfigüre edilmiş. Bu veri kaynağı **RaporYönü** modeli sabit listesi temel alınarak yapılandırıldı.
- Bu işlevin parametresi olarak model numaralandırmaya dayalı **$Direction** veri kaynağı kullanmak için tasarlanan `$IsArrivals` ifadesi.
- Bu karşılaştırma ifadenin değeri **DOĞRU**'dur.

![Veri modeli numaralandırması örneği](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>Örnek 2

`GETENUMVALUEBYNAME` ve [`LISTOFFIELDS`](er-functions-list-listoffields.md) işlevleri, desteklenen numaralandırmalar değerlerini ve etiketlerini metin değerleri olarak getirir. (Desteklenen numaralandırmalar uygulama numaralandırmalar, veri modeli numaralandırmaları ve biçim numaralandırmalarıdır.)

Aşağıdaki örnekte, bir model eşlemesinde oluşturulan **TransType** veri kaynağı gösterilmektedir. Bu veri kaynağı **LedgerTransType** uygulama numaralandırması anlamına gelir.

![Uygulama numaralandırmasına başvuran model eşlemesinin veri kaynağı](./media/er-functions-text-getenumvaluebyname-example2-1.png)

Aşağıdaki resim, bir model eşlemesinde yapılandırılan **TransTypeList** veri kaynağını göstermektedir. Bu veri kaynağı **TransType** uygulama numaralandırması temel alınarak yapılandırıldı. `LISTOFFIELDS` işlevi, alan içeren kayıtların listesi olarak tüm numaralandırma değerlerini döndürmek için kullanılır. Bu şekilde, her numaralandırma değerinin ayrıntıları gösterilir.

> [!NOTE]
> **EnumValue** alanı, `GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` ifadesi kullanılarak **TranstTypeList** veri kaynağı için yapılandırılır. Bu alan, bu listedeki her kayıt için bir numaralandırma değeri döndürür.

![Seçilen bir numaralandırmanın tüm numaralandırma değerlerini kayıt listesi olarak döndüren model eşleme veri kaynağı](./media/er-functions-text-getenumvaluebyname-example2-2.png)

Aşağıdaki resim, bir model eşlemesinde yapılandırılan **VendTrans** veri kaynağını göstermektedir. Bu veri kaynağı, **VendTrans** uygulama tablosundaki satıcı hareket kayıtlarını döndürür. Her hareketin genel muhasebe türü, **TransType** alanının değeriyle tanımlanır.

> [!NOTE]
> **TransTypeTitle** alanı, `FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` ifadesi kullanılarak **VendTrans** veri kaynağı için yapılandırılır. Bu numaralandırma değeri kullanılabilir ise, bu alan geçerli hareketin numaralandırma değerinin etiketini metin olarak döndürür. Aksi halde, boş bir dize değeri döndürür.
>
> **TransTypeTitle** alanı, veri modelini veri kaynağı olarak kullanan her ER biçiminde bu bilginin kullanılmasına olanak sağlayan bir veri modelinin **LedgerType** alanına bağlıdır.

![Satıcı hareketlerini döndüren model eşlemesinin veri kaynağı](./media/er-functions-text-getenumvaluebyname-example2-3.png)

Aşağıdaki şekil, yapılandırılmış model eşlemesini test etmek için [veri kaynağı hata ayıklayıcısını](er-debug-data-sources.md) nasıl kullanabileceğinizi gösterir.

![Yapılandırılan model eşlemesini test etmek için veri kaynağı hata ayıklayıcısını kullanma](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

Bir veri modelinin **LedgerType** alanı, hareket türlerinin etiketlerini beklendiği gibi gösterir.

Bu yaklaşımı büyük miktarda hareket verisi için kullanmayı planlıyorsanız, yürütme performansını dikkate almanız gerekir. Daha fazla bilgi için, bkz. [Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)

[Performans sorunlarını gidermek için ER biçimlerinin yürütülmesini izleme](trace-execution-er-troubleshoot-perf.md)

[LISTOFFIELDS ER işlevi](er-functions-list-listoffields.md)

[FIRSTORNULL ER işlevi](er-functions-list-firstornull.md)

[WHERE ER işlevi](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]