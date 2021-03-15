---
title: Satış tekliflerinde sorun giderme
description: Bu konu, satış teklifleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 98011dbf22ff55b7651ce63557fa4a360130b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974772"
---
# <a name="troubleshoot-sales-quotations"></a>Satış tekliflerinde sorun giderme

Bu konu, satış teklifleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Bir servis malzemesi için satış teklifine ait satış miktarını değiştiremiyorum.

### <a name="issue-description"></a>Sorun açıklaması

Bir satış teklifi satırında *Servis* tipinde bulunan bir malzeme için satış miktarını (**SalesQty** alanı) ayarlamaya çalışırsanız, aşağıdaki iletiyi alırsınız: "Miktar alanı için güncelleştirmeye izin verilmez."

### <a name="issue-resolution"></a>Sorunun çözümü

Servis malzemeleri olan ürünler için bir satış miktarı ayarlayamazsınız. Örneğin, bir ögeyi yüklemek için bir servis teklif ederseniz, fiziksel öge olmadığı için bir miktar kaydetmek anlamlı olmaz. Yalnızca bir hizmet vardır.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]