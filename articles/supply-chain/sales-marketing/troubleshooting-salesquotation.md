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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 67610a833be132399b2d47ae8c6b27119be9ce95
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439253"
---
# <a name="troubleshoot-sales-quotations"></a>Satış tekliflerinde sorun giderme

Bu konu, satış teklifleri üzerinde çalışırken karşılaşabileceğiniz sorunların nasıl düzeltileceğini açıklamaktadır.

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a>Bir servis malzemesi için satış teklifine ait satış miktarını değiştiremiyorum.

### <a name="issue-description"></a>Sorun açıklaması

Bir satış teklifi satırında *Servis* tipinde bulunan bir malzeme için satış miktarını (**SalesQty** alanı) ayarlamaya çalışırsanız, aşağıdaki iletiyi alırsınız: "Miktar alanı için güncelleştirmeye izin verilmez."

### <a name="issue-resolution"></a>Sorunun çözümü

Servis malzemeleri olan ürünler için bir satış miktarı ayarlayamazsınız. Örneğin, bir ögeyi yüklemek için bir servis teklif ederseniz, fiziksel öge olmadığı için bir miktar kaydetmek anlamlı olmaz. Yalnızca bir hizmet vardır.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]