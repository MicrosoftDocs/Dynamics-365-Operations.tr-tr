---
title: İş alanına özel kategorisindeki ER işlevlerinin listesi
description: Bu makalede, Elektronik raporlama (ER) uygulamasında desteklenen iş etki alanına özel işlevler hakkında bilgi sağlanmaktadır.
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
ms.openlocfilehash: b1ac46cf10d57b40af1fa99021156ad97a17ba20
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272697"
---
# <a name="list-of-er-functions-in-the-business-domainspecific-category"></a>İş alanına özel kategorisindeki ER işlevlerinin listesi

[!include [banner](../includes/banner.md)]

Elektronik raporlama (ER) etki alanına özel işlevler, Microsoft Dynamics 365 Finance'in uygulanmasına özel hesaplamalar ve veri erişim istekleri gerçekleştirmek için kullanılabilir. Bu makale, bu işlevlerin özetini sunmaktadır.

## <a name="list-of-supported-functions"></a>Desteklenen işlevler listesi

| İşlev| Tanım |
|---------|-------------|
| [CH_Bank_Mod_10](er-functions-other-chbankmode10.md) | Bu işlev, bir alacaklı başvurusunu, belirtilen fatura numarasının basamaklara dayalı olarak MOD10 ifadesi olarak gösteren bir *dize* değeri döndürür. |
| [CN_GBT_AdditionalDimensionID](er-functions-other-cngbtadditionaldimensionid.md) | Bu işlev, belirtilen dizeden alınan tek bir mali boyut kodunu temsil eden bir *dize* değeri döndürür. Tüm boyutları virgülle ayrılmış bir kimlik listesi olarak sunan bir dize. |
| [ConvertCurrency](er-functions-other-convertcurrency.md) | Bu işlev, belirtilen parasal tutarı kaynak para biriminden, belirtilen tarihte belirtilen şirketinin ayarlarını kullanarak belirtilen hedef para birimine dönüştürme sonucunu temsil eden *Gerçek* değer döndürür. |
| [CurCredRef](er-functions-other-curcredref.md) | Bu işlev, bir alacaklı başvurusunu, belirtilen fatura numarasının basamaklara dayalı olarak gösteren bir *dize* değeri döndürür. |
| [FA_Balance](er-functions-other-fabalance.md) | Bu işlev, belirtilen sabit kıymet maddesine, değer modeli koduna, raporlama yılına ve raporlama tarihlerin dönemine ait sabit kıymet bakiyesi için verilerden oluşan bir *konteyner (kayıt)* değeri döndürür. |
| [FA_Sum](er-functions-other-fasum.md) | Bu işlev, belirtilen sabit kıymet maddesine, değer modeli koduna ve tarihlerin dönemine ait sabit kıymet tutarları için verilerden oluşan bir *konteyner (kayıt)* değeri döndürür. |
| [GetCurrentCompany](er-functions-other-getcurrentcompany.md) | Bu işlevi, bir kullanıcının oturum açmış olduğu tüzel kişiliğin (şirket) kodunu temsil eden *Dize* değeri döndürür. |
| [ISOCredRef](er-functions-other-isocredref.md) | Bu işlevi, bir Uluslararası Standartlar Kuruluşu (ISO) alacaklı başvurusunu, belirtilen fatura numarasının basamakları ve alfabetik sembollerine dayalı olarak temsil eden *Dize* değeri döndürür. |
| [IsValidCharacterISO7064](er-functions-other-isvalidchariso7064.md) | Bu işlevi, belirtilen dize, geçerli bir uluslararası banka hesap numarasını (IBAN) temsil ediyorsa, **DOĞRU** *boole* değerini döndürür. Aksi takdirde, **YANLIŞ** *Boole* değeri döndürür. |
| [Mod_97](er-functions-other-mod97.md) | Bu işlev, bir alacaklı başvurusunu, belirtilen fatura numarasının basamaklara dayalı olarak MOD97 ifadesi olarak gösteren bir *dize* değeri döndürür. |
| [NumSeqValue](er-functions-other-numseqvalue.md) | Bu işlev, belirtilen numara serisi, kapsam ve kapsam kimliğine dayalı olarak bir numara serisinin yeni oluşturulan değerini gösteren bir *dize* değeri döndürür. Kapsam kimliği, ER biçiminin altında çalıştırıldığı içerikle sağlanan şirket koduna eşittir. |
| [RoundAmount](er-functions-other-roundamount.md) | Bu işlev, belirtilen yuvarlama kuralına göre belirtilen tutarda belirtilen ondalık basamak sayısına yuvarlama sonucunu temsil eden *gerçek* bir değer döndürür. |
| [TableName2ID](er-functions-other-tablename2id.md) | Bu işlevi, belirtilen tablo için tablo kodunun sayısal gösterimini *tamsayı* değeri olarak döndürür. |

## <a name="additional-resources"></a>Ek kaynaklar

[Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)

[Elektronik raporlamada formül tasarımcısı](general-electronic-reporting-formula-designer.md)

[Elektronik raporlamada formül dili](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
