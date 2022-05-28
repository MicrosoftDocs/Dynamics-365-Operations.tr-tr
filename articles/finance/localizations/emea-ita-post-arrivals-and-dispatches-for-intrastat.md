---
title: İntrastat için gelenlerin ve gönderimleri deftere nakletme
description: Bu konuda, İntrastat için gelenlerin ve gönderimlerin deftere nasıl nakledileceğini gösteren bir örnek sağlanmaktadır.
author: anasyash
ms.date: 8/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 4ab4402740d199043519773b18732bdde9a0fb2f
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724797"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>İntrastat için gelenlerin ve gönderimleri deftere nakletme

[!include [banner](../includes/banner.md)]

Bu konuda, İntrastat için gelenlerin ve gönderimlerin deftere nasıl nakledileceğini gösteren bir örnek sağlanmaktadır. Bu örnek, **ITCO** tüzel kişiliğini kullanır.

## <a name="setup"></a>Ayar

1. Aşağıdaki Elektronik raporlama (ER) yapılandırmalarının en son sürümünü içeri aktarın:

    - Intrastat modeli
    - Intrastat raporu
    - İntrastat (IT)

    [Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indirme](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md) içinde daha fazla ayrıntı bulabilirsiniz.

2. Microsoft Dynamics 365 Finance'te aşağıdaki sayı dizilerini sürekli olarak tanımlayın: **Gene\_397**, **Acco\_16403**, **Gene\_407** ve **PUR\_EU**.

    1. **Kuruluş yönetimi** > **Numara serileri** > **Numara serileri**'ne tıklayın.
    2. Izgarada, numara serisi kodlarından birini seçin.
    3. Eylem Bölmesi'nde, **Düzenle**'yi seçin.
    4. **Genel** hızlı sekmesinde, **Kurulum** bölümünde, **Sürekli** seçeneğini **Evet** olarak ayarlayın.
    5. Eylem bölmesinde, **Kaydet**'i seçin.

3. Ambar adresi ayarlayın.

    1. **Ambar yönetimi** &gt; **Ayarlama** &gt; **Ambar** &gt; **Ambarlar**'a gidin.
    2. Listede, ambar **11**'i seçin.
    3. **Adresler** hızlı sekmesinde **Ekle**'yi seçin.
    4. **Yeni** **adres** iletişim kutusunda, **Ad** **veya** **açıklama** alanına **Ana** girin.
    5. **Ülke/bölge** alanında, **ITA (İtalya)** seçeneğini belirleyin.
    6. **Şehir** alanında, **Nisan**'ı seçin.
    7. **Tamam**'ı seçin.

4. Hareket kodlarını ayarlayın.

    1. **Vergi** > **Kurulum** > **Dış ticaret** > **Hareket kodları**'na gidin.
    2. **Yeni**'yi seçin ve özellik transferleri için bir hareket kodu ayarlayın.

        - **Hareket kodu** alanına **1** girin.
        - **Ad** alanına, **Özellik transferi** girin.

    3. **Yeni**'yi seçin ve iadeler için bir hareket kodu ayarlayın.

        - **Hareket** **kodu** alanına **2** girin.
        - **Ad** alanına **Malların iadesi** girin.

