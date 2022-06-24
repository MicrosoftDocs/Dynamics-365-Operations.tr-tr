---
title: Fransızca İntrastat
description: Bu makalede, Fransa'daki İntrastat bildirimi hakkında bilgiler yer almaktadır.
author: anasyash
ms.date: 07/9/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: e86d7c8f28b1b3df0066a588d380965c21dc98a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887867"
---
# <a name="french-intrastat"></a>Fransızca İntrastat

[!include[banner](../includes/banner.md)]

Fransa'da katma değer vergisi (KDV) için kayıtlı olan ve diğer Avrupa Birliği (AB) ülkeleriyle ticaret yapan şirketler, Fransa'ya ve Fransa'dan mal ve hizmet alışverişini beyan etmelidir. Declaration d'exchanges de biens (Mal Ticareti Beyanı veya DEB), AB Satış Listesi ve İntrastat raporunun birleşimidir. Tüm topluluk içi mal satışları için bu raporu aylık olarak göndermeniz gerekir.

DEB raporunu iki elektronik metin dosyası biçiminden herhangi biri olarak oluşturabilirsiniz: SAISUNIC 330 veya INTRACOM biçiminde.

Aşağıdaki tabloda, Fransızca İntrastat bildiriminde yer alan alanlar SAISUNIC 330 biçiminde gösterilmektedir. Tablo ayrıca alanın rapor düzeyini de gösterir. Alan **4** (basitleştirilmiş), **1** (tam) veya ikisi de olabilir.

| **Alan**                   | **Rapor düzeyi** |
|-----------------------------|------------------|
| Referans Dönemi         | 4, 1              | 
| Beyanname Sayısı       | 4, 1              |
| Satır Numarası                 | 4, 1              |
| Ülkenin ISO Kodu (FR)       | 4, 1              | 
| Tamamlayıcı Kod          | 4, 1              | 
| Siren Numarası                | 4, 1              | 
| Müşterinin KDV Kodu        | 4, 1              | 
| Yönerge Kodu              | 4, 1              |
| Hareket Türü            | 4, 1              | 
| Yükümlülük Düzeyi            | 4, 1              |
| Emtia Kodu              | 1                | 
| Ulusal NGP                | 1                | 
| İlçe (Departman)         | 1                |
| İşlemin Niteliği       | 1                | 
| Menşe Ülke      | 1                | 
| Menşe Ülke - İthalat | 1                | 
| Son Hedef - İhracat | 1                | 
| Fatura Değeri               | 4, 1              | 
| İstatistiksel Değer           | 1                |
| Net Ağırlık                  | 1                | 
| Ek Birimler            | 1                |
| Taşıma Kodu              | 1                | 

Aşağıdaki tabloda, Intracom biçiminde Fransızca İntrastat bildirimine dahil edilen alanlar gösterilmektedir.
Tablo ayrıca alanın rapor düzeyini de gösterir. Alan **4** (basitleştirilmiş), **1** (tam) veya ikisi de olabilir.

| **Alan**                   | **Rapor düzeyi**   | 
|-----------------------------|--------------------|
| Kod                        | 4, 1               | 
| Beyanname Sayısı       | 4, 1               |
| Satır Sayısı              | 4, 1               | 
| Siren                       | 4, 1               |
| İlçe (Departman)         | 1                  |          
| Taşıma Kodu              | 1                  |          
| Menşe Ülke           | 1                  |            
| İşlemin Niteliği       | 1                  |             
| Fatura Değeri               | 4, 1               |             
| Teslimat Şekilleri           | 1                  |           
| Hareket Türü            | 4, 1               |            
| Yükümlülük Düzeyi            | 4, 1               |           
| Emtia Kodu              | 1                  |            
| Ulusal NGP                | 1                  |            
| Net Ağırlık                  | 1                  |            
| İstatistiksel Değer           | 1                  |            
| Ek Birimler            | 1                  |            
| Menşe Ülke - İthalat | 1                  |            
| Son Hedef - İhracat | 1                  |            
| Müşterinin KDV Kodu        | 4, 1               |            
| Tamamlayıcı Kod          | 4, 1               |           
| Referans Dönemi         | 4, 1               |         

