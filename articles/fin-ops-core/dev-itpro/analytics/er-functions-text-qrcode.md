---
title: QRCODE ER işlevi
description: Bu makalede, QRCODE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 9de62eefb82942ccc72e81bd9bf36eed07c99dba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287203"
---
# <a name="qrcode-er-function"></a>QRCODE ER işlevi

[!include [banner](../includes/banner.md)]

Bu `QRCODE` işlev, belirtilen dizgi için hızlı yanıt kodu (QR kodu) görüntüsünü ikili biçimde gösteren bir *konteyner* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```vb
QRCODE (text)
```

## <a name="arguments"></a>Bağımsız değişkenler

`text`: *Dize*

Orijinal metni temsil eden bir *dize* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Kapsayıcı*

Sonuçta elde edilen ikili akış.

## <a name="example"></a>Örnek

Bir elektronik raporlama (ER) biçimini, önceden tanımlanmış bir şablonu kullanarak bir giden belgeyi Microsoft Office biçiminde (Excel çalışma kitapları veya Word belgeleri) oluşturmak için yapılandırabilirsiniz. Bu şablon bir QR kodu görüntüsü için yer tutucu olarak bir **resim** nesnesi (Excel çalışma kitabı) veya bir **resim içeriği denetimi** (Word belgesi) içeriyor olabilir. Yapılandırılan ER'ye bu yer tutucuyu doldurmak için kullanılacak bir **hücre** öğesi biçimini yapılandırılmış bir şekilde eklemeniz gerekir. Bir QR kodunda depolanacak bilgileri belirtmek için, bu **hücre** öğesi için bir bağlama tanımlamanız gerekir. Örneğin, bu bağlamayı aşağıdaki ifadeyi içerecek biçimde yapılandırabilirsiniz:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Yapılandırılmış ER biçimini çalıştırdığınızda, modelin **LabelText** alanının metin değerini Bir QR kod görüntüsü oluşturmak için **model.ListOfShelfLabels** veri kaynağı kullanılacak. Bu resim, belge şablonundaki bir QR kodu görüntü yer tutucusunun giden bir belge oluşturmak amacıyla kullanılarak değiştirilmesini sağlar. Oluşturulan belgenin bu görüntüsü tarandığında, **model.ListOfShelfLabels** veri kaynağının **LabelText** alanından alınan metni döndürür. Daha fazla bilgi için [Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
