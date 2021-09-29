---
title: İsveççe İntrastat
description: Bu konu, İsveç'teki İntrastat raporlaması hakkında bilgi içerir.
author: andosip
ms.date: 8/24/2021
ms.topic: article
audience: Application User
ms.reviewer: kfender
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: 152bfd24843867685b1d303484ed61ad98ec652a
ms.sourcegitcommit: 3f6cbf4fcbe0458b1515c98a1276b5d875c7eda7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/10/2021
ms.locfileid: "7486958"
---
# <a name="swedish-intrastat"></a>İsveççe İntrastat

[!include[banner](../includes/banner.md)]

**İntrastat** sayfası, Avrupa Birliği (AB) ülkeleri arasındaki ticaret hakkında bilgi oluşturmak ve raporlamak için kullanılır. İsveç İntrastat bildirimi, raporlama için mal ticareti hakkında bilgiler içerir.

Aşağıdaki alanlar, İsveççe İntrastat bildirimine dahil edilir:

   - İş ortağı ülkenin ISO kodu
   - Hareket kodu
   - Emtia Kodu
   - Ek birim
   - Ağırlık
   - Fatura tutarı

## <a name="set-up-intrastat"></a>İntrastat'ı ayarlama

Aşağıdaki Elektronik raporlama (ER) yapılandırmalarının en son sürümünü içeri aktarın:

   - Intrastat modeli
   - Intrastat raporu
   - İntrastat (SE)

