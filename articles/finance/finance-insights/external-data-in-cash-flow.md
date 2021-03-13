---
title: Nakit akışı tahminlerinde dış verileri kullanma (önizleme)
description: Bu konuda, dış verilerin nakit akışı tahminlerine girilebilmesi veya içeri aktarılması için tamamlamanız gereken kurulum adımları açıklanmıştır.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: ae0eba6d397725cf425d9781a597d904e1958d44
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009405"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Nakit akışı tahminlerinde dış verileri kullanma (önizleme)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Dış veriler nakit akışı tahminlerine girilebilir veya içeri aktarılabilir. Bu konu, dış verilerin kullanılmasına özgü kurulum adımlarını ve dış verilerin nakit akışı tahminine eklenmesini sağlayan adımları açıklar.

## <a name="external-data-setup"></a>Dış verilerin kurulumu

Nakit akışı tahminlerinde dış verilerin kullanımını destekleyen ayarlar girmek için **Nakit akışı tahmin kurulum** sayfasındaki **Dış kaynak** sekmesini (**Nakit ve banka yönetimi \> Nakit akışı tahmini**) kullanın.

Bu kurulum hakkında daha fazla bilgi için bkz. [Nakit akışı tahmini](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).

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

#### <a name="privacy-notice"></a>Gizlilik bildirimi
Önizlemeler (1), Dynamics 365 Finance and Operations hizmetinden daha az gizlilik ve güvenlik önlemleri kullanabilir, (2) bu hizmet için hizmet düzeyi sözleşmesine (SLA) dahil edilmez, (3) kişisel verileri veya yasal ya da mevzuat uyumluluğu gereksinimlerine tabi olan diğer verileri işlemek için kullanılmamalıdır ve (4) sınırlı desteğe sahiptir.