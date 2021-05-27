---
title: Ödemeler ve senetlerde TDS hesaplaması
description: Bu konu, Kaynakta Kesilen Verginin (TDS) hesaplandığı farklı ödeme hareketleri hakkında referans bilgileri sağlar.
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
ms.openlocfilehash: ea57963e41b90bbc11efa00b85aad8bc60c2357d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023660"
---
# <a name="tds-calculation-on-payments-and-promissory-notes"></a>Ödemeler ve senetlerde TDS hesaplaması

[!include [banner](../includes/banner.md)]

Bu konu, Kaynakta Kesilen Verginin (TDS) hesaplandığı farklı ödeme hareketleri hakkında referans bilgileri sağlar.

| Seri numarası | Hareket türü | Hareket tutarı | Sayfa adı ve yol | Hesap türü ve mahsup hesap türü |
|---------------|------------------|--------------------|--------------------|--------------------------------------|
| 1             | Avans ödemesi/Faturaya karşı ödeme (TDS borçları) | Borç veya Alacak | <ul><li>Genel muhasebe (**Genel muhasebe \> Günlük girişleri \> Yevmiye defterleri**).</li><li>Fatura günlüğü (**Borç hesapları \> Faturalar \> Fatura günlüğü**)</li><li>Ödeme günlüğü (**Borç hesapları \> Ödemeler \> Satıcı ödeme günlüğü**)</li></ul> | Satıcı (Dr.) Banka (Cr.) |
| 2             | Avans ödemesi/Faturaya karşı ödeme (Müşteriden yapılan satınalma - TDS borçları) | Borç veya Alacak | <ul><li>Genel muhasebe (**Genel muhasebe \> Günlük girişleri \> Yevmiye defterleri**).</li><li>Fatura günlüğü (**Borç hesapları \> Faturalar \> Fatura günlüğü**)</li><li>Ödeme günlüğü (**Borç hesapları \> Ödemeler \> Satıcı ödeme günlüğü**)</li></ul> | Müşteri (Dr.) Banka (Cr.) |
| 3             | Senetler | Borç | Düzenlenen senet günlüğü (**Borç hesapları \> Ödemeler \> Senetler \> Düzenlenen senet günlüğü**) | Satıcı (Dr.) Genel Muhasebe (Cr.) |
| 4             | Diğer gelirler (TDS alacağı) | Borç veya Alacak | Genel muhasebe (**Genel muhasebe \> Günlük girişleri \> Yevmiye defterleri**). | Banka (Dr.) Genel Muhasebe (Cr.) |
| 5             | Diğer giderler (TDS borçları) | Borç veya Alacak | Genel muhasebe (**Genel muhasebe \> Günlük girişleri \> Yevmiye defterleri**). | Banka (Dr.) Genel Muhasebe (Cr.) |

Ödemelerde ve senetlerde TDS'yi hesaplamak için bu adımları izleyin.

1. Günlük sayfalarında günlük satırları oluşturun. Hesap türü ve mahsup hesap türünü seçin.
2. **Açık hareket düzenleme** sayfasını açmak için **İşlevler \> Kapatma**'yı seçin. Ardından, kapatılması gereken belirli bir fatura seçin. TDS, fatura düzeyinde zaten hesaplanmışsa **Tutar kaynağı** alanı TDS'nin hesaplandığı taban tutarını gösterir. **TDS tutarı** alanı, hareket için hesaplanan TDS tutarını gösterir. **Tutar** alanı, net ödeme tutarını (yani, TDS kesildikten sonraki ödeme tutarını) gösterir.

    > [!NOTE]
    > Bir faturaya karşı yapılan bir ödeme için aşağıdaki koşullar geçerlidir:
    >
    > - Ödeme tutarı ve fatura tutarı aynıysa, fatura düzeyinde zaten hesaplanmış olan TDS hesaplanmaz.
    > - TDS tutarı kesildikten sonraki fatura tutarı, ödeme tutarından fazlaysa TDS hesaplanmaz.
    > - TDS kesildikten sonraki fatura tutarı ödeme tutarından azsa TDS, fatura tutarını aşan tutar üzerinde hesaplanır.

