---
title: Fransızca İntrastat
description: Bu makalede, Fransa'daki İntrastat bildirimi hakkında bilgiler yer almaktadır.
author: anasyash
ms.date: 11/30/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 2076649c7fff9f47b9c1fda62a103168b19bb973
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831818"
---
# <a name="french-intrastat"></a>Fransızca İntrastat

[!include[banner](../includes/banner.md)]

Fransa'da katma değer vergisi (KDV) için kayıtlı olan ve diğer Avrupa Birliği (AB) ülkeleriyle ticaret yapan şirketler, Fransa'ya ve Fransa'dan mal ve hizmet alışverişini beyan etmelidir. Declaration d'exchanges de biens (Mal Ticareti Beyanı veya DEB), AB Satış Listesi ve İntrastat raporunun birleşimidir. Tüm topluluk içi mal satışları için bu raporu aylık olarak göndermeniz gerekir.

DEB raporunu iki elektronik metin dosyası biçiminden herhangi biri olarak oluşturabilirsiniz: SAISUNIC 330 veya INTRACOM biçiminde.

Aşağıdaki tabloda, Fransızca İntrastat bildiriminde yer alan alanlar SAISUNIC 330 biçiminde gösterilmektedir. Tablo ayrıca her bir alanın rapor düzeylerini de gösterir. Bir alan aşağıdaki rapor düzeylerine sahip olabilir:

- **4** – Vergi beyannamesi.
- **1** – İstatistiksel yanıt.
- **5** – Sevkiyat ve vergi beyannamesi için istatistiksel yanıt ve birleşik dolum.

| Alan                       | Rapor düzeyleri |
|-----------------------------|---------------|
| Referans Dönemi         | 4, 1, 5       |
| Beyanname Sayısı       | 4, 1, 5       |
| Satır Numarası                 | 4, 1, 5       |
| Ülkenin ISO Kodu (FR)       | 4, 1, 5       |
| Tamamlayıcı Kod          | 4, 1, 5       |
| Siren Numarası                | 4, 1, 5       |
| Müşterinin KDV Kodu        | 4, 1, 5       |
| Yönerge Kodu              | 4, 1, 5       |
| Hareket Türü            | 4, 1, 5       |
| Yükümlülük Düzeyi            | 4, 1, 5       |
| Emtia Kodu              | 1, 5          |
| Ulusal NGP                | 1, 5          |
| İlçe (Departman)         | 1, 5          |
| İşlemin Niteliği       | 1, 5          |
| Menşe Ülke      | 1, 5          |
| Menşe Ülke - İthalat | 1, 5          |
| Son Hedef - İhracat | 1, 5          |
| Fatura Değeri               | 4, 1, 5       |
| İstatistiksel Değer           | 1, 5          |
| Net Ağırlık                  | 1, 5          |
| Ek Birimler            | 1, 5          |
| Taşıma Kodu              | 1, 5          |

Aşağıdaki tabloda, Intracom biçiminde Fransızca İntrastat bildirimine dahil edilen alanlar gösterilmektedir. Tablo ayrıca her bir alanın rapor düzeylerini de gösterir. Bir alan aşağıdaki rapor düzeylerine sahip olabilir:

- **4** – Vergi beyannamesi.
- **1** – İstatistiksel yanıt.
- **5** – Sevkiyat ve vergi beyannamesi için istatistiksel yanıt ve birleşik dolum.

| Alan                       | Rapor düzeyleri |
|-----------------------------|---------------|
| Yön kodu              | 4, 1, 5       |
| Beyanname Sayısı       | 4, 1, 5       |
| Satır Sayısı              | 4, 1, 5       |
| Siren                       | 4, 1, 5       |
| İlçe (Departman)         | 1, 5          |
| Taşıma Kodu              | 1, 5          |
| Menşe Ülke           | 1, 5          |
| İşlemin Niteliği       | 1, 5          |
| Fatura Değeri               | 4, 1, 5       |
| Teslimat Şekilleri           | 1, 5          |
| Hareket Türü            | 4, 1, 5       |
| Yükümlülük Düzeyi            | 4, 1, 5       |
| Emtia Kodu              | 1, 5          |
| Ulusal NGP                | 1, 5          |
| Net Ağırlık                  | 1, 5          |
| İstatistiksel Değer           | 1, 5          |
| Ek Birimler            | 1, 5          |
| Menşe Ülke - İthalat | 1, 5          |
| Son Hedef - İhracat | 1, 5          |
| Müşterinin KDV Kodu        | 4, 1, 5       |
| Tamamlayıcı Kod          | 4, 1, 5       |
| Referans Dönemi         | 4, 1, 5       |

