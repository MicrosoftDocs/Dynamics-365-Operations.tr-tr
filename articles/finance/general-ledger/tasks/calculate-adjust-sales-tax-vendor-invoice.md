---
title: Satıcı faturasındaki satış vergisini hesaplama ve ayarlama
description: Bu konuda Dynamics 365 Finance satıcı faturasındaki satış vergisinin nasıl ayarlanacağı açıklanmaktadır.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2f3521f7bc56659fc6f7a6d47f581ddbfea16523
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139979"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Satıcı faturasındaki satış vergisini hesaplama ve ayarlama

[!include [banner](../../includes/banner.md)]

Bu konuda satıcı faturasındaki satış vergisinin nasıl ayarlanacağı açıklanmaktadır. Orijinal kaynak belgesinde hesaplanandan farklı vergi tutarları görüntüleniyorsa, bu tutarları deftere nakletmeden önce ayarlayabilirsiniz. Bu görevde DEMF demo şirketi kullanılmaktadır.

1. Gezinti bölmesinde **Modüller > Borç hesapları > Faturalar > Fatura günlüğü**'ne gidin.
2. **Yeni**'yi seçin.
3. Yeni satırdaki **Ad** alanında açılır menüden bir seçenek belirleyin.
4. Eylem Bölmesinde, **Satırlar**'ı seçin.
5. **Hesap** alanında istediğiniz değerleri belirtin.
6. **Fatura** alanına bir değer girin.
7. **Alacak** alanına bir sayı girin.
8. **Mahsup hesap** alanında istediğiniz değerleri belirtin.
9. **Satış vergisi**'ni seçin.
10. **Toplam gerçek satış vergisi tutarı** alanına bir sayı girin.
11. **Ayarlama** sekmesinde, satış vergisi tutarları, tek tek satış vergisi kodlarına göre ayarlanabilir.
12. **Hesaplanan tutarlardan gerçek tutarı sıfırla**'yı seçin.
13. **Tamam**'ı seçin.
14. **Kaydet**'i seçin.

