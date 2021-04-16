---
title: Mısır için KDV beyannamesi
description: Bu konu, Mısır için KDV iade formunun nasıl yapılandırılacağını ve oluşturulacağını açıklar.
author: sndray
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3ebb78f3fa481cc63376b7d6428cf4944bbf6f4c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839828"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>Mısır için KDV beyannamesi (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

Bu konu, Mısır'daki yasal varlıklar için KDV iade formunun ve satış ve satın alma defterlerinin nasıl ayarlanacağını ve oluşturulacağını açıklar.

Mısır için KDV iade formu, vadesi gelen toplam çıkış KDV vergi tutarını, kurtarılabilir toplam giriş KDV vergisi tutarını ve ilgili KDV vergi tutarı borcunun özetini içeren resmi belgedir. Form tüm vergi mükellefi türleri için kullanılır ve vergi dairesi portalı aracılığıyla el ile doldurulmalıdır. KDV iade formu genellikle KDV iade dosyası olarak da adlandırılır.

Dynamics 365 Finance'deki KDV iade formu aşağıdaki raporları içerir:

- Mevzuatta açıklandığı şekilde, KDV iade formunda satır maddesi başına tutar, düzeltme ve KDV tutarı dökümü sağlayan 10 numaralı KDV iade formu.
- Satış hareketleri defteri
- Satın alma hareketleri defteri

## <a name="prerequisites"></a>Önkoşullar
Yasal varlığın birincil adresi Mısır'da olmalıdır.
**Özellik yönetimi** çalışma alanında aşağıdaki özelliği etkinleştirin:

   - (Mısır) Satış ve satın alma vergisi raporu için kategori hiyerarşisi.

Özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'a bakın.

**Elektronik raporlama** çalışma alanında, aşağıdaki elektronik raporlama biçimini depodan içe aktarın:

- KDV beyannamesi Excel'i(EG)

> [!NOTE]
> Yukarıdaki biçim **Vergi beyanı modeline** dayanır ve **vergi beyanı model eşleştirmesini** kullanır. Ek yapılandırmalar otomatik olarak alınır.

