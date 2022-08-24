---
title: NUMSEQVALUE ER işlevi
description: Bu makalede, NUMSEQVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlanmaktadır.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 62255f0a47d3c67468cf2cf3922a1886c29c03d6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271568"
---
# <a name="numseqvalue-er-function"></a>NUMSEQVALUE ER işlevi

[!include [banner](../includes/banner.md)]

`NUMSEQVALUE` işlev, belirtilen numara serisi, kapsam ve kapsam kimliğine dayalı olarak bir numara serisinin yeni oluşturulan değerini gösteren bir *dize* değeri döndürür. Kapsam kimliği, Elektronik raporlama (ER) biçiminin altında çalıştırıldığı içerikle sağlanan şirket koduna eşittir.

## <a name="syntax-1"></a>Sözdizimi 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Sözdizimi 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Sözdizimi 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>Bağımsız değişkenler

`number sequence code`: *Dize*

Yeni bir değerin gerekli olduğu numara serisinin kodunu temsil eden bir metin değeri.

`number sequence record ID`: *Int64*

NumberSequenceTable tablosundaki bir kaydın, yeni bir değerin gerekli olduğu numara SERISININ tanımını içeren kayıt kodunu temsil eden bir *Int64* değeri.

`scope type`: *Numaralandırma değeri*

Yeni bir değerin gerekli olduğu numara serisinin kapsamını tanımlayan **ERExpressionNumberSequenceScopeType** sabit listesinin numaralandırma değeri. Kullanılabilir kapsam türleri **paylaşılıyor**, **hukuk varlığı** ve **şirket.**

`scope ID`: *Dize*

Belirtilen kapsam türüne göre kapsamı tanımlayan *dize* değeri.

## <a name="return-values"></a>Dönüş değerleri

*Dize*

Sonuç metin değeri.

## <a name="usage-notes"></a>Kullanım notları

**Paylaşılan** kapsam türü için, kapsam kimliği olarak boş bir dize belirtin.

**Şirket** ve **Tüzel kişilik** kapsam türleri için, kapsam kimliği olarak şirket kodu belirtin. Bu tür kapsam türleri, kapsam kimliği olarak boş bir dize belirtirseniz geçerli şirket kodu kullanılır.

Sözdizimi 1 kullanıldığında, numara serisi **Şirket** kapsam türü için istenir ve şirket kodu, er biçiminin altında çalıştırıldığı içerikle sağlanır.

## <a name="example-1"></a>Örnek 1

ER biçiminizde *Kullanıcı giriş parametresi* türünün **AskNumSeq** veri kaynağını tanımlarsınız. Bu veri kaynağı **Açıklama** genişletilmiş veri türü (EDT) anlamına gelir. Daha sonra, *hesaplanmış alan* türünün **NumSeq** veri kaynağını tanımlarsınız. Bu veri kaynağı `NUMSEQVALUE (AskNumSeq)` ifadesini içeriyor. **Numseq** veri kaynağı çağrıldığında, iletişim kutusuna kodunu girerek çalışma zamanında belirtilen yeni üretilen değerini döndürür. Numara serisi **Şirket** kapsam türü için istendi. ER biçiminin altında çalıştırıldığı içerikle sağlanan şirket kodudur.

## <a name="example-2"></a>Örnek 2

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlanır:

- *Tablo* türünün **LedgerParms** veri kaynağı. Bu veri kaynağı LedgerParameters tablosuna başvurur.
- **NumSeq** veri kaynağına *hesaplanan alan* ekleyin. Bu veri kaynağı `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)` ifadesini içeriyor.

**NumSeq** veri kaynağı çağrıldığında ER biçimi altında çalışan içerik sağlayan bir şirket için Genel muhasebe parametrelerinde yapılandırılmış Gene1 numara serisinin yeni oluşturulan değeri geri döner. Bu numara serisi benzersiz biçimde günlükleri tanıtır ve hareketleri birbirine bağlayan toplu iş numarası görevi görür.

## <a name="example-3"></a>Örnek 3

Model eşlemenizde aşağıdaki veri kaynaklarını tanımlanır:

- Microsoft Dynamics 365 Finance *numaralandırma* türünün **enumScope** veri kaynağı. Bu veri kaynağı **ERExpressionNumberSequenceScopeType** numaralandırması anlamına gelir.
- **NumSeq** veri kaynağına *hesaplanan alan* ekleyin. Bu veri kaynağı `NUMSEQVALUE ("Gene_1", enumScope.Company, "")` ifadesini içeriyor.

**NumSeq** veri kaynağı çağrıldığında ER biçimi altında çalışan içerik sağlayan bir şirket için yapılandırılmış **Gene\_1** numara serisinin yeni oluşturulan değeri geri döner.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
