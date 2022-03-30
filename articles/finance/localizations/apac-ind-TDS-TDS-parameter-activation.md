---
title: TDS parametrelerini ayarlama
description: Bu konu, belirtilen hareketlerdeki Kaynakta Kesilen Vergi (TDS) işlevini etkinleştirecek şekilde parametrelerin nasıl ayarlanabileceğini açıklar. Bu, Kaynakta Kesilen Vergi TDS özelliğini kullanmak için zorunlu bir adımdır.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: ca98a74753ca0de3b376cb89ef47862bc1bfb30e
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407522"
---
# <a name="set-the-tds-parameters"></a>TDS parametrelerini ayarlama

[!include [banner](../includes/banner.md)]

Bu konu, belirtilen hareketlerdeki Kaynakta Kesilen Vergi (TDS) işlevini etkinleştirecek şekilde parametrelerin nasıl ayarlanabileceğini açıklar. Bu, Kaynakta Kesilen Vergi TDS özelliğini kullanmak için zorunlu bir adımdır.

1. **Genel muhasebe\> Genel muhasebe ayarı \> Genel muhasebe parametreleri**'ne gidin.
2. **Doğrudan vergiler** sekmesinde, **Kaynakta Kesilen Vergi** bölümünde **TDS'yi etkinleştir** seçeneğini **Evet** olarak ayarlayarak TDS işlevini ve bunun için kullanılan sayfa ve alanları etkinleştirin.
3. TDS'yi fatura düzeyinde hesaplamak ve kesmek için kullanılan alanları etkinleştirmek için **Fatura** seçeneğini **Evet** olarak ayarlayın.
4. TDS'yi ödeme düzeyinde hesaplamak ve kesmek için kullanılan alanları etkinleştirmek için **Ödeme** seçeneğini **Evet** olarak ayarlayın.

    [![Doğrudan vergiler sekmesi.](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. **Numara sıraları** sekmesinde, **Referans** alanının **Stopaj vergisi ödemesi** olarak ayarlandığı satırı bulun. **Numara sırası kodu** alanında, satır için numara sırası kodunu seçin. Numara sırası kodu, dönemsel TDS kapatma işlemi için fiş numaraları oluşturmak amacıyla kullanılır.

    > [!NOTE]
    > Dönemsel TDS kapatma işlemini çalıştırmak için, **Vergi \> Beyannameler \> Stopaj vergisi \> Stopaj vergisi ödemesi**'ne gidin.

    [![Numara serileri sekmesi.](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. Sayfayı kapatın.
