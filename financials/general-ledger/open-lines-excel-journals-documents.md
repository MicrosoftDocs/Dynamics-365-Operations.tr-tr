---
title: "Günlük satırları ve Excel belgeleri yayınlama"
description: "Bu konu girin ve yayımlamak için Microsoft Excel genel günlüklerden satırlar açıklar. Bu, girmekte olduğunuz hareket türüne bağlı olarak kullanabileceğiniz çeşitli şablonları hakkında bilgi içerir."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62213
ms.assetid: 211874a7-4bf0-4a0c-96c2-fa05042777d3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 087339cb3002b42bcb985c2ccfc2d97c752a817c
ms.lasthandoff: 03/31/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Günlük satırları ve Excel belgeleri yayınlama

Bu konu girin ve yayımlamak için Microsoft Excel genel günlüklerden satırlar açıklar. Bu, girmekte olduğunuz hareket türüne bağlı olarak kullanabileceğiniz çeşitli şablonları hakkında bilgi içerir.

Kullanıcılar girebilir ve satırlar için mali günlükler Microsoft Excel'den yayımlayabilirsiniz. Bir kullanıcı bir günlük oluşturur sonra **satırları Excel'de açmak** düğmesi kullanılabilir olan şablonları görüntüler. Şablonlar, ancak her birleşimi bir hesap türü günlük'te desteklenen belirli senaryoları desteklemek üzere tasarlanmıştır. Aşağıdaki tablo kullanılabilir şablonlar ve destekledikleri hesap türlerini gösterir.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Template**             | **Desteklenen hesap türleri**                                                                                             | **Şablon erişmek nasıl**                                                          |
| Genel muhasebe günlüğü satırları     | Firma: Genel muhasebe, müşteri, satıcı, banka mahsup hesabı: Genel muhasebe, müşteri, satıcı, banka şirketlerarası desteklenir.       | Yevmiye fişi                                                                         |
| Fatura defteri         | Firma: Satıcı mahsup hesabı: Şirketlerarası muhasebe değil desteklenen.                                                    | AP fatura kaydı                                                                     |
| Fatura günlüğü          | Firmalar: Satıcı mahsup hesabı: Şirketlerarası muhasebe desteklenir.                                                      | BH fatura günlüğü                                                                      |
| Satıcı faturası           |                                                                                                                         | Satıcı faturası                                                                          |
| Müşteri fatura günlüğü | Firma: Müşteri mahsup hesabı: Şirketlerarası muhasebe desteklenir.                                                     | Yevmiye fişi                                                                         |
| Dekont / Serbest metin faturası        |                                                                                                                         | Üzerinde **serbest metin faturası** sayfasında,'ı **Excel'de Aç** (Microsoft Office simge). |
| Sabit kıymet günlüğü     | Kıymet genel muhasebe, banka, müşteri veya satıcı için. Şirketlerarası desteklenmiyor.                                               | Sabit kıymet günlüğü                                                                     |
| Satıcı ödeme günlüğü   | Firma: Satıcı mahsup hesabı: banka defter, şirketlerarası desteklenir.                                                 | Satıcı ödeme günlüğü                                                                  |
| Müşteri ödeme günlüğü | Firma: Müşteri mahsup hesabı: banka defter, şirketlerarası desteklenir.                                               | Müşteri ödeme günlüğü                                                                |
| Proje gider günlüğü  | Firma: Proje, defter, müşteri, satıcı mahsup hesabı: Proje, defter, müşteri, satıcı şirketlerarası desteklenir. | Yevmiye defterine gider (altında proje yönetimi ve muhasebe)                       |

Satırları yayımlandığında, mali günlükler ayarlamak kurallarıyla uyumlu emin olmak için doğrulanır. Satırları yayımladıktan sonra kullanıcılar düzenleyebilir veya işlemleri için Microsoft Dynamics 365 fişleri deftere. 

Mali boyutları için bir şablon eklemek için ek değişiklikler gereklidir. Ek bilgi için bkz: [boyutlar eklemek için Microsoft Excel şablonunu](\dev-itpro\financial-dimensions\add-dimensions-excel-templates). Boyutlar için varlık eklendikten sonra Excel Tasarımcısı'nda kullanılabilir ve şablonuna eklenebilir.




