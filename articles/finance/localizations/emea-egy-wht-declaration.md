---
title: Mısır için stopaj vergisi beyanı
description: Bu konu, Mısır için stopaj vergisi beyanının nasıl yapılandırılacağını ve oluşturulacağını açıklar.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: afb9f95458089e854335399ea3d14ba229c02bbd
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349885"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a>Mısır için stopaj vergisi beyanı (EG-00005)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a>Genel bakış
Bu konu, Mısır'da yasal varlıklar için stopaj vergisi beyanı ve stopaj vergisi beyanı formları Form 41 ve Form 11'in nasıl ayarlanacağını ve oluşturulacağını açıklamaktadır. 

Tüm Mısırlı varlıklar yerel tedarikçiler ve servis sağlayıcılarından alınan tüm vergileri özetleyen Form 41'i hazırlamalıdır. Form 41'in yanı sıra, yabancı sağlayıcılardan alınan tüm vergilerin ayrıntılarını belirtmek için form 11'i oluşturulmalıdır. 

Dynamics 365 Finance'deki **stopaj vergisi beyan** raporu aşağıdaki raporları içerir:

- Beyan formu No. 41
- Beyan formu No. 11
    
    
## <a name="prerequisites"></a>Önkoşullar
Yasal varlığın birincil adresi Mısır'da olmalıdır.
**Özellik yönetimi** çalışma alanında şu özellik etkinleştirilmelidir:

   - **Genel stopaj vergisi**

Özellikleri etkinleştirme hakkında daha fazla bilgi için [Özellik yönetimine genel bakış](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)'a bakın

1. **Vergi** > **Kurulum** > **Parametreler** > **Genel kayıt defteri parametreleri**'ne gidin ve **Stopaj vergisi** sekmesinde **Genel stopaj vergisini etkinleştir** seçeneğini **Evet** olarak ayarlayın.
2. **Elektronik raporlama** çalışma alanında, aşağıdaki elektronik raporlama biçimlerini depodan içe aktarın:

    - WHT Beyannamesi Excel'i(EG)

    > [!NOTE]
    > Yukarıdaki biçim **Vergi beyanı modeline** dayanır ve **vergi beyanı model eşleştirmesini** kullanır. Bu ek yapılandırmalar otomatik olarak alınır.

