---
title: Serbest metin faturası sayfasındaki faturalarda TDS hesaplaması
description: Bu konu, faturalardaki Kaynakta Kesilen Verginin (TDS) serbest metin faturası sayfasını kullanarak nasıl hesaplanacağını açıklamaktadır.
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
ms.openlocfilehash: 5a1960974dff90ef5f0cc8eab018351a9e412858
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725191"
---
# <a name="tds-calculation-on-invoices-from-the-free-text-invoice-page"></a>Serbest metin faturası sayfasındaki faturalarda TDS hesaplaması

[!include [banner](../includes/banner.md)]

Bu konu, faturalardaki Kaynakta Kesilen Verginin (TDS) **Serbest metin faturası** sayfasını kullanarak nasıl hesaplanacağını açıklamaktadır.

1. **Alacak hesapları \> Faturalar \> Tüm serbest metin faturaları**'na gidin.

    [![Serbest metin faturası sayfası.](./media/apac-ind-TDS-57-1.png)](./media/apac-ind-TDS-57-1.png)

2. Serbest metin faturası oluşturmak için **Yeni**'yi seçin ve gerekli ayrıntıları girin.
3. **Fatura** sekmesini seçin. **Stopaj vergisi grubu** bölümündeki **Değerlendirilenin yapısı** alanı, müşterinin değerlendirilen kategorisinin yapısını gösterir.
4. **TDS grubu** alanında, satıcı veya müşteri için tanımlanmış varsayılan TDS grubunu görüntüleyebilir veya değiştirebilirsiniz.

    > [!NOTE]
    > **TDS grubu** alanında bir değer seçtiğinizde, **TCS grubu** alanı kullanılamaz hale gelir. TDS yalnızca, **Tüm müşteriler** sayfasındaki müşteri için **Stopaj vergisini hesapla** seçeneği **Evet** olarak belirlenmişse hesaplanır.

5. **Vergi bilgileri** sekmesinde, **Şirket bilgileri** bölümünde, **Ad** alanında, şirket için ayarlanmış alternatif adresin şirket adını seçin.

    **Stopaj vergisi** bölümünde, **Vergi Hesap Numarası (TAN)** alanı, seçilen şirketin vergi hesap numarasını (TAN) gösterir.

6. **Fatura satırları** sekmesinde, fatura satırları oluşturun ve gerekli ayrıntıları girin.

    **Stopaj vergisi grubu** bölümünde, **Vergi hesap numarası (TAN)** alanı TAN'ı gösterirken **TDS grubu** alanı ise TDS grubunu gösterir.

7. **Geçici stopaj vergisi hareketleri** sayfasını açmak için **Stopaj vergisi**'ni seçin. Bu sayfanın üst bölümünde aşağıdaki alanlar vardır:

    - **Stopaj vergisinin toplam tutar değeri** – TDS grubunun hareketleri için hesaplanan toplam TDS.
    - **Değer** – Hareket için TDS hesaplamasında kullanılan toplam yüzde. Toplam yüzde, TDS grubu ve iliştirilmiş TDS vergi kodları için tanımlanan formüle dayanır.
    - **Düzeltilmiş stopaj vergisi tutarı** –  TDS grubundaki tüm vergi kodları için toplam düzeltilmiş TDS tutarı.
    - **TDS** – Seçili bir onay kutusu, TDS grubunun harekete iliştirildiği anlamına gelir.

    **Genel bakış**, **Genel** ve **Düzeltme** sekmelerindeki alanlar, TDS grubuna iliştirilmiş her TDS vergi kodu için hesaplanmış TDS tutarı ve düzeltilmiş TDS tutarı ayrıntılarını görüntüler.

8. Belirli bir TDS vergi koduna iliştirilmiş TDS vergi bileşeni için tanımlanan eşik sınırını gözden geçirmek için **Eşik** sayfasını açmak üzere **Eşik**'i seçin.
9. Belirli bir TDS vergi kodu için tanımlanan formülü gözden geçirebileceğiniz **Formül tasarımcısı** sayfasını açmak için **Formül tasarımcısı**'nı seçin.
10. Serbest metin faturasını deftere nakledin. Serbest metin faturaları için hesaplanan TDS tutarı, TDS grubundaki her bir TDS vergi kodu için tanımlanan alacak hesabına nakledilir. TDS vergi kodları için borç hesapları **Stopaj vergisi kodları** sayfasında tanımlanmıştır.
11. **Stopaj vergisi hareketleri** sayfasını açmak için **Deftere nakledilen stopaj vergisi**'ni seçin. **Değer** alanı, hareket için TDS hesaplamasında kullanılan toplam yüzdeyi gösterir.

    **Genel bakış**, **Genel** ve **Tutar** sekmelerindeki alanlar, fatura satırlarında hesaplanan TDS tutarlarını gösterir.

12. TDS grubuna iliştirilmiş her TDS vergi kodu için TDS hesaplama bilgilerini inceleyin.
