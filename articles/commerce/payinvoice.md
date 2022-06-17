---
title: Fatura ödeme senaryolarını ayarlama
description: Bu makalede, Dynamics 365 Commerce'in fatura ödemeleriyle ilgili çeşitli senaryoları destekleyecek şekilde nasıl yapılandırılacağı açıklanmaktadır.
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 78af54fec771e5012aca095d07fd772988a56029
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885388"
---
# <a name="set-up-pay-invoice-scenarios"></a>Fatura ödeme senaryolarını ayarlama

[!include [banner](includes/banner.md)]

Dynamics 365 Commerce'daki Fatura öde işlevi aşağıdakileri destekleyecek şekilde genişletilmiştir:

- Tek bir POS hareketinde birden fazla satış siparişi faturasının ödenmesi.
- Serbest metin faturaları, proje tabanlı faturalar ve alacak dekontları gibi çeşitli müşteri faturası türlerinin ödenmesi.

Bu senaryoları etkinleştirmek üzere, mağazalar için işlev profilinin aşağıda belirtildiği gibi yapılandırılması gerekir.

1. **Retail ve Commerce \> Kanal kurulumu \> POS ayarı \> POS profilleri \> İşlevsellik profilleri**'ne gidin ve değişiklikleri yapmak istediğiniz mağazalarla ilişkili bir profil seçin.
2. **İşlevler** sekmesinde, aşağıdaki parametreleri gerektiği gibi yapılandırın.

    - **Satış siparişi faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla satış siparişi tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.
    - **Serbest metin faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla serbest metin tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.
    - **Proje faturası**: Kullanıcıların tek bir POS hareketinde bir veya daha fazla proje tabanlı faturayı ödemesine izin vermek için **Evet**'i seçin.
    - **Satış siparişi alacak dekontu**: Kullanıcıların birden fazla satış siparişi tabanlı alacak dekontunu açık faturalara göre kapatmasına veya açık bir alacak dekontu için bir geri ödeme işlemi yapmasına izin vermek için **Evet**'i seçin.

> [!NOTE]
> Kısmi tutarları ödeme veya kapatma henüz desteklenmemektedir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]