---
title: TDS parametrelerini ayarlama
description: Bu makalede, parametrelerin belirtilen hareketlerde Kaynakta Kesilen Vergi (TDS) işlevini etkinleştirecek şekilde nasıl ayarlanabileceği açıklanmaktadır. Bu, Kaynakta Kesilen Vergi TDS özelliğini kullanmak için zorunlu bir adımdır.
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
ms.openlocfilehash: 3390cad6979858fbff73769d0d25132ba18a2157
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865627"
---
# <a name="set-the-tds-parameters"></a>TDS parametrelerini ayarlama

[!include [banner](../includes/banner.md)]

Bu makalede, parametrelerin belirtilen hareketlerde Kaynakta Kesilen Vergi (TDS) işlevini etkinleştirecek şekilde nasıl ayarlanabileceği açıklanmaktadır. Bu, Kaynakta Kesilen Vergi TDS özelliğini kullanmak için zorunlu bir adımdır.

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
