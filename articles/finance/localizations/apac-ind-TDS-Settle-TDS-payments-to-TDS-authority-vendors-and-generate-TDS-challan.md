---
title: TDS yetkili satıcılarına TDS ödemelerini kapatma ve TDS irsaliyesi oluşturma
description: Bu konu, TDS yetkili satıcılarına yapılan Kaynakta Kesilen Vergi (TDS) ödemelerinin nasıl kapatılacağını açıklar.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023665"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a>TDS yetkili satıcılarına TDS ödemelerini kapatma ve TDS irsaliyesi oluşturma

[!include [banner](../includes/banner.md)]

Bu konu, TDS yetkili satıcılarına yapılan Kaynakta Kesilen Vergi (TDS) ödemelerinin nasıl kapatılacağını açıklar.

1. **Borç hesapları \> Ödemeler \> Satıcı ödeme günlüğü**'ne gidin.

    [![Satıcı ödeme günlüğü sayfası](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)

2. **Satıcı ödeme günlüğü** sayfasında, günlük satırı oluşturmak için **Yeni**'yi seçin.
3. **Hesap** alanında adına TDS ödemelerinin kapatılacağı TDS yetkili satıcısını seçin.
4. TDS yetkili satıcısı için kapatılan TDS hareketlerini görüntüleyebileceğiniz **Kapatma hareketleri** sayfasını açmak için **Kapatma hareketleri**'ni seçin.

    Bir kapatma dönemi için kapatılan TDS hareketleri aşağıdaki şekilde görüntülenir:

    - Değerlendirilen kategori yapısı **Şirket** olan TDS hareketleri bir hareket satırı olarak gösterilir.
    - Değerlendirilen kategori hapısı **HUF**, **Firma**, **Birey**, **AOP**, **BOI**, **Yerel makam** veya **Diğer** olan TDS hareketleri bir hareket satırı olarak gösterilir.
    - **Tutar** alanı, TDS yetkili satıcısına ödenmesi gereken toplam TDS tutarını gösterir.

5. Kapatma kaydı için dahil edilen farklı TDS hareketlerini görüntülemek için **Stopaj vergisi hareketleri**'ni seçin. Bu sayfadaki kapatma dönemine ait kapatma işlemine dahil edilen her TDS hareketinin bölünmesini görüntüleyebilirsiniz.
6. **Genel bakış** sekmesinde, TDS yetkili satıcısına kapatılacak TDS hareketlerinin **İşaretle** onay kutusunu seçin.

    **Genel bakış** sekmesi, her açık TDS hareketiyle ilgili olarak aşağıdaki bilgileri gösterir:

    - **Tarih** – TDS hareketi tarihi.
    - **Fiş** – Fiş numarası.
    - **Kaynak** – TDS hareketinin içinde deftere nakledildiği modül.
    - **Satıcı/Müşteri** – TDS'nin kesildiği satıcı veya müşteri hesap numarası.
    - **Kesinti yapılan kişi/tarafın adı** – TDS'nin kesildiği satıcı veya müşterinin adı.
    - **Değerlendirilen yapısı** – Kesinti yapılan tarafın ait olduğu değerlendirilen kategorisi yapısı.
    - **Tutar** – TDS'nin üzerinde hesaplandığı fatura tutarı.
    - **Vergi tutarı** – Hareket için hesaplanan TDS tutarı.

    > [!NOTE]
    > TDS yetkili satıcısına kapatılmaması gereken tüm TDS hareketleriyle ilgili **İşaret** onay kutusunu kaldırın.

    **Genel** sekmesinde, **PAN** alanı kesinti yapılan tarafın kalıcı hesap numarasını (PAN) görüntüler. **Tarih** alanı TDS hesaplamasının tarihini ve **Değer** alanı, TDS hesaplaması için kullanılan toplam yüzdeyi gösterir.

7. TDS hareketiyle ilgili fiş girişlerini görüntülemek için **Fiş**'i seçin.
8. Sayfayı kapatın.
10. Belirli bir TDS vergi koduyla ilgili her TDS vergi bileşeni için hesaplanan TDS'yi görüntüleyebileceğiniz **Stopaj vergisi bileşenleri** sayfasını açmak için **Stopaj vergisi bileşenleri**'ni seçin.

    **Genel bakış** sekmesinde, **Vergi bileşeni** alanı hareket için kullanılan TDS vergi bileşenini gösterir. **Tutar** alanı, TDS vergi bileşeni için hesaplanan TDS tutarını baz para birimi cinsinden gösterir. **Birikmiş tutar** alanı, tüm kapatılan hareketleriyle ilgili olarak TDS vergisi bileşeni için hesaplanan toplam TDS tutarını gösterir.

    **Tutar** sekmesinde, **Varsayılan para birimi** bölümü, TDS vergisi bileşeni için hesaplanan TDS tutarını varsayılan para birimi cinsinden gösterir. **İkincil para birimi** bölümü, tutarı ikincil para birimi cinsinden gösterir.

11. **Stopaj vergisi bileşenleri** sayfasını kapatın.
12. **Açık hareket düzenlemesi** sayfasındaki **Tutar** alanında, kapatma dönemi için TDS yetkili satıcısına kapatılacak toplam tutarın güncelleştirilip güncelleştirilmediğine dikkat edin.
13. Farklı TDS kapatma dönemlerindeki TDS hareketlerini, TDS yetkili satıcısına kapatmak için harekete ait **İşaret** onay kutusunu seçin.
14. **Açık hareket düzenleme** sayfasını kapatın.

    > [!NOTE]
    > **Stopaj vergisi hareketleri** sayfasında kapatılmak üzere yalnızca birkaç hareket seçilmişse, seçili hareketlerin toplam TDS tutarı **Açık hareket düzenleme** sayfasındaki **Düzeltme** alanında güncelleştirilir. Düzeltme tutarı, **Günlük fişi** sayfasındaki günlük satırında güncelleştirilir ve **Açık hareket düzenleme** sayfası kapatılır.

    **Günlük fişi** sayfasında, **Borç** alanı, TDS yetkili satıcısına ödenecek toplam tutarı gösterir.

15. Mahsup hesap ayrıntılarını girin.

    > [!NOTE]
    > TDS hareketlerinin farklı Vergi Hesap Numaraları (TAN'lar) olması durumunda, **Günlük fişi** sayfasında günlük satırları TAN başına oluşturulur.

16. **Ödeme ücreti** sekmesinde, **Ücret kodu** alanında, TDS yetkili satıcısına yapılan gecikmeli ödemeler için ödeme ücreti almak üzere ücret tipi **Faiz** veya **Diğer** olan bir ücret kimliği seçin.

    **Vergi bilgileri** sekmesinde, **Şirket bilgileri** bölümünde, **Ad** alanında şirket adı gösterilir. **Stopaj vergisi** bölümünde, **Vergi Hesap Numarası (TAN)** alanı hareket satırına iliştirilen TAN'ı gösterir.

17. Günlüğü doğrulayın ve deftere nakledin.
18. Harekete ait irsaliye ayrıntılarını girmek için **Stopaj vergisi \> İrsaliye bilgileri**'ni seçin.

    **Fiş** alanı, hareketin fiş numarasını görüntüler.
    
19. TDS tutarı, defter girişi kullanılarak yatırılmışsa **Defter girişiyle yatırılan TDS** onay kutusunu seçin.
20. **İrsaliye numarası** alanına, TDS yetkili satıcısına yapılacak ödemeyi gerçekleştirmek için kullanılan irsaliye numarasını girin.
21. **Tarih** alanına irsaliye tarihini girin.
22. **Banka adı** alanında, TDS yetkili satıcısına ödenecek TDS tutarının yatırılması gereken bankanın adını seçin. Bu alan, TDS yetkili satıcısı için **Borç hesapları \>Tüm satıcılar \> Kurulum \> Banka hesapları**'nda kurulan tüm banka hesaplarını listeler.
23. **BSR kodu** alanında, bankanın Temel İstatistik İade (BSR) kodunu girin.
24. Sayfayı kapatın.

### <a name="example"></a>Örnek

Dönemsel TDS kapatma işlemi kullanılarak 01/04/2009 döneminin **Kira** TDS bileşen grubu kapatılmış. Toplam TDS tutarı olan 141.625,00 değeri, TDS kapatma dönemi için TDS satıcısı yetkili hesabına nakledilmiş. Bu tutarı, TDS yetkili satıcısının **Açık hareket düzenleme** sayfasındaki **Tutar** alanında görüntüleyebilirsiniz.

Dönem için kapatılan farklı TDS hareketlerini görüntülemek için **Stopaj vergisi hareketleri**'ni seçerseniz, aşağıdaki bilgiler görüntülenir.

| TDS tutarı |
|------------|
| 16,995.00  |
| 22,660.00  |
| 28,325.00  |
| 16,995.00  |
| 28,325.00  |
| 16,995.00  |
| 11,330.00  |

Belirli bir TDS tutarı için, belirli bir TDS vergi koduyla ilgili her TDS vergi bileşeni için hesaplanan TDS'yi görüntülemek için **Stopaj vergisi bileşenleri**'ni seçebilirsiniz. Bu örnekte, 16.995,00 değerindeki TDS tutarı için **Stopaj vergisi bileşenleri**'ni seçtiniz. Hareket için bileşen başına hesaplanan vergi tutarı görüntülenir.

| Vergi bileşeni | Tutar    | Kümülatif tutar |
|---------------|-----------|--------------------|
| TDS           | 1,5000.00 | 125,000.00         |
| Ek maliyet     | 1,500.00  | 12,500.00          |
| PE-Cess       | 330.00    | 2,750.00           |
| SHE Cess      | 165.00    | 1,375.00           |

**Stopaj vergi hareketleri** sayfasında TDS tutarları olarak yalnızca 16.995,00, 22.660,00 ve 28.325,00 değerlerini seçtiyseniz **Açık hareket düzenleme** sayfasında **Düzeltme** alanında kapatmanın toplam tutarı olarak **67.980,00** gösterilir. Bu hareket kapatılmak üzere işaretlenmişse ve **Açık hareket düzenleme** sayfası kapatılırsa, **67.980,00** tutarı, **Günlük fişi** sayfasındaki **Borç** alanında gösterilir.

Artık günlüğü deftere nakledebilir ve TDS irsaliyesi oluşturabilirsiniz.

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a>TDS yetkili satıcılarına yapılan avans ödemesi düzeltmeleri

TDS yetkili satıcısına yapılan bir avans ödemesini gerçek bir ödemeye düzeltmek için **Borç hesapları \> Satıcılar \> Tüm satıcılar \> Hareketleri düzenleme**'ye gidin. Yapılan gerçek ödeme, avans ödemesini aşıyorsa hareket için iki irsaliye numarası oluşturulur. Ancak, TDS sorgusunda yalnızca ilk irsaliye numarası görüntülenir.