5.  Dış ticaret parametrelerini ayarlayın.

    1. **Vergi** > **Kurulum** > **Dış ticaret** > **Dış ticaret parametreleri**'ne gidin.
    2. **İntrastat** sekmesindeki **Genel** hızlı sekmesinde **Hareket** **kodu** alanına **1**'i seçin.
    3. **Alacak dekontu** alanında, **2**'i seçin.
    4. **Satış raporlama dönemi** alanında, **Ay** seçeneğini belirleyin.
    5. **Satın alma raporlama dönemi** alanında, **Ay** seçeneğini belirleyin.
    6. **Elektronik raporlama** hızlı sekmesindeki **Dosya biçimi eşlemesi** alanında **İntrastat (IT)** seçeneğini belirleyin.
    7. **Raporlama formatı eşlemesi** alanında, **İntrastat raporu**'nu seçin.
    8. **Emtia kodu hiyerarşi** hızlı sekmesinde, **Kategori hiyerarşisi** alanında **İntrastat**'ı seçin.
    9. **İstatistiksel değer** hızlı sekmesinde, **İstatistiksel verileri yazdır ve dışarı aktar** seçeneğini **Evet** olarak ayarlayın.
    10. **Ülke/bölge özellikleri** sekmesinde, aşağıdaki satırların var olduğunu doğrulayın.

        | **Taraf/ülke/bölge** | **Intrastat kodu** | **Para Birimi** | **Ülke/bölge türü** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | EUR          | Yerel                |
        | SMR                      | SM                 | EUR          | Yurtiçi özel        |

    11. Aşağıdaki satırı oluşturmak için araç çubuğunda **Yeni**'yi seçin.

        | **Taraf/ülke/bölge** | **Intrastat kodu** | **Para Birimi** | **Ülke/bölge türü** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | DKK          | AB                      |

6. Vergi muafiyet numaraları ayarlayın.

    1. **Vergi** > **Kurulum** > **Satış vergisi** > **Vergi muafiyet numaraları**'na gidin.
    2. Eylem Bölmesi'nde, aşağıdaki satırları oluşturmak için **Yeni**'yi seçin.

        | **Ülke/bölge** | **Vergi muafiyet numarası** | **Şirket adı** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | UE SATICISI        |
        | DNK                | DK0987654321          | Müşteri ER'si      |

7. Satıcı adresini ayarlayın.

    1. **Borç hesapları** &gt; **Satıcılar** &gt; **Tüm satıcılar**'a gidin.
    2. Izgarada, **UE Satıcısı**'nı seçin.
    3. **Adresler** hızlı sekmesinde, **Ekle**'yi seçin.
    4. **Yeni adres** iletişim kutusunda, **Ad veya açıklama** alanına **Almanya** girin.
    5. **Ülke/bölge** alanında **DEU**'yu seçin.
    6. Yeni adresi oluşturmak için **Tamam**'ı seçin.
    7. **Fatura ve teslimat** hızlı sekmesinde, **Satış vergisi** bölümünde, **Vergi muafiyet numarası** alanında **Tümü** seçeneğini belirleyin ve ardından **DE1234567890**'ı seçin.
    8. Eylem bölmesinde, **Kaydet**'i seçin.

8. Müşteri adreslerini ayarlayın.

    1. **Alacak hesapları** > **Müşteriler** > **Tüm müşteriler**'e gidin.
    2. Izgarada, **ITCO-000001**'i seçin.
    3. **Adresler** hızlı sekmesinde, **Düzenle**'yi seçin.
    4. **Yeni adres** iletişim kutusunda, **Ad veya açıklama** alanına **San Marino** girin.
    5. **Ülke/bölge** alanında **SMR**'yu seçin.
    6. Yeni adresi oluşturmak için **Tamam**'ı seçin.
    7. **Fatura ve teslimat** hızlı sekmesinde, **Fatura** bölümündeki **Fatura hesabı** alanında **ITCO-000001**'i seçin.
    8. **Numara sırası grubu** alanında, **IT\_VENDOM**'u seçin.
    9. Eylem Bölmesi'nde **Kaydet**'i seçin ve ardından sayfayı kapatın.
    10. **Tüm müşteriler** sayfasındaki ızgarada **ITCO-000002**'yi seçin.
    11. **Adresler** hızlı sekmesinde, **Ekle**'yi seçin.
    12. **Yeni adres** iletişim kutusunda, **Ad veya açıklama** alanına **Danimarka** girin.
    13. **Ülke/bölge** alanında **DNK**'yu seçin.
    14. Yeni adresi oluşturmak için **Tamam**'ı seçin.
    15. **Satış demografisi** hızlı sekmesindeki **Para birimi** alanında **DKK**'yı seçin.
    16. **Fatura ve teslimat** hızlı sekmesinde, **Satış vergisi** bölümündeki **Satış vergisi grubu** alanında **IT\_PUREU**'yu seçin.
    17. **Vergi muafiyet numarası** alanında, **Tümü** seçeneğini belirleyin ve ardından **DK0987654321**'i seçin.
    18. Eylem bölmesinde, **Kaydet**'i seçin.

