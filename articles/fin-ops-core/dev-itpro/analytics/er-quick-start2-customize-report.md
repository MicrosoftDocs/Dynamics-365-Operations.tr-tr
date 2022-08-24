---
title: Özel elektronik belge oluşturmak için ER biçimini ayarlama
description: Bu makalede, Microsoft tarafından sağlanan elektronik raporlama (ER) biçiminin özel elektronik belge oluşturması için nasıl ayarlanacağı açıklanmaktadır.
author: kfend
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314,  ""intro-internal
ms.assetid: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
ms.openlocfilehash: 8b0bcdbd011c4c04e2693a3dcb8033c3cbe2adc7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283573"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>Özel elektronik belge oluşturmak için ER biçimini ayarlama

[!include[banner](../includes/banner.md)]

Bu makaledeki yordamlarda, Sistem Yöneticisi veya Elektronik Raporlama İşlev Danışmanı rolündeki bir kullanıcının bu görevleri nasıl gerçekleştireceği açıklanmaktadır:

- [Elektronik raporlama (ER) altyapısını](general-electronic-reporting.md) parametrelerini yapılandırın.
- Microsoft tarafından sağlanan ve bir [satıcı ödemesi](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) işlenirken bir ödeme dosyası oluşturmak için kullanılan ER konfigürasyonlarını içe aktar.
- Microsoft tarafından sağlanan standart bir ER biçimi yapılandırmasının özel sürümünü oluşturun.
- Özel ER formatı konfigürasyonunu, belirli bir bankanın gereksinimlerine uyan ödeme dosyaları oluşturacak şekilde değiştirin.
- Özel ER biçimi konfigürasyonundaki standart ER biçimi konfigürasyonuna yapılan değişiklikleri benimseme.

Aşağıdaki yordamların tümü **GBSI** şirketinde yapılabilir. Kodlama gerekmez.

