---
title: Şirketlerarası müşteri faturaları için ödemeleri otomatik olarak kaydetme
description: Bu konuda, şirketlerarası müşteri faturaları için ödemelerin nasıl otomatik olarak kaydedileceği açıklanmaktadır
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
ms.openlocfilehash: 4e8f784cd310026f0a647a0f509999e11ab26ce5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878801"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>Şirketlerarası müşteri faturaları için ödemeleri otomatik olarak kaydetme

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management, şirketlerarası müşteri faturası deftere nakledildiğinde bir müşteri hareketi oluşturur. Bu müşteri hareketi kapatılana kadar açık kalır, bu da ödendiği anlamına gelir. Şirketlerarası satınalma siparişi ile karşılık gelen fatura güncelleştirildiğinde, müşteri hareketiyle eşleşen bir satıcı hareketi oluşturulur. Bu satıcı hareketi de kapatılana kadar açık kalır. Fark riskini azaltmak için bir alacak hesabı ödeme günlüğü otomatik olarak oluşturulabilir ve borç hesapları ödeme günlüğü deftere nakledildiğinde, deftere nakledilebilir.

1. **Satış ve pazarlama \> Müşteriler \> Tüm müşteriler** öğesine gidin.
1. Eylem Bölmesi'ndeki **Genel** sekmesinde, **Şirketlerarası**'nı seçin.
1. Satış siparişleri için **Şirketlerarası** sayfasında şirketlerarası alacak hesapları ödemelerini ayarlamak için **Satış siparişi politikaları** bağlantısını seçin.
1. **Ödeme günlüğü** alanında, şirketlerarası satıcı ödemelerini kaydetmek istediğiniz alacak hesapları ödeme günlüğünü seçin. Bu ayarı **Alacak hesapları parametreleri** sayfasından yapabilirsiniz.
1. Bu günlüğü otomatik olarak deftere nakletmek istiyorsanız **Günlüğü otomatik olarak deftere naklet** onay kutusunu seçin.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
