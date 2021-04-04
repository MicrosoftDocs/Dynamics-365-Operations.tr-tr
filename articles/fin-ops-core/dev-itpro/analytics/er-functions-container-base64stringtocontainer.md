---
title: Base64StringToContainer ER işlevi
description: Bu konu, Base64StringToContainer Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 612590dacc1887b87677c12eddaef42660a7a154
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561554"
---
# <a name="base64stringtocontainer-er-function"></a>Base64StringToContainer ER işlevi

[!include [banner](../includes/banner.md)]

`BASE64STRINGTOCONTAINER` [işlevi](er-formula-language.md#functions), belirtilen *Dize* veri türündeki girişi *[Konteyner](er-functions-category-container.md)* türünde bir veri öğesine dönüştürür.

## <a name="syntax"></a>Sözdizimi

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a>Bağımsız değişkenler

`input`: *Dize*

*Dize* türünün veri kaynağının geçerli yolu.

## <a name="return-values"></a>Dönüş değerleri

*Konteyner*

Sonuçta elde edilen ikili büyük nesne (BLOB) biçimindeki ikili değer.

## <a name="usage-notes"></a>Kullanım notları

Giriş dizesi doğru bir Base64 ikili değerden metne kodlama şeması grubu sağlamazsa Parametre geçerli değil özel durumu oluşur.

## <a name="example"></a>Örnek

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlayın:

- **DocuTypeGroup** uygulama numaralandırmasına başvuran *Dynamics 365 for Operations / Numaralandırma* türündeki kök **DocuTypeGroupEnum** veri kaynağı
- **CustTable** uygulama tablosuna başvuran *Dynamics 365 for Operations / Tablo kayıtları* türünün kök **Müşteri** veri kaynağı
- Aşağıdaki şekilde yapılandırılan *Hesaplanmış alan* türünün **\#Ortam** veri kaynağı:

    - **Müşteri** veri kaynağının alt veri kaynağı olarak eklenmiştir.
    - `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)` ifadesini içerir.

- Aşağıdaki şekilde yapılandırılan *Hesaplanmış alan* türünün **\#MediaAsBase64String** veri kaynağı:

    - **Customer.'\#Media'** veri kaynağının alt veri kaynağı olarak eklenmiştir.
    - `Customer.'#Media'.'getFileContentAsBase64String()'` ifadesini içerir.

- Aşağıdaki şekilde yapılandırılan *Hesaplanmış alan* türünün **\#BlobFomBase64** veri kaynağı:

    - **Customer.'\#Media'** veri kaynağının alt veri kaynağı olarak eklenmiştir.
    - `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'` ifadesini içerir.

Bu örnekte, **\#MediaAsBase64String** veri kaynağı, geçerli ortam ekinin ikili içeriğini Base64 ikili değerden metne kodlama şeması grubunu temsil eden bir metin olarak kodlar. **\#BlobFomBase64** veri kaynağı Base64 dizesinin kodunu çözer ve BLOB biçiminde bir ikili değer döndürür.

![ER Model eşleme tasarımcı sayfasındaki örnek veri kaynakları](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Konteyner işlevleri](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]