- [ER altyapısını yapılandırma](#ConfigureFramework)

    - [ER parametrelerini yapılandırma](#ConfigureParameters)
    - [ER yapılandırma sağlayıcısı etkinleştirin](#ActivateProvider)

        - [ER yapılandırma sağlayıcıları listesini gözden geçirin](#ReviewProvidersList)
        - [Yeni bir ER yapılandırması sağlayıcısı ekleme](#ActivateProvider)
        - [ER yapılandırma sağlayıcısı etkinleştirin](#ActivateAddedProvider)

- [Standart ER biçimi yapılandırmalarını içe aktarın](#ImportERSolution1)

    - [Standart ER yapılandırmalarını içe aktarın](#ImportERFormat1)
    - [İçe aktarılan ER yapılandırmalarını gözden geçirin](#ReviewImportedERSolution)

- [İşleme için satıcı ödemesini hazırlayın](#PrepareVendorPayment)

    - [Satıcı hesabı için banka bilgileri ekleme](#AddBankAccount)
    - [Satıcı ödemesini girin](#EnterVendorPayment)

- [Standart ER biçimini kullanarak bir satıcı ödemesini işleme](#ProcessVendorPayment1)

    - [Elektronik ödeme yöntemini ayarlama](#ConfigureMethodOfPayment1)
    - [Satıcı ödemesini işleme](#ProcessPayment1)

- [Standart ER biçimini Özelleştirme](#CustomizeProvidedFormat)

    - [Özel biçim oluşturma](#DeriveProvidedFormat)
    - [Özel biçim düzenleme](#ConfigureDerivedFormat)
    - [Özel biçimi çalıştırılabilir olarak işaretleme](#MarkFormatRunnable)

- [Özel ER biçimini kullanarak bir satıcı ödemesini işleme](#ProcessVendorPayment2)

    - [Elektronik ödeme yöntemini ayarlama](#ConfigureMethodOfPayment2)
    - [Satıcı ödemesini işleme](#ProcessPayment2)

- [Standart ER biçimi yapılandırmalarının yeni sürümlerini içe aktarın](#ImportERSolution2)

    - [Standart ER yapılandırmalarının yeni sürümlerini içe aktarın](#ImportERFormat2)
    - [İçe aktarılan ER biçimi yapılandırmalarını gözden geçirin](#ReviewImportedERFormat)

- [Özel bir biçimde, içe aktarılan bir biçimin yeni sürümündeki Değişiklikleri benimseme](#AdoptNewBaseVersion)

    - [Özel biçimin geçerli taslak sürümünü tamamlama](#CompleteDerivedFormat)
    - [Özel biçimi yeni bir temel sürüme yeniden temellendir](#RebaseDerivedFormat)
    - [Yeniden temellendirilen ER biçimini kullanarak bir satıcı ödemesini işleme](#ProcessPayment3)

- [Ek kaynaklar](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>ER altyapısını yapılandırma

Elektronik raporlama işlevi ile ilgili bir kullanıcı olarak, standart bir ER biçiminin özel bir sürümünü tasarlamak için ER çerçevesini kullanmaya başlamadan önce en düşük ER alt uygulama parametreleri kümesini konfigüre etmelisiniz.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ER parametrelerini yapılandırma

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Elektronik raporlama parametreleri** kutucuğunu seçin.
3. **Elektronik raporlama parametreler** sayfasında, **Genel** sekmesinde, **Tasarım modunu etkinleştir** seçeneğini **Evet** olarak ayarlayın.
4. **Ekler** sekmesinde, aşağıdaki parametreleri ayarlayın:

    - **Konfigürasyonlar** alanında, **USMF** şirketi için **dosya** türünü seçin.
    - **İş arşivi**, **Geçici**, **temel** ve **diğer** alanlarında **Dosya** tipini seçin.

ER parametresi hakkında daha fazla bilgi için, bkz. [ER çerçevesini yapılandırma](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>ER yapılandırma sağlayıcısı etkinleştirin.

Eklenen her ER yapılandırması bir ER konfigürasyon sağlayıcısı tarafından sahiplenilimli olarak işaretlenir. **Elektronik raporlama** çalışma alanında etkinleştirilen ER yapılandırma sağlayıcısı Bu amaçla kullanılır. Bu nedenle, ER konfigürasyonlarını eklemeye veya düzenlemeye başlamadan önce, **elektronik raporlama** çalışma alanında bir er yapılandırma sağlayıcısını etkinleştirmelisiniz.

> [!NOTE]
> Yalnızca ER yapılandırmasının sahibi bunu düzenleyebilir. Bu nedenle, ER konfigürasyonu düzenlemeye başlamadan önce, uygun ER yapılandırma sağlayıcısı **elektronik raporlama** çalışma alanında etkinleştirilmelidir.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER yapılandırma sağlayıcıları listesini gözden geçirin

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sağlayıcıları** kutucuğunu seçin.
3. **Yapılandırma sağlayıcısı tablosu** sayfasında, her sağlayıcı kaydının benzersiz bir adı ve URL'si vardır. Bu sayfanın içeriğini gözden geçirin. **Litware, Inc.** (`https://www.litware.com`) için zaten bir kayıt varsa, sonraki yordamı atlayıp [Yeni bir ER yapılandırma sağlayıcısı ekleyin](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Yeni bir ER yapılandırması sağlayıcısı ekleme

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **İlgili bağlantılar** bölümünde **Yapılandırma sağlayıcıları** kutucuğunu seçin.
3. **Yapılandırma sağlayıcıları** sayfasında, **Yeni**'yi seçin.
4. **Ad** alanına **Litware, Inc.** yazın.
5. **İnternet adresi** alanına `https://www.litware.com` girin.
6. **Kaydet**'i seçin.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>ER yapılandırma sağlayıcısı etkinleştirin.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme konfigürasyonları** sayfasında, **Konfigürasyon sağlayıcıları** bölümünde, **Litware, Inc.** döşemesini seçin ve sonra **etkin ayarla**'yı seçin.

ER yapılandırma sağlayıcıları hakkında daha fazla bilgi için bkz. [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Standart ER biçimi yapılandırmalarını içe aktarın

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>Standart ER yapılandırmalarını içe aktarın

Geçerli Microsoft Dynamics 365 Finance örneğinize standart ER yapılandırmalarını eklemek için bu yapılandırmaları söz konusu örnek için yapılandırılmış olan ER [deposundan](general-electronic-reporting.md#Repository) içeri aktarmanız gerekir.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında, **Yapılandırma Sağlayıcıları** bölümünde **Microsoft** kutucuğunu seçin ve Microsoft sağlayıcısı için depolar listesini görüntülemek için **Depolar**'ı seçin.
3. **Yapılandırma depoları** sayfasında, **Global** türünün deposunu seçin ve sonra **Aç**'ı seçin. Regulatory Configuration Service bağlanmak için yetkilendirme istenirse, yetkilendirme yönergelerini uygulayın.
4. **Konfigürasyon depoları** sayfasında, sol bölmedeki yapılandırma ağacında, **BACS (UK)** biçim yapılandırmasını seçin.
5. **Sürümler** FastTab üzerinde, seçili ER biçim yapılandırmasının gerekli **1.1** sürümünü seçin.
6. Seçili sürümü Global depo'dan mevcut Finance örneğine indirmek için **İçe Aktarma**'ya tıklayın.

![Yapılandırma deposu sayfası.](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> [Global depoya](er-download-configurations-global-repo.md) erişmede sorun yaşıyorsanız, Microsoft Dynamics Lifecycle Services'den (LCS) gelen [yapılandırmaları karşıdan yükleyebilirsiniz](download-electronic-reporting-configuration-lcs.md).

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>İçe aktarılan ER yapılandırmalarını gözden geçirin

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.
3. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin.
4. Seçili **BACS (UK)** ER biçimine ek olarak, gerekli diğer acil yapılandırmalar konfigürasyonlarının da içe aktarıldığına dikkat edin. Aşağıdaki ER yapılandırmaların konfigürasyon ağacında kullanılabilir durumda olduğundan emin olun:

    - **Ödeme modeli** – Bu yapılandırma, ödeme iş etki alanının veri yapısını temsil eden veri modeli ER bileşenini içerir.
    - **Ödeme modeli eşleştirmesi 1611** – Bu yapılandırma, veri modelinin çalışma zamanında uygulama verileriyle nasıl doldurulduğunu açıklayan model eşleme ER bileşenini içerir.
    - **BACS (UK)** – Bu yapılandırma biçim ve biçim eşleme ER bileşenlerini içerir. Format bileşeni rapor düzenini belirtir. Biçim eşleme bileşeni model veri kaynağını içerir ve çalışma süresinde bu veri kaynağı kullanılarak rapor düzeninin nasıl doldurulacağını belirtir.

![Belirtilen ER konfigürasyonlara sahip yapılandırmalar sayfası ağaçta kullanılabilir.](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>İşleme için satıcı ödemesini hazırlayın

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Satıcı hesabı için banka bilgileri ekleme

Bir satıcı hesabının, daha sonra kayıtlı bir ödemede başvurulacak banka bilgilerini eklemeniz gerekir.

1. **Borç hesapları** \> **Satıcılar** \> **Tüm satıcılar**'a gidin.
2. **Tüm satıcılar** sayfasında, **GB_SI_000001** satıcı hesabını seçin ve eylem bölmesinde, **satıcı** sekmesinde, **kurulumu** gerçekleştir grubunda **Banka hesapları**'nı seçin.
3. **Satıcı banka hesapları** sayfasında, **Yeni**'yi seçin ve aşağıdaki bilgileri girin:

    1. **Banka hesabı** alanında **GBP OPER** öğesini girin.
    2. **Banka grupları** alanında, **BankGBP** öğesini seçin.
    3. **Banka hesabı numarası** alanında **202015** girin.
    4. **SWIFT kodu** alanına <a id="DefineSWIFTCode"></a>**CHASDEFXXXX** girin.
    5. **IBAN** alanına **GB33BUKB20201555555555** girin.
    6. **Rota numarası** alanında, <a id="DefineRoutingNumber"></a>**123456** varsayılan değerini saklayın.

    ![Satıcı banka hesapları sayfası.](./media/er-quick-start2-bank-account.png)

4. **Kaydet**'i seçin.
5. Sayfayı kapatın.
6. **Tüm satıcılar** sayfasında, **GB_SI_000001** satıcı hesabını açın.
7. Satıcı ayrıntıları sayfasında, gerekirse sayfayı düzenlenebilir yapmak için **Düzenle** seçin.
8. **Ödeme** hızlı sekmesinde, **Banka hesabı** alanında, **GBP Operasyon** seçin.

    ![Satıcı ayrıntıları sayfası.](./media/er-quick-start2-bank-account-reference.png)

9. **Kaydet**'i seçin.
10. Sayfayı kapatın.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Satıcı ödemesini girin

[Ödeme teklifi](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md) kullanarak yeni satıcı ödemesi girmeniz gerekir.

1. **Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.
2. **Satıcı ödeme günlüğü** sayfasında, **Yeni**'yi seçin.
3. **Ad** alanına **VendPay** seçin.
4. **Satırlar**'ı seçin.
5. **Ödeme teklifi** \> **Ödeme teklifi oluştur**'a tıklayın.
6. **Satıcı ödeme teklifi** iletişim kutusunda, yalnızca **GB_SI_000001** satıcı hesabına ait kayıtları filtrelemek üzere koşulları konfigüre edin ve **Tamam**'ı seçin.
7. **00000007_Inv** fatura için satırı seçin ve sonra **ödeme oluştur**'u seçin.

    ![Satıcı ödeme teklifi iletişim kutusu.](./media/er-quick-start2-payment-proposal.png)

8. Girilen ödemenin **elektronik** ödeme yöntemini kullanacak şekilde konfigüre edilmiş olduğunu doğrulayın.

    ![Satıcı ödemeleri sayfası.](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Standart ER biçimini kullanarak bir satıcı ödemesini işleme

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>Elektronik ödeme yöntemini ayarlama

Elektronik ödeme yöntemini içe aktarılan ER biçim konfigürasyonu kullanacak şekilde konfigüre etmelisiniz.

1. **Borç hesapları** \> **Ödeme kurulumu** \> **Ödeme yöntemleri**'ne gidin.
2. **Ödeme yöntemleri - satıcılar** sayfasında, sol bölmedeki **elektronik** ödeme yöntemini seçin.
3. **Düzenle** öğesini seçin.
4. **Dosya formatları** Hızlı sekmesinde **Genel elektronik Dışa aktarma biçimi** seçeneğini **Evet** olarak ayarlayın.
5. **Dışa aktarma biçimi yapılandırması** alanında, **BACS (UK)** biçim yapılandırması seçin.

    ![Satıcı ödemelerini standart bir biçim kullanarak işlemek üzere elektronik ödeme yöntemi ayarlamak için ödeme yöntemleri sayfası.](./media/er-quick-start2-method-of-payment1.png)

6. **Kaydet**'i seçin.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Satıcı ödemesini işleme

1. **Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.
2. **Satıcı ödeme günlüğü** sayfasında, önceden eklediğiniz ödeme günlüğünü ve ardından **Satırlar**'ı seçin.
3. **Satıcı ödemeleri** sayfasında, **ödemeleri oluştur**'u seçin.
4. **Ödemeler oluşturun** iletişim kutusuna, aşağıdaki bilgileri girin:

    - **Ödeme yöntemi** alanında **Elektronik**'i seçin.
    - **Banka hesabı** alanında **GBSI OPER** öğesini seçin.

5. **Tamam**'ı seçin.
6. **Elektronik rapor parametreleri** iletişim kutusunda, **yazdırma denetimi raporu** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.

    ![Elektronik rapor parametreleri iletişim kutusu sayfası.](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > Ödeme dosyasına ek olarak, artık kontrol raporu oluşturabilirsiniz.

7. Zip dosyasını karşıdan yükleyin ve sonra aşağıdaki dosyaları dosyadan ayıklayın:

    - Excel biçimindeki denetim raporu
    - TXT biçiminde ödeme dosyası

        Sağlanan er biçiminin [yapısına](#PositionRoutingNumber) uygun olarak, oluşturulan dosyadaki ödeme satırının konfigüre edilen Banka hesabı için [tanımlanan](#DefineRoutingNumber) rota numarasıyla başladığını unutmayın.

        ![TXT biçiminde ödeme dosyası.](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Standart ER biçimini Özelleştirme

Bu bölümde gösterilen örnek için, BACS formatında satıcı ödeme dosyaları oluşturmak üzere Microsoft tarafından sağlanan ER konfigürasyonlarını kullanmak istiyorsunuz, ancak belirli bir bankanın gereksinimlerini destekleyecek bir özelleştirme eklemeniz gerekir. Ayrıca, ER konfigürasyonlarının yeni sürümleri kullanılabilir olduğunda da özel biçiminizi yükseltebilmeniz gerekir. Ancak, yükseltme yapabilmek için en düşük maliyette olmasını isteyebilirsiniz.

Bu durumda, Litware, Inc. temsilcisi olarak, **BACS (UK)** Microsoft tarafından temel olarak sağlanan bir yapılandırmayı tkullanarak yeni bir ER biçim konfigürasyonu oluşturmanız (türetmeniz) gerekir.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Özel biçim oluşturma

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **BACS (UK)** seçin. Litwin, Inc. özel sürümün temeli olarak bu ER biçim yapılandırmasının sürüm 1,1 ' sini kullanacaktır.
3. Açılır iletişim kutusunu açmak için **Yapılandırma oluştur**'u seçin. Bu iletişim kutusunu, özel ödeme biçimi için yeni bir konfigürasyon oluşturmanıza olanak sağlar.
4. **Yeni** alan grubunda, **Addan türetilen: BACS (UK), Microsoft** seçeneği.
5. **Ad** alanına, **BACS (UK özel)** girin.

    ![Yapılandırma oluşturma açılan iletişim kutusu.](./media/er-quick-start2-add-derived-format.png)

6. **Yapılandırma oluştur**'u seçin.

**BACS (Birleşik Krallık özel)** ER biçimi yapılandırmasının sürüm 1.1.1 oluşturulur. Bu sürüm **Taslak** durumuna sahiptir ve düzenlenebilir. Özel ER biçiminizin geçerli içeriğinin,  Microsoft tarafından sağlanan biçimin içeriğiyle aynıdır.

![BACS (Birleşik Krallık özel) ER biçimi yapılandırmasının sürüm 1.1.1 ile yapılandırmalar sayfası.](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Özel biçim düzenleme

Özel biçiminizi, bankaya özel gereksinimleri karşılayacak şekilde konfigüre etmelisiniz. Örneğin bir banka, oluşturulan ödeme dosyalarının, bir bankanın işlenmiş olan satıcı ödemesine atanan, tüm dünyada Interbank Financial telekomünikasyon (SWIFT) kodu için Society içermesini gerektirebilir. SWIFT kodları, tüm dünyada belirli bankaların tanımlanmasında kullanılan uluslararası banka kodlarıdır. Bunlar banka tanımlayıcı kodları (BIC'ler) olarak da bilinir. SWIFT kodu 11 karakter uzunluğunda olmalıdır ve oluşturulan bir ödeme dosyasındaki her bir ödeme satırının başına girilmelidir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **BACS (UK özel)** seçin.
3. **Sürümler** FastTab üzerinde, seçili yapılandırmasının gerekli **1.1.1** sürümünü seçin.
4. **Tasarımcı**’yı seçin.
5. **Biçim tasarımcısı** sayfasında Format öğeleriyle ilgili daha fazla bilgi görüntülemek için **ayrıntıları göster** 'i seçin.
6. Aşağıdaki öğeleri genişletip gözden geçirin:

    - **Klasör** türünün **bacsreportsfolder** öğesi. Bu öge ZIP biçiminde çıktı oluşturmak için kullanılır.
    - **Dosya** türünün **dosya** öğesi. Bu öge TXT biçiminde ödeme dosyası oluşturmak için kullanılır.
    - **Sıra** türünün **işlemler** öğesi. Bu öge, ödeme dosyası tekli ödeme oluşturmak için kullanılır.
    - **Sıra** türünün **işlem** öğesi. Bu öge, tekli ödeme satırınsa ayrı alanlar oluşturmak için kullanılır.

7. **İşlem** öğesini seçin.

    ![ER İşlemleri tasarımcısında hareket ögesi.](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Sağlanan rapor, <a id="PositionRoutingNumber"></a>her ödeme satırının Banka rota numarasıyla başlaması için konfigüre edilir. **Vendbankroutenum** biçim öğesi bu amaçla kullanılır. 

8. **Ekle**'i seçin ve sonra eklemekte olduğunuz Format öğesinin **metin\\dizesi** türünü seçin:

    1. **Ad** alanına **vendBankSWIFT** yazın.
    2. **Minimum uzunluk** alanında **11** girin.
    3. **Maksimum uzunluk** alanında **11** girin.
    4. **Tamam**'ı seçin.

    > [!NOTE]
    > **vendBankSWIFT** öğesi, oluşturulan dosyalardaki satıcı bankasının SWIFT kodunu girmek için kullanılır.

9. Biçim yapısı ağacında, **vendBankSWIFT** seçeneğini belirleyin.
10. Seçili biçim öğesini bir düzey yukarı taşımak için **yukarı taşı** seçeneğini seçin. Bu adımı, **vendBankSWIFT** öğesi <a id="PositionSWIFTCode"></a>ana **işlem** öğesinin altındaki ilk öğe olana kadar tekrarlayın.

    ![ER İşlemleri tasarımcısında hareketin altındaki ilk öğe olarak VendBankSWIFT.](./media/er-quick-start2-derived-format1.png)

11. Biçim yapısı ağacında **vendBankSWIFT** 'un hala seçili olmasına karşın, **eşleme** sekmesini seçin ve **model** veri kaynağını genişletin.
12. **model.Payment** \> **model.Payment.CreditorAgent** genişletin ve **model.Payment.CreditorAgent.BICFI** veri kaynağı alanı seçin. Bu veri kaynağı alanı, işlenmiş satıcı ödemesine aracı rolü atanan satıcı bankasının SWIFT kodunu sunar.
13. **Bağla**'yı seçin. **vendBankSWIFT** format ögesi artık **model.Payment.CreditorAgent.BICFI** veri kaynağı alanıyla bağlıdır, böylece oluşturulan ödeme dosyalarına SWIFT kodları girilecaktır.

    ![vendBankSWIFT biçim öğesi, ER İşlemleri tasarımcısında model.Payment.CreditorAgent.BICFI veri kaynağı alanıyla ilişkilidir.](./media/er-quick-start2-derived-format2.png)

14. **Kaydet**'i seçin.
15. Tasarımcı sayfasını kapatın.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Özel biçimi çalıştırılabilir olarak işaretleme

Şimdi özel biçimin ilk sürümü oluşturulduğundan ve **taslak** durumunda olduğundan, bunu test amacıyla çalıştırabilirsiniz. Raporu çalıştırmak için, özel işlem biçiminizi ifade eden ödeme yöntemini kullanarak bir satıcı ödemesini işlemelisiniz. Varsayılan olarak, uygulamadan ER biçimini çağırdığınızda yalnızca **Tamamlandı** ve **Paylaşıldı** durumuna sahip sürümler dikkate alınır. Bu davranış, bitmemiş tasarımları bulunan ER biçimlerinin kullanılmasını önlemeye yardımcı olur. Ancak, test çalışmalarınız için, uygulamayı **taslak** durumunda olan ER formatının biçimini kullanmaya zorlayabilirsiniz. Bu şekilde, herhangi bir değişiklik gerekiyorsa geçerli biçim sürümünü ayarlayabilirsiniz. Daha fazla bilgi için bkz. [Uygulanabilirlik](electronic-reporting-destinations.md#applicability).

ER biçiminin taslak sürümünü kullanmak için, ER biçimini açık olarak işaretlemeniz gerekir.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Kullanıcı parametreleri** iletişim kutusunda, **Çalıştırma ayarları** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.
4. Geçerli sayfayı düzenlemeye hazır hale getirmek için gerektiğinde **Düzenle**'yi seçin.
5. Sol bölmedeki konfigürasyon ağacında, **BACS (UK özel)** öğesini seçin.
6. **Taslak Çalıştır** seçeneğini **Evet** olarak ayarlayın.

    ![Yapılandırmalar sayfasındaki Taslak Çalıştır seçeneği.](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Özel ER biçimini kullanarak bir satıcı ödemesini işleme

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>Elektronik ödeme yöntemini ayarlama

Satıcı ödemelerini işlemek için özel ER formatının kullanılabilmesi için elektronik ödeme yöntemini konfigüre etmelisiniz.

1. **Borç hesapları** \> **Ödeme kurulumu** \> **Ödeme yöntemleri**'ne gidin.
2. **Ödeme yöntemleri - satıcılar** sayfasında, sol bölmedeki **elektronik** ödeme yöntemini seçin.
3. **Düzenle** öğesini seçin.
4. **Dosya formatı** Hızlı sekmesinde **Genel elektronik Dışa aktarma biçimi** seçeneğini **Evet** olarak ayarlayın.
5. **Dışa aktarma biçimi yapılandırması** alanında, **BACS (UK özel)** biçim yapılandırması seçin.

    ![Satıcı ödemelerini özel bir biçim kullanarak işlemek üzere elektronik ödeme yöntemi ayarlamak için ödeme yöntemleri sayfası.](./media/er-quick-start2-method-of-payment2.png)

6. **Kaydet**'i seçin.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Satıcı ödemesini işleme

1. **Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.
2. **Satıcı ödeme günlüğü** sayfasında, önceden oluşturduğunuz ödeme günlüğünü seçin.
3. **Satırlar**'ı seçin.
4. **Satıcı ödemeleri** sayfasında, kılavuzun üstünde, **ödeme durumu** \> **yok** seçeneğini belirleyin.
5. **Ödeme oluştur** seçin.
6. **Ödemeler oluşturun** iletişim kutusuna, aşağıdaki bilgileri girin:

    - **Ödeme yöntemi** alanında **Elektronik**'i seçin.
    - **Banka hesabı** alanında **GBSI OPER** öğesini seçin.

7. **Tamam**'ı seçin.
8. **Elektronik rapor parametreleri** iletişim kutusunda, **yazdırma denetimi raporu** seçeneğini **Evet** olarak ayarlayıp **Tamam**'ı seçin.

    > [!NOTE]
    > Ödeme dosyasına ek olarak, artık kontrol raporu oluşturabilirsiniz.

9. Zip dosyasını karşıdan yükleyin ve sonra aşağıdaki dosyaları dosyadan ayıklayın:

    - Excel biçimindeki denetim raporu
    - TXT biçiminde ödeme dosyası

        Özel ER formatının yapısına uygun olarak, oluşturulan dosyadaki ödeme satırı şimdi, ödemesi işlenmiş olan Satıcının banka hesabı için [girilen](#DefineSWIFTCode) SWIFT koduyla [başlar](#PositionSWIFTCode).

        ![Satıcının ödemesini işlemek için kullanılan, TXT biçimindeki ödeme dosyası.](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Standart ER biçimi yapılandırmalarının yeni sürümlerini içe aktarın

Bu bölümde gösterilen örnek için, Bilgi Bankası makalesi [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046) hakkında bir bildirim alırsınız. Bu bildirim, Microsoft tarafından yayımlanmış olan **BACS (UK)** ER biçiminin yeni sürümü hakkında sizi bilgilendirir. Kontrol raporuna ek olarak, bu yeni sürüm, bir satıcı ödemesi işlenirken kullanıcıların ödeme önerisi raporunu ve ilişkili Not raporunu oluşturmasını sağlar. Bu işlevi kullanmaya başlamak istediğinizde.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Standart ER yapılandırmalarının yeni sürümlerini içe aktarın

Geçerli Finans örneğine standart ER yapılandırmalarının yeni sürümlerini eklemek için onları o örnek için yapılandırılmış olan ER [deposundan](general-electronic-reporting.md#Repository) içe aktarmanız gerekir.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında, **Yapılandırma Sağlayıcıları** bölümünde **Microsoft** kutucuğunu seçin ve Microsoft sağlayıcısı için depolar listesini görüntülemek için **Depolar**'ı seçin.
3. **Yapılandırma depoları** sayfasında, **Global** türünün deposunu seçin ve sonra **Aç**'ı seçin. Regulatory Configuration Service bağlanmak için yetkilendirme istenirse, yetkilendirme yönergelerini uygulayın.
4. **Konfigürasyon depoları** sayfasında, sol bölmedeki yapılandırma ağacında, **BACS (UK)** biçim yapılandırmasını seçin.
5. **Sürümler** FastTab üzerinde, seçili ER biçim yapılandırmasının gerekli **3.3** sürümünü seçin.
6. Seçili sürümü Global depo'dan mevcut Finance örneğine indirmek için **İçe Aktarma**'ya tıklayın.

![Konfigürasyon havuzu sayfası, sürümler hızlı sekmesi, Içe aktar düğmesi.](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> [Global depoya](er-download-configurations-global-repo.md) erişmede sorun yaşıyorsanız, bunun yerine LCS'den gelen [yapılandırmaları karşıdan yükleyebilirsiniz](download-electronic-reporting-configuration-lcs.md).

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>İçe aktarılan ER biçimi yapılandırmalarını gözden geçirin

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.
3. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **BACS (UK)** seçin.
4. **Sürümler** hızlı sekmesinde, sürüm **3.3**' i seçin.
5. **Tasarımcı**’yı seçin.
6. **Biçim tasarımcısı** sayfasında **BACSReportsFolder** biçim öğesini genişletin.
7.  3,3 sürümü, satıcı ödemesi işlenirken bir ödeme önerisi raporu oluşturmak için kullanılan **PaymentAdviceReport** biçim öğesini içerir.

    ![ER İşlemleri tasarımcısında PaymentAdviceReport biçim ögesi.](./media/er-quick-start2-imported-solution2.png)

8. Tasarımcı sayfasını kapatın.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>Özel bir biçimde, içe aktarılan bir biçimin yeni sürümündeki Değişiklikleri benimseme

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>Özel biçimin geçerli taslak sürümünü tamamlama

Özel biçimizin geçerli durumunu korumak istiyorsanız, **taslak** durumundan **tamamlandı** durumuna değiştirerek draft sürüm 1.1.1'ı tamamlayın.

1. **Organizasyon yönetimi** \> **Çalışma alanları** \> **Elektronik raporlama**'ya gidin.
2. **Yerelleştirme yapılandırmaları** sayfasında **Yapılandırmalar** bölümünde **Raporlama yapılandırmaları** kutucuğunu seçin.
3. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **BACS (UK)** seçin ve **BACS (UK özel)**'i seçin.
4. **Sürümler** hızlı sekmesinde, **durumu değiştir** \> **tamamlandı** olarak seçin ve **Tamam** 'ı seçin.

Sürüm 1.1.1 durumu **Taslak** iken **Tamamlandı** olarak değişir ve sürüm salt okunur olur. Yeni bir düzenlenebilir sürüm olan 1.1.2 eklendi ve **taslak** durumuna sahip. Bu sürümü, özel ER biçiminiz üzerinde başka değişiklikler yapmak için kullanabilirsiniz.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Özel biçimi yeni bir temel sürüme yeniden temellendir

Özelleştirmenizin 3,3 **BACS (Birleşik Krallık)** biçiminin yeni işlevlerini kullanmaya başlamak için , özel konfigürasyon, **BACS (Birleşik Krallık özel)** için temel konfigürasyon sürümünü değiştirmeniz gerekir. Bu işlem [yeniden temelleme](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase)olarak bilinmektedir. **BACS (UK)** 1.1 sürümü yerine yeni sürüm 3.3 kullanın.

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında soldaki yapılandırma ağacında, **Ödeme modeli**'ni genişletin ve **BACS (UK özel)** seçin.
3. **Sürümler** hızlı sekmesinde, sürüm **1.1.2** seçin ve yeniden **temellendir** 'i seçin.
4. **Yeniden temellendirme** iletişim kutusunda, **hedef sürüm** alanında, bunu yeni temel olarak uygulamak ve konfigürasyonu güncelleştirmek için kullanmak üzere temel yapılandırmanın **3,3** sürümünü seçin.

    ![Yeniden temellendirme iletişim kutusu.](./media/er-quick-start2-rebase1.png)

5. **Tamam**'ı seçin.
6. Taslak sürümün sayısının temel sürümdeki değişikliği yansıtmak için **1.1.2** olan sayının **3.3.2** olarak değiştiğine dikkat edin.

    Otomatik olarak birleştirilemeyen bazı biçim değişikliklerini temsil eden, yeni temel sürüm ile özel sürümün birleştirilmesi sırasında bazı çakışmaların ortaya çıktığını göz önünde tutun.

    ![Yapılandırmalar sayfasındaki çakışmalarla yeniden temellendirme yapılandırması.](./media/er-quick-start2-rebase2.png)

    Çakışmalar keşfedildiğinde, biçim Tasarımcısı 'nda el ile çözülmesi gerekir.

7. **Sürümler** hızlı sekmesinde, sürüm **3.3.2**' i seçin.
8. **Tasarımcı**’yı seçin.
9. **Biçim Tasarımcısı** sayfasında, **Ayrıntılar** hızlı sekmesinde, yeniden temellendirme çakışma kaydını seçin ve **temel değer Uygula**'yı seçin.

    ![ER İşlemleri Tasarımcısı'nda çakışma kaydını yeniden temellendirme.](./media/er-quick-start2-rebase3.png)

10. **Kaydet**'i seçin.

    Yeniden temellendirme çakışma kaydı **Ayrıntılar** hızlı sekmesinde artık görünolmamalıdır.

    ![ER İşlemleri Tasarımcısı'nda çözümlenen çakışma.](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > Bu ER biçiminde temel modelin sürüm 3'ün kullanılması gerektiğini onaylayarak çakışmayı çözdünüz.

11. **BACSReportsFolder** \> **dosya** \> **işlemler** \> **işlem**'i genişletin.
12. **Eşleme** sekmesinde, özel ER biçimlendirmenizin 3.3.2 sürümü hem özelleştirmenizi (**vendBankSWIFT** biçim öğesi ve bağlaması) içerir, hem de Microsoft (**PaymentAdviceReport** biçim öğesi iç içe geçirilmiş öğeler ve yapılandırılmış bağlamalar ile birlikte) tarafından sağlanan temel ER biçiminin sürüm 3,3 ' inin yeni işlevselliğinden emin olun. Yalnızca birkaç fare tıklatmasıyla, özelleştirmeyle birleştirerek yeni bir temel sürümün değişikliklerini benimsemiş olursunuz.

    ![ER İşlemleri tasarımcısında birleştirilmiş biçim.](./media/er-quick-start2-rebase5.png)

13. Tasarımcı sayfasını kapatın.

> [!NOTE]
> Yeniden temellendirme eylemi geri alınamaz. Bu yeniden temellendirme iptal etmek için, **sürümler** hızlı sekmesinde **BACS (Birleşik Krallık özel)** biçiminin sürüm **1.1.1** öğesini seçin ve sonra **Bu sürümü Al**'ı seçin. Daha sonra 3.3.2 sürüm 1.1.2 yeniden numaralandırılır ve taslak sürümü 1.1.2 içeriği sürüm 1.1.1 içeriğiyle eşleşir.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Yeniden temellendirilen ER biçimini kullanarak bir satıcı ödemesini işleme

1. **Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.
2. **Satıcı ödeme günlüğü** sayfasında, önceden oluşturduğunuz ödeme günlüğünü seçin.
3. **Satırlar**'ı seçin.
4. **Satıcı ödemeleri** sayfasında, kılavuzun üstünde, **ödeme durumu** \> **yok** seçeneğini belirleyin.
5. **Ödeme oluştur** seçin.
6. **Ödemeler oluşturun** iletişim kutusuna, aşağıdaki bilgileri girin:

    - **Ödeme yöntemi** alanında **Elektronik**'i seçin.
    - **Banka hesabı** alanında **GBSI OPER** öğesini seçin.

7. **Tamam**'ı seçin.
8. **Elektronik rapor parametreleri** iletişim kutusuna, aşağıdaki bilgileri girin:

    - **Kontrol raporu yazdır** seçeneğini **Evet** olarak ayarlayın.
    - **Ödeme önerisi yazdır** seçeneğini **Evet** olarak ayarlayın.

    ![Elektronik rapor parametreleri iletişim kutusu.](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > Ödeme dosyasına ek olarak, artık hem denetim raporunu hem de ödeme önerisi raporunu oluşturabilirsiniz.

9. **Tamam**'ı seçin.
10. Zip dosyasını karşıdan yükleyin ve sonra aşağıdaki dosyaları dosyadan ayıklayın:

    - Excel biçimindeki denetim raporu
    - Excel biçimindeki ödeme önerisi raporu

        ![Excel biçimindeki ödeme ihbarı raporu.](./media/er-quick-start2-payment-advice-report.png)

    - TXT biçiminde ödeme dosyası

        Özel ER formatının yapısına uygun olarak, oluşturulan dosyadaki ödeme satırı şimdi, ödemesi işlenmiş olan Satıcının banka hesabı için girilen SWIFT koduyla başlar.

        ![Yeniden temellendirilen ER biçimi kullanarak satıcının ödemesini işlemek için kullanılan, TXT biçimindeki ödeme dosyası.](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Ek kaynaklar

- [Elektronik Raporlamaya genel bakış](general-electronic-reporting.md)
- [Lifecycle Services'dan ER yapılandırma indirme](download-electronic-reporting-configuration-lcs.md)
- [Yapılandırma hizmeti genel deposundan ER yapılandırmalarını indir](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
