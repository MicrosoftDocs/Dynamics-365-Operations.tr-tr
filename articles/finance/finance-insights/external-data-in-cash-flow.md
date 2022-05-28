---
title: Nakit akışı tahminlerinde dış veriler
description: Bu konuda, dış verilerin nakit akışı tahminlerine girilebilmesi veya içeri aktarılması için tamamlamanız gereken kurulum adımları açıklanmıştır.
author: RyanCCarlson2
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f7fac80b7ad0fde273fbd33aa5df146e569be46e
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713740"
---
# <a name="external-data-in-cash-flow-forecasts"></a>Nakit akışı tahminlerinde dış veriler

[!include [banner](../includes/banner.md)]

Dış veriler nakit akışı tahminlerine girilebilir veya içeri aktarılabilir. Bu konu, dış verilerin kullanılmasına özgü kurulum adımlarını ve dış verilerin nakit akışı tahminine eklenmesini sağlayan adımları açıklar.

## <a name="external-data-setup"></a>Dış verilerin kurulumu

Nakit akışı tahminlerinde dış verilerin kullanımını destekleyen ayarlar girmek için **Nakit akışı tahmin kurulum** sayfasındaki **Dış kaynak** sekmesini (**Nakit ve banka yönetimi \> Nakit akışı tahmini \> Nakit akışı tahmini kurulum**) kullanın.

Dış veriler nakit akışı tahminlerine girilebilir veya içeri aktarılabilir. Harici veriler girilmeden veya içe aktarılmadan önce, harici kaynakların ayarlanması gerekir. **Harici kaynak** sekmesinde harici nakit akışı kategorileri ayarlayın. Kategori, **Giden** veya **Gelen** olabilir. **Likidite**, deftere nakil türü olarak seçilmelidir. **Yasal varlık ayarları** kılavuzunda, yasal varlıkları ve harici nakit akışı kategorilerinin uygulanacağı ilgili ana firmaları seçin.

Nakit akışı tahminlerini ayarlamak hakkında daha fazla bilgi için bkz: [Nakit akışı tahmini](../cash-bank-management/cash-flow-forecasting.md).

## <a name="enter-external-data"></a>Dış verileri girme

Nakit akışı tahminlerine dış veriler girmek ve değiştirmek için **Excel'de Aç** deneyimini kullanabilirsiniz. **Nakit akışı tahmini** çalışma alanında **Dış veri** düğmesini seçin ve ardından **Dış Veri Ekle** veya **Mevcut dış verileri düzenle** seçeneklerinden birini belirleyin. Microsoft Excel dosyası açıldığında, aşağıdaki alanlara bilgi girebilirsiniz:

- **Giriş Kodu** (benzersiz)
- **Açıklama** (isteğe bağlı)
- **Dış Kaynak adı**: Finance Insights ayarlarken tanımladığınız listedeki değerlerden birini seçin.
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
