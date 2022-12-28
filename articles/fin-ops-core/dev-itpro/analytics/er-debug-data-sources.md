---
title: Veri akışı ve dönüşümünü analiz etmek için yürütülen bir ER biçiminin veri kaynaklarında hata ayıklama
description: Bu makalede, yapılandırılmış veri akışını ve dönüştürmeyi daha iyi anlamak için yürütülen bir ER biçiminin veri kaynaklarında nasıl hata ayıklayabileceğiniz açıklanmaktadır.
author: kfend
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, EROperationDesigner
ms.openlocfilehash: 61bc5e3f36bd2ae6e38ed0f511d70a7ae62e045c
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832044"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>Veri akışı ve dönüşümünü analiz etmek için yürütülen bir ER biçiminin veri kaynaklarında hata ayıklama

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

Giden belgeler oluşturmak için bir Elektronik raporlama (ER) çözümü [yapılandırdığınızda](tasks/er-format-configuration-2016-11.md) uygulamadan veri almak ve oluşturulan çıktıya bu verileri girmek için kullanılan yöntemleri belirlersiniz. ER çözümünün yaşam döngüsü desteğini daha etkili hale getirmek için, bir ER veri modeli ve onun eşlemesini ve ayrıca bir ER biçimi  ve onun eşleme bileşenlerini oluşturmanız gerekir; böylece model eşleme uygulamaya özel olacak ve diğer bileşenler uygulama belirsiz olarak kalacaktır. Bu nedenle, birkaç ER bileşeni oluşturulan çıktıya veri girme işlemini etkileyebilir.

Bazı durumlarda, oluşturulan çıktının verileri uygulama veritabanındaki aynı verilerden farklı görünür. Bu durumlarda, veri dönüştürme için hangi ER bileşeninin sorumlu olduğunu belirlemek istersiniz. ER veri kaynağı hata ayıklama özelliği, bu araştırmaya harcanan zamanı ve maliyeti önemli ölçüde azaltır. Bir ER biçimi yürütmesini kesebilir ve veri kaynağı hata ayıklama arabirimini açabilirsiniz. Arabirimde, kullanılabilir veri kaynaklarına göz atabilir ve yürütme için tek bir veri kaynağı seçebilirsiniz. Bu el ile yürütme, bir ER biçiminin gerçek çalışması sırasındaki veri kaynağı yürütmesinin benzetimi yapar. Sonuç, alınan verileri analiz edebileceğiniz bir sayfada gösterilir.

Veri kaynağı hata ayıklama özelliğini etkinleştirmek için, **Biçim çalıştırmada veri hata ayıklamasını etkinleştir** seçeneğini ER kullanıcı parametrelerinde **Evet** olarak ayarlayın. Böylece, giden belgeler oluşturmak üzere bir ER biçimi çalıştırırken veri kaynağı hata ayıklaması başlatabilirsiniz. Ayrıca, [ER İşlem tasarımcısında](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document) yapılandırılan bir ER biçimi için veri kaynağı hata ayıklamasını başlatmak için **Hata ayıklamayı başlat** seçeneğini kullanabilirsiniz.

Bu makalede, yürütülen ER biçimlerinde veri kaynağı hata ayıklamasını başlatmak için yönergeler sağlanmaktadır. Veri akışını ve veri dönüştürme işlemlerini anlamanıza yardımcı olabilecek bilgiler açıklanır. Bu makaledeki örnekler, satıcı ödemelerini işlemede kullanılan iş sürecini kullanır.

## <a name="limitations"></a>Sınırlamalar

Veri kaynağı hata ayıklayıcı, giden belgeler oluşturmak üzere çalıştırılan ER biçimlerinde kullanılan veri kaynaklarının verilerine erişmek için kullanılabilir. Gelen belgeleri ayrıştırmak üzere tasarlanan ER biçimlerinin veri kaynaklarında hata ayıklamak için kullanılamaz.

Aşağıdaki ER biçimi ayarlarına şu anda veri kaynağı hata ayıklama için erişilemez:

- Biçim dönüşümleri
- Biçim ve eşleme doğrulama kuralları
- İfadeleri etkinleştirme
- Bellek içi veri toplama ayrıntıları

## <a name="prerequisites"></a>Ön Koşullar

