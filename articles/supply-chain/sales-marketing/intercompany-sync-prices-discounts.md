---
title: Şirketlerarası fiyatları ve iskontoları eşitleme
description: Bu konuda, şirketlerarası satış siparişleri ve satın alma siparişleri için fiyatların ve iskontoların eşitlenmesi açıklanmaktadır
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a9467e8d06a44cfaab9e3c8ea3944675c3eb8fb5
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548575"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Şirketlerarası fiyatları ve iskontoları eşitleme

[!include [banner](../../includes/banner.md)]

Şirketlerarası satış siparişi ve şirketlerarası satın alma siparişi arasında iskonto ve fiyatlar her zaman eşitlenir. Ayrıca, tüm siparişlerin aynı fiyatlara ve iskontoları sahip olması için özgün satış siparişindeki fiyat ve iskontoları eşitleyebilirsiniz. Bunu, **Tüm müşteriler** liste sayfasındaki **Genel** sekmesinden erişilen **Şirketlerarası** sayfasındaki **Satış ve pazarlama** ya da **Tedarik ve kaynak atama** bölümünde gerçekleştirebilirsiniz.

**Fiyat ve iskonto** alanı şirketlerarası satış sipariş satırı ile eşitlenir. Böylece, **Fiyat düzenlemesine izin ver** ve **İskonto düzenlemesine izin ver** alanlarını seçerek şirketlerarası satış siparişi ve şirketlerarası satın alma siparişi arasında bir değişikliğe izin vermiş olursunuz. Şirketlerarası satış siparişindeki birim fiyat, fiyat birimi veya satış masraflarında yapılan değişiklikler şirketlerarası satın alma siparişi satırındaki fiyatı belirler.

Şirketlerarası satış siparişinde veya şirketlerarası satın alma siparişinde **Fiyat düzenlemesine izin ver** ve **İskonto düzenlemesine izin ver** alanları etkinleştirilmişse her iki siparişte de fiyatı veya iskontoyu el ile değiştirebilirsiniz. Bunun dışında, değiştiremezsiniz.

Şirketlerarası satış siparişinde **Fiyat düzenlemesine izin ver** ve **İskonto düzenlemesine izin ver** alanları etkinleştirilmemişse şirketlerarası satış siparişinde fiyatta (veya masraflarda) ya da iskontoda el ile değişiklik yapamazsınız.

Şirketlerarası satın alma siparişinde **Fiyat düzenlemesine izin ver** ve **İskonto düzenlemesine izin ver** alanları etkinleştirilmemişse şirketlerarası satın alma siparişinde fiyatta (veya masraflarda) ya da iskontoda el ile değişiklik yapamazsınız.

Hem şirketlerarası satın alma siparişinde hem de şirketlerarası satış siparişinde **Fiyat düzenlemesine izin ver** ve **İskonto düzenlemesine izin ver** alanları etkinleştirilmişse her iki siparişte de el ile değişiklik yapabilirsiniz. Ancak bu, bir kişi tarafından yapılan güncelleştirmelerin başka bir şirkette aynı siparişte başka bir kişi tarafından yapılan güncelleştirmeler ile geçersiz kılınmasına neden olabilir.

> [!NOTE]
> Hem şirketlerarası satın alma siparişinde hem de şirketlerarası satış siparişinde **Fiyat ve iskonto** alanını etkinleştirdiyseniz fiyatlandırmanın denetimi sizde değildir.

Bu tür çatışmaları önlemek için yapılacak en iyi uygulama, fiyatların ve iskontoların yalnızca şirketlerarası satış veya satın alma siparişinde değiştirilmesine izin vermektir. Bu durum, bu siparişlerden herhangi birinde **Fiyat düzenlemesine izin ver** ve **İskonto düzenlemesine izin ver** alanlarının etkinleştirilmesiyle gerçekleştirilir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
