---
title: QRCODE ER işlevi
description: Bu konu, QRCODE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bac0910d213ee05a2a7a7b218a6714d4f935be16
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916764"
---
# <a name="QRCODE">QRCODE ER işlevi</a>

[!include [banner](../includes/banner.md)]

Bu `QRCODE` işlev, belirtilen dizgi için hızlı yanıt kodu (QR kodu) görüntüsünü ikili biçimde gösteren bir *konteyner* değeri döndürür.

## <a name="syntax"></a>Sözdizimi

```
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

```
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Yapılandırılmış ER biçimini çalıştırdığınızda, modelin **LabelText** alanının metin değerini Bir QR kod görüntüsü oluşturmak için **model.ListOfShelfLabels** veri kaynağı kullanılacak. Bu resim, belge şablonundaki bir QR kodu görüntü yer tutucusunun giden bir belge oluşturmak amacıyla kullanılarak değiştirilmesini sağlar. Oluşturulan belgenin bu görüntüsü tarandığında, **model.ListOfShelfLabels** veri kaynağının **LabelText** alanından alınan metni döndürür. Daha fazla bilgi için [Er kullanarak oluşturduğunuz belgelere resimler ve şekiller katıştırma](electronic-reporting-embed-images-shapes.md)

## <a name="additional-resources"></a>Ek kaynaklar

[Metin işlevleri](er-functions-category-text.md)
