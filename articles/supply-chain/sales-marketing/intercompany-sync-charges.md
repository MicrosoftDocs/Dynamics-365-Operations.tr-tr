---
title: Şirketlerarası masrafları eşitleme
description: Bu konuda, şirketlerarası masrafların eşitlenmesi açıklanmaktadır
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
ms.openlocfilehash: c4854b698c8046fc603454c4d9d7059c938c70b3
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548588"
---
# <a name="synchronize-intercompany-charges"></a>Şirketlerarası masrafları eşitleme

[!include [banner](../../includes/banner.md)]

Masraflar yalnızca şirketlerarası satış siparişi ile şirketlerarası satın alma siparişi arasında eşitlenir ve eşitleme her zaman gerçekleşir.

Şirketlerarası satın alma siparişinde veya şirketlerarası satış siparişinde **Fiyat düzenlemesine izin ver** alanı seçilirse şirketlerarası satış siparişine ya da şirketlerarası satın alma siparişine el ile masraf ekleyebilirsiniz. Bunun dışında, ekleyemezsiniz.

Şirketlerarası satış siparişinde **Fiyat düzenlemesine izin ver** alanı seçilmemişse şirketlerarası satış siparişine el ile masraf ekleyemezsiniz.

Şirketlerarası satın alma siparişinde **Fiyat düzenlemesine izin ver** alanı seçili değilse şirketlerarası satın alma siparişine masraf ekleyemezsiniz.

Hem şirketlerarası satın alma siparişinde hem de şirketlerarası satış siparişinde **Fiyat düzenlemesine izin ver** alanı etkinleştirilirse masrafları her iki siparişe de el ile ekleyebilirsiniz. Ancak bu, birçok masrafın yanlış eklenmesine neden olabilir.

Bu tür çakışmalardan kaçınmak için en iyi uygulama masrafların şirketlerarası satış siparişine veya şirketlerarası satın alma siparişine eklenmesine izin verilmesidir, ancak her ikisine birden değil.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