9. Kategori hiyerarşisini ayarlayın.

    1. **Ürün bilgileri yönetimi** > **Kurulum** > **Kategoriler ve öznitelikler** > **Kategori hiyerarşileri**'ne gidin.
    2. Kılavuzda **İntrastat**'ı seçin.
    3. Eylem Bölmesi'nde **Yeni kategori düğümü**'nü seçin.
    4. **Ad** alanına, **Servis** girin.
    5. **Kod** alanına **123456** girin.
    6. Eylem bölmesinde, **Kaydet**'i seçin.

10. Ürünlerini ayarlayn.

    1. **Ürün Bilgi yönetimi** > **Ürünler** > **Serbest bırakılmış ürünler**'e gidin.
    2. Izgarada, **ITEM**'i seçin.
    3. **Satınalma** hızlı sekmesinde, **Yönetim** bölümündeki **Satıcı** alanında **ITCO-000001** seçeneğini belirleyin.
    4. **Dış ticaret** hızlı sekmesindeki **İntrastat** bölümünde, **Emtia** alanında **\[100 200 30\] Hoparlör**'ü seçin.
    5. **Menşe** bölümündeki **Ülke/bölge** alanında, **DEU**'yu seçin.
    6. **Eyalet/il** alanında **BE**'yi seçin.
    7. **Stok yönetimi** hızlı sekmesinde, **Net ölçümler** bölümündeki **Net ağırlık** alanına **5** girin.
    8. Eylem bölmesinde, **Kaydet**'i seçin.
    9. **Serbest bırakılan ürünler** sayfasındaki ızgarada **Servis maddesi**'ni seçin.
    10. **Dış Ticaret** hızlı sekmesinde, **İntrastat** bölümündeki **Emtia** alanında **\[123456\] Servis**'i seçin.
    11. Eylem bölmesinde, **Kaydet**'i seçin.

11. Taşıma yöntemlerini ayarlayın.

    1. **Vergi** > **Kurulum** > **Dış ticaret** > **Taşıma yöntemi**'ne gidin.
    2. Eylem Bölmesi'nde, aşağıdaki taşıma yöntemlerini oluşturmak için **Yeni**'yi seçin.

        | **Taşıma** | **Açıklama** |
        |---------------|-----------------|
        | 1             | Yol            |
        | 2             | Hava             |

12. Teslimat şeklini ayarlayın.

    1. **Tedarik ve kaynak atama** > **Kurulum** > **Dağıtım** > **Teslimat modları**'na gidin.
    2. Eylem Bölmesinde, **Yeni**'yi seçin.
    3. **Teslimat şekli** alanına **1** girin.
    4. **Açıklama** alanına **Kamyon** girin.
    5. **Dış Ticaret** hızlı sekmesindeki **Taşıma** alanında **1 Yol**'u seçin.
    6. Eylem bölmesinde, **Kaydet**'i seçin.

13. Teslimat koşullarını ayarlayın.

    1. **Borç hesapları** > **Kurulum** > **Teslimat koşulları**'na gidin.
    2. Listede, **CFR**'yi seçin.
    3. **Genel** hızlı sekmesindeki **İntrastat kodu** alanında **1**'i seçin.

## <a name="post-arrivals-for-intrastat"></a>İntrastat için gelenleri deftere nakletme

### <a name="purchase-goods-by-using-a-purchase-order"></a>Satınalma siparişi kullanarak mal satın alma

