---
title: Satış tekliflerinde sorun giderme
description: Bu konu, satış teklifleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 92b77c1b7de1f5c946e677c810c0d0e43427473e7ba26679df23f7663946dbc0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765406"
---
# <a name="troubleshoot-sales-quotations"></a>Satış tekliflerinde sorun giderme

Bu konu, satış teklifleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Bir servis malzemesi için satış teklifine ait satış miktarını değiştiremiyorum.

### <a name="issue-description"></a>Sorun açıklaması

Bir satış teklifi satırında *Servis* tipinde bulunan bir malzeme için satış miktarını (**SalesQty** alanı) ayarlamaya çalışırsanız, aşağıdaki iletiyi alırsınız: "Miktar alanı için güncelleştirmeye izin verilmez."

### <a name="issue-resolution"></a>Sorunun çözümü

Servis malzemeleri olan ürünler için bir satış miktarı ayarlayamazsınız. Örneğin, bir ögeyi yüklemek için bir servis teklif ederseniz, fiziksel öge olmadığı için bir miktar kaydetmek anlamlı olmaz. Yalnızca bir hizmet vardır.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]