3. **Günlük fişi** sayfasında, **Genel bakış** sekmesinde, **TDS grupları** alanında satıcı veya müşteri için tanımlanan varsayılan TDS grubunu görüntüleyin veya değiştirin. Günlük satırlarında hesaplanan TDS, TDS grubunda listelenen TDS vergi kodları için belirlenen formüle dayanır.

    > [!NOTE]
    > TDS yalnızca, **Satıcıları** sayfasındaki satıcı için **Stopaj vergisini hesapla** seçeneği **Evet** olarak belirlenmişse hesaplanır.

4. **Vergi bilgileri** sekmesinde, **Şirket bilgileri** bölümünde, **Ad** alanında, şirket için ayarlanmış alternatif adresler için bir şirket adı seçebilirsiniz.

    **Stopaj vergisi** alan grubunun altındaki **Değerlendirilenin yapısı** alanı, satıcı veya müşterinin değerlendirilen yapısı kategorisini gösterir. **Vergi hesap numarası (TAN)** alanı, seçilen şirketin vergi hesap numarasını (TAN) gösterir.

5. **Geçici stopaj vergisi hareketleri** sayfasını açmak için **Stopaj vergisi düğmesi \> stopaj vergisi**'ni seçin. Bu sayfanın üst bölümünde aşağıdaki alanlar vardır:

    - **Stopaj vergisinin toplam tutar değeri** – TDS grubunun hareketleri için hesaplanan toplam TDS.
    - **Değer** – Hareket için TDS hesaplamasında kullanılan toplam yüzde. Toplam yüzde, TDS grubu ve iliştirilmiş TDS vergi kodları için tanımlanan formüle dayanır.
    - **Düzeltilmiş stopaj vergisi tutarı** –  TDS grubundaki tüm vergi kodları için toplam düzeltilmiş TDS tutarı.
    - **TDS** – Seçili bir onay kutusu, TDS grubunun harekete iliştirildiği anlamına gelir.

    **Genel bakış**, **Genel** ve **Düzeltme** sekmelerindeki alanlar, TDS grubuna iliştirilmiş her TDS vergi kodu için hesaplanmış TDS tutarı ve düzeltilmiş TDS tutarı ayrıntılarını görüntüler.

6. Belirli bir TDS vergi koduna iliştirilmiş TDS vergi bileşeni için tanımlanan eşik sınırını gözden geçirmek için **Eşik** sayfasını açmak üzere **Eşik**'i seçin.
7. Belirli bir TDS vergi kodu için tanımlanan formülü gözden geçirebileceğiniz **Formül tasarımcısı** sayfasını açmak için **Formül tasarımcısı**'nı seçin.
8. **Günlük fişi** sayfasına dönmek için **Formül tasarımcısı**'nı ve **Geçici stopaj vergisi hareketleri** sayfalarını kapatın.
9. Günlüğü doğrulayın ve deftere nakledin. Hesaplanan TDS tutarı, TDS grubundaki her bir TDS vergi kodu için tanımlanan borç hesabına nakledilir. TDS vergi kodları için borç hesapları **Stopaj vergisi kodları** sayfasında tanımlanmıştır.
10. **Stopaj vergisi hareketleri** sayfasını açmak için **Deftere nakledilen stopaj vergisi**'ni seçin. **Değer** alanı, hareket için TDS hesaplamasında kullanılan toplam yüzdeyi gösterir.

    **Genel bakış**, **Genel** ve **Tutar** sekmelerindeki alanlar, harekete iliştirilen TDS grubu için hesaplanan TDS tutarlarını gösterir.

11. TDS grubuna iliştirilmiş her TDS vergi kodu için TDS hesaplama bilgilerini inceleyin.

## <a name="generate-payments"></a>Ödeme oluştur

Ödemeler oluşturmak için aşağıdaki adımları izleyin.

1. Şu adımlardan birini izleyin:

    - **Borç hesapları \> Ödemeler \> Satıcı ödeme günlüğü**'ne gidin.
    - **Alacak hesapları \> Ödemeler \> Müşteri ödeme günlüğü** seçeneğine gidin.
    - **Borç hesapları \> Ödemeler \> Senetler \> Düzenlenen senet günlüğü**'ne gidin.
    - **Alacak hesapları \> Ödemeler \> Kambiyo senedi \> Düzenlenen kambiyo senetleri günlüğü'** ne gidin.
    - **Alacak hesapları \> Ödemeler \> Kambiyo senedi \> Yeniden düzenlenen kambiyo senetleri günlüğü**'ne gidin.

2. **Satırlar**'ı seçin.
3. **İşlevler \> Ödemeler oluştur**'u seçin.
