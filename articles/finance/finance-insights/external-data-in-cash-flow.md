---
title: Nakit akışı tahminlerinde dış verileri kullanma
description: Bu konuda, dış verilerin nakit akışı tahminlerine girilebilmesi veya içeri aktarılması için tamamlamanız gereken kurulum adımları açıklanmıştır.
author: rcarlson
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 855f428ae8ce79f2b7ce9a6f3347cd454bad9566
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386474"
---
# <a name="use-external-data-in-cash-flow-forecasts"></a>Nakit akışı tahminlerinde dış verileri kullanma

[!include [banner](../includes/banner.md)]

Dış veriler nakit akışı tahminlerine girilebilir veya içeri aktarılabilir. Bu konu, dış verilerin kullanılmasına özgü kurulum adımlarını ve dış verilerin nakit akışı tahminine eklenmesini sağlayan adımları açıklar.

## <a name="external-data-setup"></a>Dış verilerin kurulumu

Nakit akışı tahminlerinde dış verilerin kullanımını destekleyen ayarlar girmek için **Nakit akışı tahmin kurulum** sayfasındaki **Dış kaynak** sekmesini (**Nakit ve banka yönetimi \> Nakit akışı tahmini**) kullanın.

Bu kurulum hakkında daha fazla bilgi için bkz. [Nakit akışı tahmini](../cash-bank-management/cash-flow-forecasting.md).

Nakit akışı tahminlerine dış veriler girmek için dış verileri girerken ve değiştirirken Excel'de Aç deneyimini kullanabilirsiniz. **Dış veri** düğmesini seçin ve ardından **Dış Veri Ekle** veya **Mevcut dış verileri düzenle** seçeneklerinden birini belirleyin. Microsoft Excel dosyası açıldığında, aşağıdaki alanlara bilgi girebilirsiniz:

- **Giriş Kodu**
- **Açıklama** (isteğe bağlı)
- **Dış Kaynak adı**: Mali İçgörüleri ayarlarken tanımladığınız listedeki değerlerden birini seçin.
- **Tüzel Kişilik**
- **Date**
- **Hareket para birimi cinsinden tutar**
- **Para Birimi Kodu**
- **Varsayılan Boyut** (isteğe bağlı)
- **Belge numarası** (isteğe bağlı)
- **Hesap numarası** (isteğe bağlı)
- **Hesap adı** (isteğe bağlı)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Veri Yönetimi çerçevesi kullanarak dış verileri içe aktarma

**Veri Yönetimi** çalışma alanı ve **Nakit akışı tahmini dış kaynak girişi** olarak adlandırılan varlığı kullanarak nakit akışı tahminleri için dış verileri içeri aktarabilirsiniz.

Ek olarak, kurulum verilerini bir ortamdan diğerine taşımanız gerekiyorsa gereken kurulum tablolarında aşağıdaki varlıklar alanı kullanılabilir:

- Nakit akışı tahmini harici kaynak ayarı
- Nakit akışı tahmini harici kaynak tüzel kişiliği ayarı

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
