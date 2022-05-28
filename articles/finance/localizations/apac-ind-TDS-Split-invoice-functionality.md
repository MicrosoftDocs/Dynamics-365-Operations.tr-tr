---
title: Fatura bölme işlevi
description: Bu konu, faturaları teslimat adresine ve vergi hesap numarasına (TAN) göre bölmeye yönelik kurulum ve işlevleri açıklamaktadır.
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
ms.openlocfilehash: f1dac8d51c24009dcf0c4acbc49f06f32abf0dec
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724683"
---
# <a name="split-invoice-functionality"></a>Fatura bölme işlevi

[!include [banner](../includes/banner.md)]

Bu konu, faturaları teslimat adresine ve vergi hesap numarasına (TAN) göre bölmeye yönelik kurulum ve işlevleri açıklamaktadır.

**Satınalma siparişi** sayfasında farklı teslimat adresleri ve TAN'ları olan bir ürün girişini veya faturasını deftere nakletmek ve bölmek için **Borç hesapları parametreleri** sayfasında **Genel** sekmesinde **Ürün girişi** veya **Fatura** onay kutusunu seçin. Deftere nakledilen fatura, teslimat adresine ve TAN'a göre bölünür.

**Satış siparişi** sayfasında farklı fatura satırları için farklı teslimat adresleri ve TAN'lar belirlenmiş bir onayı, malzeme çekme listesini, sevk irsaliyesini ya da faturayı deftere nakletmek ve bölmek için **Özet güncelleştirmesi** sekmesinde, **Bölme temeli** hızlı sekmesinde, **Teslimat bilgileri** satırında, **Onay**, **Malzeme çekme listesi**, **Sevk irsaliyesi** veya **Fatura** seçeneğini **Evet** olarak ayarlayın. Fatura öncelikle teslimat adresine göre ve ardından TAN'a göre bölünür.

> [!IMPORTANT]
> - **Teslimat bilgileri** için hiçbir seçenek **Evet** olarak ayarlanmamışsa , fatura tek bir fatura olarak deftere nakledilir. Fatura bölme gerçekleştirilmez.
> - Fatura satırlarının farklı teslimat adresleri ve TAN'ları bulunan bir sevk irsaliyesini ayırmak ve deftere nakletmek için **Teslimat bilgileri**'nin **Sevk irsaliyesi** seçeneğini **Evet** olarak ayarlamalısınız.
> - Fatura satırlarının farklı teslimat adresleri ve TAN'ları bulunan bir faturayı ayırmak ve deftere nakletmek için **Teslimat bilgileri**'nin **Fatura** seçeneğini **Evet** olarak ayarlamalısınız.
> - Fatura satırlarının teslimat adresleri farklı olup TAN'ları aynı olan faturayı ayırmak ve deftere nakletmek için **Teslimat bilgileri**'nin **Fatura** seçeneğini **Hayır** olarak ayarlamalısınız. Fatura, teslimat adresine göre bölünür.

## <a name="example"></a>Örnek

Bu örnekte, **Teslimat bilgileri**'nin **Fatura** seçeneği **Borç hesapları parametreleri** sayfasındaki **Özet güncelleştirmesi** sekmesinde **Evet** olarak ayarlanır. Satırlarda teslimat adresleri ve TAN'ları için aşağıdaki ayarlara sahip olan bir satınalma faturası deftere nakledilir:

- **Madde satırı 1:** Teslimat adresi 1, TAN-ABCD12345A
- **Madde satırı 2:** Teslimat adresi 1, TAN-ABCD12345A
- **Madde satırı 3:** Teslimat adresi 2, TAN-ABCE12345B
- **Madde satırı 4:** Teslimat adresi 3, TAN-ABCD12345A

Bu durumda, orijinal fatura iki faturaya bölünür ve aşağıdaki şekilde deftere nakledilir:

- İki satırın da teslimat adresi ve TAN'ı aynı olduğu için Fatura 1 madde satırı 1 ve madde satırı 2 için deftere nakledilir.
- Fatura 2, madde satırı 3 için deftere nakledilir.
- Fatura 3, madde satırı 4 için deftere nakledilir.
