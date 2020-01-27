---
title: NUMSEQVALUE ER işlevi
description: Bu konu, NUMSEQVALUE Elektronik raporlama (ER) işlevinin nasıl kullanıldığı hakkında bilgi sağlar.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d68784524a5639d8d447daa2cda940680d795542
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915844"
---
# <a name="NUMSEQVALUE">NUMSEQVALUE ER işlevi</a>

[!include [banner](../includes/banner.md)]

`NUMSEQVALUE` işlev, belirtilen numara serisi, kapsam ve kapsam kimliğine dayalı olarak bir numara serisinin yeni oluşturulan değerini gösteren bir *dize* değeri döndürür. Kapsam kimliği, Elektronik raporlama (ER) biçiminin altında çalıştırıldığı içerikle sağlanan şirket koduna eşittir.

## <a name="syntax-1"></a>Sözdizimi 1

```
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>Sözdizimi 2

```
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>Sözdizimi 3

```
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

- Microsoft Dynamics 365 Finance *numaralandırma* türünün **enumscope** veri kaynağı. Bu veri kaynağı **ERExpressionNumberSequenceScopeType** numaralandırması anlamına gelir.
- **NumSeq** veri kaynağına *hesaplanan alan* ekleyin. Bu veri kaynağı `NUMSEQVALUE ("Gene_1", enumScope.Company, "")` ifadesini içeriyor.

**NumSeq** veri kaynağı çağrıldığında ER biçimi altında çalışan içerik sağlayan bir şirket için yapılandırılmış **Gene\_1** numara serisinin yeni oluşturulan değeri geri döner.

## <a name="additional-resources"></a>Ek kaynaklar

[Diğer (belirli iş etki alanı) işlevleri](er-functions-category-other.md)
