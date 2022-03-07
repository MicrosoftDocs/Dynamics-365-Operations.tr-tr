---
title: Genel muhasebe hareketine göre satış vergisi belirtimi raporu
description: Bu konu altında, Genel muhasebe hareketine göre satış vergisi belirtimi raporunun nasıl kullanılacağı, satış vergisi hesaplanan genel muhasebe hareketleri hakkındaki bilgilerin nasıl görüntüleneceği ve yazdırılacağı açıklanmaktadır.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e2aafa90b8dbc6642737fc1834a7c992a9883033
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975520"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>Genel muhasebe hareketine göre satış vergisi belirtimi raporu
[!include [banner](../includes/banner.md)]

Bu konu altında, **Genel muhasebe hareketine göre satış vergisi belirtimi** raporunun nasıl kullanılacağı, satış vergisi hesaplanan genel muhasebe hareketleri hakkındaki bilgilerin nasıl görüntüleneceği ve yazdırılacağı açıklanmaktadır.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Vergi hesapları - vergi dışı hesaplar karşılaştırması

**Genel muhasebe hareketine göre satış vergisi belirtimi** raporu, hem vergi hesapları hem de vergi dışı hesaplar için vergi hareketlerini gösterir. Bu hesaplar aşağıdaki şekilde kategorize edilir:

- **Vergi hesabı** – Bir vergi hareketi deftere nakledildiğinde hesap bir vergi hesabı olarak değerlendirilir ve **Satış Vergisi** günlük satırındaki ana hesap satış vergisi borç hesabı veya satış vergisi alacak hesabı gibi bir vergi hesabıdır.
- **Vergi dışı hesap** – Bir vergi hareketi deftere nakledildiğinde hesap bir vergi dışı hesap olarak değerlendirilir ve orijinal hareketteki ana hesap, gelir hesabı veya gider hesabı gibi vergi dışı bir hesaptır.

Vergi hesapları için, rapordaki **Kaynak**, **Satış vergisi alacağı** ve **Satış vergisi borcu** sütunları **0** (sıfır) değerini gösterir. Vergi dışı hesaplar için bu sütunlar tutarları gösterir.

## <a name="filtering-the-data-on-the-report"></a>Rapordaki verileri filtreleme

Raporu oluşturduğunuz zaman aşağıdaki varsayılan alanlar kullanılabilir. Bu alanları, raporda gösterilen verileri filtrelemek için kullanabilirsiniz.

| Alan                      | Tanım |
|----------------------------|-------------|
| Tarih                       | Vergi hareketlerinin tarih aralığını tanımlamak için **Başlangıç** ve **Bitiş** bölümlerindeki alanları kullanın. |
| Ana hesap               | Bir ana hesaplar aralığı tanımlamak için **Başlangıç** ve **Bitiş** bölümlerindeki alanları kullanın. |
| Satış vergisi kodu             | Bir satış vergisi kodları aralığı tanımlamak için **Başlangıç** ve **Bitiş** bölümlerindeki alanları kullanın. |
| Gruplama                   | Raporun genel muhasebe hesabına göre mi yoksa satış vergisi koduna göre mi gruplandırılacağını seçin. |
| Satış vergisi koduna göre alt toplamlar | Satış vergisi koduna göre ara toplamları göstermek için bu seçeneği **Evet** olarak ayarlayın. |
| Yalnızca toplamlar                | Yalnızca toplamları göstermek için bu seçeneği **Evet** olarak ayarlayın. |
| Yalnızca ana hesaplar         | Rapora yalnızca ana hesapları eklemek için bu seçeneği **Evet** olarak ayarlayın. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Raporda yalnızca vergi dışı hesapları gösterme

Raporda yalnızca vergi dışı hesapları göstermek için aşağıdaki şekilde gösterildiği gibi bir filtre koşulu ayarlayın (örneğin yıldız (\*) girin).

![Vergi dışı hesapları gösteren rapor](media/taxspecperledgertrans.png)
