---
title: TDS imtiyaz sertifikası numaralarını kaydetme
description: Bu konu, satıcılara verilen Kaynakta Kesilen Vergi (TDS) imtiyaz sertifikası numaralarının nasıl kaydedileceğini açıklar.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 97fce25ea8c556f001c84f6836a0a270a9f3524f
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358398"
---
# <a name="record-tds-concession-certificate-numbers"></a>TDS imtiyaz sertifikası numaralarını kaydetme

[!include [banner](../includes/banner.md)]

Bu konu, satıcılara verilen Kaynakta Kesilen Vergi (TDS) imtiyaz sertifikası numaralarının nasıl kaydedileceğini açıklar.

1. **Vergi \> Dolaylı vergiler \> Stopaj vergisi \> Stopaj vergisi imtiyazları**'na gidin.
2. **Vergi türü** alanında, TDS vergi türü için imtiyaz sertifikalarını kaydetmek üzere **TDS**'yi seçin.
3. Bir satır oluşturmak için, **Genel bakış** sekmesinde **Alt+N**'yi seçin.

    [![Yeni satırın başlığı.](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. **Stopaj vergisi kodu** alanında, satıcı imtiyaz sertifikalarının verildiği TDS vergi kodunu seçin. **Stopaj vergisi kodu adı** alanı, TDS vergi kodunun adını gösterir.
5. **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında, imtiyazlı temele göre satıcı için TDS'yi hesaplamak üzere TDS vergi kodunu kullanan imtiyaz sertifikasının geçerlilik süresini tanımlayın.
6. **Açıklamalar** alanına açıklamaları girin.
7. **Bölüm** alanında, TDS imtiyaz sertifikasının altında bulunduğu yasal bölüm kodunu girin.

    Bölüm kodu 197 ise, "A" değeri Form 26Q'daki "Kesinti olmaması/düşük kesinti nedeni" sütununda ve Form 27Q'da "Kesinti olmaması/düşük kesinti/brütleştirme (varsa) nedeni" sütununda görüntülenir. Bölüm kodu 197A ise, bu iki sütunda da "B" değeri görünür.

8. Satıcılara ait TDS imtiyaz sertifikası numaralarını kaydetmek için **Sertifika** hızlı sekmesini seçin.
9. **Satıcı hesabı** alanında, TDS imtiyaz sertifikasının verildiği satıcı hesabını seçin.
10. **Başlangıç tarihi** ve **Bitiş tarihi** alanlarında, TDS imtiyaz sertifikasının geçerlilik dönemini belirtin.

    TDS'nin imtiyazlı temele göre hesaplanması, satıcı için sertifikanın oluşturulduğu döneme dayanır.

11. **Sertifika** alanında, TDS imtiyaz sertifika numarasını girin.

    [![Sertifika hızlı sekmesi.](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Sayfayı kapatın.
