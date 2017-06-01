---
title: "Excel&quot;den günlük satırlarını ve belgeleri yayımlama"
description: "Bu konu genel muhasebe günlükleri için satırların nasıl girileceğini ve Microsoft Excel&quot;den nasıl yayımlanacağını açıklar. Girdiğiniz hareket türüne bağlı olarak kullanabileceğiniz çeşitli şablonları hakkında bilgi içerir."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a43bf66de7602aa9fb47925996ec5b979e1f8dac
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2017


---

# <a name="publish-journal-lines-and-documents-from-excel"></a>Excel'den günlük satırlarını ve belgeleri yayımlama

[!include[banner](../includes/banner.md)]


Bu konu genel muhasebe günlükleri için satırların nasıl girileceğini ve Microsoft Excel'den nasıl yayımlanacağını açıklar. Girdiğiniz hareket türüne bağlı olarak kullanabileceğiniz çeşitli şablonları hakkında bilgi içerir.

Kullanıcılar mali günlükler için satırlar girebilir ve Microsoft Excel'den yayımlayabilir. Bir kullanıcı bir günlük oluşturduktan sonra **Satırları Excel'de aç** düğmesi kullanılabilir olan şablonları görüntüler. Şablonlar, belirli senaryoları desteklemek üzere tasarlanmıştır ancak hesap türünün her birleşimi günlükte desteklenmez. Aşağıdaki tablo kullanılabilir şablonları ve destekledikleri hesap türlerini gösterir.
|                          |                                                                                                                         |                                                                                         |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| **Şablon**             | **Desteklenen hesap türleri**                                                                                             | **Şablona erişim**                                                          |
| Genel muhasebe günlüğü satırları     | Hesap: Genel muhasebe, Müşteri, Satıcı, Banka mahsup hesabı: Genel muhasebe, Müşteri, Satıcı, Banka şirketlerarası desteklenir.       | Yevmiye fişi                                                                         |
| Fatura defteri         | Hesap: Satıcı Mahsup hesabı: Şirketlerarası muhasebe desteklenmez.                                                    | AP fatura kaydı                                                                     |
| Fatura günlüğü          | Hesaplar: Satıcı Mahsup hesabı: Şirketlerarası Muhasebe desteklenir.                                                      | BH fatura günlüğü                                                                      |
| Satıcı faturası           |                                                                                                                         | Satıcı faturası                                                                          |
| Müşteri fatura günlüğü | Hesap: Müşteri Mahsup hesabı: Şirketlerarası Muhasebe desteklenir.                                                     | Yevmiye fişi                                                                         |
| Dekont / Serbest metin faturası        |                                                                                                                         | **Serbest metin faturası** sayfasında, **Excel'de Aç**'a (Microsoft Office simgesi) tıklayın. |
| Sabit kıymet günlüğü     | Genel muhasebeye kıymet, banka, müşteri veya satıcı. Şirketlerarası desteklenmez.                                               | Sabit kıymet günlüğü                                                                     |
| Satıcı ödeme günlüğü   | Hesap: Satıcı Mahsup hesabı: Genel muhasebe, Banka Şirketlerarası desteklenmez.                                                 | Satıcı ödeme günlüğü                                                                  |
| Müşteri ödeme günlüğü | Hesap: Müşteri Mahsup hesabı: Genel Muhasebe, Banka Şirketlerarası desteklenir.                                               | Müşteri ödeme günlüğü                                                                |
| Proje gider günlüğü  | Hesap: Proje, Genel muhasebe, Müşteri, Satıcı Mahsup hesabı: Proje, Genel muhasebe, Müşteri, Satıcı Şirketlerarası desteklenir. | Yevmiye defteri Gider (Proje yönetimi ve muhasebe altında)                       |

Satırlar yayımlandığında, mali günlüklerde ayarlanan kurallarla uyumlu olduğundan emin olmak amacıyla doğrulanır. Satırlar yayımladıktan sonra, kullanıcılar fişleri Microsoft Dynamics 365 for Operations'dan düzenleyebilir veya deftere nakledebilir. 

Şablona mali boyutları eklemek için ek değişiklikler gereklidir. Ek bilgi için bkz. [Microsoft Excel şablonuna boyutlar ekleme](/dynamics365/operations/dev-itpro/financial/add-dimensions-excel-templates). Boyutlar varlığa eklendikten sonra, Excel tasarımcısında kullanılabilir ve şablona eklenebilir.






