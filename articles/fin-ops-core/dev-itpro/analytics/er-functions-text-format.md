---
title: FORMAT ER işlevi
description: Bu makalede, FORMAT Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: a7eb3d4a4c72e8faf40d28a724cda5ba7d7e8a47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286014"
---
# <a name="format-er-function"></a>FORMAT ER işlevi

[!include [banner](../includes/banner.md)]

`FORMAT` işlevi, belirtilen dizeyi, tüm **%N** oluşumlarını *N*'ci bağımsız değişken ile değiştirerek biçimlendirdikten sonra *Dize* değeri olarak döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>Bağımsız değişkenler

`string`: *Dize*

Biçimlendirilecek *Dize* veri türünün veri kaynağına yönelik referans. Bu bağımsız değişken gereklidir.

`argument 1`: *Dize*

**%1** oluşumlarını değiştirmek için kullanılan ilk bağımsız değişken. Bu bağımsız değişken gereklidir.

`argument N`: *Dize*

**%2**, **%3** vb. oluşumlarını değiştirmek için kullanılan *N*'ci bağımsız değişken. Bu ek bağımsız değişkenler isteğe bağlıdır.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

Bir parametre için bir bağımsız değişken sağlanmamışsa, parametre izede **"%N"** olarak döndürülür. *Gerçek* türün değerleri için, varsayılan dize dönüşümü iki ondalık basamakla sınırlıdır.

## <a name="example"></a>Örnek

Aşağıdaki çizimde, **ÖdemeModeli** veri kaynağı **müşteri** bileşenini kullanarak müşteri kayıtları listesini döndürür. Bu, **İşlemTarihi** alanını kullanarak işlem tarihi değerini döndürür.

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

Seçilen müşteriler için elektronik dosya oluşturmak üzere tasarlanmış elektronik raporlama (ER) biçiminde veri kaynağı olarak **PaymentModel** seçilir ve işlem akışını denetler. Seçilmiş bir müşteri raporun işlendiği tarihte durdurulmuşsa, kullanıcıyı bilgilendirmek için bir özel durum oluşturulur. Bu tür bir işleme denetimi için tasarlanmış formül aşağıdaki kaynakları kullanabilir:

- Aşağıdaki metine sahip SYS70894 etiketi:

    - **TR-TR dili için:** "Yazdırılacak hiçbir şey yok"
    - **DE dili için** "Nichts zu drucken"

- Aşağıdaki metine sahip SYS18389 etiketi:

    - **TR-TR dili için:** "Müşteri %1 şunun için durduruldu: %2."
    - **DE dili için:** "Debitor '%1' wird für %2 gesperrt."

Tasarlanabilen ifade şudur:

```vb
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

Rapor **Litware Retail** müşterisi için Aralık 17, 2015 tarihinde **EN-US** kültüründe ve **EN-US** dilinde işlenmişse bu formül son kullanıcıya özel durum iletisi olarak sunulabilecek aşağıdaki metni içerir:

*Yazdırılacak birşey yok. Müşteri Litware perakende 17/12/2015 için durduruldu.*

Aynı rapor **Litware Retail** müşterisi için Aralık 17, 2015 tarihinde **DE** kültürü ve **DE** dilinde işlenmişse, formül başka bir tarih biçimini kullanan aşağıdaki metni döndürür:

*Nichts zu drucken. Debitor 'Litware Retail' wird für 17.12.2015 gesperrt.*

>[!NOTE]
> Aşağıdaki sözdizimi, etiketler için ER formüllerinde kullanılır:
>
> - **Microsoft Dynamics 365 Finance uygulamasındaki kaynaklardan etiketler için**: **\@X** (burada **X**, Uygulama Nesne Ağacı (AOT) etiket kimliğidir)
> - **ER yapılandırmaları içinde bulunan etiketler için:** **@"GER_LABEL:X"**, burada **X**, ER yapılandırma etiket kimliğidir.

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
