---
title: TDS tahsisatıyla ödeme planlarını ayarlama
description: Bu konu, Kaynakta Kesilen Vergi (TDS) tahsisatıyla ödeme planlarının nasıl ayarlanacağını açıklar.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 63628e84da4e430df236f3afa89110b652110fcb
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726619"
---
# <a name="set-up-payment-schedules-with-tds-allocation"></a>TDS tahsisatıyla ödeme planlarını ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, Kaynakta Kesilen Vergi (TDS) tahsisatıyla ödeme planlarının nasıl ayarlanacağını açıklar.

1. **Borç hesapları \> Ödeme kurulumu \> Ödeme planları**'na gidin.

    [![Ödeme planları sayfası.](./media/apac-ind-TDS-27.png)](./media/apac-ind-TDS-27.png)

2. Eylem bölmesinde, ödeme planı oluşturmak üzere **Yeni**'yi seçin ve gerekli ayrıntıları girin.
3. **Tahsisat** alanında, ödeme planı için ödemeyi tahsis etmek üzere kullanılacak yöntemi seçin:

    - Toplam
    - Sabit tutar
    - Sabit miktar
    - Belirtilen

    **Stopaj vergisi tahsisatı** alanı, ödeme planı için TDS tahsisat yöntemini gösterir. **Tahsisat** alanında **Toplam**'ı seçerseniz, **Stopaj vergisi tahsisatı** alanı otomatik olarak **Toplam**'a ayarlanır. **Sabit tutar**, **Sabit miktar**'ı veya **Tahsisat** alanında **Belirtilen**'i seçerseniz, **Stopaj vergisi tahsisatı** alanı otomatik olarak **Orantılı** olarak ayarlanır.

    > [!NOTE]
    > **Stopaj vergisi tahsisatı** alanı **Toplam** olarak ayarlanmışsa, ödeme taksitleri TDS tutarını içeren brüt tutar temel alınarak hesaplanır. **Stopaj vergisi tahsisatı** alanı **Orantılı** olarak ayarlanmışsa, ödeme taksitleri TDS tutarı kesildikten sonra net fatura tutarı temel alınarak hesaplanır.

4. Gerekli diğer ayrıntıları girin ve sayfayı kapatın.
