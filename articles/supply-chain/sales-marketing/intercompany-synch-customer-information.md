---
title: Şirketlerarası müşteri bilgilerini eşitleme
description: Bu konuda, şirketlerarası siparişler için müşteri bilgilerinin eşitlenmesi açıklanmaktadır
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
ms.openlocfilehash: c82216c8391f6c447bec74f25cd16b9db18d468d
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548589"
---
# <a name="synchronize-intercompany-customer-information"></a>Şirketlerarası müşteri bilgilerini eşitleme

[!include [banner](../../includes/banner.md)]

Satış siparişi oluşturulurken veya müşteri, satıcı referansı ya da müşteri talep numarasında değişiklik yapıldığında **Müşteri bilgileri** alanı etkinleştirilirse müşteri bilgileri eşitlenir.

Bu eşitleme alanlarındaki değeri her zaman değiştirebilirsiniz. Ancak bu değerin diğer şirketlerarası siparişlere kopyalanıp kopyalanmayacağını ancak bu parametreyi seçerek belirleyebilirsiniz. Şirketlerarası satış siparişi üzerindeki **Müşteri bilgileri** alanını etkinleştirdiyseniz şirketlerarası satış siparişindeki değişiklik, şirketlerarası satın alma siparişiyle eşitlenir. Ayrıca, şirketlerarası satın alma siparişi üzerindeki **Müşteri bilgileri** alanını da etkinleştirmişseniz bu alan da özgün satış siparişine eşitlenir.

> [!NOTE]
> Hem şirketlerarası satın alma siparişinde hem de şirketlerarası satış siparişinde **Müşteri bilgileri** alanını etkinleştirdiyseniz bir şirkette bir kişi tarafından yapılan güncelleştirmeler, aynı siparişte başka bir şirkette başka bir kişi tarafından yapılan güncelleştirmeler tarafından geçersiz kılınır.

En iyi uygulama, şirketlerarası satın alma siparişinde **Müşteri bilgileri** alanını etkinleştirmektir. Bu, özgün satış siparişi ile şirketlerarası satın alma siparişi arasında ve şirketlerarası satın alma siparişinden şirketlerarası satış siparişine eşitlemeyi sağlar.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