Daha fazla bilgi için bkz. [Yapılandırma hizmeti Genel deposundan ER yapılandırmalarını indirme](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-foreign-trade-parameters"></a>Dış ticaret parametreleri ayarla

1. Microsoft Dynamics 365 Finance uygulamasında, **Vergi** > **Kurulum** > **Dış ticaret parametreleri**'ne gidin.
2. **İntrastat** sekmesindeki **Elektronik raporlama** hızlı sekmesinde **Dosya biçimi eşlemesi** alanında, **İntrastat (SE)** seçeneğini belirleyin.
3. **Rapor biçimi eşlemesi** alanında **İntrastat raporu**'nu seçin.
4. **Emtia kodu hiyerarşisi** hızlı sekmesinde, **Kategori hiyerarşisi** alanında **İntrastat**'ı seçin.
5. **Hareket kodu** alanında mal transferleri için hareket kodunu seçin. Bu kodu, ücret (mali veya başka türlü) karşılığında fiili ya da planlı bir mal aktarımına neden olan hareketler için kullanırsınız. Düzeltmeler için de kullanırsınız. İsveç'teki şirketler tek basamaklı işlem kodları kullanır.
6. **Alacak dekontu** alanında malların iadesi için hareket kodunu seçin.
7. **Ülke/bölge özellikleri** sekmesinde, **Ülke/bölge** alanında, şirketinizin iş yaptığı tüm ülke veya bölgeleri listeleyin. AB üyesi olan her ülkenin İntrastat raporunuzda görüntülenmesi amacıyla her ülke için **Ülke/bölge türü** alanında **EU** seçeneğini belirleyin.

## <a name="set-up-the-product-parameters-for-the-intrastat-declaration"></a>İntrastat bildirimi için ürün parametrelerini ayarlama

1. **Ürün bilgileri yönetimi** > **Ürünler** > **Serbest bırakılan ürünler**'e gidin.
2. Kılavuzda, bir ürün seçin.
3. **Dış ticaret** hızlı sekmesindeki **İntrastat** bölümünde **Emtia** alanında emtia kodunu seçin.
4. **Stok yönetimi** hızlı sekmesinde, **Net ağırlık** alanına ürünün ağırlığını kilogram olarak girin.
5. **Vergi** > **Kurulum** > **Dış ticaret** > **İntrastat Sıkıştırması** seçeneğine gidin ve İntrastat bilgileri özetlendiğinde karşılaştırılacak alanları seçin. İsveççe İntrastat için aşağıdaki alanları seçin:

    - Emtia
    - Hareket kodu
    - Yön
    - Ülke/bölge
    - Düzeltme
    - Fatura

## <a name="intrastat-transfer"></a>İntrastat transferi

**İntrastat** sayfasında, Eylem Bölmesi'nde, satış siparişlerinizden, serbest metin faturalarınızdan, satın alma siparişlerinizden, satıcı faturalarınızdan, satıcı ürün girişlerinden, proje faturalarından ve transfer emirlerinizden topluluk içi ticaret hakkındaki bilgileri otomatik olarak aktarmak için **Transfer**'i seçebilirsiniz. Yalnızca varış ülkesi veya bölgesi (gönderimler için) veya konsinye (gelişler için) olarak bir AB ülkesine sahip belgeler aktarılacaktır.

Alternatif olarak, Eylem Bölmesi'nde **Yeni**'yi seçerek hareketleri el ile girebilirsiniz.

### <a name="generate-an-intrastat-report"></a>İntrastat raporu oluşturma

1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
2. Eylem Bölmesi'nde **Çıkış** > **Rapor**'u seçin.
3. **İntrastat Raporu** iletişim kutusunda aşağıdaki alanları ayarlayın.

    | Alan            | Tanım                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Başlangıç tarihi        | Raporun başlangıç tarihini seçin.                                                                                               |
    | Bitiş tarihi          | Raporun bitiş tarihini seçin.                                                                                                 |
    | Dosya oluştur    | İntrastat raporunuzda bir .txt dosyası oluşturmak için bu seçeneği **Evet** olarak ayarlayın.                                                       |
    | Dosya adı        | .txt dosyasının adını girin.                                                                                                    |
    | Rapor oluştur  | İntrastat raporunuzda bir .xlsx dosyası oluşturmak için bu seçeneği **Evet** olarak ayarlayın.                                                     |
    | Rapor dosyası adı | .xlsx dosyasının adını girin.                                                                                                   |
    | Yön        | Topluluk içi gelenlerle ilgili bir rapor için **Gelenler**'i seçin. Topluluk için gönderimler hakkında rapor için **Gönderimler**'i seçin. |

4. **Tamam**'ı seçin ve oluşturulan raporları inceleyin.

## <a name="example"></a>Örnek

Bu örnekte, İntrastat için gelenlerin ve gönderimlerin deftere nasıl nakledileceğini gösterilmektedir. Tüzel kişilik olarak **DEMF**'yi kullanın.

### <a name="preliminary-setup"></a>Ön kurulum

1. **Kuruluş yönetimi** > **Kuruluş** > **Tüzel kişilikler**'e gidin ve **DEMF** tüzel kişiliğini seçin.
2. **Adresler** hızlı sekmesinde **Düzenle**'yi seçin ve ardından **Ülke/bölge** alanında **SWE (İsveç)** seçeneğini belirleyin.
3. Aşağıdaki ER yapılandırmalarının en son sürümünü içeri aktarın:

    - Intrastat modeli
    - Intrastat raporu
    - İntrastat (SE)

### <a name="create-transaction-codes"></a>Hareket kodları oluşturma

1. **Vergi** > **Kurulum** > **Dış ticaret** > **Hareket kodları**'na gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Hareket** **kodu** alanına **1** girin.
4. **Ad** alanına **Normal hareketler** girin.
5. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-foreign-trade-parameters"></a>Dış ticaret parametreleri ayarla

1. **Vergi** > **Kurulum** > **Dış ticaret** > **Dış ticaret parametreleri**'ne gidin.
2. **İntrastat** sekmesindeki **Genel** hızlı sekmesinde **Hareket** **kodu** alanına **1**'i seçin.
3. **Elektronik raporlama** hızlı sekmesindeki **Dosya biçimi eşlemesi** alanında **İntrastat (SE)** seçeneğini belirleyin.
4. **Rapor biçimi eşlemesi** alanında, **İntrastat Raporu**'nu seçin.
5. **Emtia kodu hiyerarşisi** hızlı sekmesindeki **Kategori hiyerarşisi** alanında **İntrastat**'ı seçtiğinize emin olun.
6. **Ülke/bölge özellikleri** sekmesinde, **Yeni**'yi seçin.
7. **Taraf ülkesi/bölgesi** alanında **SWE**'yı seçin.
8. **Ülke/bölge türü** alanında, **Yurtiçi** seçeneğini belirleyin.
9. **Taraf ülkesi/bölgesi** alanında **DEU** seçeneğini belirleyin ve ardından **Ülke/bölge türü** alanında, **EU**'yu seçin.

### <a name="set-up-product-information"></a>Ürün bilgilerini ayarlama

1. **Ürün bilgileri yönetimi** > **Ürünler** > **Serbest bırakılan ürünler**'e gidin.
2. Izgarada, **D0001**'i seçin.
3. **Dış ticaret** hızlı sekmesindeki **İntrastat** bölümünde, **Emtia** alanında **100 200 30**'ü seçin.
4. **Stok yönetimi** hızlı sekmesindeki **Ağırlık ölçümleri** bölümünde **Net ağırlık** alanına **5** girin.
5. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="change-the-site-address"></a>Tesis adresini değiştirme

1. **Ambar yönetimi** > **Kurulum** > **Ambar** > **Tesisler**'e gidin.
2. Kılavuzda, **1**'i seçin.
3. **Adresler** hızlı sekmesinde, **Düzenle**'yi seçin.
4. **Adresi düzenle** iletişim kutusunda, **Ülke/bölge** alanında **SWE**'yi seçin.
5. **Tamam**'ı seçin.

### <a name="create-a-sales-order-with-an-eu-customer"></a>AB müşterisiyle bir satış siparişi oluşturma

1. **Alacak hesapları** > **Siparişler** > **Tüm satış siparişleri**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Satış siparişi oluşturma** iletişim kutusunda, **Müşteri** hızlı sekmesindeki **Müşteri** bölümünde **Müşteri hesabı** alanında **DE-015**'yi seçin.
4. **Genel** hızlı sekmesinde **Depolama boyutları** bölümündeki **Site** alanında **1**'i seçin.
5. **Ambar** alanında **11**'i seçin.
6. **Tamam**'ı seçin.
7. **Satırlar** sekmesindeki **Satış siparişi satırları** hızlı sekmesinde **Madde numarası** alanında **D0001**'i seçin. Ardından, **Miktar** alanına **10** yazın.
8. **Satır ayrıntıları** hızlı sekmesindeki **Dış ticaret** sekmesinde **Hareket kodu** ve **Emtia** alanlarının otomatik olarak ayarlandığından emin olun.
9. Eylem bölmesinde, **Kaydet**'i seçin.
10. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** bölümünde **Fatura**'yı seçin.
11. **Faturayı deftere naklet** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Parametre** bölümünde, **Miktar** alanında **Tümü**'nün öğesini seçin.
12. Faturayı deftere nakletmek için **Tamam**'ı seçin.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Hareketi İntrastat günlüğüne transfer etme ve sonucu inceleme

1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
3. **İntrastat (Transfer)** iletişim kutusunda, **Parametreler** bölümünde, **Müşteri faturası** seçeneğini **Evet** olarak ayarlayın.
4. **Filtre**'yi seç.
5. **İntrastat Filtresi** iletişim kutusundaki **Aralık** sekmesinde ilk satırı seçin ve **Alan** alanının **Tarih** olarak ayarlandığından emin olun.
6. **Ölçüt** alanında geçerli tarihi seçin.
7. **İntrastat Filtresi** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
8. **İntrastat (Transfer)** iletişim kutusunu kapatmak için **Tamam**'ı seçin ve sonucu inceleyin. Satır, daha önce oluşturduğunuz satış siparişini temsil eder.

    ![Satış siparişi için İntrastat günlük satırları](media/swe_intrastat_journal_sales_order.png)

9. Hareket satırını seçin ve ardından daha fazla ayrıntı görüntülemek için **Genel** sekmesini seçin.

    ![Satış siparişi için İntrastat günlük satırı ayrıntıları](media/swe_intrastat_journal_sales_order_line_details.png)

10. Eylem Bölmesi'nde **Çıkış** > **Rapor**'u seçin.
11. **İntrastat Raporu** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Tarih** bölümünde, oluşturduğunuz satış siparişinin ayını seçin.
12. **Dışarı Aktarma** **seçenekleri** bölümünde, **Dosya oluştur** seçeneğini **Evet** olarak ayarlayın. Ardından, **Dosya adı** alanına gerekli adı girin.
13. **Rapor oluştur** seçeneğini **Evet** olarak ayarlayın. Ardından, **Rapor dosyası adı** alanına gerekli adı girin.
14. **Yön** alanında, **Gönderimler**'i seçin.
15. **Tamam**'ı seçin ve .txt biçiminde oluşturulan raporu inceleyin. Aşağıdaki tabloda örnek raporlardaki değerler gösterilmektedir.

    | İş ortağı ülkenin ISO kodu | Hareket kodu | Emtia Kodu | Ek birim | Ağırlık | Fatura tutarı |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 50     | 3290           |

16. Excel biçiminde oluşturulan raporu inceleyin.

    ![Intrastat raporu](media/swe_intrastat_report_for_dispatches.png)

### <a name="create-a-purchase-order"></a>Satınalma siparişi oluşturma

1. **Borç hesapları** > **Satınalma siparişleri** > **Tüm satınalma siparişleri**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Satınalma siparişi oluştur** iletişim kutusundaki **Satıcı hesabı** alanında **DE-001**'i seçin.
4. **Tamam**'ı seçin.
5. **Üst Bilgi** sekmesinde, **Dış** **ticaret** hızlı sekmesinde **İşlem kodu** alanının **1** olarak ayarlandığını doğrulayın.
6. **Satırlar** sekmesindeki **Satınalma siparişi satırları** hızlı sekmesinde **Madde numarası** alanında **D0001**'i seçin. Ardından, **Miktar** alanına **6** yazın.
7. Eylem Bölmesi'nde, **Satınalma** sekmesindeki **Eylemler** grubunda **Onayla**'yı seçin.
8. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda **Fatura**'yı seçin.
9. Eylem Bölmesinde, **Varsayılan başlangıç** seçeneğini belirleyin. **Satırlar için varsayılan miktar** alanında **Sipariş edilen miktar**'ı seçin. Daha sonra **Tamam**'ı seçin.
10. **Satıcı faturası başlığı** hızlı sekmesinde, **Fatura kimliği** bölümünde **Numara** alanına **0001** girin.
11. Eylem Bölmesi'nde, faturayı deftere nakletmek için **Deftere Naklet**'i seçin.

### <a name="create-an-intrastat-declaration-for-arrivals"></a>Gelenler için bir İntrastat bildirimi oluşturma

1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
3. **İntrastat (Transfer)** iletişim kutusunda, **Satıcı faturası** seçeneğini **Evet** olarak ayarlayın.
4. İşlemleri transfer etmek ve İntrastat günlüğünü incelemek için **Tamam**'ı seçin.

    ![Satınalma siparişi için İntrastat günlüğü](media/swe_intrastat_journal_purchase_order.png)

5. Satınalma siparişi için **Genel** sekmesini inceleyin.

    ![Satınalma siparişi için İntrastat günlük satırı ayrıntıları](media/swe_intrastat_journal_purchase_order_line_details.png)

6. Eylem Bölmesi'nde **Çıkış** > **Rapor**'u seçin.
7. **İntrastat Raporu** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Tarih** bölümünde, oluşturduğunuz satış siparişinin ayını seçin.
8. **Dışarı Aktarma** **seçenekleri** bölümünde, **Dosya oluştur** seçeneğini **Evet** olarak ayarlayın. Ardından, **Dosya adı** alanına gerekli adı girin.
9. **Rapor oluştur** seçeneğini **Evet** olarak ayarlayın. Ardından, **Rapor dosyası adı** alanına gerekli adı girin.
10. **Yön** alanında **Gelenler**'i seçin.
11. **Tamam**'ı seçin ve .txt biçiminde oluşturulan raporu inceleyin. Aşağıdaki tabloda örnek raporlardaki değerler gösterilmektedir.

    | İş ortağı ülkenin ISO kodu | Hareket kodu | Emtia Kodu | Ek birim | Ağırlık | Fatura tutarı |
    |--------------------------|------------------|----------------|-----------------|--------|----------------|
    | IT                       | 1                | 10020030       | 0               | 30     | 1714           |

12. Excel biçiminde oluşturulan raporu inceleyin.

    ![İntrastat gelenler raporu](media/swe_intrastat_arrivals_report.png)