Elektronik raporlama yapılandırmalarını içe aktarma hakkında daha fazla bilgi için, bkz. [Elektronik raporlama yapılandırmalarını Lifecycle Services'den indirme](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Elektronik raporlama yapılandırmalarını indirme

Mısır için KDV iade formunun uygulanması, elektronik raporlama (ER) yapılandırmalarına dayanır. Yapılandırılabilir raporlamanın özellikleri ve kavramları hakkında daha fazla bilgi için [Elektronik raporlama](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) konusuna bakın.

Üretim ve Kullanıcı kabul sınamaları (UAT) ortamları için, bkz. [Elektronik raporlama yapılandırmalarını Lifecycle Services'den indirme](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Bir Mısır legal varlığında KDV iade formunu ve ilgili raporları oluşturmak için, aşağıdaki yapılandırmaları yükleyin:

- Vergi beyanı modeli.sürüm.70.xml veya sonraki sürüm
- Vergi beyanı modeli eşleme.sürümü.70.120.xml veya sonraki sürüm
- KDV Beyanı Excel'i (EG).sürüm.70.32 veya sonraki bir sürüm

Lifecycle Services (LCS) veya genel depodan ER yapılandırmalarını indirdikten sonra aşağıdaki adımları tamamlayın.

1. **Elektronik raporlama** çalışma alanına gidin ve **Raporlama yapılandırmaları** kutucuğunu seçin.
1. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Değiştir** > **XML dosyasından yükle**'yi seçin.
1. Dosyaları yukarıda listelendikleri sırayla yükleyin. Tüm yapılandırmalar yüklendikten sonra, yapılandırma ağacının Finance'te bulunması gerekir.

## <a name="set-up-application-specific-parameters"></a>Uygulamaya özgü parametreleri ayarlama

Uygulamaya özgü parametreler, rapor oluşturulduğunda vergi işlemlerinin her satırda nasıl sınıflandırılacağını ve hesaplanacağını belirten kriterleri sağlar. Bu belirleme madde satış vergisi grubu, satış vergisi grubu, satış vergisi kodu ve arama tanımında oluşturulan diğer ölçütlerin yapılandırılmasına bağlıdır.

Mısır için satış ve Satın alma defteri raporları, Mısır'a özgü işlem, ürün ve belge türleri olarak belirli işlem sınıflandırmalarına karşılık gelen bir sütun kümesi içerir. İşlemler deftere nakledilirken bu yeni sınıflandırmaları yeni giriş verileri olarak eklemek yerine, sınıflandırmalar, Mısır için KDV raporlarının gereksinimlerini karşılayacak şekilde **Yapılandırmalar** > **Uygulamaya özgü parametreler ayarla** > **Ayarla** bölümünde sunulan farklı aramalara göre belirlenecektir. 

![Uygulamaya özgü parametreler sayfası](media/egypt-vat-declaration-setup1.png)

Aşağıdaki arama yapılandırmaları satın alma ve satış KDV defterleri raporlarındaki işlemleri sınıflandırmak için kullanılır:

- **PurchaseItemTypeLookup** > Sütun O: Madde türü
- **VATRateTypeLookup** > Sütun B: Vergi türü
- **VATRateTypeLookup** > Sütun C: Tablo madde türü
- **PurchaseOperationTypeLookup** > Sütun A: Belge türü
- **SalesOperationTypeLookup** > Sütun N: İşlem türü
- **SalesItemTypeLookup** > Sütun O: Madde türü

KDV beyanı ve ilgili defter raporları oluşturmak için kullanılan farklı aramaları ayarlamak üzere aşağıdaki adımları tamamlayın. 

1. **Elektronik raporlama** çalışma alanında, KDV iade formunun ilgili kutusundaki vergi işlemini tanımlayacak kuralları ayarlamak için **Yapılandırmalar** > **Ayarla**'yı seçin.
2. Geçerli sürümü seçin ve **aramalar** hızlı sekmesinde arama adını seçin. Örneğin, **SalesItemTypeLookup**. Bu arama, vergi dairesi tarafından istenen satış KDV defterindeki sınıflandırmaların listesini tanımlar.
3. **Koşullar** hızlı sekmesinde, **Ekle**'yi seçin ve **Arama sonucu** sütunundaki yeni satıra **O sütunundaki** sınıflandırmayı temsil eden ilgili satırı seçin.
4. **Satış vergisi grubu** sütununda, Sınıflandırmayı tanımlamak için kullanılan satış vergisi grubunu seçin. Örneğin, **Yurtiçi satış faturası**. Yapılandırma başka bir şekilde tanımlanırsa, madde satış vergisi grubunu, vergi kodunu veya ağaç nitelikleri birleşimini de kullanabilirsiniz. 
5. **Ad** sütununda, vergi işlemi sınıflandırmasını seçin.
6. Tüm kullanılabilir aramalar için 3-5 arasındaki adımları yineleyin.
7. Son kayıt satırını eklemek için **Ekle**'yi seçin ve **Arama sonucu** sütununda **Geçerli değil**'i seçin. 
8. Kalan sütunlarda, **boş değil** seçeneğini belirleyin. 

> [!NOTE]
> Son kaydı eklediğinizde, **Geçerli değil**, şu kuralı tanımlarsınız: Bağımsız değişken olarak iletilen satış vergisi grubu, madde satış vergisi grubu, vergi kodu ve ad önceki kurallardan herhangi birini karşılamadığında işlemler satış KDV defterine dahil edilmez. Bu kural rapor oluşturulurken kullanılmasa da, eksik bir kural yapılandırması olduğunda, rapor oluşturmada hataları önlemek için kural size yardımcı olur.

Aşağıdaki tablolarda, tanımlanan arama yapılandırmaları için önerilen yapılandırma örnekleri verilmiştir. 

**SalesItemTypeLookup**

| Arama sonucu         | Satır | Satış vergi grubu    | Madde satış vergisi grubu    | Vergi kodu (kod) | Kuruluş adı                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Yerel              | 1    | VAT_LOCAL          | *Boş değil*             | *Boş değil*     | Satışlar                 |
| Yerel              | 2    | VAT_LOCAL          | *Boş değil*             | *Boş değil*     | SalesCreditNote       |
| Yerel              | 3    | VAT_FINALC         | *Boş değil*             | *Boş değil*     | Satışlar                 |
| Yerel              | 4    | VAT_FINALC         | *Boş değil*             | *Boş değil*     | SalesCreditNote       |
| Yerel              | 5    | VAT_PUBLIO         | *Boş değil*             | *Boş değil*     | Satışlar                 |
| Yerel              | 6    | VAT_PUBLIO         | *Boş değil*             | *Boş değil*     | SalesCreditNote       |
| Dışarı aktar                | 7    | VAT_EXPORT         | *Boş değil*             | *Boş değil*     | Satışlar                 |
| Dışarı aktar                | 8    | VAT_EXPORT         | *Boş değil*             | *Boş değil*     | SalesCreditNote       |
| Makine ve ekipman | 9    | *Boş değil*        | VAT_M&E                 | *Boş değil*     | Satışlar                 |
| Makine ve ekipman | 10   | *Boş değil*        | VAT_M&E                 | *Boş değil*     | SalesCreditNote       |
| Parça makineleri        | 11   | *Boş değil*        | VAT_PARTS               | *Boş değil*     | Satışlar                 |
| Parça makineleri        | 12   | *Boş değil*        | VAT_PARTS               | *Boş değil*     | SalesCreditNote       |
| Muafiyetler            | 13   | VAT_EXE            | *Boş değil*           | *Boş değil*     | SaleExempt            |
| Muafiyetler            | 14   | VAT_EXE            | *Boş değil*           | *Boş değil*     | SalesExemptCreditNote |
| Geçerli değil        | 15   | *Boş*            | *Boş*                 | VAT_ADJ         | *Boş değil*           |
| Geçerli değil        | 16   | *Boş değil*        | *Boş değil*             | *Boş değil*     | *Boş değil*           |

 **SalesOperationTypeLookup**

| Arama sonucu  | Satır | Madde satış vergisi grubu    | Vergi kodu.    | Kuruluş adı                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Mallar          | 1    | VAT_GOODS               | *Boş değil* | Satışlar                 |
| Mallar          | 2    | VAT_GOODS               | *Boş değil* | SalesCreditNote       |
| Mallar          | 3    | VAT_GOODS               | *Boş değil* | SaleExempt            |
| Mallar          | 4    | VAT_GOODS               | *Boş değil* | SalesExemptCreditNote |
| Hizmetler       | 5    | VAT_SERV                | *Boş değil* | Satışlar                 |
| Hizmetler       | 6    | VAT_SERV                | *Boş değil* | SalesCreditNote       |
| Hizmetler       | 7    | VAT_SERV                | *Boş değil* | SaleExempt            |
| Hizmetler       | 8    | VAT_SERV                | *Boş değil* | SalesExemptCreditNote |
| Düzeltmeler    | 9    | *Boş*                 | VAT_ADJ     | Satışlar                 |
| Düzeltmeler    | 10   | *Boş*                 | VAT_ADJ     | Satınalma              |
| Geçerli değil | 11   | *Boş değil*             | *Boş değil* | *Boş değil*           |

**PurchaseItemTypeLookup**

| Arama sonucu          | Satır | Madde satış vergisi grubu    | Vergi kodu.    | Kuruluş adı                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Mallar                  | 1    | VAT_GOODS               | *Boş değil* | Satınalma                 |
| Mallar                  | 2    | VAT_GOODS               | *Boş değil* | PurchaseCreditNote       |
| Hizmetler               | 3    | VAT_SERV                | *Boş değil* | Satınalma                 |
| Hizmetler               | 4    | VAT_SERV                | *Boş değil*  | PurchaseCreditNote       |
| Makine ve ekipman  | 5    | VAT_M&E                 | *Boş değil* | Satınalma                 |
| Makine ve ekipman  | 6    | VAT_M&E                 | *Boş değil* | PurchaseCreditNote       |
| Parça makineleri         | 7    | VAT_PARTS               | *Boş değil* | Satınalma                 |
| Parça makineleri         | 8    | VAT_PARTS               | *Boş değil* | PurchaseCreditNote       |
| Muafiyetler             | 9    | VAT_EXE                 | *Boş değil*  | PurchaseExempt           |
| Muafiyetler             | 10   | VAT_EXE                 | *Boş değil* | PurchaseExemptCreditNote |
| Geçerli değil         | 11   | *Boş*                 | VAT_ADJ     | *Boş değil*              |
| Geçerli değil         | 12   | *Boş değil*             | *Boş değil* | *Boş değil*              |
| Geçerli değil         | 13   | *Boş*                 | *Boş değil* | *Boş değil*              |

**PurchaseOperationTypeLookup**

| Arama sonucu  | Satır | Satış vergi grubu  | Vergi kodu.    | Kuruluş adı                     |
|----------------|------|------------------|-------------|--------------------------|
| Yerel       | 1    | VAT_LOCAL        | *Boş değil* | Satınalma                 |
| Yerel       | 2    | VAT_LOCAL        | *Boş değil* | PurchaseCreditNote       |
| Yerel       | 3    | VAT_LOCAL        | *Boş değil* | PurchaseExempt           |
| Yerel       | 4    | VAT_LOCAL        | *Boş değil* | PurchaseExemptCreditNote |
| İçe aktarıldı       | 5    | VAT_IMPORT       | *Boş değil* | Satınalma                 |
| İçe aktarıldı       | 6    | VAT_IMPORT       | *Boş değil* | PurchaseCreditNote       |
| İçe aktarıldı       | 7    | VAT_IMPORT       | *Boş değil* | PurchaseExempt           |
| İçe aktarıldı       | 8    | VAT_IMPORT       | *Boş değil* | PurchaseExemptCreditNote |
| Düzeltmeler    | 9    | *Boş*          | VAT_ADJ     | PurchaseCreditNote       |
| Düzeltmeler    | 10   | *Boş*          | VAT_ADJ     | Satınalma                 |
| Geçerli değil | 11   | *Boş değil*      | *Boş değil* | *Boş değil*              |

**VATRateTypeLookup**

| Arama sonucu  | Satır | Vergi kodu (kod) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *Boş değil*     |
| SecondTable    | 4    | *Boş değil*     |
| Geçerli değil | 5    | *Boş değil*     |


## <a name="set-up-general-ledger-parameters"></a>Genel kayıt defteri parametreleri ayarlama

Microsoft Excel biçiminde KDV iade formu raporu oluşturmak için **Genel kayıt defteri parametreleri** sayfasında bir ER biçimi tanımlayın.

1. **Vergi** > **Ayar** > **Genel kayıt defteri parametreleri**'ne gidin.
2. **Satış vergisi** sekmesinde, **vergi seçenekleri** bölümünde **KDV beyannamesi biçim eşlemesi** alanında, **KDV beyanname Excel'i (EG)** seçeneğini belirleyin. Alanı boş bırakırsanız, SSRS biçiminde standart satış vergisi raporu oluşturulur.
3. **Kategori hiyerarşisi**'ni seçin. Bu kategori, dış ticaret sekmesi işlemlerinde bulunan ve kullanıcıların mal ve servisleri seçip sınıflandırmasına olanak veren Emtia kodunu etkinleştirir. Bu sınıflandırmanın açıklaması satış ve satın alma işlemleri raporlarında ayrıntılı olarak belirtilir. Bu yapılandırma isteğe bağlıdır.

![Beyan formu](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>KDV iadesi raporu oluşturma
Bir döneme ait bir KDV iadesi raporu hazırlama ve gönderme süreci, Satış vergisini kapatma ve deftere nakletme işi sırasında deftere nakledilen satış vergisi ödeme işlemlerine dayanır. Satış vergisi kapatma ve bildirme hakkında daha fazla bilgi için bkz. [Satış vergisine genel bakış](../general-ledger/indirect-taxes-overview.md).

Vergi beyanı raporunu oluşturmak için aşağıdaki adımları tamamlayın.

1. **Vergi** > **Beyanlar** > **Satış vergisi** > **Kapatma dönemi için satış vergisini bildir** veya **Satış vergisini kapat ve deftere naklet** bölümüne gidin.
2. **Kapatma dönemi**'ni seçin.
3. Başlangıç tarihini seçin ve satış vergisi ödeme sürümünü seçin.
5. **Tamam**'ı seçin. 
6. Varsa, önceki dönemden alacak tutarını girin veya tutarı sıfır olarak bırakın.
7. **Rapor ayrıntıları** alanında aşağıdaki mevcut seçeneklerden birini belirleyin: 
   - **Satınalma KDV'si defteri**: Satın alma vergisi işlem ayrıntıları raporunu oluşturun.
   - **Satış KDV'si defteri**: Satış vergisi işlem ayrıntıları raporunu oluşturun.
   - **KDV beyanı**: Yalnızca KDV beyanı iade formunu oluşturun.
8. Formu atamak için kayıtlı olan kişinin adını girin.
9. Dili seçin. Tüm raporlar **en-us** ve **ar-eg** dillerine çevrilir.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


