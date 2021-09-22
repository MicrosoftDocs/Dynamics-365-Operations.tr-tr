---
title: Satış teklifi satırında servis maddesi miktarı ayarlanamıyor
description: Satış teklifleriyle çalışırken, sayılacak fiziksel madde olmadığından servis maddeleri olan ürünler için satış miktarı ayarlayamazsınız.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea0f8f246e95f90b6ac5e78ee63950c9ca836a0e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477889"
---
# <a name="cant-change-the-sales-quantity-of-a-service-item-on-a-sales-quotation-line"></a>Bir satış teklifi satırında servis maddesinin satış miktarı değiştirilemiyor

## <a name="symptoms"></a>Belirtiler

Bir satış teklifi satırında *Servis* tipinde bulunan bir madde için satış miktarını (**SalesQty** alanı) ayarlamaya çalışırsanız aşağıdaki iletiyi alırsınız:

> Miktar alanı için güncelleştirmeye izin verilmez.

## <a name="cause"></a>Nedeni

Bu, tasarımdan kaynaklanır. Servis malzemeleri olan ürünler için bir satış miktarı ayarlayamazsınız. Örneğin, bir maddeyi yüklemek için servis sunarsanız sayılacak fiziksel madde olmadığından miktar kaydetmek anlamlı olmaz. Yalnızca bir hizmet vardır.