Örneğin bu kısmında, Avrupa Birliği (AB) ülkelerinden mal (maddeler) satın almak için bir satınalma siparişinin nasıl kullanılacağı gösterilmektedir.

1. **Borç hesapları** > **Satınalma siparişleri** > **Tüm satınalma siparişleri**'ne gidin.
2.  Eylem Bölmesinde, **Yeni**'yi seçin.
3.  **Satınalma siparişi oluşturma** iletişim kutusunda, **Satıcı hesabı** alanında **UE Satıcısı**'nı seçin.
4.  **Yönetim** hızlı sekmesindeki **Dil** alanında **it** seçeneğini belirleyin.
5.  **Tamam**'ı seçin.
6.  **Üst Bilgi** sekmesindeki **Dış** **ticaret** hızlı sekmesinde, **Hareket kodu** alanının **1** olarak ayarlandığını doğrulayın.
7.  **Menşe/hedef** alanının **RM** olarak ayarlandığını doğrulayın.
8.  **Teslimat** hızlı sekmesinde, **Teslimat** bölümündeki **Teslimat şekli** alanında **1**'i seçin.
9.  **Teslimat koşulları** alanında, **CFR**'yi seçin.
10. **Satırlar** görünümünde, **Satınalma siparişi satırları** hızlı sekmesindeki **Madde numarası** alanında **Madde**'yi seçin.
11. **Site** alanında, **1**'i seçin.
12. **Ambar** alanında **11**'i seçin.
13. **Miktar** alanına **10** yazın.
14. **Birim fiyatı** alanına **100** yazın.
15. **Kurulum** sekmesinde, **Satış vergisi** bölümündeki **Madde satış vergisi grubu** alanında **22%EU** seçeneğini belirleyin.
16. Eylem Bölmesi'nde, **Satınalma** sekmesindeki **Eylemler** grubunda **Onayla**'yı seçin.
17. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda **Fatura**'yı seçin.
18. Eylem Bölmesinde, **Varsayılan başlangıç** seçeneğini belirleyin.
19. **Satırlar için varsayılan miktar** alanında, **Sipariş miktarı**'nı ve **Tamam**'ı seçin.
20. **Satıcı faturası başlığı** hızlı sekmesinde, **Fatura kimliği** bölümünde **Numara** alanına **0001** girin.
21. **Fatura tarihleri** bölümündeki **Fatura tarihi** alanında **9.7.2021**'i seçin.
22. Eylem Bölmesi'nde, faturayı deftere nakletmek için **Deftere Naklet**'i seçin.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Satınalma faturası kullanarak hizmetleri satın alma

Örneğin bu kısmında, AB ülkelerinden hizmet satın almak için bir satıcı faturasının nasıl kullanılacağı gösterilmektedir.

1. **Borç hesapları** > **Faturalar** > **Fatura günlüğü**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Ad** alanında **VEND\_EUINV**'yi seçin.
4. Eylem Bölmesi'nde, **Satırlar**'ı seçin.
5. **Tarih** alanına **9.7.2021** girin.
6. **Hesap türü** alanında **Satıcı**'yı seçin.
7. **Hesap** alanında, **UE Satıcısı**'nı seçin.
8. **Fatura tarihi** alanında, **9.7.2021**'i seçin.
9. **Fatura** alanına **ITA-0004** girin.
10. **Kredi** alanına **120000** girin.
11. **Mahsup hesap** **türü** alanında, **Kayıt Defteri**'ni seçin.
12. **Mahsup hesap** alanında, **110130**'u seçin.
13. **Satış vergisi grubu** alanında, **IT\_PUREU** seçeneğini belirleyin.
14. **Madde satış vergisi grubu** alanında, **22%EU** seçeneğini belirleyin.
15. **Dış Ticaret** sekmesinde şu adımları izleyin:

    1. **Hareket kodu** alanında, **1**'i seçin.
    2. **Taşıma** alanında, **2 Hava**'yı seçin.
    3. **Emtia** alanında, **\[123456\] Servis**'i seçin.
    4. **Ülke/bölge** alanında **ITA**'yu seçin.
    5. **Eyalet/il** alanında, **LAZ**'ı seçin.
    6. **Menşe/hedef** bölümünde **LT**'yi seçin.


