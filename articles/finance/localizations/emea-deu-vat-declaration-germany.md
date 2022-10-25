---
title: KDV Beyannamesi (Almanya)
description: Bu makalede, resmi XML biçiminde Almanya'ya ilişkin ön katma değer vergisi (KDV) bildiriminin nasıl ayarlanacağı ve oluşturulacağı açıklanmaktadır.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 04c625b554d96f8ed28ceffef9647fe9cbf7fe2f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689473"
---
# <a name="vat-declaration-germany"></a>KDV Beyannamesi (Almanya)

[!include [banner](../includes/banner.md)]

Bu makalede, resmi XML biçiminde Almanya'ya ilişkin ön katma değer vergisi (KDV) bildiriminin nasıl ayarlanacağı ve oluşturulacağı açıklanmaktadır. Bu makalede, KDV beyannamesinin Microsoft Excel'de nasıl önizlenebileceğini de açıklanmaktadır.

Raporu otomatik olarak oluşturmak için, ön KDV beyannamesindeki her kutu için ayrı bir KDV hesabı tutacak yeterli satış vergisi kodu oluşturun. Ek olarak, ön KDV beyannamesi için Elektronik raporlama (ER) biçiminin uygulamaya özel parametrelerinde, satış vergisi kodlarını, KDV beyannamesindeki kutuların aramalarının arama sonucuyla ilişkilendirin.

