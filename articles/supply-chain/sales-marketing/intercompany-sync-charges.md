---
title: Şirketlerarası masrafları eşitleme
description: Bu konuda, şirketlerarası masrafların eşitlenmesi açıklanmaktadır
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e7b3de3d7da7be6c1c8b5c3842862e7bccd78277
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857300"
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