### <a name="set-up-intrastat"></a>İntrastat'ı ayarlama

1.  [Microsoft Dynamics Lifecycle Services'te (LCS),](https://lcs.dynamics.com/Logon/Index) paylaşılan varlık kitaplığında, İntrastat bildirimi için aşağıdaki Elektronik raporlama (ER) yapılandırmalarının en son sürümlerini yükleyin:

    - Intrastat modeli
    - Intrastat raporu
    - Intrastat INTRACOM (FR)
    - Intrastat SAISUNIC (FR)

    Daha fazla bilgi için bkz. [Lifecycle Services'dan Elektronik raporlama yapılandırmalarını yükleme](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  Dynamics 365 Finance'te, **Vergi** > **Kurulum** >  **Dış ticaret** > **Dış ticaret parametreleri**'ne gidin ve şu adımları izleyin:

    1. **İntrastat** sekmesinde, **Elektronik raporlama** hızlı sekmesinde, **Dosya biçimi eşleme** alanında **İntrastat INTRACOM (FR)** veya **İntrastat SAISUNIC (FR)**'yi seçin.
    2. **Rapor biçimi eşlemesi** alanında **İntrastat raporu**'nu seçin.
    3. **Emtia kodu hiyerarşisi** hızlı sekmesinde, **Kategori hiyerarşisi** alanında **İntrastat**'ı seçin.
    4. **Genel** hızlı sekmesinde, **Hareket kodu** alanında, malların transferleri için kullanılan kodu seçin.
    5. **Alacak dekontu** alanında, malların iadeleri için kullanılan kodu seçin.
    6. **İhracat için yükümlülük düzeyi** alanına, ihracat raporunun ayrıntı düzeyini girin. Seçtiğiniz düzey raporda gösterilen satırları etkiler. Daha fazla bilgi için bu makalenin başındaki tablolara bakın.

3. **Kuruluş yönetimi** > **Kuruluşlar** > **Tüzel kişilikler**'e gidin, şirketinizi seçin ve ardından şu adımları izleyin:

    1. **Sicil numaraları** hızlı sekmesinde, **NAF kodu** alanına NAF kodunuzu girin. Daha fazla bilgi için bkz. [FR-00003 NAF kodları ve Siret numaraları](tasks/fr-00003-naf-codes-siret-numbers.md).
    2. **Dış ticaret ve lojistik** hızlı sekmesinde, **İntrastat** bölümünde, **KDV muafiyet numarası ihracat** ve **KDV muafiyet numarası ithalat** alanlarını ayarlayın.
    3. **Vergi kaydı** hızlı sekmesinde, **Vergi sicil numarası** alanına şirketinizin vergi sicil numarasını girin.

4. Müşteriler için NAF kodları ve vergiden muafiyet numaralarını belirtmek üzere **Alacak hesapları** > **Müşteriler** > **Tüm müşteriler**'e gidin ve şu adımları izleyin:

    1. Müşteri seçin.
    2. **Fatura ve teslimat** hızlı sekmesinde, **Satış vergisi** bölümünde, **Vergi muafiyet numarası** alanına müşterinin vergiden muafiyet numarasını girin.
    3. **Satış demografisi** hızlı sekmesinde, **Fransızca Siret** alanına şirketin Siret numarasını girin.
    4. **NAF kodu** alanına şirketin NAF kodunu girin.
    5. Diğer müşteriler için bu adımları yineleyin.

5. Satıcılar için NAF kodları ve vergiden muafiyet numaraları belirtmek üzere **Borç hesapları** > **Satıcılar** > **Tüm satıcılar**'a gidin ve şu adımları izleyin:

    1. Bir satıcı seçin.
    2. **Fatura ve teslimat** hızlı sekmesinde, **Satış vergisi** bölümünde, **Vergi muafiyet numarası** alanına satıcının vergiden muafiyet numarasını girin.
    3. **Satın alma demografisi** hızlı sekmesinde, **Fransızca Siret** alanına şirketin Siret numarasını girin.
    4. **NAF kodu** alanına şirketin NAF kodunu girin.
    5. Diğer satıcılar için bu adımları yineleyin.

6. **Vergi** > **Kurulum** > **Dış ticaret** > **İntrastat Sıkıştırması** seçeneğine gidin ve İntrastat bilgileri özetlendiğinde karşılaştırılacak alanları seçin. Fransızca İntrastat için **İstatistik prosedürü**, **Menşe İl**, **Menşe ülke/bölge**, **Teslimat şartları**, **Taşıma**, **Düzeltme**, **Ülke/bölge**, **Menşe/hedef ilçe**, **Yön**, **Gönderenin ülkesi/bölgesi**, **Gönderenin eyaleti**, **Eyalet**, **Hareket kodu** ve **Emtia**'yı seçin.

7. **Ambar yönetimi** > **Kurulum** > **Ambar** > **Ambarlar**'a gidin, bir ambar seçin ve ardından şu adımları izleyin:

    1. **Adresler** hızlı sekmesinde **Ekle** veya **Düzenle**'yi seçin.
    2. İletişim kutusunda, **Şehir** alanında ambarın şehrini seçin. Şehrin durumu eyalet, DEB raporunuz için ilçe olarak kullanılacaktır.

### <a name="ngp-codes"></a>NGP kodları

DEB raporunda, ürünlerin kodlanması aşağıdaki unsurlardan oluşur:

  - AB'nin tarifesini ve istatistiksel isimlendirmesini temsil eden sekiz basamaklı CN8 kodu.
  - Varsa tek haneli Nomenclature Générale des Produits (NGP) ulusal ürün kodu.

2021'de NGP sadece üç tür ürün için geçerlidir:

  - İnek, koyun ve keçilerden elde edilen bazı ürünler
  - Askeri teçhizat
  - Fransız şarapları

 NGP kodlarını ayarlamalı ve ilgili ürünlere atamalısınız. **NGP** alanı daha sonra **İntrastat günlüğü** sayfasında otomatik olarak ayarlanır.

#### <a name="set-up-an-ngp-code"></a>NGP kodu ayarlama

1. **Vergi** > **Kurulum** > **Dış ticaret** > **NGP kodları**'na gidin.
2. Eylem bölmesinde **Yeni**'yi seçerek yeni bir NGP kodu oluşturun.
3. **NGP** alanına tek basamaklı bir kod girin.
4. **Açıklama** alanına, kodun açıklamasını girin.

#### <a name="assign-an-ngp-code-to-a-product"></a>Ürüne NGP kodu atama

1. **Ürün bilgileri yönetimi** > **Ürünler** > **Serbest bırakılan ürünler**'e gidin.
2. Kılavuzda, bir ürün seçin.
3. **Dış ticaret** hızlı sekmesinde, **İntrastat** bölümünde, **NGP** alanında uygun NGP kodunu seçin.

## <a name="intrastat-journal"></a>İntrastat günlüğü

AB ülkeleriyle dış ticaret için geçerli olan hareketlerinizi yönetmek üzere **Vergi** > **Bildirimler** > **Dış** **ticaret** > **Intrastat**'a gidin. Daha fazla bilgi için bkz. [İntrastat'a genel bakış](emea-intrastat.md).

**NGP** sütunu Fransa'ya özgüdür. Ürünün NGP kodunu gösterir. NGP bir ürün için geçerli değilse **0** (sıfır) gösterilir. NGP kodunu ayarlayabilirsiniz. Hareketi seçin ve sonra **Genel** sekmesinde, **Kodlar** bölümünde, **NGP** alanında gerekli NGP kodunu seçin.

### <a name="intrastat-transfer"></a>İntrastat transferi

**İntrastat** sayfasında, Eylem Bölmesi'nde, satış siparişlerinizden, serbest metin faturalarınızdan, satın alma siparişlerinizden, satıcı faturalarınızdan, satıcı ürün girişlerinden, proje faturalarından ve transfer emirlerinizden topluluk içi ticaret hakkındaki bilgileri otomatik olarak aktarmak için **Transfer**'i seçebilirsiniz. Yalnızca varış ülkesi veya bölgesi (gönderimler için) veya konsinye (gelişler için) olarak bir AB ülkesine sahip belgeler aktarılacaktır.

DEB raporu; AB Satış Listesi ve İntrastat raporunun bir kombinasyonu olduğundan, bir AB ülkesinden (taraf A) başka bir AB ülkesine (taraf C) doğrudan teslimat yapıldığı ve üçgen anlaşmanın ortasında bir Fransız tüzel kişiliğinin (taraf B) bulunduğu *üçgen* işlemleri de içerir.

### <a name="generate-a-deb-intrastat-report"></a>DEB (İntrastat) raporu oluşturma

1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin.
2. Eylem Bölmesi'nde **Çıkış** > **Rapor**'u seçin.
3. **İntrastat Raporu** iletişim kutusunda aşağıdaki alanları ayarlayın.

    | Alan            | Tanım                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Başlangıç tarihi        | Raporun başlangıç tarihini seçin.                                                                                               |
    | Bitiş tarihi          | Raporun bitiş tarihini seçin.                                                                                                 |
    | Dosya oluştur    | .txt dosyası oluşturmak için bu seçeneği **Evet** olarak ayarlayın.                                                                                 |
    | Dosya adı        | İntrastat raporunuz için .txt dosyasının adını girin.                                                                          |
    | Rapor oluştur  | .xml dosyası oluşturmak için bu seçeneği **Evet** olarak ayarlayın.                                                                                |
    | Rapor dosyası adı | Gerekli adı girin.                                                                                                            |
    | Yalnızca düzeltmeler | Yalnızca düzeltmeleri göstermek için bu seçeneği **Evet** olarak ayarlayın. Hem normal hareketleri hem de düzeltmeleri raporlamak için **Hayır** olarak ayarlayın.         |
    | Yön        | Topluluk içi gelenlerle ilgili bir rapor için **Gelenler**'i seçin. Topluluk için gönderimler hakkında rapor için **Gönderimler**'i seçin. |

## <a name="example"></a>Örnek

Aşağıdaki örnekte, Fransızca İntrastat'ın nasıl ayarlanacağı ve DEB raporunun nasıl oluşturulacağı gösterilmektedir. Tüzel kişilik olarak **DEMF**'yi kullanın.

1. [Microsoft Dynamics Lifecycle Services'te (LCS),](https://lcs.dynamics.com/Logon/Index) paylaşılan varlık kitaplığında, İntrastat bildirimi için aşağıdaki ER yapılandırmalarının en son sürümlerini yükleyin:

    - Intrastat modeli
    - Intrastat raporu
    - Intrastat INTRACOM (FR)

2. Finance'te bir hareket kodu ayarlayın:

    1. **Vergi** > **Kurulum** > **Dış ticaret** > **Hareket kodları**'na gidin.
    2. Eylem Bölmesinde, **Yeni**'yi seçin.
    3. **Hareket kodu** alanına **11** girin.
    4. **Ad** alanına **Satınalma veya Satış** girin.
    5. Eylem bölmesinde, **Kaydet**'i seçin.

3.  Ürün hiyerarşisi ayarlama:

    1. **Ürün bilgileri yönetimi** > **Kurulum** > **Kategoriler ve öznitelikler** > **Kategori hiyerarşileri**'ne gidin.
    2. Kılavuzda **İntrastat**'ı seçin. Ardından, Eylem Bölmesi'nde, **Kategori hiyerarşisi** sekmesinin **Koru** grubunda **Düzenle**'yi seçin.
    3. Eylem Bölmesi'nde **Yeni kategori düğümü**'nü seçin.
    4. **Ad** alanına **Autres Libournais** girin.
    5. **Kod** alanına **2204 21 42** girin
    6. Eylem bölmesinde, **Kaydet**'i seçin.

4. **Vergi** > **Kurulum** > **Dış ticaret** > **Dış ticaret parametreleri**'ne gidin ve şu adımları izleyin:

    1. **İntrastat** sekmesinde, **Genel** hızlı sekmesinde, **Hareket kodu** alanında **11**'i seçin.
    2. **Elektronik raporlama** hızlı sekmesinde, **Dosya biçimi eşlemesi** alanında **İntrastat INTRACOM (FR)** öğesini seçin.
    3. **Rapor biçimi eşlemesi** alanında **İntrastat raporu**'nu seçin.
    4. **Emtia kodu hiyerarşisi** hızlı sekmesinde, **Kategori hiyerarşisi** alanında **İntrastat**'ı seçin.

5. NGP kodu ayarlama:

    1. **Vergi** > **Kurulum** > **Dış ticaret** > **NGP kodları**'na gidin.
    2. Eylem Bölmesinde, **Yeni**'yi seçin.
    3. **NGP** alanına **8** girin.
    4. **Açıklama adı** alanına **NGP 8** girin.
    5. Eylem bölmesinde, **Kaydet**'i seçin.

6. NGP kodunu bir ürüne atama:

    1. **Ürün bilgileri yönetimi** > **Ürünler** > **Serbest bırakılan ürünler**'e gidin.
    2. Kılavuzda, **0001**'i seçin.
    3. **Dış ticaret** hızlı sekmesinde, **NGP** alanında **8**'i seçin.
    4. **Emtia** alanında, **2204 21 42**'yi seçin.
    5. Eylem bölmesinde, **Kaydet**'i seçin.

7. Yeni ürünü içeren bir satış siparişi oluşturun:

    1. **Alacak hesapları** > **Siparişler** > **Tüm satış siparişleri**'ne gidin.
    2. Eylem Bölmesinde, **Yeni**'yi seçin.
    3. **Satış** **siparişi** **oluştur** iletişim kutusunda, **Müşteri** bölümünde, **Müşteri** **hesabı** alanında **100001**'i seçin.
    4. **Adres** bölümünde, **Teslimat adresi** alanında, adres oluşturmak için artı işaretini (**+**) seçin.
    5. **Yeni adres** iletişim kutusunda, **Açıklamanın Adı** alanına **Almanya** girin.
    6. **Ülke/bölge** alanında **DEU**'yu seçin.
    7. **Tamam**'ı seçin.
    8. **Satış siparişi oluştur** iletişim kutusunda **Tamam**'ı seçin.
    9. **Satış** **siparişi satırları** hızlı sekmesinde, **Madde numarası** alanında **0001**'i seçin.
    10. Eylem bölmesinde, **Kaydet**'i seçin.
    11. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda **Fatura**'yı seçin.
    12. **Faturayı deftere naklet** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Parametre** bölümünde, **Miktar** alanında **Tümü**'nün öğesini seçin. Ardından faturayı deftere nakletmek için **Tamam**'ı seçin.

8.  DEB raporunu oluşturma:

    1. **Vergi** > **Bildirimler** > **Dış ticaret** > **İntrastat**'a gidin:
    2. Eylem Bölmesi'nde. **Transfer**'i seçin.
    3. **İntrastat (Transfer)** iletişim kutusunda, **Parametreler** bölümünde, **Müşteri faturası** seçeneğini **Evet** olarak ayarlayın. Daha sonra **Tamam**'ı seçin.
    4. Hareketleri **Tarih** alanına göre sıralayın. En üstteki hareket sonuç hareketidir. **NGP** alanı otomatik olarak ayarlanır.
    5. Eylem Bölmesi'nde **Çıktı** &gt; **Rapor**'u seçin.
    6. **İntrastat Raporu** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Tarih** bölümünde, oluşturduğunuz satış siparişinin ayını seçin.
    7. **Dışarı aktarma seçenekleri** bölümünde, **Dosya oluştur** seçeneğini **Evet** olarak ayarlayın.
    8. **Dosya adı** alanına gerekli adı girin.
    9. **Tamam**'ı seçin ve raporu gözden geçirin.

