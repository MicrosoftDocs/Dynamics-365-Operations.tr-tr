---
title: Almanca İntrastat
description: Bu konu, Almanya'daki İntrastat bildirimi hakkında bilgi içerir.
author: andosip
ms.date: 08/2/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: e1dbf0997417f9f1ad313e6a7b3c2c9cfae41efc6b1cfda60a5500ae0af94709
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759855"
---
# <a name="german-intrastat"></a>Almanca İntrastat

**İntrastat** sayfası, Avrupa Birliği (AB) ülkeleri arasındaki ticaret hakkında bilgi oluşturmak ve raporlamak için kullanılır. Alman Intrastat bildirimi, raporlama için mal ticareti hakkında bilgi içerir.

Aşağıdaki tabloda, Almanca İntrastat bildirimine dahil edilen alanlar gösterilmektedir.

| Alanlar | Gönderimler | Gelenler |
|-------------------------|-------------------------|-------------------------|
| Başvuru dönemi | X | X |
| Yön kodu | X | X |
| İntrastat bildiriminin para birimi</br>**Not**: Bu para birimi <em>muhasebe para birimidir</em>. | X | X |
| Emtia kodu | X | X |
| Emtia adı | X | X |
| Tamamlayıcı birim kodu | X | X |
| Konsinye/hedefin Üye Devleti | X | X |
| Net kütle | X | X |
| Tamamlayıcı birimlerin miktarı | X | X |
| Menşe ülke |  | X |
| Fatura tutarı | X |  |
| İstatistiksel değer | X | X |
| Hareketlerin niteliği | X | X |
| Taşıma modu | X | X |
| Bölge kodu</br>**Not:**</br><ul></br><li>Menşe ülke veya bölge Almanya ise ve fatura gönderimler içinse menşe için bir intrastat kodu gösterilir.</li></br><li>Menşe ülke veya bölge Almanya değilse ve fatura gönderimler içinse kod **99** gösterilir.</li></br><li>Fatura gelenler içinse durum için bir İntrastat kodu gösterilir.</li></br></ul> | X | X |
| Kapı/Havaalanı/İç kapı kodu | X | X |
| Teslimat koşulları | X | X |


## <a name="set-up-intrastat"></a>İntrastat'ı ayarlama

1. Şirketin kodlarını ayarlayın.

    1. **Kuruluş yönetimi** > **Kuruluşlar** > **Tüzel kişilikler**'e gidin.
    2. **Dış ticaret ve lojistik** hızlı sekmesinde **Kimlik saptama** bölümündeki **DVR** alanına değişim sözleşmesi kodunu girin. Bu kod rapora dahil edilir.
    3. **KDV muafiyet numarası ihracat** alanına, ihracat için şirketinizin katma değer vergisi (KDV) numarasını girin.
    4. **KDV muafiyet numarası ithalat** alanına, ithalat için şirketinizin katma değer vergisi (KDV) numarasını girin.
    5. **İntrastat kodu** alanına tüzel kişiye atanan İntrastat kodunu girin.
    6. **Vergi kaydı** hızlı sekmesinde, **Vergi sicil numarası** alanına şirketinizin vergi sicil numarasını girin.

    > [!NOTE]
    > Bağlı kuruluşlar için bir İntrastat raporu oluşturursanız **Vergi sicil numarası** alanına ana şirketinizin vergi sicil numarasını girin.