16. Eylem Bölmesinde **Deftere naklet**'i seçin.
17. Gelenler için bir İntrastat bildirimi oluşturun.

    1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
    2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
    3. **İntrastat (Transfer)** iletişim kutusunda, **Satıcı faturası** seçeneğini **Evet** olarak ayarlayın.
    4. Hareketleri transfer etmek için **Tamam**'ı seçin ve ardından İntrastat günlüğünü inceleyin.

   ![Intrastat günlüğü sayfası, Genel Bakış sekmesi.](media/ita_intrastat_journal_vendor_invoice.png)

18. Satınalma siparişi için **Genel** sekmesini inceleyin.

    ![Satınalma siparişi için İntrastat günlük satırı ayrıntıları](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Satıcı faturası için **Genel** sekmesini inceleyin.

    ![Satıcı faturası için intrastat günlük satırı ayrıntıları](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. Gelenler için Intrastat raporunu oluşturun.

    1. Eylem Bölmesi'nde **Çıkış** > **Rapor**'u seçin.
    2. **İntrastat Raporu** iletişim kutusunda, **Tarih** bölümündeki **Başlangıç tarihi** alanında **1.7.2021**'i seçin.
    3. **Bitiş tarihi** alanıa **31.7.2021** girin.
    4. **Dışarı aktarma seçenekleri** bölümünde, **Dosya oluştur** ve **Rapor oluştur** seçeneklerini **Evet** olarak ayarlayın.
    5. **Dosya adı** alanına **Gelenler Dosyası** girin.
    6. **Rapor dosyası adı** alanına **Gelenler Raporu** girin.
    7. **Yön** alanında **Gelenler**'i seçin.
    8. **Referans numarası** alanına **123456** girin.
    9. İntrastat raporunu ve İntrastat dosyasını oluşturmak ve incelemek için **Tamam**'ı seçin.

    Aşağıdaki şekilde bir İntrastat raporu örneği gösterilmektedir.

    ![İntrastat gelenler raporu.](media/ita_intrastat_arrivals_report.png)

    Aşağıdaki şekilde bir İntrastat dosyası örneği gösterilmektedir.

    ![İntrastat gelenler dosyası.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>İntrastat için gönderimleri deftere nakletme

### <a name="sell-goods-by-using-a-sales-order"></a>Satış siparişi kullanarak mal satma

Örneğin bu kısmında, Avrupa Birliği (AB) ülkelerine mal (maddeler) satmak için bir satış siparişinin nasıl kullanılacağı gösterilmektedir.

1. **Alacak hesapları** > **Siparişler** > **Tüm satış siparişleri**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Satış siparişi oluşturma** iletişim kutusundaki **Müşteri hesabı** alanında **ITCO-000002**'yi seçin.
4. **Tamam**'ı seçin.
5. **Üst Bilgi** görünümünde **Teslimat** hızlı sekmesindeki **Çeşitli teslim bilgileri** bölümünde **Teslimat modu** alanında **1 Kamyon**'u seçin.
6. **Teslimat koşulları** alanında, **CFR**'yi seçin.
7. **Satırlar** görünümünde, **Satış siparişi satırları** hızlı sekmesindeki **Madde numarası** alanında **MADDE**'yi seçin.
8. **Miktar** alanına **50** yazın.
9. **Site** alanında, **1**'i seçin.
10. **Ambar** alanında **11**'i seçin.
11. **Birim fiyatı** alanına **250** yazın.
12. **Satır ayrıntıları** hızlı sekmesinde, **Kurulum** sekmesindeki **Satış vergisi** bölümünde **Madde satış vergisi grubu** alanında **22%EU** seçeneğini belirleyin.
13. Eylem bölmesinde, **Kaydet**'i seçin.
14. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda sipariş için faturayı oluşturmak için **Fatura**'yı seçin.
15. **Faturayı deftere nakletme** iletişim kutusundaki **Parametreler** hızlı sekmesinde, **Parametre** bölümündeki **Miktar** alanında **Tümü**'nü seçin.
16. **Kurulum** hızlı sekmesindeki **Fatura** **tarihi** alanında **9.7.2021**'i seçin.
17. **Tamam**'ı seçin.
18. İntrastat günlüğündeki satırları inceleyin.

    1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
    2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
    3. **İntrastat (Transfer)** iletişim kutusunda, **Müşteri faturası** seçeneğini **Evet** olarak ayarlayın.
    4. İşlemleri transfer etmek ve İntrastat günlüğünü incelemek için **Tamam**'ı seçin. Alacak dekontu hareketi, bir düzeltme olarak işaretlendi ve negatif fatura tutarı var.

        ![İntrastat günlüğü sayfası](media/ita_intrastat_journal_sales_order.png)

        ![Satış siparişi için İntrastat günlük satırı ayrıntıları](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Alacak dekontu kullanarak malları iade etme

Örneğin bu kısmında, Avrupa Birliği (AB) ülkelerinden mal (maddeler) iade etmek için bir alacak dekontunun nasıl kullanılacağı gösterilmektedir.

1. **Alacak hesapları** > **Siparişler** > **Tüm satış siparişleri**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Satış siparişi oluşturma** iletişim kutusundaki **Müşteri hesabı** alanında **ITCO-000002**'yi seçin.
4. **Tamam**'ı seçin.
5. **Üst Bilgi** görünümünde **Teslimat** hızlı sekmesindeki **Çeşitli teslim bilgileri** bölümünde **Teslimat modu** alanında **1 Kamyon**'u seçin.
6. **Teslimat koşulları** alanında, **CFR**'yi seçin.
7. **Dış Ticaret** hızlı sekmesindeki **Hareket kodu** alanında **2**'yi seçin.
8. **Satırlar** sekmesindeki **Satış siparişi satırları** hızlı sekmesinde **Madde numarası** alanında **MADDE**'yi seçin.
9. **Miktar alanına** **-10** yazın.
10. **Site** alanında, **1**'i seçin.
11. **Ambar** alanında **11**'i seçin.
12. **Birim fiyatı** alanına **250** yazın.
13. **Satır ayrıntıları** hızlı sekmesinde, **Kurulum** sekmesindeki **Satış vergisi** bölümünde **Madde satış vergisi grubu** alanında **22%EU** seçeneğini belirleyin.
14. **İade edilen sipariş** bölümündeki **İade lot kodu** alanında daha önce oluşturduğunuz lotu seçin.
15. Eylem bölmesinde, **Kaydet**'i seçin.
16. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda sipariş için faturayı oluşturmak için **Fatura**'yı seçin.
17. **Parametreler** hızlı sekmesinde, **Parametre** alanındaki **Miktar** alanında **Tümü**'nü seçin.
18. **Faturayı deftere nakletme** iletişim kutusunda, **Kurulum** hızlı sekmesindeki **Fatura** **tarihi** alanında **9.7.2021**'i seçin.
19. Faturayı deftere nakletmek için **Tamam**'ı seçin.
20. İntrastat günlüğündeki satırları inceleyin.

    1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
    2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
    3. **İntrastat (Transfer)** iletişim kutusunda, **Müşteri faturası** seçeneğini **Evet** olarak ayarlayın.
    4. İşlemleri transfer etmek ve İntrastat günlüğünü incelemek için **Tamam**'ı seçin. Alacak dekontu hareketi, bir düzeltme olarak işaretlendi ve negatif fatura tutarı var.

    ![İntrastat günlüğü alacak dekontu](media/ita_intrastat_journal_credit_note.png)

    ![Alacak dekontu için İntrastat günlük satırı ayrıntıları](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Satış siparişi kullanarak San Marino'ya mal satma

Örneğin bu kısmında, San Marino'dan mal (maddeler) satın almak için bir satış siparişinin nasıl kullanılacağı gösterilmektedir.

1. **Alacak hesapları** > **Siparişler** > **Tüm satış siparişleri**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Satış siparişi oluşturma** iletişim kutusundaki **Müşteri hesabı** alanında **ITCO-000001**'i seçin.
4. **Tamam**'ı seçin.
5. **Üst Bilgi** görünümünde, **Teslimat** hızlı sekmesindeki **Çeşitli teslim bilgileri** bölümünde **Teslimat modu** alanında **1**'i seçin.
6. **Teslimat koşulları** alanında, **CFR**'yi seçin.
7. **Satırlar** sekmesindeki **Satış siparişi satırları** hızlı sekmesinde **Madde numarası** alanında **MADDE**'yi seçin.
8. **Miktar** alanına **30** yazın.
9. **Site** alanında, **1**'i seçin.
10. **Ambar** alanında **11**'i seçin.
11. **Birim fiyatı** alanına **200** yazın.
12. Eylem bölmesinde, **Kaydet**'i seçin.
13. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda sipariş için faturayı oluşturmak için **Fatura**'yı seçin.
14. **Parametreler** hızlı sekmesinde, **Parametre** alanındaki **Miktar** alanında **Tümü**'nü seçin.
15. **Faturayı deftere nakletme** iletişim kutusunda, **Kurulum** hızlı sekmesindeki **Fatura** **tarihi** alanında **9.7.2021**'i seçin.
16. Faturayı deftere nakletmek için **Tamam**'ı seçin.
17. İntrastat günlüğündeki satırları inceleyin.

    1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
    2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
    3. **İntrastat (Transfer)** iletişim kutusunda, **Müşteri faturası** seçeneğini **Evet** olarak ayarlayın.
    4. İşlemleri transfer etmek ve İntrastat günlüğünü incelemek için **Tamam**'ı seçin.

   ![San Marino için İntrastat günlüğü](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![San Marino için İntrastat günlük satırı ayrıntıları](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. Gönderimler için bir İntrastat bildirimi oluşturun.

    1. **Vergi** &gt; **Beyannameler** &gt; **Dış Ticaret** &gt; **İntrastat**'a gidin.
    2. Eylem Bölmesi'nde **Çıktı** &gt; **Rapor**'u seçin.
    3. **İntrastat Raporu** iletişim kutusunda, **Tarih** bölümündeki **Başlangıç tarihi** alanında **1.7.2021**'i seçin.
    4. **Bitiş tarihi** alanıa **31.7.2021** girin.
    5. **Dışarı aktarma seçenekleri** bölümünde, **Dosya oluştur** ve **Rapor oluştur** seçeneklerini **Evet** olarak ayarlayın.
    6. **Dosya adı** alanına **Gönderimler Dosyası** girin.
    7. **Rapor dosyası adı** alanına **Gönderimler Raporu** girin.
    8. **Yön** alanında, **Gönderimler**'i seçin.
    9. **Referans numarası** alanına **98754** girin.
    10. İntrastat raporunu ve İntrastat dosyasını oluşturmak için **Tamam**'ı seçin.

        Aşağıdaki şekilde, yazdırılmış bir İntrastat raporu örneği gösterilmektedir.

        ![Intrastat raporu](media/ita_intrastat_report_for_dispatches.png)

        Aşağıdaki şekilde, yazdırılmış bir İntrastat dosyası örneği gösterilmektedir.

        ![Gönderimler için İntrastat dosyası](media/ita_intrastat_file_for_dispatches.png)
