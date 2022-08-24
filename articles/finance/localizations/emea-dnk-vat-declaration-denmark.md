---
title: KDV beyannamesi (Danimarka)
description: Bu makalede, Danimarka'ya ilişkin ön katma değer vergisi (KDV) bildiriminin nasıl ayarlanacağı ve oluşturulacağı açıklanmaktadır.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: a47b2b98d86daf50876c783f879362ec1addb579
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272155"
---
# <a name="vat-declaration-denmark"></a>KDV beyannamesi (Danimarka)

[!include [banner](../includes/banner.md)]

Bu makalede, Danimarka'ya ilişkin ön katma değer vergisi (KDV) bildiriminin nasıl ayarlanacağı ve Microsoft Excel'de nasıl önizlemesinin yapılacağı açıklanmaktadır.

Raporu otomatik olarak oluşturmak için, öncelikle ön KDV beyannamesindeki her kutu için ayrı bir KDV hesabı tutacak yeterli satış vergisi kodu oluşturun. Ek olarak, ön KDV beyannamesi için Elektronik raporlama (ER) biçiminin uygulamaya özel parametrelerinde, satış vergisi kodlarını, KDV beyannamesindeki kutuların aramalarının arama sonucuyla ilişkilendirin.

Danimarka için **Rapor alanı aramasını** konfigüre etmelisiniz. Uygulamaya özel parametrelerin nasıl ayarlanacağı hakkında daha fazla bilgi için, bu makalenin ilerleyen kısımlarındaki [KDV beyannamesi alanları için uygulamaya özel parametreler ayarlama](#set-up-application-specific-parameters) bölümüne bakın.

Aşağıdaki tabloda, "Arama sonucu" sütunu, KDV beyanname biçimindeki belirli bir KDV Beyanname satırı için önceden konfigüre edilmiş arama sonucunu gösterir. Satış vergisi kodlarını arama sonucu ve daha sonra KDV beyannamesi satırı ile ilişkilendirmek için bu bilgileri kullanın.

### <a name="vat-declaration-overview"></a>KDV beyannamesine genel bakış

Danimarka'daki KDV beyannamesi aşağıdaki bilgileri içerir.

**Ödenecek VAT**

| Açıklama                                                  | Vergi temeli/Vergi tutarı | Arama sonucu/Toplam                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Çıkış KDV'si                                                   | Vergi tutarı          | **OutputVAT**</br> **DomesticVATUseTax** ("giriş KDV'si" kutusunda da raporlanır)                                                                                                                                                                                                                                                                       |
| Mal vs. ile ilgili KDV yurt dışında satın alındı                           | Vergi tutarı          | **PurchaseGoodsAbroad**</br>**PurchaseGoodsAbroadUseTax** ("giriş KDV'si" kutusunda da raporlanır)</br>**PurchaseGoodsEU** (vergi matrahı, "kutu A - malların alımı" olarak raporlanır.)</br>**PurchaseGoodsEUUseTax** (Vergi tutarı, "giriş KDV'si" kutusunda da raporlanır. Vergi matrahı, "kutu A - malların alımı" olarak raporlanır.)                   |
| Ters kaydedilecek KDV'ye tabi olarak yurtdışından satın alınan hizmetler için KDV | Vergi tutarı          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax** ("giriş KDV'si" kutusunda da raporlanır)</br>**PurchaseServicesEU** (Vergi matrahı, "kutu A - hizmetlerin alımı" olarak raporlanır.)</br>**PurchaseServicesEUUseTax** (Vergi tutarı, "giriş KDV'si" kutusunda da raporlanır. Vergi matrahı, "kutu A - hizmetlerin alımı" olarak raporlanır.) |
| Toplam borç                                                | Vergi tutarı          | Önceki üç kutunun toplamı                                                                                                                                                                                                                                                                                                            |

**Kesintiler**

| Açıklama                                                                               | Vergi temeli/Vergi tutarı | Arama sonucu/Toplam                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Giriş KDV'si                                                                                 | Vergi tutarı          | **InputVAT**</br> **DomesticVATUseTax** ("çıkış KDV'si" kutusunda da raporlanır)</br>**PurchaseGoodsAbroadUseTax** ("yurt dışında satın alınan mallar vs. KDV'si" kutusunda da raporlanır)</br>**PurchaseServicesAbroadUseTax** ("satın alınan hizmetlerin KDV'si, geriye dönük gidere tabidir" kutusuna da bildirilir)</br>**PurchaseGoodsEUUseTax** ("yurt dışında satın alınan mallar vs. KDV'si" kutusunda da raporlanır)</br> **PurchaseServicesEUUseTax** ("satın alınan hizmetlerin KDV'si, geriye dönük gidere tabidir" kutusuna da bildirilir) |
| Petrol ve LPG harcı                                                                  | Vergi tutarı          | **OilGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Doğal gaz ve hava gazı harcı                                                             | Vergi tutarı          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Karbon harcı                                                                               | Vergi tutarı          | **CarbonDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2Duty                                                                                   | Vergi tutarı          | **CO2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Su gideri                                                                              | Vergi tutarı          | **WaterCharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Toplam kesintiler                                                                          | Vergi tutarı          | Önceki altı kutunun toplamı                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Toplam harç tutarı (pozitif tutar = ödeme yapma, negatif tutar = geri ödeme alma) | Vergi tutarı          | "Toplam borç" – "Toplam kesintiler"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Tamamlayıcı bilgiler**

| Açıklama                                                                                                                                                                                                                                | Vergi temeli/Vergi tutarı | Arama sonucu/Toplam                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| Kutu A - malların alımı. Birlik içi mal alımı KDV'si olmadan değer.                                                                                                                                                   | Vergi matrahı            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| Kutu A - hizmetlerin alımı. Birlik içi hizmet alımı KDV'si olmadan değer.                                                                                                                                             | Vergi matrahı            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| Kutu B - mal kaynağı - "KDV hariç AB satışlar"/DK VIES olarak bildirilecek. Birlik içi mal kaynağı KDV'si olmadan değer                                                                                                           | Vergi matrahı            | **SalesGoodsEU**                                |
| Kutu B - kaynaklar - "KDV hariç AB satışlar"/DK VIES olarak bildirilmeyecek.. Yükleme, montaj, mesafe satış ve vergiye tabi olmayan kişilere taşıma işleminin yeni yolu gibi Birlik içi kaynaklar için KDV'siz değer. | Vergi matrahı            | **SalesInstallationAssemblyEtcEU**              |
| Kutu B - hizmetlerin kaynağı. Satın almacının geriye dönük gider olarak KDV ödeme yükümlülüğüne sahip olduğu Birlik içi hizmetler kaynağı KDV'si olmadan değer - "KDV'siz AB Satışları"/DK VIES olarak bildirilmelidir.                          | Vergi matrahı            | **SalesServicesEU**                             |
| Kutu C - diğer malzemeler. Danimarka bölgesinde, diğer AB Üyesi Devletlere ve üçüncü ülkelere veya üçüncü bölgelere KDV'siz olarak teslim edilen mal ve hizmetlerin kaynak değeri.                                     | Vergi matrahı            | **OtherSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Satın alma karşı ödeme KDV'si

Satış vergisi kodlarını, kullanım vergisi kullanarak gelen karşı ödeme KDV'sini deftere nakletmek üzere konfigüre ederseniz, satış vergisi kodlarınızı, adda "UseTax" içeren **Rapor alanı aramasının** arama sonucu ile ilişkilendirin.

Alternatif olarak, iki ayrı satış vergisi kodu konfigüre edebilirsiniz: ödenmesi gereken KDV için bir adet ve KDV kesintisi için bir adet. Sonra her kodu **Rapor alanı aramasının** ilgili arama sonuçlarıyla ilişkilendirin.

Örneğin, vergiye tabi topluluk içi alımları için, kullanım vergisiyle **UT_S_EU** satış vergisi kodunu konfigüre edin ve bunu **Rapor alanı aramasının** **PurchaseGoodsEUUseTax** arama sonucu ile ilişkilendirin. Bu durumda, **UT_S_EU** satış vergisi kodunu kullanan vergi tutarları, "yurt dışında satın alınan mallar vs. KDV'si" ve "Giriş KDV'si" kutularına yansıtılır. Veri temelleri, "Kutu A - malların alımı"nda yansıtılır.

Alternatif olarak, iki satış vergisi kodu konfigüre edebilirsiniz:

- Vergi oranı değeri yüzde -25 olan **VAT_S_EU**
- Vergi oranı değeri yüzde 25 olan **InVAT_S_EU**

Sonra kodları **Rapor alanı aramasının** arama sonuçlarıyla aşağıdaki şekilde ilişkilendirin:

- **VAT_S_EU** öğesini, **PurchaseGoodsEU** arama sonucu ile ilişkilendirin.
- **InVAT_S_EU** öğesini, **InputVAT** arama sonucu ile ilişkilendirin.

Bu durumda, **VAT_S_EU** satış vergisi kodunu kullanan tutarlar, "yurt dışında satın alınan mallar vs. KDV'si" kutusu ve "Kutu A - malların alımı"nda yansıtılır. **InVAT_S_EU** satış vergisi kodu "Giriş KDV'si" kutusunda yansıtılır.

Ters kaydedilecek KDV yapılandırma hakkında daha fazla bilgi için bkz. [Ters masraflar](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Sistem parametrelerini yapılandırma

Bir KDV beyannamesi oluşturmak için KDV numarasını konfigüre etmelisiniz.

1. **Kuruluş yönetimi** > **Kuruluşlar** > **Tüzel kişilikler**'e gidin.
2. Tüzel kişiliği ve ardından **Kayıt kimlikleri**'ni seçin.
3. Danimarka'da adres seçin veya oluşturun, sonra da **Kayıt kodu** hızlı sekmesinde, **Ekle**'yi seçin.
4. **Kayıt türü** alanında, Danimarka'ya adanmış ve **KDV No** kayıt kategorisini kullanan kayıt türünü seçin.
5. **Kayıt numarası** alanına vergi numarasını girin.
6. **Genel** sekmesinde, **Etkin** alanına numaranın geçerli olacağı tarihi girin.

Kayıt kategorilerinin ve kayıt tiplerinin nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Kayıt Kimlikleri](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Danimarka için KDV beyannamesi önizlemesini ayarlama

### <a name="import-er-configurations"></a>ER yapılandırmaları içe aktarın

**Elektronik raporlama** çalışma alanını açın ve **KDV beyannamesi Excel (DK)** ER biçimini içe aktarın.

Daha fazla bilgi için bkz. [Yapılandırma hizmeti Genel deposundan ER yapılandırmalarını indirme](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a>KDV beyanname alanları için uygulamaya özel parametreleri ayarlama

> [!NOTE]
> **Özellik yönetimi** çalışma alanındaki **Önceki ER biçimleri sürümünden uygulamaya özel parametreleri kullan** özelliğini etkinleştirmenizi öneririz. Bu özellik etkinleştirildiğinde, bir ER biçiminin önceki sürümü için yapılandırılmış parametreler, aynı biçimin sonraki sürümü için otomatik olarak uygulanabilir duruma gelir. Bu özellik etkinleştirilmemişse, uygulamaya özel parametreleri her biçim sürümü için açık olarak konfigüre etmelisiniz. **Özellik yönetimi** çalışma alanındaki **Önceki ER biçimleri sürümünden uygulamaya özel parametreleri kullan** özelliği, Finans sürüm 10.0.23'ten itibaren kullanılabilir. Her yasal varlık için bir ER biçimi parametrelerinin nasıl ayarlanacağı hakkında daha fazla bilgi için, bkz. [Yasal varlık başına ER biçimi parametrelerini ayarlama](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Otomatik olarak bir KDV beyannamesi oluşturmak için uygulama ve arama sonuçlarında satış vergisi kodlarını, ER konfigürasyonuyla ilişkilendirin.

KDV beyannamesindeki kutuları hangi satış vergisi kodlarının oluşturacağını tanımlamak için bu adımları izleyin.

1. **Çalışma alanları** > **Elektronik raporlama**'ya gidin ve **Raporlama yapılandırmaları**'nı seçin.
2. **KDV beyanname Excel (DK)** yapılandırmasını seçin ve sonra **Konfigürasyonlar \> Uygulamaya özgü parametreler kurulumunu** seçin.
3. **Uygulamaya özel parametreler** sayfasında, **Aramalar** hızlı sekmesinde, **Rapor alanı araması**'nı seçin.
4. **Koşullar** hızlı sekmesinde, satış vergisi kodları ve rapor alanlarını ilişkilendirmek için aşağıdaki alanları ayarlayın.

    | Alan                  | Tanım                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Arama sonucu          | Rapor alanının değerini seçin. Değerler ve bunların KDV beyanname satırlarına atanması hakkında daha fazla bilgi için, bu makalenin önceki kısımlarında yer alan [KDV beyannamesine genel bakış](#vat-declaration-overview) bölümüne bakın.                                                                                               |
    | Vergi kodu.               | Rapor alanıyla ilişkilendirilecek satış vergisi kodunu seçin. Seçili satış vergisi kodunu kullanan deftere nakledilen vergi hareketleri ilgili bildirim kutusunda toplanır. Satış vergisi kodlarını, tek bir bildirim kutusunda tutarlar oluşturacak şekilde ayırmanızı öneririz. |
    | Hareket sınıflandırıcı | Bir bildirim kutusunu belirlemek için yeterli satış vergisi kodu oluşturduysanız, **\*Boş değil\*** seçeneğini belirleyin. Bir satış vergisi kodunun yalnızca bir bildirim kutusunda tutarlar oluşturması için yeterli satış vergisi kodu oluşturmadıysanız, bir hareket sınıflandırıcısı ayarlayabilirsiniz. Aşağıdaki hareket sınıflandırıcıları kullanılabilir:</br>-   **Satınalma**</br>-   **PurchaseExempt** (vergiden muaf satın alma)</br>-   **PurchaseReverseCharge** (bir satın alma ters masrafından elde edilen vergi alacağı)</br>-   **Satışlar**</br>-   **SalesExempt** (vergiden muaf satış)</br>-   **SalesReverseCharge** (bir satın alma ters masrafı veya satış ters masrafına ait vergi borcu)</br>-   **Kullanım vergisini kullanır**. </br>Her bir hareket sınıflandırıcısı için, alacak dekontuyla ilgili bir sınıflandırıcı da mevcuttur. Örneğin, bu sınıflandırıcılardan biri **PurchaseCreditNote**'tır (satın alma alacak dekontu).</br>Her satış vergisi kodu için iki satır oluşturmayı unutmayın: hareket sınıflandırıcı değerine sahip olan bir tane ve alacak dekontu değeri için hareket sınıflandırıcılarına sahip olan bir tane. |


    > [!NOTE]
    > Tüm satış vergisi kodlarını arama sonuçlarıyla ilişkilendirin. Herhangi bir satış vergisi kodunun KDV beyannamesinde değer üretmeleri gerekiyorsa, bunları **Diğer** arama sonucuyla ilişkilendirin.

    ![Uygulamaya özgü parametreler sayfası.](media/7db74920fad66a0db7fad60758698cc0.png)


5. **Durum** alanında, değeri **Tamamlandı** olarak değiştirin.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Excel'de önizleme tutarları için KDV raporlama biçimini ayarlama

1. **Özellik yönetimi** çalışma alanında, **KDV beyannamesi biçim raporları** özelliğini bulup seçin. Ardından **Şimdi etkinleştir**'i seçin.
2. **Genel muhasebe** > **Kurulum** > **Genel muhasebe parametreleri**'ne gidin.
3. **Satış vergisi** sekmesinde, **Vergi seçenekleri** hızlı sekmesinde, **KDV beyannamesi biçim eşlemesi** alanında, **KDV beyannamesi Excel'i (DK)** ER biçimini belirleyin.

   Bu biçim, **Kapatma dönemi raporu için satış vergisini bildir** raporunu çalıştırdığınızda yazdırılır. Ayrıca, **Satış vergisi ödemeleri** sayfasında **Yazdır**'ı seçtiğinizde de yazdırılır.

4. **Vergi daireleri** sayfasında vergi dairesini seçin ve sonra **Rapor düzeni** alanında, **Varsayılan**'ı seçin.

KDV beyanını, [birden çok KDV kaydına](emea-reporting-for-multiple-vat-registrations.md) sahip olan bir tüzel kişilikte konfigüre ediyorsanız, aşağıdaki adımları izleyin.

1. **Genel muhasebe** \> **Kurulum** \> **Genel muhasebe parametreleri**'ne gidin.
2. **Satış vergisi** sekmesinde, **Ülkeler/bölgeler için elektronik raporlama** hızlı sekmesinde, **DEU** için olan satırda, **KDV beyannamesi Excel'i (DK)** ER biçimini seçin.

## <a name="set-up-electronic-messages"></a>Elektronik iletileri ayarlama

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Elektronik iletiler için örnek ayarlara sahip veri paketini karşıdan yükleyin ve içe aktarın

Veri paketi, KDV beyanını Excel'de önizlemek için kullanılan elektronik ileti ayarları içerir. Bu ayarları genişletebilir veya kendi kendinize oluşturabilirsiniz. Elektronik mesajlarla nasıl çalışılacağı ve kendi ayarlarınızı nasıl oluşturacağınız hakkında daha fazla bilgi için, bkz. [Elektronik mesajlaşma](../general-ledger/electronic-messaging.md).

1. [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) içinde, Paylaşılan varlık kitaplığında, varlık türü olarak **Veri paketi**'ni seçin ve **DK KDV beyannamesi EM paketini** indirin. İndirilen dosya adı **DK VAT declaration package.zip**'dir.
2. Finance'te, **Veri yönetimi** çalışma alanında **İçe aktar**'ı seçin.
3. **İçe aktar** hızlı sekmesinde, **Grup adı** alanına iş için bir ad girin.
4. **Seçili varlıklar** hızlı sekmesinde **Dosya ekle**'yi seçin.
5. **Dosya ekle** iletişim kutusunda, **Kaynak veri biçimi** alanının **Paket** olarak ayarlandığını doğrulayın, **Yükle ve ekle**'yi seçin ve daha önce yüklediğiniz ZIP dosyasını seçin.
6. **Kapat**'ı seçin.
7. Veri varlıkları karşıya yüklendikten sonra, Eylem Bölmesinde **İçe aktar**'ı seçin.
8. **Vergi** > **Sorgular ve raporlar** > **Elektronik iletiler** > **Elektronik iletiler**'e gidin ve içe aktardığınız elektronik ileti işlemeyi doğrulayın (**DK KDV beyannamesi**).

### <a name="configure-electronic-messages"></a>Elektronik iletileri konfigüre etme

1. **Vergi** > **Kurulum** > **Elektronik iletiler** > **Kayıtlar eylemlerini doldur**'a gidin.
2. **DK KDV beyannamesi kayıtlarını doldur** satırını seçin ve **Sorguyu düzenle**'yi seçin.
3. Rapora dahil edilecek kapatma dönemlerini belirtmek için filtreyi kullanın.
4. Farklı bir bildirimdeki vergi hareketlerini diğer kapatma dönemlerinden rapor etmeniz gerekiyorsa, yeni bir **Kayıt doldurma** eylemi oluşturun ve uygun kapatma dönemlerini seçin.

## <a name="preview-the-vat-declaration-in-excel"></a>KDV beyannamesini Excel'de önizleme

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a>Kapatma dönemi için satış vergilerini raporla dönemsel görevinden KDV beyannamesini Excel'de önizleme

1. **Vergi** >  **Dönemsel görevler** > **Beyannameler** > **Satış vergisi** > **Kapatma dönemi için satış vergisini raporla**'ya gidin.
2. **Kapatma dönemi** alanında bir değer seçin.
3. **Satış vergisi ödemesi sürümü** alanında aşağıdaki değerlerden birini seçin:

    - **Orijinal**: Orijinal satış vergisi ödemesine veya satış vergisi ödemesi oluşturulmadan önce satış vergisi hareketleri için bir rapor oluşturun.
    - **Düzeltmeler**: Döneme ait sonraki tüm satış vergisi ödemeleriyle ilgili satış vergisi hareketleri için bir rapor oluşturun.
    - **Toplam liste**: Döneme ait sonraki tüm satış vergisi ödemeleriyle ilgili, orijinal ve tüm düzeltmeler de dahil bir rapor oluşturun.

4. **Başlangıç tarihi** alanında, raporlama döneminin başlangıç tarihini seçin.
5. **Tamam**'ı seçin ve Excel raporunu gözden geçirin.

### <a name="settle-and-post-sales-tax"></a>Satış vergisini kapat ve deftere naklet

1. **Vergi** > **Dönemsel görevler** > **Beyannameler** > **Satış vergisi** > **Satış vergisini kapat ve deftere naklet**'e gidin.
2. **Kapatma dönemi** alanında bir değer seçin.
3. **Satış vergisi ödemesi sürümü** alanında aşağıdaki değerlerden birini seçin:

    - **Orijinal**: Kapatma dönemi için orijinal satış vergisi ödemesini oluşturun.
    - **En son düzeltmeler**: Kapatma dönemi için orijinal satış vergisi ödemesi oluşturulduktan sonra düzeltme satış vergisi ödemesi oluşturun.

4. **Başlangıç tarihi** alanında, raporlama döneminin başlangıç tarihini seçin.
5. **Tamam**'ı seçin.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Bir satış vergisi ödemesiyle Excel'de KDV Beyannamesini önizleme

1. **Vergi** > **Sorgular ve raporlar** > **Satış vergisi sorguları** > **Satış vergisi ödemeleri**'ne gidin ve bir satış vergisi ödeme satırı seçin.
2. **Raporu yazdır**'ı seçin ve **Tamam** öğesini belirleyin.
3. Seçili satış vergisi ödeme satırı için oluşturulan Excel dosyasını gözden geçirin.

> [!NOTE]
> Rapor, yalnızca satış vergisi ödemesinin seçili satırı için oluşturulur. Örneğin, dönem için tüm düzeltmeleri içeren bir düzeltme bildirimi veya orijinal verileri ve tüm düzeltmeleri içeren bir değiştirme bildirimi oluşturmak istiyorsanız, **Kapatma dönemi için satış vergisini bildir** dönemsel görevini kullanın.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Elektronik iletilerden KDV beyannamesi oluşturma

Raporu oluşturmak için elektronik iletiler kullandığınızda, birden çok yasal varlıklardan vergi verileri toplayabilirsiniz. Daha fazla bilgi için, bu makalenin ilerleyen kısımlarında yer alan [Birden fazla tüzel kişilik için KDV beyannamesi çalıştırma](#run-vat-declaration) bölümüne bakın.

Aşağıdaki yordam, daha önce LCS Paylaşılan varlık kitaplığından içe aktardığınız elektronik ileti işleme örneği için geçerlidir.

1. **Vergi \> Sorgular ve raporlar \> Elektronik iletiler \> Elektronik iletiler**'e gidin.
2. Sol bölmede **DK KDV beyannamesi**'ni seçin.
3. **İletiler** hızlı sekmesinde, **Yeni**'yi seçin ve sonra **İşlemeyi çalıştır** iletişim kutusunda **Tamam**'ı seçin.
4. Oluşturulan ileti satırını seçin, bir açıklama girin ve sonra beyannamenin başlangıç ve bitiş tarihlerini belirtin.

   > [!NOTE]
   > 5 ile 7 arasındaki adımlar isteğe bağlıdır.

5. İsteğe bağlı: **İletiler** hızlı sekmesinde, **Veri topla**'yı seçin ve **Tamam**'ı seçin. Daha önce oluşturulan satış vergisi ödemeleri iletiye eklenir. Daha fazla bilgi için bu makalenin önceki kısımlarında yer alan [Satış vergisini kapatma ve deftere nakletme](#settle-and-post-sales-tax) bölümüne bakın. Bu adımı atlarsanız, **Beyanname** iletişim kutusundaki **Vergi beyanı sürümü** alanını kullanarak yine de bir KDV beyannamesi oluşturabilirsiniz.
6. İsteğe bağlı: **İleti maddeleri** hızlı sekmesinde, işlenmek üzere aktarılan satış vergisi ödemelerini gözden geçirin. Varsayılan olarak, aynı işleme ait başka bir iletiye dahil edilmemiş olan seçili döneme ait tüm satış vergisi ödemeleri dahil edilir.
7. İsteğe bağlı: Satış vergisi ödemelerini incelemek için **Orijinal belge**'yi seçin veya işlemeden satış vergisi ödemelerini hariç tutmak için **Sil**'i seçin. Bu adımı atlarsanız, **Beyanname** iletişim kutusundaki **Vergi beyanı sürümü** alanını kullanarak yine de bir KDV beyannamesi oluşturabilirsiniz.
8. **İletiler** hızlı sekmesinde, **Durumu güncelleştir**'i seçin. **Güncelleştirme durumu** iletişim kutusunda, **Oluşturmak için hazırla**'yı seçin ve **Tamam**'ı seçin. İleti durumunun, **Üretmeye hazır** olarak değiştiğini doğrulayın.
9. **Rapor oluştur** seçeneğini belirleyin. KDV beyannamesi tutarlarının önizlemesini yapmak için, **İşlemeyi çalıştır** iletişim kutusunda **Rapor önizleme**'yi seçin ve **Tamam**'ı seçin.
10. **Elektronik raporlama parametreleri** iletişim kutusunda, alanları bu makalenin önceki kısımlarında yer alan [Kapatma dönemi için satış vergilerini raporla dönemsel görevinden KDV beyannamesini Excel'de önizleme](#preview-vat-excel) bölümünde açıklanan şekilde ayarlayın ve ardından **Tamam**'ı seçin.
11. Sayfanın sağ üst köşesindeki **Ekler** düğmesini seçin ve ardından dosyayı açmak için **Aç**'ı seçin. Tutarları Excel belgesinde inceleyin.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a>Birden fazla tüzel kişilik için KDV beyannamesi çalıştırma

Geçerli bir varlık grubu için KDV beyanını raporlamak amacıyla biçimleri kullanmak için, önce tüm gerekli tüzel kişilikler için satış vergisi kodlarının ER biçimlerinin uygulamaya özgü parametrelerini ayarlamanız gerekir.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Birkaç yasal varlığın vergi verilerini toplamak üzere elektronik iletiler ayarlama

Birden çok yasal varlıklardan veri toplayan elektronik iletileri ayarlamak için aşağıdaki adımları izleyin.

1. **Çalışma alanları** > **Özellik yönetimi**'ne gidin.
2. Listedeki, **Kayıtları doldur eylemleri için şirket arası sorgular** özelliğini bulup seçin ve sonra **Şimdi etkinleştir**'i seçin.
3. **Vergi** > **Kurulum** > **Elektronik iletiler** > **Kayıtlar eylemlerini doldur**'a gidin.
4. **Kayıtları doldur eylemi** sayfasında **DK KDV iade kayıtlarını doldur** satırını seçin.

   **Veri kaynakları kurulumu** kılavuzunda yeni bir **Şirket** alanı kullanılabilir. Varolan kayıtlar için bu alan, geçerli yasal varlığın tanımlayıcısını gösterir.

5. **Veri kaynakları kurulumu** kılavuzunda, raporlamaya dahil edilmesi gereken her ek yasal varlık için bir satır ekleyin. Her yeni satırda, aşağıdaki alanları ayarlayın.

    | Alan                  | Tanım                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Ad                   | Bu kaydın nereden geldiğini anlamanıza yardımcı olacak bir değer girin. Örneğin, **Alt Şirket 1'in KDV ödemesi** girin. |
    | İleti maddesi türü      | **KDV dönüşünü** seçin. Bu değer, tüm kayıtlar için kullanılabilir tek değerdir.                                    |
    | Hesap türü           | **Tümü**'nü seçin.                                                                                                               |
    | Ana tablo adı      | Tüm kayıtlar için **TaxReportVoucher** belirleyin.                                                                             |
    | Belge numarası alanı  | Tüm kayıtlar için **Fiş** belirleyin.                                                                                      |
    | Belge tarihi alanı    | Tüm kayıtlar için **TransDate** belirleyin.                                                                                    |
    | Belge hesabı alanı | Tüm kayıtlar için **TaxPeriod** belirleyin.                                                                                    |
    | Şirket                | Yasal varlığın kimliğini seçin.                                                                                            |
    | Kullanıcı sorgusu             | Bu onay kutusu, **Sorguyu düzenle**'yi seçerek ölçüt tanımladığınızda otomatik olarak seçilir.                                 |

6. Her yeni satır için **Sorguyu düzenle**'yi seçin ve satırdaki **Şirket** alanında belirtilen tüzel kişilik için bir kapatma dönemi belirtin.

Kurulum tamamlandığında, **Elektronik iletiler** sayfasındaki **Veri topla** işlevi, tanımladığınız tüm yasal varlıklardan gelen satış vergisi ödemelerini toplar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
