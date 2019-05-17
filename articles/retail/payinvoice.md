---
title: Ödeme faturası senaryolarını ayarlama
description: Bu konuda, Dynamics 365 for Retail'ın nasıl fatura ödemeleriyle ilgili çeşitli senaryoları destekleyecek şekilde yapılandırılacağı açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 158d8ca8a97c473e940f76dd3f35cecc4e9dd7f4
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517188"
---
# <a name="set-up-pay-invoice-scenarios"></a>Ödeme faturası senaryolarını ayarlama

[!include [banner](includes/banner.md)]

Dynamics 365 for Retail'daki Fatura öde işlevi aşağıdakileri destekleyecek şekilde genişletilmiştir:

- Tek bir POS hareketinde birden fazla satış siparişi faturasının ödenmesi.
- Serbest metin faturaları, proje tabanlı faturalar ve alacak dekontları gibi çeşitli müşteri faturası türlerinin ödenmesi.

Bu senaryoları etkinleştirmek üzere, mağazalar için işlev profilinin aşağıda belirtildiği gibi yapılandırılması gerekir.

1. **Perakende \> Kanal ayarı \> POS ayarı \> POS profilleri \> İşlev profilleri**'ne gidin ve değişiklikleri yapmak istediğiniz mağazalarla ilişkili bir profil seçin.
2. **İşlevler** sekmesinde, aşağıdaki parametreleri gerektiği gibi yapılandırın.

    - **Satış siparişi faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla satış siparişi tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.
    - **Serbest metin faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla serbest metin tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.
    - **Proje faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla proje tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.
    - **Satış siparişi alacak dekontu**: Kullanıcıların birden fazla satış siparişi tabanlı alacak dekontunu açık faturalara göre kapatmasına veya açık bir alacak dekontu için bir geri ödeme işlemi yapmasına izin vermek için **Evet**'i seçin.

> [!NOTE]
> Kısmi tutarları ödeme veya kapatma henüz desteklenmemektedir.