Elektronik raporlama yapılandırmalarını içe aktarma hakkında daha fazla bilgi için, bkz. [Elektronik raporlama yapılandırmalarını Lifecycle Services'den indirme](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Elektronik raporlama yapılandırmalarını indirme

Mısır için WHT beyan formunun uygulanması, elektronik raporlama (ER) yapılandırmalarına dayanır. Yapılandırılabilir raporlamanın özellikleri ve kavramları hakkında daha fazla bilgi için [Elektronik raporlama](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) konusuna bakın.

Üretim ve Kullanıcı kabul sınamaları (UAT) ortamları için, [Elektronik raporlama yapılandırmalarını Lifecycle Services'den indirme](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) konusundaki yönergeleri izleyin.

Bir Mısır yasal varlığında stopaj beyanları oluşturmak için, aşağıdaki yapılandırmaları yüklemeniz gerekir:

- Vergi beyanı modeli.sürüm.82.xml veya sonraki sürüm
- Vergi beyanı modeli eşleme.sürümü.82.133.xml veya sonraki sürüm
- WHT Beyanı Excel'i (EG).sürüm.82.21 veya sonraki bir sürüm

Lifecycle Services (LCS) veya genel depodan ER yapılandırmalarını indirmeyi tamamladıktan sonra aşağıdaki adımları tamamlayın.

1. **Elektronik raporlama** çalışma alanına gidin ve **Raporlama yapılandırmaları** kutucuğunu seçin.
1. **Yapılandırmalar** sayfasında Eylem Bölmesindeki **Değiştir > XML dosyasından yükle**'yi seçin.
1. Tüm dosyaları önceki madde işaretlerinde listelendikleri sırayla yükleyin. Tüm yapılandırmalar yüklendikten sonra, yapılandırma ağacının Finance'te bulunması gerekir.

## <a name="set-up-application-specific-parameters"></a>Uygulamaya özgü parametreleri ayarlama

Uygulamaya özgü parametreler seçeneği, **Stopaj vergisi öğe grubu** yapılandırmasına veya aramanın tanımında belirtilen başka kriterlere bağlı olarak kullanıcıların vergi işlemlerinin oluşturulan raporun her satırında nasıl sınıflandırılacağını ve hesaplanacağını belirten kriterleri belirlemesine olanak sağlar.

Stopaj beyanı formu Form 41, stopaj vergisi işlemlerinin **indirim kodu türü** adlı vergi dairesi sınıflandırmasına göre sınıflandırılmasının gerektiği belirli bir sütun içerir. İşlemler deftere nakledilirken bu yeni sınıflandırmaları yeni giriş verileri olarak eklemek yerine, sınıflandırmalar, Mısır için stopaj raporlarının gereksinimlerini karşılayacak şekilde **Yapılandırmalar** > **Uygulamaya özgü parametreler ayarla** > **Ayarla** bölümünde sunulan farklı aramalara göre belirlenecektir. 

Aşağıdaki yapılandırma stopaj beyanı formu Form 41 raporunda bulunan işlemleri sınıflandırmak için kullanılır:

- **DiscountTaxTypeLookup** -> Sütun No 18 

WHT beyanı ve ilgili defter raporları oluşturmak için kullanılan farklı aramaları ayarlamak üzere aşağıdaki adımları tamamlayın. 

1. **Elektronik raporlama** çalışma alanında, WHT beyan raporunda işlemleri sınıflandırma kurallarını ayarlamak için **Yapılandırmalar** > **Ayarla**'yı seçin. 
2. Geçerli sürümü seçin ve **aramalar** hızlı sekmesinde arama adını seçin. Örneğin, **DiscountTaxTypeLookup**. Bu arama vergi dairesi için gereken indirim tiplerinin listesini tanımlar.
3. **Koşullar** hızlı sekmesinde, **Ekle**'yi seçin ve **Arama sonucu** sütunundaki yeni satıra **Sütun 18**'deki sınıflandırmayı temsil eden ilgili satırı seçin.
4. **Stopaj vergisi öğe grubu** sütununda, Sınıflandırmayı tanımlamak için kullanılan ilgili kodu seçin. Örneğin, **izin verilen indirim**.  
5. Tüm kullanılabilir aramalar için 3. ve 4. adımları yineleyin.
6. Son kayıt satırını eklemek için **Ekle**'yi tekrar seçin ve **Arama sonucu** sütununda **Geçerli değil**'i seçin. 
7. Kalan sütunlarda, **boş değil** seçeneğini belirleyin. 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a>Genel kayıt defteri parametreleri ayarlama

Microsoft Excel biçiminde WHT beyan formu raporları oluşturmak için **Genel kayıt defteri parametreleri** sayfasında bir ER biçimi tanımlayın.

1. **Vergi** > **Ayar** > **Genel kayıt defteri parametreleri**'ne gidin.
2. **Stopaj vergisi** sekmesinde, **WHT beyan biçimi eşlemesi** alanında, **WHT Beyanı Excel'i (EG)** seçeneğini belirleyin. Alanı boş bırakırsanız, SSRS biçiminde standart satış vergisi raporu oluşturulur.


![Beyan formu.](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a>Stopaj beyanı formlarını oluştur
Stopaj beyanı formunun belirli bir dönem için hazırlanması ve gönderilmesi işlemi, ödeme vergisini kapatma ve deftere nakletme işi sırasında deftere nakledilen stopaj vergisi işlemlerine dayanır. Genel stopaj vergisi hakkında daha fazla bilgi için bkz. [Genel stopaj vergisi](../general-ledger/global-withholding-tax-overview.md).

Vergi beyanı raporunu oluşturmak için aşağıdaki adımları tamamlayın.

1. **Vergi** > **Beyanlar** > **Stopaj vergisi** > **Stopaj vergisi ödemesi*'ne gidin.
2. Kapatma dönemini seçin ve rapor için başlangıç tarihini seçin. 
3. İşlem tarihini girin ve ardından **Tamam**'ı seçin.
4. Açılan iletişim kutusunda bir veya daha fazla form türü seçin **Form No. 41**, **Form No. 11** veya **yok**. **Yok** seçeneğini belirlerseniz standart rapor oluşturulur. 
5. Dili seçin. Tüm raporlar **en-us** ve **ar-eg** dillerine çevrilir.
6. Vergi ödemesinin yapılacağı bankanın adını ve şubesini girin.
7. İş türünü seçin ve sonra çek ve belge numaralarını girin. 
8. Varlık tipini girin. 
9. Formu atamak için kayıtlı kişinin adını girin ve rapor oluşturmayı onaylamak için **Tamam**'ı seçin. 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