- Bu makaledeki örnekleri tamamlamak için aşağıdaki [rollerden](../sysadmin/tasks/assign-users-security-roles.md) birine erişiminiz olmalıdır:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

- Şirketin **DEMF** olarak ayarlanması gerekir.

- Bu makalenin [Ek 1](#appendix1) bölümündeki adımları izleyerek satıcı ödemelerini işlemek için gerekli olan Microsoft ER çözümü bileşenlerini indirin.
- İndireceğiniz ER çözümünü kullanarak satıcı ödemesi işleme için Borç hesaplarını hazırlamak üzere bu makalenin [Ek 2](#appendix2) bölümündeki konuları izleyin.

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>Ödeme dosyasını almak için satıcı ödemesini işleme

1. Satıcı ödemelerini işlemek için bu makaledeki [Ek 3](#appendix3) bölümünde yer alan adımları izleyin.

    ![Satıcı ödeme işlemi devam ediyor.](./media/er-data-debugger-process-payment.png)

2. Zip dosyasını indirin ve yerel bilgisayarınıza kaydedin.
3. **ISO20022 Credit transfer.xml** ödeme dosyasını zip dosyasından çıkarın.
4. XML dosya görüntüleyicisini kullanarak çıkarılan ödeme dosyasını açın.

    Ödeme dosyasında, satıcı banka hesabının Uluslararası Banka Hesabı Numarası (IBAN) kodu boşluk içermez. Bu nedenle, **Banka hesapları** sayfasına [girilmiş](#enteredIBANcode) olan değerden farklılık gösterir.

    ![Boşluk içermeyen IBAN kodu.](./media/er-data-debugger-payment-file.png)

    ER veri kaynağı hata ayıklayıcısını, IBAN kodundaki boşlukları kırpmak için ER çözümünün hangi bileşeninin kullanıldığını öğrenmek üzere kullanabilirsiniz.

## <a name="turn-on-data-source-debugging"></a>Veri kaynağı hata ayıklamayı açma

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasındaki Eylem Bölmesinde, **Yapılandırmalar** sekmesinin **Gelişmiş ayarlar** grubunda **Kullanıcı parametreleri**'ni seçin.
3. **Biçim çalıştırma sırasında veri hatası ayıklamayı etkinleştir** seçeneğini **Evet** olarak ayarlayın.

    > [!NOTE]
    > Bu parametre kullanıcıya özel ve şirkete özeldir.

    ![Kullanıcı parametreleri iletişim kutusu.](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>Hata ayıklama için satıcı ödemesini işleme

1. Satıcı ödemelerini işlemek için bu makaledeki [Ek 3](#appendix3) bölümünde yer alan adımları izleyin.
2. İleti kutusunda, satıcı ödeme işlemini kesintiye uğratmak istediğinizi doğrulamak için **Evet**'i seçin ve bunun yerine **Veri Kaynaklarında Hata Ayıkla** sayfasında veri kaynağı hata ayıklama işlemini başlatın.

    ![Onay iletisi kutusu.](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>Ödeme işlemede kullanılan veri kaynaklarında hata ayıklama

### <a name="debug-the-model-mapping"></a>Model eşlemesinde hata ayıklama

1. **Veri Kaynaklarında Hata Ayıkla** sayfasında, Eylem Bölmesinde, hata ayıklamayı bu ER bileşinden başlatmak için **Model eşleme**'yi seçin.
2. Soldaki veri kaynağı bölmesinde, **\$notSentTransactions** veri kaynağını seçin ve **Tüm kayıtları oku**'yu seçin.

    Seçilen veri kaynağından okunacak uygun kayıt sayısını zorlamak için **1 kayıt oku**, **10 kayıt oku**, **100 kayıt oku** veya **Tüm kayıtları oku** seçeneğini seçebilirsiniz. Bu şekilde, çalışan ER biçiminden veri kaynağına erişim benzetimi yapabilirsiniz.

3. Sağdaki veri bölmesinde **Tümünü genişlet**'i seçin.

    **Kayıt listesi** türündeki seçili kaynağın tek bir kayıt içerdiğini görebilirsiniz.

4. **\$notSentTransactions** veri kaynağını genişletin ve iç içe geçmiş **vendBankAccountInTransactionCompany()** yöntemini seçin.
5. **vendBankAccountInTransactionCompany()** yöntemini genişletin ve iç içe geçmiş **IBAN** alanını seçin.
6. **Değeri al**'ı seçin.

    Seçili veri kaynağının seçili alanının değerini okunacak şekilde zorlamak için **Değeri al**'ı seçebilirsiniz. Bu şekilde, çalışan ER biçiminden bu alana erişim benzetimi yapabilirsiniz.

7. **Tümünü genişlet**'i seçin.

    ![Model eşlemedeki IBAN alanının değeri.](./media/er-data-debugger-debugging-model-mapping.png)

    Gördüğünüz gibi, satıcı banka hesabı için döndürdüğü IBAN kodu boşluklar içerdiğinden model eşleme kesilen boşluklardan sorumlu değildir. Bu nedenle, veri kaynağı hata ayıklamasını sürdürmelisiniz.

### <a name="debug-the-format-mapping"></a>Biçim eşlemede hata ayıklama

1. **Veri Kaynaklarında Hata Ayıkla** sayfasında, Eylem Bölmesinde, hata ayıklamayı bu ER bileşininden sürdürmek için **Biçim eşleme**'yi seçin.
2. **\$PaymentByDebtor** veri kaynağını seçin ve ardından **Tüm kayıtları oku**'yu seçin.
3. **\$PaymentByDebtor** öğesini genişletin.
4. **\$PaymentByDebtor.Lines** öğesini genişletin ve ardından **Tüm kayıtları oku**'yu seçin.
5. **\$PaymentByDebtor.Lines.CreditorAccount** öğesini genişletin.
6. **\$PaymentByDebtor.Lines.CreditorAccount.Identification** öğesini genişletin ve **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN** öğesini seçin.
7. **Değeri al**'ı seçin.
8. **Tümünü genişlet**'i seçin.

    ![Biçim eşlemedeki IBAN alanının değeri.](./media/er-data-debugger-debugging-format-mapping.png)

    Gördüğünüz gibi, satıcı banka hesabı için döndürdükleri IBAN kodu boşluklar içerdiğinden biçim eşlemenin veri kaynakları kesilen boşluklardan sorumlu değildir. Bu nedenle, veri kaynağı hata ayıklamasını sürdürmelisiniz.

### <a name="debug-the-format"></a>Biçimde hata ayıklama

1. **Veri Kaynaklarında Hata Ayıkla** sayfasında, Eylem Bölmesinde, hata ayıklamayı bu ER bileşininden sürdürmek için **Biçim**'i seçin.
2. **ISO20022CTReports** \> **XMLHeader** \> **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** öğesini seçmek için biçim öğelerini genişletin ve ardından **Tüm kayıtları oku**'yu seçin.
3. **ISO20022CTReports** \> **XMLHeader** \> **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** öğesini seçmek için biçim öğelerini genişletin ve ardından **Tüm kayıtları oku**'yu seçin.
4. **ISO20022CTReports** \> **XMLHeader** \> **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** öğesini seçmek için biçim öğelerini genişletin ve ardından **Değeri al**'ı seçin.
5. **Tümünü genişlet**'i seçin.

    ![Biçimdeki IBAN alanının değeri.](./media/er-data-debugger-debugging-format.png)

   Gördüğünüz gibi, satıcı banka hesabı için döndürdüğü IBAN kodu boşluklar içerdiğinden biçim bağlaması kesilen boşluklardan sorumlu değildir. Bu nedenle, **BankIBAN** öğesi, boşlukları kesen bir biçim dönüşümü kullanacak şekilde yapılandırılmıştır.

6. Veri kaynağı hata ayıklayıcısını kapatın.

### <a name="review-the-format-transformations"></a>Biçim dönüştürmelerini gözden geçirme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Yapılandırmalar** sayfasında, **Ödeme modeli** \> **ISO20022 Alacak transferi** seçeneğini belirleyin.
3. **Tasarımcı**'yı seçin ve ardından **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**'ı seçmek için öğeleri genişletin.

    ![Biçim tasarımcısı sayfasındaki BankIBAN öğesi.](./media/er-data-debugger-referred-transformation.png)

    Gördüğünüz gibi, **BankIBAN** öğesi **alfasayısal olmayanı kaldır** dönüşümünü kaldırmak için yapılandırılmışır.

4. **Dönüştürmeler** sekmesini seçin.

    ![BankIBAN öğesi için dönüştürmeler sekmesi.](./media/er-data-debugger-transformation.png)

    Gördüğünüz gibi, **alfasayısal olmayanı kaldır** dönüştürme işlemi, sağlanan metin dizesinden boşlukları kesen bir ifade kullanacak şekilde yapılandırılmıştır.

## <a name="start-to-debug-in-the-operation-designer"></a>İşlem tasarımcısında hata ayıklamaya başlatma

Doğrudan İşlem tasarımcısından çalıştırılabilen ER biçiminin taslak sürümünü yapılandırdığınızda, Eylem Bölmesinde **Hata Ayıklamayı Başlat**'ı seçerek veri kaynağı hata ayıklayıcıya erişebilirsiniz.

![Biçim tasarımcısı sayfasındaki Hata Ayıklamayı Başlat düğmesi.](./media/er-data-debugger-run-from-designer.png)

Düzenlenen ER biçiminin biçim eşlemesi ve biçim bileşenleri hata ayıklama için kullanılabilir.

## <a name="start-to-debug-in-the-model-mapping-designer"></a>Model eşleme tasarımcısında hata ayıklamaya başlatma

**Model eşleme** sayfasından çalıştırılabilen bir ER model eşlemesi yapılandırdığınızda, Eylem Bölmesinde **Hata Ayıklamayı Başlat**'ı seçerek veri kaynağı hata ayıklayıcıya erişebilirsiniz.

![Model eşleme tasarımcısı sayfasındaki Hata Ayıklamayı Başlat düğmesi.](./media/er-data-debugger-run-from-designer-mapping.png)

Düzenlenmekte olan ER eşlemesinin model eşleme bileşeni hata ayıklama için kullanılabilir.

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>Ek 1: ER çözümü alma

### <a name="download-an-er-solution"></a>ER çözümü indirme

İşlenen bir satıcı ödemesi için elektronik ödeme dosyası oluşturmak üzere bir ER çözümü kullanmak istiyorsanız, Microsoft Dynamics LifeCycle Services'taki (LCS) Paylaşılan varlık kitaplığından veya Genel depodan **ISO20022 Alacak transferi** ER ödeme biçimini [indirebilirsiniz](download-electronic-reporting-configuration-lcs.md).

![Yapılandırma deposu sayfasındaki ER ödeme biçimini içe aktarma.](./media/er-data-debugger-import-from-repo.png)

Seçili ER biçimine ek olarak, aşağıdaki [yapılandırmalar](general-electronic-reporting.md#Configuration) Microsoft Dynamics 365 Finance örneğinize **ISO20022 Alacak transferi** ER çözümünüzün bir parçası olarak otomatik olarak aktarılmalıdır:

- **Ödeme modeli** ER veri modeli yapılandırması
- **ISO20022 Alacak transferi** ER biçimi yapılandırması
- **Ödeme modeli eşleme 1611** ER modeli eşleme yapılandırması
- **ISO20022 hedefine ödeme modeli eşleme** ER modeli eşleme yapılandırması

Bu yapılandırmaları ER çerçevesinin **Yapılandırmalar** sayfasında bulabilirsiniz (**Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**).

![Yapılandırmalar sayfasında içe aktarılan yapılandırmalar.](./media/er-data-debugger-configurations.png)

Daha önce listelenmiş yapılandırmalardan herhangi bir yapılandırma ağacında eksikse, bunları **ISO20022 Alacak transferi** ER ödeme biçimini indirdiğiniz şekilde LCS paylaşılan varlık kitaplığından el ile indirmeniz gerekir.

### <a name="analyze-the-downloaded-er-solution"></a>İndirilen ER çözümünü analiz etme

#### <a name="review-the-model-mapping"></a>Model eşlemeyi gözden geçirme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Ödeme modeli** \> **Ödeme modeli eşlemesi 1611**'i seçin.
3. **Tasarımcı**’yı seçin.
4. **Ödeme modeli eşlemesi ISO20022 CT** eşleme kaydını seçin.
5. **Tasarımcı**'yı seçin ve sonra açılan model eşlemeyi gözden geçirin.

    Veri modelinin **Ödemeler** alanının, işlenmekte olan satıcı ödemesi satırlarını döndüren **\$notSentTransactions** veri kaynağına bağlı olduğuna dikkat edin.

    ![Model eşleme tasarımcısı sayfasındaki ödemeler alanı.](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>Biçim eşlemeyi gözden geçirme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Ödeme modeli** \> **ISO20022 Alacak transferi**'ni seçin.
3. **Tasarımcı**’yı seçin.
4. **Eşleme** sekmesinde, açılan biçim eşlemesini gözden geçirin.

    **ISO20022CTReports** \> **XMLHeader** dosyasının **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** öğesinin veri modelinin **Ödemeler** alanındaki kayıtları gruplandırılan **\$PaymentByDebtor** veri kaynağına bağlı olduğuna dikkat edin.

    ![Biçim tasarımcısı sayfasındaki PmtInf öğesi.](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>Biçimi gözden geçirme

1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Yapılandırmalar**'a gidin.
2. **Ödeme modeli** \> **ISO20022 Alacak transferi**'ni seçin.
3. **Tasarımcı**'yı seçin ve sonra açılan biçimi gözden geçirin.

    **Belge** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** altındaki biçimin ödeme dosyasındaki satıcı hesabının IBAN kodunu girmek üzere yapılandırıldığından emin olun.

    ![Biçim tasarımcısı sayfasındaki BankIBAN biçim öğesi.](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>Ek 2: Borç hesaplarını yapılandırma

### <a name="modify-a-vendor-property"></a>Satıcı özelliğini değiştirme

1. **Borç hesapları** \> **Satıcılar** \> **Tüm satıcılar**'a gidin.
2. **DE-01002** satıcısını seçin ve ardından Eylem Bölmesinde, **Satıcı** sekmesinde **Ayar** grubunda, **Banka hesapları**'nı seçin.
3. **Kimlik** hızlı sekmesinde, **IBAN** alanına <a name="enteredIBANcode"></a> **GB33 BUKB 2020 1555 5555 55** girin.
4. **Kaydet**'i seçin.

![Satıcı banka hesapları sayfasında ayarlanan IBAN alanı.](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>Ödeme yöntemi ayarlama

1. **Borç hesapları** \> **Ödeme kurulumu** \> **Ödeme yöntemleri**'ne gidin.
2. **SEPA CT** ödeme yöntemini seçin.
3. **Dosya biçimleri** Hızlı sekmesinde **Dosya biçimlerşi** bölümünde **Genel elektronik Dışa aktarma biçimi** seçeneğini **Evet** olarak ayarlayın.
4. **Dışa aktarma biçimi yapılandırması** alanında, **ISO20022 Alacak transferi** ER biçimini seçin.
5. **Kaydet**'i seçin.

![Ödeme yöntemleri sayfasındaki dosya biçimi ayarları.](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>Satıcı ödemesi ekleme

1. **Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.
2. Yeni bir ödeme günlüğü ekleyin.
3. **Satırlar**'ı seçin ve yeni bir ödeme satırı ekleyin.
4. **Hesap** alanında satıcı **DE-01002**'yi seçin.
5. **Borç** alanına bir değer girin.
6. **Ödeme yöntemi** alanında **SEPA CT**'yi seçin.
7. **Kaydet**'i seçin.

![Satıcı ödemeleri sayfasına eklenen satıcı ödemesi.](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>Ek 3: Satıcı ödemesini işleme

1. **Borç hesapları** \> **Ödemeler** \> **Satıcı ödeme günlüğü**'ne gidin.
2. **Satıcı ödeme günlüğü** sayfasında, önceden oluşturduğunuz ödeme günlüğünü ve ardından **Satırlar**'ı seçin.
3. Ödeme satırını seçin ve **Ödeme durumu** \> **Hiçbiri**'ni seçin.
4. **Ödemeleri oluştur**'u seçin.
5. **Ödeme yöntemi** alanında **SEPA CT**'yi seçin.
6. **Banka hesabı** alanında **DEMF OPER** öğesini seçin.
7. **Ödeme oluştur** iletişim kutusunda **Tamam**'ı seçin.
8. **Elektronik rapor parametreleri** iletişim kutusunda **Tamam**'ı seçin.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
