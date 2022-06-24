---
title: Borç hesaplarında ve Alacak hesaplarında TDS parametrelerini ayarlama
description: Bu makalede, Kaynakta Kesilen Vergi (TDS) kesintilerini desteklemek için Borç hesapları ve Alacak hesaplarının parametrelerinin nasıl ayarlanacağı açıklanmaktadır.
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
ms.openlocfilehash: e547b92f9f7e0ccc5b92df4cd991ce402369b568
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883164"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>Borç hesaplarında ve Alacak hesaplarında TDS parametrelerini ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, Kaynakta Kesilen Vergi (TDS) kesintilerini desteklemek için Borç hesapları ve Alacak hesaplarının parametrelerinin nasıl ayarlanacağı açıklanmaktadır.

1. **Vergi \> Kurulum \> Parametreler \> Alacak hesapları parametreleri**'ne gidin.
2. **Güncelleştirmeler** sekmesinde, **Sipariş satırlarını güncelleştir** iletişim kutusunu açmak için **Sipariş satırlarını güncelleştir**'i seçin.
3. **TDS grubu** bölümünde, **TDS grubunu güncelleştirme** alanında, satır düzeyinde TDS grubunu güncelleştirmek için kullanılacak yöntemi belirtin. Bu ayar, bir sipariş başlığında TDS grubu güncelleştirildiğinde kullanılır. Aşağıdaki seçenekler bulunur:

    - **Hiçbir zaman** – TDS grubu sipariş başlığında güncelleştirildiğinde, sipariş satırlarında güncelleştirilmez.
    - **Her zaman** – TDS grubu sipariş başlığında güncelleştirildiğinde, sipariş satırlarında otomatik olarak güncelleştirilir.
    - **İstek** – Kullanıcılar, sipariş satırlarında TDS grubunu güncelleştirmelerini isteyen bir ileti alır.
4. **Tamam**'ı seçin.

    [![Sipariş satırlarını güncelleştirme iletişim kutusu.](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. **Vergi \> Kurulum \> Parametreler \> Borç hesapları parametreleri**'ne gidin.
6. **Genel** sekmesinde **Teslimat bilgilerine göre böl** hızlı sekmesinde, farklı teslimat adresleri ve vergi hesap numaraları (TAN'lar) olan bir ürün girişini nakletmek ve bölmek için **Ürün girişi** seçeneğini **Evet** olarak ayarlayın. Bu seçenek **Hayır** olarak ayarlanırsa, farklı teslimat adresleri ve TAN'ları bulunan bir satınalma sevk irsaliyesini deftere nakledemezsiniz.
7. Farklı teslimat adresleri ve TAN'ları olan bir satınalma faturasını deftere nakletmek ve bölmek için **Fatura** seçeneğini **Evet** olarak ayarlayın.

    [![Teslimat bilgilerine göre böl hızlı sekmesi.](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Sayfayı kapatın.