2. [Microsoft Dynamics Lifecycle Services'te (LCS),](https://lcs.dynamics.com/Logon/Index) Paylaşılan varlık kitaplığında, İntrastat bildirimi için aşağıdaki Elektronik raporlama (ER) yapılandırmalarının en son sürümlerini indirin.

    - Intrastat modeli
    - Intrastat raporu
    - INSTAT XML
    - INSTAT XML (DE)

3. Dış ticaret parametrelerini ayarlayın:

    1. Dynamics 365 Finance'de **Vergi** > **Kurulum** > **Dış ticaret parametreleri**'ne gidin.
    2. **İntrastat** sekmesindeki **Elektronik raporlama** hızlı sekmesinde **Dosya biçimi eşlemesi** alanında, **İntrastat XML (DE)** seçeneğini belirleyin.
    3. **Rapor biçimi eşlemesi** alanında **İntrastat raporu**'nu seçin.
    4. **Emtia kodu hiyerarşisi** hızlı sekmesinde, **Kategori hiyerarşisi** alanında **İntrastat**'ı seçin.
    5. **Hareket kodu** alanında mal transferleri için hareket kodunu seçin. Bu kodu, ücret karşılığında fiili veya planlı bir mal aktarımına neden olan hareketler ve ayrıca düzeltmeler için kullanırsınız. Düzeltmeler için de kullanırsınız.
    6. **Alacak dekontu** alanında malların iadesi için hareket kodunu seçin. Bu kodu, hareket kodu altında kaydedilen orijinal hareketten sonra malların iadesi için kullanılırsınız.
    7. **Yetkili** alanında, İntrastat yetkilisini seçin.
    8. **Vergi** > **Dolaylı vergiler** > **Satış vergisi** > **Satış vergisi makamları**'na gidin ve önceki adımda seçtiğiniz İntrastat yetkilisi için aşağıdaki bilgileri girin:

       - Yetki tanımlaması
       - Adres
       - İletişim bilgileri

    9. **Ülke/bölge özellikleri** sekmesinde, **Ülke/bölge** alanında, şirketinizin iş yaptığı tüm ülke veya bölgeleri listeleyin. Ülke veya bölgenin İntrastat raporunuzda görüntülenmesi amacıyla her ülke veya bölge için **Ülke/bölge türü** alanında **EU** seçeneğini belirleyin.

4. Bölge kodlarını ayarlayın.

    1. **Kuruluş yönetimi** > **Genel adres defteri** > **Adresler** > **Adres kurulumu**'na gidin.
    2. **Eyalet/il** sekmesindeki **Ülke/bölge** alanında **DEU** seçeneğini belirleyin ve ardından **Filtre uygula**'yı seçin.
    3. Izgarada eyaleti seçin. Ardından, **İntrastat kodu** alanına benzersiz bir İntrastat kodu girin.

5. Ürünün menşe adresini ayarlayın.

    1. **Ürün bilgileri yönetimi** > **Ürünler** > **Serbest bırakılan ürünler**'e gidin.
    2. Izgarada ürünü seçin.
    3. **Dış ticaret** hızlı sekmesindeki **İntrastat** bölümünde, **Menşe ülke** alanında **DEU** seçeneğini belirleyin.

6. **Vergi** > **Kurulum** > **Dış ticaret** > **İntrastat Sıkıştırması** seçeneğine gidin ve İntrastat bilgileri özetlendiğinde karşılaştırılacak alanları seçin. Almanca İntrastat için aşağıdaki alanları seçin:

    - Emtia
    - Ülke/bölge
    - Düzeltme
    - Yön
    - Teslimat koşulları
    - Fatura
    - Menşei ülke/bölge
    - Liman
    - Gönderenin ülkesi/bölgesi
    - Gönderenin eyaleti
    - İstatistiksel yordam
    - Hareket kodu
    - Taşıma
    - Vergi muafiyet numarası

### <a name="intrastat-transfer"></a>İntrastat transferi

**İntrastat** sayfasındaki Eylem Bölmesi'nde satış siparişleri, serbest metin faturaları, satınalma siparişleri, satıcı faturaları, satıcı ürün makbuzları **,** proje faturaları ve transfer emirlerinden topluluk içi ticaret hakkındaki bilgileri otomatik olarak aktarmak için **Transfer Et**'i seçin. Yalnızca varış ülkesi veya bölgesi (gönderimler için) veya konsinye (gelenler için) olarak bir AB ülkesine sahip belgeler aktarılır.

Alternatif olarak, Eylem Bölmesi'nde **Yeni**'yi seçerek hareketleri el ile girebilirsiniz.

### <a name="generate-an-intrastat-report"></a>İntrastat raporu oluşturma

1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
2. Eylem Bölmesi'nde **Çıkış** > **Rapor**'u seçin.
3. **İntrastat Raporu** iletişim kutusunda aşağıdaki alanları ayarlayın.

    | Alan | Tanım |
    |-------------------------|-------------------------|
    | Başlangıç tarihi | Raporun başlangıç tarihini seçin. |
    | Bitiş tarihi | Raporun bitiş tarihini seçin. |
    | Dosya oluştur | .xml dosyası oluşturmak için bu seçeneği **Evet** olarak ayarlayın. |
    | Dosya adı | Bu alanı boş bırakın. Dosya adı otomatik olarak oluşturulur ve **&lt;envelopeId&gt;** XML etiketinin değeri ile **.xml** dosya adı uzantısından oluşur.</br>**&lt;envelopeId&gt;** değeri aşağıdaki öğelerin bu sırayla birleştirilmiş halidir:</br><ol type="1"></br><li>**&lt;interchangeAgreementId&gt;** etiketinin değeri</li></br><li>Tire (-)</li></br><li>**&lt;YYYYAA biçiminde referencePeriod&gt;** etiketinin değeri</li></br><li>Tire (-)</li></br><li>**&lt;YYYYAAGG biçiminde Zarf/Tarih/Saat/tarih&gt;** etiketinin değeri</li></br><li>Tire (-)</li></br><li>**&lt;ssdd biçiminde arf/Tarih/Saat/tarih&gt;** etiketinin değeri</li></br></ol> |
    | Yön | <ul></br><li>Topluluk içi gelenleri raporlamak için **Gelenler**'i seçin.</li></br><li>Topluluk içi gönderimler hakkında rapor için **Gönderimler**'i seçin.</li></br><li>Hem gelenler hem de gönderimler hakkında rapor vermek için **Her İkisi**'ni seçin.</li></br></ul> |
    | Vergi kayıt numarası | Gönderenin kimlik kodunu oluşturmak için kullanılacak kayıt numarası tüzel kişinin vergi kayıt numarasından farklıysa kayıt numarasını girin. |


## <a name="example"></a>Örnek

Bu örnekte, İntrastat için gelenlerin ve gönderimlerin deftere nasıl nakledileceğini gösterilmektedir. Tüzel kişilik olarak **DEMF**'yi kullanın.

1. [LCS](https://lcs.dynamics.com/Logon/Index)'deki Paylaşılan varlık kitaplığında, İntrastat bildirimi biçimi için aşağıdaki ER yapılandırmalarının en son sürümlerini indirin:

    - Intrastat modeli
    - Intrastat raporu
    - İntrastat XML
    - İntrastat XML (DE)

2. Hareket kodları oluşturun.

    1. **Vergi** > **Kurulum** > **Dış ticaret** > **Hareket kodları**'na gidin.
    2. Eylem Bölmesinde, **Yeni**'yi seçin.
    3. **Hareket** **kodu** alanına **21** girin.
    4. **Ad** alanına **Malların iadesi** girin.
    5. Eylem bölmesinde, **Kaydet**'i seçin.

3. Yetkili kimlik numarasını ayarlayın.

    1. **Vergi** > **Dolaylı vergiler** > **Satış vergisi** > **Satış vergisi makamları**'na gidin.
    2. Listeden **TA**'yı seçin.
    3. **Yetkili kimliği** alanına **123**'ü girin.

4. Bölge kodlarını ayarlayın.

    1. **Kuruluş yönetimi** > **Genel adres defteri** > **Adresler** > **Adres kurulumu**'na gidin.
    2. **Eyalet/il** sekmesindeki **Ülke/bölge** alanında **DEU** seçeneğini belirleyin ve ardından **Filtre uygula**'yı seçin.
    3. Izgarada, **BE**'yi seçin ve ardından **İntrastat kodu** alanına **11**'i girin.
    4. Eylem bölmesinde, **Kaydet**'i seçin.

5. Dış ticaret parametrelerini ayarlayın.

    1. **Vergi** > **Kurulum** > **Dış ticaret** > **Dış ticaret parametreleri**'ne gidin.
    2. **İntrastat** sekmesindeki **Genel** hızlı sekmesinde **Hareket** **kodu** alanına **11**'i seçin.
    3. **Alacak dekontu** alanında, **21**'i seçin.
    4. **Yetkili** alanında, **TA**'yı seçin.
    5. **Elektronik raporlama** hızlı sekmesinde **Dosya biçimi eşlemesi** alanında **INSTAT XML (DE)** seçeneğini belirleyin.
    6. **Rapor biçimi eşlemesi** alanında, **İntrastat Raporu**'nu seçin.
    7. **Emtia kodu hiyerarşisi** hızlı sekmesindeki **Kategori hiyerarşisi** alanında **İntrastat**'ı seçtiğinize emin olun.
    8. **Ülke/bölge özellikleri** sekmesinde, **Yeni**'yi seçin.
    9. **Taraf ülkesi/bölgesi** alanında **FRA**'yı seçin.
    10. **Ülke/bölge türü** alanında **EU** seçeneğini belirleyin.

6. Ürüne emtia kodu atayın ve ürünün menşeini ayarlayın. **Emtia kodu**, **Menşe ülke/bölge** ve **Menşe ülke** alanları, ürünü seçtiğinizde satış siparişlerinde ve satınalma siparişlerinde otomatik olarak ayarlanır.

    1. **Ürün bilgileri yönetimi** > **Ürünler** > **Serbest bırakılan ürünler**'e gidin.
    2. Izgarada, **D0001**'i seçin.
    3. **Dış ticaret** hızlı sekmesindeki **İntrastat** bölümünde, **Emtia** alanında **920 20 34**'ü seçin.
    4. **Menşe** bölümündeki **Ülke/bölge** alanında, **DEU**'yu seçin.
    5. **Stok yönetimi** hızlı sekmesindeki **Ağırlık ölçümleri** bölümünde **Net ağırlık** alanına **12** girin.
    6. Eylem bölmesinde, **Kaydet**'i seçin.

7. Taşımayı bir teslimat moduna atayın. Teslimat modunu seçtiğinizde, taşıma kodu otomatik olarak siparişlerde ayarlanır.

    1. **Tedarik ve kaynak atama** > **Kurulum** > **Dağıtım** > **Teslimat modları**'na gidin.
    2. Listede **10**'u seçin.
    3. **Dış ticaret** hızlı sekmesindeki **Taşıma** alanında **01**'i seçin.

8. Bir AB müşterisiyle bir satış siparişi oluşturun.

    1. **Alacak hesapları** > **Siparişler** > **Tüm satış siparişleri**'ne gidin.
    2. Eylem Bölmesinde, **Yeni**'yi seçin.
    3. **Satış siparişi oluşturma** iletişim kutusunda, **Müşteri** hızlı sekmesindeki **Müşteri** bölümünde **Müşteri hesabı** alanında **DE-012**'yi seçin.
    4. **Genel** hızlı sekmesinde **Depolama boyutları** bölümündeki **Site** alanında **1**'i seçin.
    5. **Ambar** alanında **11**'i seçin.
    6. **Tamam**'ı seçin.
    7. **Üst Bilgi** sekmesindeki **Dış ticaret** hızlı sekmesinde **Liman** alanında **53**'ü seçin.
    8. **İstatistiksel yordam** alanında, **31710**'u seçin.
    9.  **Satırlar** sekmesindeki **Satış siparişi** **satırları** hızlı sekmesinde **Madde numarası** alanında **D0001**'i seçin. Ardından, **Miktar** alanına **10** yazın.
    10. **Satır ayrıntıları** hızlı sekmesindeki **Dış ticaret** sekmesinde **Hareket kodu**, **Taşıma**, **Emtia** ve **Menşe ülke/bölge** alanlarının otomatik olarak ayarlandığından emin olun.
    11. Eylem bölmesinde, **Kaydet**'i seçin.
    12. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** bölümünde **Fatura**'yı seçin.
    13. **Faturayı deftere naklet** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Parametre** bölümünde, **Miktar** alanında **Tümü**'nün öğesini seçin.
    14. Faturayı deftere nakletmek için **Tamam**'ı seçin.

9.  Hareketi İntrastat günlüğüne transfer edin ve sonucu inceleyin.

    1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
    2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
    3. **İntrastat (Transfer)** iletişim kutusunda, **Parametreler** bölümünde, **Müşteri faturası** seçeneğini **Evet** olarak ayarlayın.
    4. **Filtre**'yi seç.
    5. **İntrastat Filtresi** iletişim kutusundaki **Aralık** sekmesinde ilk satırı seçin ve **Alan** alanının **Tarih** olarak ayarlandığından emin olun.
    6. **Ölçüt** alanında geçerli tarihi seçin.
    7. **İntrastat Filtresi** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
    8. **İntrastat (Transfer)** iletişim kutusunu kapatmak için **Tamam**'ı seçin ve sonucu inceleyin. Satır, daha önce oluşturduğunuz satış siparişini temsil eder.

        ![intrastat sayfasındaki satış siparişini temsil eden satır](media/intrastat_deu_1.png)

10. Hareket satırını seçin ve ardından daha fazla ayrıntı görüntülemek için **Genel** sekmesini seçin.

    ![İntrastat sayfasının Genel sekmesindeki satış siparişi ayrıntıları](media/intrastat_deu_2.png)

11. Satış siparişi kullanarak alacak dekontu oluşturun.

    1. **Alacak hesapları** > **Siparişler** > **Tüm satış siparişleri**'ne gidin.
    2. Eylem Bölmesinde, **Yeni**'yi seçin.
    3. **Satış siparişi oluşturma** iletişim kutusunda, **Müşteri** hızlı sekmesindeki **Müşteri** bölümünde **Müşteri hesabı** alanında **DE-012**'yi seçin.
    4. **Genel** hızlı sekmesinde **Depolama boyutları** bölümündeki **Site** alanında **1**'i seçin.
    5. **Ambar** alanında **11**'i seçin.
    6. **Üst Bilgi** sekmesindeki **Dış ticaret** hızlı sekmesinde **Liman** alanında **53**'ü seçin.
    7. **İstatistiksel yordam** alanında, **31710**'u seçin.
    8. **Satırlar** sekmesindeki **Satış siparişi** **satırları** hızlı sekmesinde **Madde numarası** alanında **D0001**'i seçin. Ardından, **Miktar** alanına **-2** yazın.
    9. **Satır ayrıntıları** hızlı sekmesindeki **Dış ticaret** sekmesinde **Hareket kodu** alanında **21**'i seçin.
    10. **Taşıma**, **Emtia** ve **Menşe ülke/bölge** alanlarının otomatik olarak ayarlandığından emin olun.
    11. Eylem bölmesinde, **Kaydet**'i seçin.
    12. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** bölümünde **Fatura**'yı seçin.
    13. **Faturayı deftere naklet** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Parametre** bölümünde, **Miktar** alanında **Tümü**'nün öğesini seçin.
    14. Faturayı deftere nakletmek için **Tamam**'ı seçin.

12. Hareketi İntrastat günlüğüne transfer edin ve sonucu inceleyin.

    1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
    2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
    3. **İntrastat (Transfer)** iletişim kutusunda, **Parametreler** bölümünde, **Müşteri faturası** seçeneğini **Evet** olarak ayarlayın.
    4. **İntrastat (Transfer)** iletişim kutusunu kapatmak için **Tamam**'ı seçin ve sonucu inceleyin. **Yön** alanının **Gelenler** olarak ayarlandığı yeni bir satır eklendi.            
        Bu satır malların fiziksel iadesini temsil eder.

        ![İntrastat sayfasındaki mallar için fiziksel iade satırı](media/intrastat_deu_3.png)

13. Hareket satırını seçin ve ardından daha fazla ayrıntı görüntülemek için **Genel** sekmesini seçin.

    ![İntrastat sayfasının Genel sekmesinde malların fiziksel iadesinin ayrıntıları](media/intrastat_deu_4.png)

14. Satış siparişi kullanarak bir düzeltme oluşturun:

    1. **Alacak hesapları** > **Siparişler** > **Tüm satış siparişleri**'ne gidin.
    2. Eylem Bölmesinde, **Yeni**'yi seçin.
    3. **Satış siparişi oluşturma** iletişim kutusunda, **Müşteri** hızlı sekmesindeki **Müşteri** bölümünde **Müşteri hesabı** alanında **DE-012**'yi seçin.
    4. **Genel** hızlı sekmesinde **Depolama boyutları** bölümündeki **Site** alanında **1**'i seçin.
    5. **Ambar** alanında **11**'i seçin.
    6. **Üst Bilgi** sekmesindeki **Dış ticaret** hızlı sekmesinde **Liman** alanında **53**'ü seçin.
    7. **İstatistiksel yordam** alanında, **31710**'u seçin.
    8. **Satırlar** sekmesindeki **Satış siparişi** **satırları** hızlı sekmesinde **Madde numarası** alanında **D0001**'i seçin. Ardından, **Miktar** alanına **-3** yazın.
    9. **Satır ayrıntıları** hızlı sekmesindeki **Dış ticaret** sekmesinde **Hareket kodu** alanında **11**'i seçin.
    10. **Taşıma**, **Emtia** ve **Menşe ülke/bölge** alanlarının otomatik olarak ayarlandığından emin olun.
    11. Eylem bölmesinde, **Kaydet**'i seçin.
    12. **Hareket kodu** alanın 11 olarak ayarlandığından emin olun.
    13. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** bölümünde **Fatura**'yı seçin.
    14. **Faturayı deftere naklet** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Parametre** bölümünde, **Miktar** alanında **Tümü**'nün öğesini seçin.
    15. Faturayı deftere nakletmek için **Tamam**'ı seçin.

15. Hareketi İntrastat günlüğüne transfer edin ve sonucu inceleyin:

    1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
    2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
    3. **İntrastat (Transfer)** iletişim kutusunda, **Parametreler** bölümünde, **Müşteri faturası** seçeneğini **Evet** olarak ayarlayın.
    4. **İntrastat (Transfer)** iletişim kutusunu kapatmak için **Tamam**'ı seçin ve sonucu inceleyin. **Düzeltme** sütununda bir onay işaretinin göründüğü yeni bir satır eklenmiştir.

        ![İntrastat sayfasındaki düzeltme satırı](media/intrastat_deu_5.png)

16. Hareket satırını seçin ve ardından daha fazla ayrıntı görüntülemek için **Genel** sekmesini seçin.

    ![İntrastat sayfasının Genel sekmesindeki düzeltmenin ayrıntıları](media/intrastat_deu_6.png)

17. Eylem Bölmesi'nde **Çıkış** > **Rapor**'u seçin.
18. **İntrastat Raporu** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Tarih** bölümünde, oluşturduğunuz satış siparişinin ayını seçin.
19. **Dışarı Aktarma** **seçenekleri** bölümünde, **Dosya oluştur** seçeneğini **Evet** olarak ayarlayın.
20. **Dosya adı** alanına gerekli adı girin.
21. **Tamam**'ı seçin ve oluşturulan raporu inceleyin. Aşağıdaki tabloda örnek raporlardaki değerler gösterilmektedir.

    | **Kuruluş adı**                  | **Satış faturası**  |   **Düzeltme**   | **Alacak dekontu** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | referencePeriod           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | flowCode                  | B                  | A                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | goodsDescription          | Hoparlör            | Hoparlör            | Hoparlör         |
    | MSConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netMass                   | 120                | -36                | 24              |
    | invoicedAmount            | 3290               | -987               | \-              |
    | StatisticalValue          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 01                 | 01                 | 01              |
    | regionCode                | 11                 | 11                 | 11              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |

