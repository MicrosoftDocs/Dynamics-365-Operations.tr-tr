---
title: Şirketlerarası müşteri bilgilerini eşitleme
description: Bu makalede, şirketlerarası siparişler için müşteri bilgilerinin eşitlenmesi açıklanmaktadır
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
ms.openlocfilehash: a3a67c9bcf93f88375d2d4d78d87175200626d50
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897530"
---
# <a name="synchronize-intercompany-customer-information"></a>Şirketlerarası müşteri bilgilerini eşitleme

[!include [banner](../../includes/banner.md)]

Satış siparişi oluşturulurken veya müşteri, satıcı referansı ya da müşteri talep numarasında değişiklik yapıldığında **Müşteri bilgileri** alanı etkinleştirilirse müşteri bilgileri eşitlenir.

Bu eşitleme alanlarındaki değeri her zaman değiştirebilirsiniz. Ancak bu değerin diğer şirketlerarası siparişlere kopyalanıp kopyalanmayacağını ancak bu parametreyi seçerek belirleyebilirsiniz. Şirketlerarası satış siparişi üzerindeki **Müşteri bilgileri** alanını etkinleştirdiyseniz şirketlerarası satış siparişindeki değişiklik, şirketlerarası satın alma siparişiyle eşitlenir. Ayrıca, şirketlerarası satın alma siparişi üzerindeki **Müşteri bilgileri** alanını da etkinleştirmişseniz bu alan da özgün satış siparişine eşitlenir.

> [!NOTE]
> Hem şirketlerarası satın alma siparişinde hem de şirketlerarası satış siparişinde **Müşteri bilgileri** alanını etkinleştirdiyseniz bir şirkette bir kişi tarafından yapılan güncelleştirmeler, aynı siparişte başka bir şirkette başka bir kişi tarafından yapılan güncelleştirmeler tarafından geçersiz kılınır.

En iyi uygulama, şirketlerarası satın alma siparişinde **Müşteri bilgileri** alanını etkinleştirmektir. Bu, özgün satış siparişi ile şirketlerarası satın alma siparişi arasında ve şirketlerarası satın alma siparişinden şirketlerarası satış siparişine eşitlemeyi sağlar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