Almanya için **Rapor alanı aramasını** konfigüre etmelisiniz. Uygulamaya özel parametrelerin nasıl ayarlanacağı hakkında daha fazla bilgi için, bu makalenin ilerleyen kısımlarındaki [KDV beyannamesi alanları için uygulamaya özel parametreler ayarlama](#set-up-application-specific-parameters-for-vat-declaration-fields) bölümüne bakın.

Aşağıdaki tabloda, "Arama sonucu" sütunu, KDV beyanname biçimindeki belirli bir KDV Beyanname satırı için önceden konfigüre edilmiş arama sonucunu gösterir. Satış vergisi kodlarını arama sonucu ve daha sonra KDV beyannamesi satırı ile ilişkilendirmek için bu bilgileri kullanın.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a>KDV beyannamesine genel bakış

Almanya'daki ön KDV beyannamesi aşağıdaki bilgileri içerir.

**BÖLÜM – TESLİMATLAR VE DİĞER HİZMETLER**

**Vergiye tabi satış**

| Satır | Kutu – vergi tabanı | Kutu – vergi tutarı | Tanım                                                                                                                                      | Arama sonucu                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Kod olmadan     | %19 vergi oranında vergiye tabi satışlar.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – eksi işaretli             |
| 21  | 86             | Kod olmadan     | %7 vergi oranında vergiye tabi satışlar.                                                                                                        | 21-TaxableSalesReduced</br>73-BadDebtsWriteOffReduced (86/50) – eksi işaretli               |
| 22  | 35             | 36               | Diğer vergi oranlarındaki vergiye tabi satışlar.                                                                                                                | 22-TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – eksi işaretli      |
| 23  | 77             | *Vergi tutarı yok*  | KDV kimlik numarası olan müşterilere, Alman KDV Yasası §24'e göre (UStG), tarım ve ormancılık şirketleri tarafından yapılan teslimatlar. | 23-EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – eksi işaretli |
| 24  | 76             | 80               | UStG'nin §24'üne göre (değirmen ürünleri, meşrubat ve alkollü içecekler) vergi ödenmesi gereken satışlar.                                | 24-SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Girdi vergisi kesintisiyle vergiden muaf satışlar**

| Satır | Kutu – vergi tabanı | Kutu – vergi tutarı | Tanım                                                                       | Arama sonucu                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Vergi tutarı yok*  | KDV koduna sahip müşterilere topluluk içi teslimatlar.                       | 26-EUSales                          |
| 27  | 44             | *Vergi tutarı yok*  | Bir KDV koduna sahip olmayan alıcılara, yeni taşıtlar için topluluk içi teslimatlar.    | 27-EUSalesNewVehicles               |
| 28  | 49             | *Vergi tutarı yok*  | Şirket dışındaki yeni taşıtların topluluk içi teslimatları.                     | 28-EUSalesNewVehiclesOutsideCompany |
| 29  | 43             | *Vergi tutarı yok*  | İhracat teslimatları gibi giriş vergisi kesintisi olan diğer vergiden muaf satışlar. | 29-ExportOtherTaxFreeSales          |

**Girdi vergisi kesintisi olmadan vergiden muaf satışlar**

| Satır | Kutu – vergi tabanı | Kutu – vergi tutarı | Tanım                                            | Arama sonucu                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Vergi tutarı yok*  | Giriş vergi kesintisi olmayan vergiden muaf satışlar. | 30-TaxFreeSalesWithoutInputTaxDeduction |

**Topluluk içi alımlar**

| Satır | Kutu – vergi tabanı | Kutu – vergi tutarı | Tanım                                                                                                                   | Arama sonucu                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Vergi tutarı yok*  | Bazı nesnelerin ve yatırım altının vergiden topluluk içi alımı.                                                    | 33-TaxFreeEUPurchase                                             |
| 34  | 89             | Kod olmadan     | %19 vergi oranında topluluk içi alımlar.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Kod olmadan     | %7 vergi oranında topluluk içi alımlar.                                                              | 35-EUPurchaseReduced</br>35-UseTaxEUPurchaseReduced (93/61)          |
| 36  | 95             | 98               | Diğer vergi oranlarında topluluk içi alımlar.                                                                      | 36-EUPurchaseOtherRates</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Genel vergi oranında KDV kodu bulunmayan tedarikçilere ait yeni taşıtlar için vergiye tabi topluluk içi alımlar. | 37-EUPurchaseVehicles</br>37-UseTaxEUPurchaseVehicles (94/96/61)     |

**BÖLÜM – VERGİ BORÇLUSU OLARAK LEHTAR**

| Satır | Kutu – vergi tabanı | Kutu – vergi tutarı | Tanım                                                                        | Arama sonucu                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Topluluk alanının geri kalanı temel alınarak, bir girişimcinin diğer hizmetleri.        | 40-BeneficiaryTaxDebtor</br>40-UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Bölüm 13b (2) no. altında kalan satışlar. UStG'nin 3 numarası.                               | 41-BeneficiaryTaxDebtorRealEstateTransfer</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Bölüm 13b (2) no. altında kalan diğer hizmetler. UStG'nin 1, 2 ve 4 ile 12 arası numaraları. | 42-BeneficiaryTaxDebtorOther</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**BÖLÜM – SATIŞLARLA İLGİLİ EK BİLGİLER**

| Satır | Kutu – vergi tabanı  | Kutu – vergi tutarı | Tanım                                                                                                | Arama sonucu                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Vergi tutarı yok*  | Topluluk içi üç taraflı hareket durumunda ilk müşteriye ait teslimatlar.                   | 48-DeliveriesFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Vergi tutarı yok*  | Hizmet alıcısının vergi ile ilgili olarak ödemesi gereken, aktör girişimcinin vergiye tabi satışları. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Vergi tutarı yok*  | Diğer vergiye tabi olmayan hizmetler.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Vergi tutarı yok*  | Performans yerinin Almanya olmadığı, vergiye tabi olmayan diğer satışlar.                                    | 51-OtherSalesNonTaxable                                                                          |
| 52  | *Vergi tutarı yok* | *Vergi tutarı yok*  | KDV.                                                                                                       | Satır 20 + Satır 21 + Satır 22 + Satır2 4 + Satır 34 + Satır 35 + Satır 36 + Satır 37 + Satır 40 + Satır 41 + Satır 42 |

**BÖLÜM – İNDİRİLEBİLECEK GİRİŞ VERGİSİ**

| Satır | Kutu – vergi tutarı | Tanım                                                                                                | Arama sonucu                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Diğer şirketlerden, hizmetlerden ve topluluk içi üç taraflı hareketlerden gelen fatura vergisi tutarlarını girin.     | 55-InputTax 40-UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – eksi işaretli                                                                   |
| 56  | 61               | Topluluk içi mal alımlarından kaynaklanan girdi vergisi tutarları.                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35-UseTaxEUPurchaseReduced (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37-UseTaxEUPurchaseVehicles (94/96/61) |
| 57  | 62               | Tahakkuk eden ithalat satış vergisi.                                                                                 | 57-InputTaxImport                                                                                                                                                            |
| 58  | 67               | UStG §13b'nin anlamı kapsamında hizmetlerden gelen giriş vergisi tutarları.                                        | 58-InputTaxServices</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Genel ortalama oranlar doğrultusunda hesaplanan giriş vergisi tutarları.                                  | 59-InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – eksi işaretli                                                                                    |
| 60  | 59               | Şirket ve küçük işletmeler dışında, yeni taşıtların topluluk içi teslimatları için giriş vergisi kesintisi. | 60-InputTaxEUPurchaseNewVehicles</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37) – eksi işaretli                                                                  |
| 61  | 64               | Giriş vergi kesintisi düzeltmesi.                                                                     | 61-InputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Kalan tutar.                                                                                      | Satır 52 – Satır 55 – Satır 56 – Satır 57 – Satır 58 – Satır 50 – Satır 60 – Satır 61                                                                                                        |

**BÖLÜM – DİĞER VERGİ TUTARLARI**

| Satır | Kutu – vergi tutarı | Tanım                                                                                                                                                                                                                                                         | Arama sonucu                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Vergilendirme formunda değişiklik nedeniyle vergi ve vergi oranındaki değişim nedeniyle vergilendirilen peşinat üzerindeki ilave vergi.                                                                                                                                        | 64-AdditionalTaxDueChangeTaxRate              |
| 65  | 69               | Fatura üzerinde gösterilen yanlış veya bloklanmamış vergi tutarları ve UStG bölüm 6a (4) cümle 2, Bölüm 17 (1) cümle 7 veya bölüm 25b (2) bölüm ile ilgili olarak ya da bir dış kaynak ya da ambar sahibi tarafından en uygun şekilde ödenmesi gereken vergi tutarları. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Kalıcı uzantı için sabit özel avans ödemesinin kesintisi. Bu satır, tipik olarak yalnızca vergi döneminin son öncelikli bildirimi ile doldurulur.                                                                                                  | Rapor iletişim kutusunda kullanıcı giriş parametresi |
| 68  | 83               | Geriye kalan ön satış vergisi ödemesi ve kalan fazlalık. Tutarın önüne eksi işareti ekleyin.                                                                                                                                                          | Satır 62 + Satır 64 – Satır 65 – Satır 66             |

**BÖLÜM – AZALTMALARLA İLGİLİ EK BİLGİLER**

| Satır | Kutu – vergi tabanı | Kutu – vergi tutarı | Tanım                                                            | Arama sonucu                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | 20 ile 24 arasındaki satırların vergi tabanındaki azalması.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffReduced (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | 55, 59 ve 60 numaralı satırlardaki kesinti yapılabilen giriş vergisi tutarlarının azaltılması. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Satın alma karşı ödeme KDV'si

Satış vergisi kodlarını, kullanım vergisi kullanarak gelen karşı ödeme KDV'sini deftere nakletmek üzere konfigüre ederseniz, satış vergisi kodlarınızı, adda "UseTax" içeren **Rapor alanı aramasının** arama sonucu ile ilişkilendirin.

Alternatif olarak, iki ayrı satış vergisi kodu konfigüre edebilirsiniz: ödenmesi gereken KDV için bir adet ve KDV kesintisi için bir adet. Sonra her kodu **Rapor alanı aramasının** ilgili arama sonuçlarıyla ilişkilendirin.

Örneğin, standart bir fiyata ait vergiye tabi topluluk içi alımları için, kullanım vergisiyle **UT_S_EU** satış vergisi kodunu konfigüre edin ve bunu **Rapor alanı aramasının** **34-UseTaxEUPurchaseStandard** arama sonucu ile ilişkilendirin. Bu durumda, **UT_S_EU** satış vergisi kodunu kullanan tutarlar 089 ve 061 (satır 34 ve 56) kutularına yansıtılır.

Alternatif olarak, iki satış vergisi kodu konfigüre edebilirsiniz:

  - Vergi oranı değeri yüzde -19 olan **VAT_S_EU**
  - Vergi oranı değeri yüzde 19 olan **InVAT_S_EU**

Sonra kodları **Rapor alanı aramasının** arama sonuçlarıyla aşağıdaki şekilde ilişkilendirin:

  - **VAT_S_EU** öğesini, **34-EUPurchaseStandard** arama sonucu ile ilişkilendirin.
  - **InVAT_S_EU** öğesini, **56-InputTaxEUPurchase** arama sonucu ile ilişkilendirin.

Bu durumda, **VAT_S_EU** satış vergisi kodu 089 (satır 34) kutusuna yansıtılır. **InVAT_S_EU** satış vergisi kodu 061 (satır 56) kutusuna yansıtılır.

Ters kaydedilecek KDV yapılandırma hakkında daha fazla bilgi için bkz. [Ters masraflar](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Sistem parametrelerini yapılandırma

Bir KDV beyannamesi oluşturmak için, organizasyonunuzun vergi numarasını (Steuernummer) konfigüre etmelisiniz.

1. **Kuruluş yönetimi** > **Kuruluşlar** > **Tüzel kişilikler**'e gidin.
2. Tüzel kişiliği ve ardından **Kayıt kimlikleri**'ni seçin.
3. Almanya'da adres seçin veya oluşturun, sonra da **Kayıt kodu** hızlı sekmesinde, **Ekle**'yi seçin.
4. **Kayıt türü** alanında, Almanya'ya adanmış ve **Kuruluş kodu (COID)** kayıt kategorisini kullanan kayıt türünü seçin.
5. **Kayıt numarası** alanına vergi numarasını girin.
6. **Genel** sekmesinde, **Etkin** alanına numaranın geçerli olacağı tarihi girin.

Kayıt kategorilerinin ve kayıt tiplerinin nasıl ayarlanacağı hakkında daha fazla bilgi için bkz. [Kayıt Kimlikleri](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-for-germany"></a>Almanya için KDV beyannamesi ayarlama

### <a name="import-er-configurations"></a>ER yapılandırmaları içe aktarın

**Elektronik raporlama** çalışma alanını açın ve aşağıdaki sürümleri ya da bu ER biçimlerini içe aktarın:

   - KDV Beyannamesi Excel (DE).sürüm.101.16.12.xml
   - KDV Beyannamesi XML (DE).sürüm.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a>KDV beyanname alanları için uygulamaya özel parametreleri ayarlama

Otomatik olarak bir KDV beyannamesi oluşturmak için uygulama ve arama sonuçlarında satış vergisi kodlarını, ER konfigürasyonuyla ilişkilendirin.

> [!NOTE]
> **Özellik yönetimi** çalışma alanındaki **Önceki ER biçimleri sürümünden uygulamaya özel parametreleri kullan** özelliğini etkinleştirmenizi öneririz. Bu özellik etkinleştirildiğinde, bir ER biçiminin önceki sürümü için yapılandırılmış parametreler, aynı biçimin sonraki sürümü için otomatik olarak uygulanabilir duruma gelir. Bu özellik etkinleştirilmemişse, uygulamaya özel parametreleri her biçim sürümü için açık olarak konfigüre etmelisiniz. **Özellik yönetimi** çalışma alanındaki **Önceki ER biçimleri sürümünden uygulamaya özel parametreleri kullan** özelliği, Finans sürüm 10.0.23'ten itibaren kullanılabilir. Her yasal varlık için bir ER biçimi parametrelerinin nasıl ayarlanacağı hakkında daha fazla bilgi için, bkz. [Yasal varlık başına ER biçimi parametrelerini ayarlama](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

KDV beyannamesindeki kutuları hangi satış vergisi kodlarının oluşturacağını tanımlamak için bu adımları izleyin.

1. **Çalışma alanları** > **Elektronik raporlama**'ya gidin ve **Raporlama yapılandırmaları**'nı seçin.
2. **KDV beyanname XML (DE)** yapılandırmasını seçin ve sonra **Konfigürasyonlar \> Uygulamaya özgü parametreler kurulumunu** seçin.
3. **Uygulamaya özel parametreler** sayfasında, **Aramalar** hızlı sekmesinde, **Rapor alanı araması**'nı seçin.
4. **Koşullar** hızlı sekmesinde, satış vergisi kodları ve rapor alanlarını ilişkilendirmek için aşağıdaki alanları ayarlayın.

    | Alan                  | Tanım                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Arama sonucu          | Rapor alanının değerini seçin. Değerler ve bunların KDV beyanname satırlarına atanması hakkında daha fazla bilgi için, bu makalenin önceki kısımlarında yer alan [KDV beyannamesine genel bakış](#vat-declaration-overview) bölümüne bakın.                                                                                               |
    | Vergi kodu.               | Rapor alanıyla ilişkilendirilecek satış vergisi kodunu seçin. Seçili satış vergisi kodunu kullanan deftere nakledilen vergi hareketleri ilgili bildirim kutusunda toplanır. Satış vergisi kodlarını, tek bir bildirim kutusunda tutarlar oluşturacak şekilde ayırmanızı öneririz. |
    | Hareket sınıflandırıcı | Bir bildirim kutusunu belirlemek için yeterli satış vergisi kodu oluşturduysanız, **\*Boş değil\*** seçeneğini belirleyin. Bir satış vergisi kodunun yalnızca bir bildirim kutusunda tutarlar oluşturması için yeterli satış vergisi kodu oluşturmadıysanız, bir hareket sınıflandırıcısı ayarlayabilirsiniz. Aşağıdaki hareket sınıflandırıcıları kullanılabilir:</br>-   **Satınalma**</br>-   **PurchaseExempt** (vergiden muaf satın alma)</br>-   **PurchaseReverseCharge** (bir satın alma ters masrafından elde edilen vergi alacağı)</br>-   **Satışlar**</br>-   **SalesExempt** (vergiden muaf satış)</br>-   **SalesReverseCharge** (bir satın alma ters masrafı veya satış ters masrafına ait vergi borcu)</br>-   **Kullanım vergisini kullanır**. </br>Her bir hareket sınıflandırıcısı için, alacak dekontuyla ilgili bir sınıflandırıcı da mevcuttur. Örneğin, bu sınıflandırıcılardan biri **PurchaseCreditNote**'tır (satın alma alacak dekontu).</br>Her satış vergisi kodu için iki satır oluşturmayı unutmayın: hareket sınıflandırıcı değerine sahip olan bir tane ve alacak dekontu değeri için hareket sınıflandırıcılarına sahip olan bir tane. |

    > [!NOTE]
    > Tüm satış vergisi kodlarını arama sonuçlarıyla ilişkilendirin. Herhangi bir satış vergisi kodunun KDV beyannamesinde değer üretmeleri gerekiyorsa, bunları **Diğer** arama sonucuyla ilişkilendirin.

    ![Uygulamaya özgü parametreler sayfası](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. **Durum** alanında, değeri **Tamamlandı** olarak değiştirin.
6. Eylem Bölmesinde, uygulamaya özgü parametrelerin ayarlarını dışa aktarmak için **Dışa aktar**'ı seçin.
7. **KDV beyannamesi Excel (DE)** konfigürasyonunu seçin ve sonra Eylem Bölmesinde **KDV beyannamesi XML'si (DE)** için konfigüre ettiğiniz parametreleri içe aktarmak için **İçe aktar**'ı seçin.
8. **Durum** alanında **Tamamlandı**'yı seçin.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Excel'de önizleme tutarları için KDV raporlama biçimini ayarlama

1. **Özellik yönetimi** çalışma alanında, **KDV beyannamesi biçim raporları** özelliğini bulup etkinleştirin.
2. **Genel muhasebe** > **Kurulum** > **Genel muhasebe parametreleri**'ne gidin.
3. **Satış vergisi** sekmesinde, **Vergi seçenekleri** hızlı sekmesinde, **KDV beyannamesi biçim eşlemesi** alanında, **KDV beyannamesi Excel'i (DE)** seçeneğini belirleyin.

   Bu biçim, **Kapatma dönemi raporu için satış vergisini bildir** raporunu çalıştırdığınızda yazdırılır. Ayrıca, **Satış vergisi ödemeleri** sayfasında **Yazdır**'ı seçtiğinizde de yazdırılır.

4. Düzeltmeleri raporlamanız gerekirse **Özel rapor** bölümünde **Düzeltmeleri dahil et** seçeneğini **Evet** olarak ayarlayın.
5. **Vergi daireleri** sayfasında vergi dairesini seçin ve **Rapor düzeni** alanında **Varsayılan** seçeneğini belirleyin.

KDV beyanını, [birden çok KDV kaydına](emea-reporting-for-multiple-vat-registrations.md) sahip olan bir tüzel kişilikte konfigüre ediyorsanız, aşağıdaki adımları izleyin:

1. **Genel muhasebe** > **Kurulum** > **Genel muhasebe parametreleri**'ne gidin.
2. **Satış vergisi** sekmesinde, **Ülkeler/bölgeler için elektronik raporlama** hızlı sekmesinde, **DEU** için olan satırda, **KDV beyannamesi Excel'i (de)** ER biçimini seçin.

## <a name="set-up-electronic-messages"></a>Elektronik iletileri ayarlama

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Elektronik iletiler için örnek ayarlara sahip veri paketini karşıdan yükleyin ve içe aktarın

Veri paketi, KDV beyanını XML biçiminde oluşturmak ve daha sonra Excel'de önizlemek için kullanılan elektronik ileti ayarları içerir. Bu ayarları genişletebilir veya kendi kendinize oluşturabilirsiniz. Elektronik mesajlarla nasıl çalışılacağı ve kendi ayarlarınızı nasıl oluşturacağınız hakkında daha fazla bilgi için, bkz. [Elektronik mesajlaşma](../general-ledger/electronic-messaging.md).

1. [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2) içinde, Paylaşılan varlık kitaplığında, varlık türü olarak **Veri paketi**'ni seçin ve **DE KDV beyannamesi EM paketini** indirin. İndirilen dosya adı **EM paketinde DE KDV beyanname.zip**'dir.
2. Dynamics 365 Finance'te, **Veri yönetimi** çalışma alanında **İçeri aktar**'ı seçin.
3. **İçe aktar** hızlı sekmesinde, **Grup adı** alanına iş için bir ad girin.
4. **Seçili varlıklar** hızlı sekmesinde **Dosya ekle**'yi seçin.
5. **Dosya ekle** iletişim kutusunda, **Kaynak veri biçimi** alanının **Paket** olarak ayarlandığını doğrulayın, **Yükle ve ekle**'yi seçin ve daha önce yüklediğiniz ZIP dosyasını seçin.
6. **Kapat**'ı seçin.
7. Veri varlıkları karşıya yüklendikten sonra, Eylem Bölmesinde **İçe aktar**'ı seçin.
8. **Vergi** > **Sorgular ve raporlar** > **elektronik İletiler** > **Elektronik iletiler**'e gidin ve içe aktardığınız elektronik ileti işlemeyi doğrulayın.

### <a name="configure-electronic-messages"></a>Elektronik iletileri konfigüre etme

1. **Vergi** > **Kurulum** > **Elektronik iletiler** > **Kayıtlar eylemlerini doldur**'a gidin.
2. **DE KDV beyannamesi kayıtlarını doldur** satırını seçin ve **Sorguyu düzenle**'yi seçin.
3. Rapora dahil edilecek kapatma dönemlerini belirtmek için filtreyi kullanın.
4. Farklı bir bildirimdeki vergi hareketlerini diğer kapatma dönemlerinden rapor etmeniz gerekiyorsa, yeni bir **Kayıt doldurma** eylemi oluşturun ve uygun kapatma dönemlerini seçin.

## <a name="preview-the-vat-declaration-in-excel"></a>KDV beyannamesini Excel'de önizleme

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Kapatma dönemi için satış vergilerini raporla dönemsel görevinden KDV beyannamesini Excel'de önizleme

1. **Vergi** >  **Dönemsel görevler** > **Beyannameler** > **Satış vergisi** > **Kapatma dönemi için satış vergisini raporla**'ya gidin.
2. **Kapatma dönemi** alanında bir değer seçin.
3. **Satış vergisi ödemesi sürümü** alanında aşağıdaki değerlerden birini seçin:

    - **Orijinal**: Orijinal satış vergisi ödemesine veya satış vergisi ödemesi oluşturulmadan önce satış vergisi hareketleri için bir rapor oluşturun.
    - **Düzeltmeler**: Döneme ait sonraki tüm satış vergisi ödemeleriyle ilgili satış vergisi hareketleri için bir rapor oluşturun.
    - **Toplam liste**: Döneme ait sonraki tüm satış vergisi ödemeleriyle ilgili, orijinal ve tüm düzeltmeler de dahil bir rapor oluşturun.

4. **Başlangıç tarihi** alanında, raporlama döneminin başlangıç tarihini seçin.
5. **Tamam**'ı seçin ve Excel raporunu gözden geçirin.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Satış vergisini kapat ve deftere naklet

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

Raporu oluşturmak için elektronik iletiler kullandığınızda, birden çok yasal varlıklardan vergi verileri toplayabilirsiniz. Daha fazla bilgi için, bu makalenin ilerleyen kısımlarında yer alan [Birden fazla tüzel kişilik için KDV beyannamesi çalıştırma](#run-a-vat-declaration-for-multiple-legal-entities) bölümüne bakın.

Aşağıdaki yordam, LCS Paylaşılan varlık kitaplığından içe aktardığınız elektronik ileti işleme örneği için geçerlidir.

1. **Vergi** > **Sorgular ve raporlar** > **Elektronik iletiler** > **Elektronik iletiler**'e gidin.
2. Sol bölmede **DE KDV beyannamesi**'ni seçin.
3. **İletiler** hızlı sekmesinde, **Yeni**'yi seçin ve sonra **İşlemeyi çalıştır** iletişim kutusunda **Tamam**'ı seçin.
4. Oluşturulan ileti satırını seçin, bir açıklama girin ve sonra beyannamenin başlangıç ve bitiş tarihlerini belirtin.

    > [!NOTE]
    > 5 ile 7 arasındaki adımlar isteğe bağlıdır.

5. İsteğe bağlı: **İletiler** hızlı sekmesinde, **Veri topla**'yı seçin ve **Tamam**'ı seçin. Daha önce oluşturulan satış vergisi ödemeleri iletiye eklenir. Daha fazla bilgi için bu makalenin önceki kısımlarında yer alan [Satış vergisini kapatma ve deftere nakletme](#settle-and-post-sales-tax) bölümüne bakın. Bu adımı atlarsanız, **Beyanname** iletişim kutusundaki **Vergi beyanı sürümü** alanını kullanarak yine de bir KDV beyannamesi oluşturabilirsiniz.
6. İsteğe bağlı: **İleti maddeleri** hızlı sekmesinde, işlenmek üzere aktarılan satış vergisi ödemelerini gözden geçirin. Varsayılan olarak, aynı işleme ait başka bir iletiye dahil edilmemiş olan seçili döneme ait tüm satış vergisi ödemeleri dahil edilir.
7. İsteğe bağlı: Satış vergisi ödemelerini incelemek için **Orijinal belge**'yi seçin veya işlemeden satış vergisi ödemelerini hariç tutmak için **Sil**'i seçin. Bu adımı atlarsanız, **Beyanname** iletişim kutusundaki **Vergi beyanı sürümü** alanını kullanarak yine de bir KDV beyannamesi oluşturabilirsiniz.
8. **İletiler** hızlı sekmesinde, **Durumu güncelleştir**'i seçin. **Güncelleştirme durumu** iletişim kutusunda, **Oluşturmak için hazırla**'yı seçin ve **Tamam**'ı seçin. İleti durumunun, **Üretmeye hazır** olarak değiştiğini doğrulayın.
9. **Rapor oluştur** seçeneğini belirleyin. KDV beyannamesi tutarlarının önizlemesini yapmak için, **İşlemeyi çalıştır** iletişim kutusunda **Rapor önizleme**'yi seçin ve **Tamam**'ı seçin.
10. **Elektronik raporlama parametreleri** iletişim kutusunda aşağıdaki alanları ayarlayın ve **Tamam**'ı seçin.

    | **Alan**                                   | **Tanım**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Kapatma dönemi                           | Kapatma dönemini seçin. Adım 5'te **Veri toplama**'yı seçtiyseniz, bu alanı boş bırakabilirsiniz. Rapor, toplanan satış vergisi ödemelerine dahil edilen satış vergisi hareketleri için oluşturulur. |
    | Vergi beyannamesi sürümü                     | Aşağıdaki değerlerden birini seçin:</br>-   **Orijinal** - Orijinal satış vergisi ödemesine veya satış vergisi ödemesi oluşturulmadan önce satış vergisi hareketleri için bir rapor oluşturun.</br>-   **Düzeltmeler** - Döneme ait sonraki tüm satış vergisi ödemeleriyle ilgili satış vergisi hareketleri için bir rapor oluşturun.</br>-   **Toplam liste** - Döneme ait sonraki tüm satış vergisi ödemeleriyle ilgili, orijinal ve tüm düzeltmeler de dahil bir rapor oluşturun.|
    | Vergi temsilcisi | Varsa, KDV beyannamesi için bir vergi temsilcisi olan tarafı seçin. Seçilen taraf hakkındaki bilgiler **DatenLieferant** XML öğesine dışa aktarılır. |
    | İlgili kişi | Kuruluşta veri sağlayıcı olan bir kişi seçin. Seçilen kişi hakkındaki bilgiler **DatenLieferant** XML öğesine dışa aktarılır. |
    | Düzeltme amaçlı iade | Bu düzeltici KDV beyanname ise **Evet**'i seçin. Bu durumda, XML öğesinin KZ10 değeri **1** olacaktır.|
    | Destekleyen belgeler | Destek belgeleri de gönderiyorsanız, **Evet**'i seçin. Bu durumda, XML öğesinin KZ22 değeri **1** olacaktır.|
    | SEPA talimatlı ödeme talimatı özel durum olarak iptal edilecektir| Bu ön kayıt dönemi için SEPA doğrudan ödeme talimat özel durumu olarak iptal edilecekse **Evet**'i seçin. Örneğin, mahsup istekleri nedeniyle. Kalan tüm bakiyeleri ayrı olarak ödemelidir. Bu durumda, XML öğesinin KZ26 değeri **1** olacaktır. |
    | İstenilen geri ödeme tutarının mahsuplaştırması | Geri ödeme tutarı mahsuplaştırması isteniyorsa veya geri ödeme tutarı atanmışsa **Evet**'i seçin. Bu durumda, XML öğesinin KZ29 değeri **1** olacaktır. |
    | Özel avans ödemesi kalıcı uzantısı | Kalıcı uzantı için sabit özel avans ödemesinin kesintisi tutarını girin. Bu kesinti tutarı genellikle, vergi döneminin son ön kaydında tamamlanır. Tutar, satır 67'de (kutu 39) ve KDV beyannamesinin XML öğesi KZ39'da dışa aktarılır. |

11. Sayfanın sağ üst köşesindeki **Ekler**'i seçin ve sonra **Aç**'ı seçin.
12. Excel belgesindeki tutarları gözden geçirin ve sonra **Rapor oluştur**'u seçin.
13. KDV beyannamesi tutarlarını XML biçiminde oluşturmak için, **İşlemeyi çalıştır** iletişim kutusunda **Rapor oluştur**'u seçin ve **Tamam**'ı seçin.
14. **Elektronik raporlama parametreleri** iletişim kutusunda, alanları adım 10'da açıklandığı şekilde ayarlayın.
15. Sayfanın sağ üst köşesindeki **Ekler**'i seçin, dosyayı karşıdan yükleyin ve vergi dairesine gönderirken kullanın.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a>Birden fazla tüzel kişilik için KDV beyannamesi çalıştırma

Geçerli bir varlık grubu için KDV beyanını raporlamak amacıyla biçimleri kullanmak için, önce tüm gerekli tüzel kişilikler için satış vergisi kodlarının ER biçimlerinin uygulamaya özgü parametrelerini ayarlamanız gerekir.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Birkaç yasal varlığın vergi verilerini toplamak üzere elektronik iletiler ayarlama

Birden çok yasal varlıklardan veri toplayan elektronik iletileri ayarlamak için aşağıdaki adımları izleyin.

1. **Çalışma alanları** > **Özellik yönetimi**'ne gidin.
2. Listedeki, **Kayıtları doldur eylemleri için şirket arası sorgular** özelliğini bulup seçin ve sonra **Şimdi etkinleştir**'i seçin.
3. **Vergi** > **Kurulum** > **Elektronik iletiler \> Kayıtlar eylemlerini doldur**'a gidin.
4. **Kayıtları doldur eylemi** sayfasında **DE KDV iade kayıtlarını doldur** satırını seçin.

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