## <a name="set-up-intrastat"></a>İntrastat'ı ayarlama

- [Microsoft Dynamics Lifecycle Services'te](https://lcs.dynamics.com/Logon/Index) Paylaşılan varlık kitaplığında, İntrastat bildirimi için aşağıdaki Elektronik raporlama (ER) yapılandırmalarının en son sürümlerini indirin:

    - Intrastat modeli
    - Intrastat raporu
    - Intrastat INTRACOM (FR)
    - Intrastat SAISUNIC (FR)

    Daha fazla bilgi için bkz. [Lifecycle Services'dan Elektronik raporlama yapılandırmalarını yükleme](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

### <a name="set-up-vat-ids"></a>KDV No ayarlama

#### <a name="set-up-vat-codes-for-your-company"></a>Şirketiniz için KDV kodları ayarlama

1. **Vergi** \> **Kurulum** \> **Satış vergisi** \> **Vergi muafiyet numaraları**'na gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Ülke/bölge** alanında **FRA**'yu seçin.
4. **Vergi muafiyet numarası ithalat** alanına, şirketinizin KDV numarası anahtarını girin.
5. **Kuruluş yönetimi** \> **Kuruluşlar** \> **Tüzel Kişilikler**'e gidin ve şirketinizi seçin.
6. **Dış ticaret ve lojistik** hızlı sekmesinde, **İntrastat** bölümünde, **KDV muafiyet numarası ihracat** ve **KDV muafiyet numarası ithalat** alanlarını adım 4'te oluşturduğunuz koda ayarlayın.
7. **Vergi kaydı** hızlı sekmesinde, **Vergi sicil numarası** alanına şirketinizin vergi sicil numarasını girin.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>Ticaret ortakları için KDV No ayarlama

##### <a name="create-a-registration-type-for-the-company-code"></a>Şirket kodu için kayıt türü oluşturma

Şirketinizin iş yapan tüm ülkeler veya bölgeler için KDV kodu kayıt türleri oluşturmanız gerekir.

1. **Kuruluş yönetimi** \> **Genel adres defteri** \> **Kayıt türleri** \> **Kayıt türleri**'ne gidin.
2. Eylem bölmesinde, KDV kimliği için kayıt türü oluşturmak üzere **Yeni**'yi seçin.
3. **Kayıt türü ayrıntıları gir** iletişim kutusunda, **Ad** alanına yeni kayıt türü için bir ad girin. Örneğin, **KDV No** girin.
4. **Ülke/bölge** alanında, ticari ortağının ülkesini veya kaynak bölgesini seçin.
5. **Oluştur**'u seçin.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Kayıt türünü kayıt kategorisiyle eşleştir

1. **Kuruluş yönetimi** \> **Genel adres defteri** \> **Kayıt türleri** \> **Kayıt kategorileri**'ne gidin.
2. Eylem bölmesinde, her kayıt türü ve bir kayıt kategorisi arasına bağlantı oluşturmak için **Yeni**'yi seçin.
3. KDV koduna ait kayıt türü için **KDV kodu** kayıt kategorisini seçin.
4. Şirketinizin iş amaçlı olduğu ülkeler veya bölgeler için oluşturduğunuz diğer kayıt türleri için 2 ve 3 numaralı adımları yineleyin.

##### <a name="set-up-the-vat-number-of-a-trading-partner"></a>Bir ticaret ortağının KDV numarasını ayarlama

1. **Alacak hesapları** \> **Müşteriler** \> **Tüm müşteriler**'e gidin.
2. Kılavuzda, bir müşteri seçin.
3. Eylem Bölmesi'nde, **Müşteri** sekmesindeki **Kayıt** grubunda **Kayıt Kimlikleri**'ni seçin.
4. **Kayıt Kodu** hızlı sekmesinde kayıt kimliği oluşturmak için **Ekle**'ye tıklayın.
5. **Kayıt türü** alanında, şirket kodu için daha önce oluşturduğunuz kayıt türlerinden birini seçin.
6. **Kayıt numarası** alanına şirketin KDV numarasını girin.
7. Eylem Bölmesi'nde **Kaydet**'i seçin ve sonra sayfayı kapatın.

Daha fazla bilgi için bkz. [Kayıt Kimlikleri](emea-registration-ids.md).

### <a name="set-up-foreign-trade-parameters"></a>Dış ticaret parametreleri ayarla

1. **Vergi** \> **Kurulum** \> **Dış ticaret** \> **Dış ticaret parametreleri**'ne gidin.
2. **İntrastat** sekmesinde, **Elektronik raporlama** hızlı sekmesinde, **Dosya biçimi eşleme** alanında **İntrastat INTRACOM (FR)** veya **İntrastat SAISUNIC (FR)**'yi seçin.
3. **Rapor biçimi eşlemesi** alanında **İntrastat raporu**'nu seçin.
4. **Emtia kodu hiyerarşisi** hızlı sekmesinde, **Kategori hiyerarşisi** alanında **İntrastat**'ı seçin.
5. **Genel** hızlı sekmesinde, **Hareket kodu** alanında, malların transferleri için kullanılan kodu seçin.
6. **Alacak dekontu** alanında, malların iadeleri için kullanılan kodu seçin.
7. **Çalışan** alanında, ilgili kişinin adını seçin.
8. **İlgili kişi** sekmesinde, ilgili kişi hakkında bilgi ekleyin:

    - **Telefon** alanına, ilgili kişinin telefon numarasını girin.
    - **Faks** alanına, ilgili kişinin faks numarasını girin.

9. **Ülke/bölge özellikleri** sekmesinde, **Ülke/bölge** alanında, şirketinizin iş yaptığı tüm ülke veya bölgeleri listeleyin. AB üyesi olan her ülkenin İntrastat raporunuzda görüntülenmesi için her ülke için **Ülke/bölge türü** alanında **EU** seçeneğini belirleyin. Fransa için **Ülke/bölge türü** alanında, **Yurtiçi** seçeneğini belirleyin.

### <a name="set-up-compression-of-intrastat"></a>Intrastat sıkıştırmasını ayarla

- **Vergi** \> **Kurulum** \> **Dış ticaret** \> **İntrastat sıkıştırması**'na gidin ve İntrastat bilgileri özetlendiğinde karşılaştırılması gereken alanları seçin. Fransa İntrastat için aşağıdaki alanları seçin:
 
    - İstatistik prosedürü
    - Menşe ülkesi/bölgesi
    - Taşıma
    - Düzeltme
    - Ülke/bölge
    - Kaynak/hedef ilçesi
    - Yön
    - Gönderenin ülkesi/bölgesi
    - Hareket kodu
    - Emtia

### <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>İntrastat bildirimi için ürün parametrelerini ayarlayın

1. **Ürün bilgileri yönetimi** \> **Ürünler** \> **Serbest bırakılmış ürünler**'e gidin.
2. Kılavuzda, bir ürün seçin.
3. **Dış ticaret** hızlı sekmesindeki **İntrastat** bölümünde **Emtia** alanında emtia kodunu seçin. Emtia adı, İntrastat raporundaki **Emtia açıklaması** alanına yazdırılır.
4. **Kaynak** bölümünde, **Ülke/bölge** alanında, ürünün ülkesini veya kaynak bölgesini seçin.
5. **Stok yönetimi** hızlı sekmesinde, **Net ağırlık** alanına ürünün ağırlığını kilogram olarak girin.

### <a name="ngp-codes"></a>NGP kodları

DEB raporunda, ürünlerin kodlanması aşağıdaki unsurlardan oluşur:

- AB'nin tarifesini ve istatistiksel isimlendirmesini temsil eden sekiz basamaklı CN8 kodu.
- Varsa tek haneli Nomenclature Générale des Produits (NGP) ulusal ürün kodu.

2022'de NGP sadece üç tür ürün için geçerlidir:

- İnek, koyun ve keçilerden elde edilen bazı ürünler
- Askeri teçhizat
- Fransız şarapları

NGP kodlarını ayarlamalı ve ilgili ürünlere atamalısınız. **NGP** alanı daha sonra **İntrastat günlüğü** sayfasında otomatik olarak ayarlanır.

#### <a name="set-up-an-ngp-code"></a>NGP kodu ayarlama

1. **Vergi** \> **Kurulum** \> **Dış ticaret** \> **NGP kodları**'na gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **NGP** alanına tek basamaklı bir kod girin.
4. **Açıklama** alanına, kodun açıklamasını girin.

#### <a name="assign-an-ngp-code-to-a-product"></a>Ürüne NGP kodu atama

1. **Ürün bilgileri yönetimi** \> **Ürünler** \> **Serbest bırakılmış ürünler**'e gidin.
2. Kılavuzda, bir ürün seçin.
3. **Dış ticaret** hızlı sekmesinde, **İntrastat** bölümünde, **NGP** alanında uygun NGP kodunu seçin.

### <a name="set-up-warehouse-parameters-for-the-intrastat-declaration"></a>İntrastat bildirimi için ambar parametrelerini ayarlayın

1. **Ambar yönetimi** \> **Ayarlama** \> **Ambar** \> **Ambarlar**'a gidin.
2. Bir ambar seçin ve sonra **Adresler** hızlı sekmesinde, **Ekle** veya **Düzenle**'yi seçin.
3. İletişim kutusunda, **Şehir** alanında ambarın şehrini seçin. Şehrin durumu eyalet veya bölge, DEB raporunuz için ilçe olarak kullanılacaktır.

### <a name="set-up-the-transport-method"></a>Taşıma yöntemini ayarlayın

1. **Vergi** \> **Kurulum** \> **Dış ticaret** \> **Taşıma yöntemi**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Taşıma** alanına benzersiz bir kod girin. Fransa'daki şirketler bir basamaklı taşıma kodları kullanır.

### <a name="intrastat-journal"></a>İntrastat günlüğü

AB ülkeleriyledış ticaret için geçerli olan hareketlerinizi yönetmek için **Vergi** \> **Beyannameler** \> **Dış ticaret** \> **İntrastat**'a gidin. Daha fazla bilgi için bkz. [İntrastat'a genel bakış](emea-intrastat.md).

**NGP** sütunu Fransa'ya özgüdür ve ürünün NGP kodunu gösterir. NGP bir ürün için geçerli değilse **0** (sıfır) gösterilir. NGP kodunu ayarlamak için hareketi seçin ve sonra **Genel** sekmesinde, **Kodlar** bölümünde, **NGP** alanında gerekli NGP kodunu seçin.

#### <a name="intrastat-transfer"></a>İntrastat transferi

**İntrastat** sayfasında, Eylem Bölmesi'nde, satış siparişlerinizden, serbest metin faturalarınızdan, satın alma siparişlerinizden, satıcı faturalarınızdan, satıcı ürün girişlerinden, proje faturalarından ve transfer emirlerinizden topluluk içi ticaret hakkındaki bilgileri otomatik olarak aktarmak için **Transfer**'i seçebilirsiniz. Yalnızca varış ülkesi veya bölgesi (gönderimler için) veya konsinye (gelişler için) olarak bir AB ülkesine sahip belgeler aktarılacaktır.

DEB raporu; AB Satış Listesi ve İntrastat raporunun bir kombinasyonu olduğundan, bir AB ülkesinden (taraf A) başka bir AB ülkesine (taraf C) doğrudan teslimat yapıldığı ve üçgen anlaşmanın ortasında bir Fransız tüzel kişiliğinin (taraf B) bulunduğu *üçgen* işlemleri de içerir.

#### <a name="generate-a-deb-intrastat-report"></a>DEB (İntrastat) raporu oluşturma

1. **Vergi** \> **Beyannameler** \> **Dış Ticaret** \> **İntrastat**'a gidin.
2. Eylem Bölmesi'nde **Çıktı** \> **Rapor**'u seçin.
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

4. **İntrastat Raporu** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
5. **Elektronik rapor parametreleri** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Rapor düzeyi** alanında rapor düzeyini seçin. Rapor düzeyi **1 - istatistiksel bir yanıt**, **4 - vergi beyanı** veya **5 - sevkiyat ve vergi beyannamesinin istatistiksel yanıtı** olabilir.

## <a name="example"></a>Örnek

Aşağıdaki örnekte, Fransızca İntrastat'ın nasıl ayarlanacağı ve DEB raporunun nasıl oluşturulacağı gösterilmektedir. Tüzel kişilik olarak **DEMF**'yi kullanın.

### <a name="preliminary-setup"></a>Ön kurulum

1. [Microsoft Dynamics Lifecycle Services'te](https://lcs.dynamics.com/Logon/Index) paylaşılan varlık kitaplığında, İntrastat bildirimi için aşağıdaki ER yapılandırmalarının en son sürümlerini yükleyin:

    - Intrastat modeli
    - Intrastat raporu
    - Intrastat INTRACOM (FR)

2. Ürün hiyerarşisi ayarlama:

    1. **Ürün bilgi yönetimi** \> **Kurulum** \> **Kategoriler ve öznitelikler** \> **Kategori hiyerarşileri**'ne gidin.
    2. Kılavuzda **İntrastat**'ı seçin.
    3. Eylem Bölmesi'nde, **Kategori hiyerarşisi** sekmesinin **Koru** grubunda **Düzenle**'yi seçin.
    4. Eylem Bölmesi'nde **Yeni kategori düğümü**'nü seçin.
    5. **Ad** alanına **Autres Libournais** girin.
    6. **Kod** alanına **2204 21 42** girin.
    7. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-vat-ids"></a>KDV No ayarlama

#### <a name="set-up-vat-codes-for-your-company"></a>Şirketiniz için KDV kodları ayarlama

1. **Vergi** \> **Kurulum** \> **Satış vergisi** \> **Vergi muafiyet numaraları**'na gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Ülke/bölge** alanında **FRA**'yu seçin.
4. **Vergi muafiyet numarası** alanında **MS123456** öğesini seçin.
5. **Kuruluş yönetimi** \> **Kuruluşlar** \> **Tüzel kişilikler**'e gidin ve **DEMF** seçin.
6. **Dış ticaret ve lojistik** hızlı sekmesinde, **İntrastat** bölümünde, **KDV muafiyet numarası ihracat** ve **KDV muafiyet numarası ithalat** alanlarını adım 4'te oluşturduğunuz koda ayarlayın.
7. **Vergi kaydı** hızlı sekmesinde, **Vergi kayıt numarası** alanında, **123456789** girin.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>Ticaret ortakları için KDV No ayarlama

##### <a name="create-a-registration-type-for-the-company-code"></a>Şirket kodu için kayıt türü oluşturma

1. **Kuruluş yönetimi** \> **Genel adres defteri** \> **Kayıt türleri** \> **Kayıt türleri**'ne gidin.
2. Eylem bölmesinde, KDV kimliği için kayıt türü oluşturmak üzere **Yeni**'yi seçin.
3. **Kayıt türü ayrıntılarını girin** iletişim kutusunda, **Ad** alanına **KDV No** girin.
4. **Ülke/bölge** alanında **DEU**'yu seçin.
5. **Oluştur**'u seçin.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Kayıt türünü kayıt kategorisiyle eşleştir

1. **Kuruluş yönetimi** \> **Genel adres defteri** \> **Kayıt türleri** \> **Kayıt kategorileri**'ne gidin.
2. Eylem bölmesinde, her kayıt türü ve bir kayıt kategorisi arasına bağlantı oluşturmak için **Yeni**'yi seçin.
3. **DEU** ülkesi için **KDV No** kayıt türünde **KDV No** kayıt kategorisini seçin.

##### <a name="set-up-the-customers-vat-registration-number"></a>Müşterinin KDV kayıt numarasını ayarlayın

1. **Alacak hesapları** \> **Müşteriler** \> **Tüm müşteriler**'e gidin.
2. Kılavuzda, **DE-016**'yı seçin.
3. Eylem Bölmesi'nde, **Müşteri** sekmesindeki **Kayıt** grubunda **Kayıt Kimlikleri**'ni seçin.
4. **Kayıt Kodu** hızlı sekmesinde kayıt kimliği oluşturmak için **Ekle**'ye tıklayın.
5. **Kayıt türü** alanında **KDV No**'yu seçin.
6. **Kayıt numarası** alanına **DE9012** girin.
7. Eylem Bölmesi'nde **Kaydet**'i seçin ve sonra sayfayı kapatın.
8. **Fatura ve teslimat** hızlı sekmesinde, **Satış vergisi** bölümünde, **Vergi muafiyet numarası** alanında **DE9012** seçin.

### <a name="set-up-foreign-trade-parameters"></a>Dış ticaret parametreleri ayarla

1. **Vergi** \> **Kurulum** \> **Dış ticaret** \> **Dış ticaret parametreleri**'ne gidin.
2. **İntrastat** sekmesinde, **Genel** hızlı sekmesinde, **Hareket kodu** alanında **11**'i seçin.
3. **Elektronik raporlama** hızlı sekmesinde, **Dosya biçimi eşlemesi** alanında **İntrastat INTRACOM (FR)** öğesini seçin.
4. **Rapor biçimi eşlemesi** alanında **İntrastat raporu**'nu seçin.
5. **Emtia kodu hiyerarşisi** hızlı sekmesinde, **Kategori hiyerarşisi** alanında **İntrastat**'ı seçin.
6. **Çalışan** alanında bir kayıt seçin.
7. **İletişim** sekmesinde, **Telefon** alanına, ilgili kişinin telefon numarasını girin
8. **Faks** alanına, ilgili kişi faks numarasını girin.

### <a name="create-ngp-code"></a>NGP kodu oluşturma

1. **Vergi** \> **Kurulum** \> **Dış ticaret** \> **NGP kodları**'na gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **NGP** alanına **8** girin.
4. **Açıklama adı** alanına **NGP 8** girin.
5. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-product-information"></a>Ürün bilgilerini ayarlama

1. **Ürün bilgileri yönetimi** \> **Ürünler** \> **Serbest bırakılmış ürünler**'e gidin.
2. Izgarada, **D0001**'i seçin.
3. **Dış Ticaret** hızlı sekmesinde, **İntrastat** bölümündeki **NPG** alanında **8**'i seçin.
4. **Emtia** alanında, **2204 21 42**'yi seçin.
5. **Menşe** bölümündeki **Ülke/bölge** alanında, **FRA**'yu seçin.
6. **Stok yönetimi** hızlı sekmesindeki **Ağırlık ölçümleri** bölümünde **Net ağırlık** alanına **2** girin.
7. Eylem Bölmesi'nde **Kaydet**'i seçin ve sonra sayfayı kapatın.
8. Izgarada, **D0003**'i seçin.
9. **Dış ticaret** hızlı sekmesindeki **İntrastat** bölümünde, **Emtia** alanında **100 200 30**'ü seçin.
10. **Menşe** bölümündeki **Ülke/bölge** alanında, **DEU**'yu seçin.
11. **Stok yönetimi** hızlı sekmesindeki **Ağırlık ölçümleri** bölümünde **Net ağırlık** alanına **5** girin.
12. Eylem bölmesinde, **Kaydet**'i seçin.

### <a name="set-up-regime-codes"></a>Rejim kodlarını ayarlama

1. **Vergi** \> **Kurulum** \> **Dış ticaret** \> **İstatistik prosedürü**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **İstatistiksel yordam** alanında, **21** girin.
4. **Metin 1** alanına **Rejim kodu 21** girin.

### <a name="change-the-site-address"></a>Tesis adresini değiştirme

1. **Ambar yönetimi** \> **Kurulum** \> **Ambar** \> **Tesisler** öğesine gidin.
2. Kılavuzda, **1**'i seçin.
3. **Adresler** hızlı sekmesinde, **Düzenle**'yi seçin.
4. **Adresi düzenle** iletişim kutusunda, **Ülke/bölge** alanında **FRA**'yi seçin.
5. **Tamam**'ı seçin.
6. **Ambar yönetimi** \> **Kurulum** \> **Ambar** \> **Ambarlar**'a gidin, bir ambar seçin.
7. **Adresler** hızlı sekmesinde, **Ekle**'yi seçin.
8. **Yeni adres** iletişim kutusunda, **Ülke/bölge** alanında **FRA**'yi seçin.
9. **Şehir** alanında, **Bordeaux** seçin.
10. İletişim kutusunu kapatmak için **Tamam**'ı seçin.

### <a name="set-up-a-transport-method"></a>Taşıma yöntemi ayarlayın

1. **Vergi** \> **Kurulum** \> **Dış ticaret** \> **Taşıma yöntemi**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Taşıma** alanına, **3** yazın.
4. **Açıklama** alanına, **Yol taşıması** girin.

### <a name="assign-a-transport-mode-to-a-mode-of-delivery"></a>Taşıma modunu bir teslimat moduna atayın

1. **Tedarik ve kaynak atama** \> **Kurulum** \> **Dağıtım** \> **Teslimat modları**'na gidin.
2. Kılavuzda, **50**'i seçin.
3. **Dış ticaret** hızlı sekmesindeki **Taşıma** alanında **3**'i seçin.

### <a name="create-a-sales-order-with-an-eu-customer-that-includes-the-new-product"></a>AB müşterisi ile yeni ürünü içeren bir satış siparişi oluşturun

1. **Alacak hesapları** \> **Siparişler** \> **Tüm satış siparişleri**'ne gidin.
2. Eylem Bölmesinde, **Yeni**'yi seçin.
3. **Satış siparişi oluştur** iletişim kutusunda, **Müşteri** bölümünde, **Müşteri hesabı** alanında **DE-016** seçin.
4. **Adres** bölümünde, **Teslimat adresi** alanında, adres oluşturmak için artı işaretini (**+**) seçin.
5. **Yeni adres** iletişim kutusunda, **Açıklamanın Adı** alanına **Almanya** girin.
6. **Ülke/bölge** alanında **DEU**'yu seçin.
7. **Tamam**'ı seçin.
8. **Satış siparişi oluştur** iletişim kutusunda **Tamam**'ı seçin.
9. **Satış siparişi satırları** hızlı sekmesinde, **Madde numarası** alanında **0001**'i seçin.
10. **Satır ayrıntıları** hızlı sekmesindeki **Dış ticaret** sekmesinde **İstatistikler prosedürü** alanında **21**'i seçin.
11. **Kaynak eyalet** bölümünde **AL**'yi seçin.
12. Eylem bölmesinde, **Kaydet**'i seçin.
13. **Başlık** sekmesinde, **Teslimat** hızlı sekmesinde, **Teslimat** modu alanında, **50**'nin seçili olduğundan emin olun.
14. Eylem Bölmesi'nde, **Fatura** sekmesindeki **Oluştur** grubunda **Fatura**'yı seçin.
15. **Faturayı deftere naklet** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Parametre** bölümünde, **Miktar** alanında **Tümü**'nün öğesini seçin. Ardından faturayı deftere nakletmek için **Tamam**'ı seçin.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Hareketi İntrastat günlüğüne transfer etme ve sonucu inceleme

1. **Vergi** \> **Beyannameler** \> **Dış Ticaret** \> **İntrastat**'a gidin.
2. Eylem Bölmesi'nde, **Transfer Et**'i seçin.
3. **İntrastat (Transfer)** iletişim kutusunda, **Parametreler** bölümünde, **Müşteri faturası** seçeneğini **Evet** olarak ayarlayın. Daha sonra **Tamam**'ı seçin.
4. Hareketleri **Tarih** alanına göre sıralayın. En üstteki hareket sonuç hareketidir.

    ![intrastat sayfasındaki satış siparişini temsil eden satır.](media/intrastat_fr_1.png)

5. Hareket satırını seçin ve ardından daha fazla ayrıntı görüntülemek için **Genel** sekmesini seçin.

    ![İntrastat sayfasının Genel sekmesindeki satış siparişi ayrıntıları.](media/intrastat_fr_2.png)

6. Eylem Bölmesi'nde **Çıktı** \> **Rapor**'u seçin.
7. **İntrastat Raporu** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Tarih** bölümünde, oluşturduğunuz satış siparişinin ayını seçin.
8. **Dışarı aktarma seçenekleri** bölümünde, **Dosya oluştur** seçeneğini **Evet** olarak ayarlayın.
9. **Dosya adı** alanına gerekli adı girin.
10. **İntrastat Raporu** iletişim kutusunu kapatmak için **Tamam**'ı seçin.
11. **Elektronik rapor parametreleri** iletişim kutusunda, **Parametreler** hızlı sekmesinde, **Rapor düzeyi** alanında, **5 - sevkiyat ve vergi beyannamelerine istatistiksel yanıt** seçin ve raporu inceleyin.

    ![Gönderimler için Intrastat Intracom raporu.](media/intrastat_fr_3.png)

12. Oluşturulan Excel raporunu inceleyin.

    ![Gönderimler için İntrastat raporu.](media/intrastat_fr_4.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
