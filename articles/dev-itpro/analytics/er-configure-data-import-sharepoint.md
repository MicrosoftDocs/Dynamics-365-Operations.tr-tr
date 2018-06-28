---
title: "SharePoint'ten veri aktarımını yapılandırma"
description: "Bu konu, Microsoft SharePoint'ten nasıl veri aktarılacağını açıklamaktadır."
author: NickSelin
manager: AnnBe
ms.date: 05/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 2fc887668171175d436b9eb281a35c1c9d089591
ms.openlocfilehash: 4285db9c71208bce45d64933e692a25ef3f46b26
ms.contentlocale: tr-tr
ms.lasthandoff: 05/25/2018

---
# <a name="configure-data-import-from-sharepoint"></a>SharePoint'ten veri aktarımını yapılandırma

[!include[banner](../includes/banner.md)]

Elektronik raporlama (ER) çerçevesini kullanarak bir gelen dosyadan verileri içe aktarmak için, içe aktarmayı destekleyen bir ER biçimi yapılandırmanız ve ardından bu biçimi veri kaynağı olarak kullanan **Hedefe** türünün bir model eşlemesini çalıştırmanız gerekir. Verileri içe aktarmak için, içe aktarmak istediğiniz dosyaya gitmeniz gerekir. Kullanıcı gelen dosyayı el ile seçebilir. Microsoft SharePoint'ten veri içe aktarmayı destekleyen yeni ER özelliği sayesinde bu işlem müdahalesiz yürüyecek şekilde yapılandırılabilir. Microsoft SharePoint klasörlerinde depolanan dosyalardan veri içe aktarmak için ER yapılandırmalarını kullanabilirsiniz. Bu konu, SharePoint'ten Microsoft Dynamics 365 for Finance and Operations'a veri aktarma işleminin nasıl yapılacağını açıklamaktadır. Örneklerde iş verisi olarak satıcı hareketleri kullanılmaktadır.

## <a name="prerequisites"></a>Ön koşullar
Bu konudaki örnekleri tamamlamak için şu erişimlere sahip olmanız gerekir:

- Aşağıdaki rollerden biri için Finance and Operations'a erişim:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

- Finance and Operations ile kullanılmak için yapılandırılmış Microsoft SharePoint Server örneğine erişim
- 1099 ödemeleri için ER biçimi ve model yapılandırmaları

### <a name="create-required-er-configurations"></a>Gerekli ER yapılandırmalarını oluşturma
**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası olan **Bir Microsoft Excel dosyasından ER veri içe aktarma** görev kılavuzlarını oynatın. Bu görev kılavuzları, harici Microsoft Excel dosyalarından satıcı hareketlerini etkileşimli olarak içe aktarmak için ER yapılandırmalarını tasarlama ve kullanma sürecinde size yol gösterir. Daha fazla bilgi için bkz. [Microsoft Excel biçiminde gelen belgeleri ayrıştırma](parse-incoming-documents-excel.md). Sonuçta elinizde şunlar olacak:

- ER yapılandırmaları:

    - ER model yapılandırması, **1099 Ödemeleri modeli**
    - ER biçim yapılandırması, **Satıcıların hareketlerini Excel'den içe aktarma biçimi**

[![SharePoint'ten veri içe aktarmak için ER yapılandırmaları](./media/GERImportFromSharePoint-01-Configurations.PNG)](./media/GERImportFromSharePoint-01-Configurations.PNG)

- Veri içe aktarmada kullanılacak gelen dosya örneği:

    - Excel dosyası **1099import-data.xlsx**: Finance and Operations'a aktarılması gereken satıcı hareketlerinin bulunduğu dosya

[![SharePoint'ten içe aktarmada kullanılacak Microsoft Excel dosyası örneği](./media/GERImportFromSharePoint-02-Excel.PNG)](./media/GERImportFromSharePoint-02-Excel.PNG)

> [!NOTE]
> Satıcı hareketlerini içe aktarmak için kullanılan biçim, varsayılan model eşleme olarak seçilidir. Bu nedenle, bir model eşlemesi çalıştırıyorsanız, **1099 Ödemeleri modeli** çalıştırıyorsanız ve söz konusu model eşleme **Hedefe** türündeyse, model eşleme, harici dosyalardan içe veri aktarmak için bu biçimi çalıştırır. Ardından bu verileri, uygulama tablolarını güncelleştirmek için kullanır.

## <a name="configure-document-management-parameters"></a>Belge yönetim parametrelerini yapılandırma
1. **Belge yönetim parametreleri** sayfasında, oturum açtığınız şirketin kullanacağı SharePoint Server örneğine erişimi yapılandırın. Bu örnekte şirket USMF'dir.
2. Size erişim verildiğinden emin olmak için SharePoint Server örneğine bağlantıyı test edin.

[![Belge yönetim ayarı – SharePoint sunucusu](./media/GERImportFromSharePoint-03-SharePointSetup.png)](./media/GERImportFromSharePoint-03-SharePointSetup.png)

3. Yapılandırılmış SharePoint sitesini açın ve gelen dosyaların depolanabileceği şu klasörleri oluşturun:

    - Dosya içe aktarma kaynağı (ana)
    - Dosya içe aktarma kaynağı (alternatif)

[![Belge yönetim ayarı – SharePoint sunucusu](./media/GERImportFromSharePoint-04-SharePointFolder1.png)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

[![Belge yönetim ayarı – SharePoint sunucusu](./media/GERImportFromSharePoint-05-SharePointFolder2.png)](./media/GERImportFromSharePoint-05-SharePointFolder2.png)

4. Finance and Operations'ta, **Belge türleri** sayfasında, yeni oluşturduğunuz SharePoint klasörlerine erişmek için kullanılacak şu belge türlerini oluşturun:

    - SP Ana
    - SP Alternatif

5. Oluşturulan belge türleri için, **Grup** alanına **Dosya** girin ve **Konum** alanına **SharePoint** girin. Bunun ardından SharePoint klasörünün adresini girin:

    - **SP Ana** belge türü için: Dosya içe aktarma kaynağı (ana)
    - **SP Alternatif** belge türü için: Dosya içe aktarma kaynağı (alternatif)

[![SharePoint ayarı – yeni belge türü](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>ER biçimi için ER kaynaklarını yapılandırma
1. **Kuruluş yönetimi** > **Elektronik raporlama** > **Elektronik raporlama kaynağı**'na tıklayın.
2. **Elektronik raporlama kaynağı** sayfasında, yapılandırılmış ER biçimini kullanarak, veri içe aktarma işlemi için kullanılacak kaynak dosyalarını yapılandırın.
3. Yalnızca .xlsx uzantılı dosyaların içe aktarılması için bir dosya adı maskesi tanımlayın. Dosya adı maskesi isteğe bağlıdır ve ancak tanımlandığı zaman kullanılır. Her bir ER biçimi için yalnızca bir maske tanımlayabilirsiniz.
4. Daha önce oluşturduğunuz her iki SharePoint klasörünü seçin.

[![ER dosyaları kaynak ayarı](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
>ER *kaynağı* her bir uygulama şirketi için ayrı ayrı tanımlanır. Bunun aksine, ER *yapılandırmaları* şirketler arasında paylaşılır.

> [!NOTE]
> Bir ER biçimine ait bir ER kaynağı ayarını sildiğiniz zaman, tüm bağlantılı dosya durumları da (aşağıya bakın) silinir.

## <a name="review-the-files-states-for-the-er-format"></a>ER biçimi için dosya durumlarını inceleme
1. Mevcut ER biçimi için yapılandırılmış dosya kaynaklarının içeriğini incelemek için **Elektronik raporlama kaynağı** sayfasında **Kaynaklar için dosya durumları**'nı seçin.
2. **Dosyalar** bölümünde, dosyalar listesini inceleyin. Bu listede aşağıdakiler sunulur:

    - Dosya adı maskesine göre (bir dosya adı maskesi tanımlandıysa) uygun ve veri içe aktarmaya hazır kaynak dosyalar. Bu dosyalar için, **İçe aktarma için kaynaklar günlüğü** bölümü boştur.
    - Daha önce içe aktarılan dosyalar. Bu dosyaların her biri için, **İçe aktarma biçimi için kaynaklar günlüğü** bölümünde, bu dosyanın içe aktarma geçmişini inceleyebilirsiniz.

**Kaynaklar için dosya durumları** sayfasını **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Kaynaklar için dosya durumları**'nı seçerek de açabilirsiniz. Bu durumda, sayfada, oturum açtığınız şirkette dosya kaynaklarının yapılandırıldığı tüm ER biçimlerinin dosya kaynakları hakkında bilgiler verilir.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Bir SharePoint klasöründeki Excel dosyalarından verileri içe aktarma
1. SharePoint'te, satıcı hareketlerini içeren Microsoft Excel dosyasını (**1099import-data.xlsx**), daha önce oluşturduğunuz **Dosya içe aktarma kaynağı (ana)** SharePoint klasörüne yükleyin.

[![SharePoint içeriği – İçe aktarmada kullanılacak Microsoft Excel dosyası](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. Finance and Operations'ta, **Kaynaklar için dosya durumları** sayfasında, **Yenile**'yi seçerek sayfayı yenileyin. SharePoint'e yüklenen Excel dosyasının bu formda **Hazır** durumda görüneceğine dikkat edin. Şu anda aşağıdaki durumlar desteklenmektedir:

    - **Hazır** - bir SharePoint klasöründeki her yeni dosyaya otomatik olarak atanır. Bu durum, dosyanın içe aktarılmaya hazır olduğu anlamına gelir.
    - **İçe Aktarılıyor** - Dosya, başka işlemler (çok sayıda işlem aynı anda çalışıyorsa) tarafından kullanılmasını önlemek için, içe aktarma işlemi tarafından kilitleneceği zaman bir ER raporu tarafından otomatik olarak atanır.
    - **İçe Aktarıldı** - Dosya içe aktarma işlemi başarıyla tamamlanınca bir ER raporu tarafından otomatik olarak atanır. Bu durum, içe aktarılan dosyanın, yapılandırılan dosya kaynağından (SharePoint klasörü) silindiği anlamına gelir.
    - **Başarısız** - Dosya içe aktarma işlemi hatalarla veya özel durumlarla tamamlanınca bir ER raporu tarafından otomatik olarak atanır.
    - **Beklemede** - Bu formda kullanıcı tarafından el ile atanır. Bu durum, dosyanın şimdilik içe aktarılmayacağı anlamına gelir. Bu durum, bazı dosyaları içe aktarma işlemini ertelemek için kullanılabilir.

[![Seçili kaynaklar için ER dosya durumları sayfası](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>SharePoint dosyalarından içe veri aktarma
1. ER yapılandırmaları ağacını açın, **1099 Ödeme modeli**'ni seçin ve ER modeli bileşenleri listesini genişletin.
2. Seçili ER model yapılandırmasının model eşlemeleri listesini açmak için model eşlemenin adını seçin.

[![Seçili kaynaklar için ER dosya durumları sayfası](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Seçili model eşlemeyi çalıştırmak için **Çalıştır**'ı seçin. ER biçimi için dosya kaynaklarını siz yapılandırdığınız için, **Dosya kaynağı** seçeneğinin ayarını gereksiniminize göre değiştirebilirsiniz. Bu seçeneğin ayarını korursanız, .xslx dosyaları, yapılandırılmış kaynaklardan (bu örnekte SharePoint klasörleri) içe aktarılır.

    Bu örnekte tek bir dosya içe aktarıyorsunuz. Ancak birden çok dosya varsa, bu dosyalar SharePoint klasörüne eklendikleri sırayla içe aktarma işlemine seçilir. Her ER biçimi çalıştırılışında, seçilen dosyalardan biri içe aktarılır.

[![ER model eşlemesini çalıştırma](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Model eşleme, toplu iş modunda müdahalesiz çalıştırılabilir. Bu durumda, bu ER biçimi bir toplu iş tarafından her çalıştırıldığında, yapılandırılan dosya kaynaklarından tek bir dosya içe aktarılır. Bu toplu çalışmasını uygulamak için aşağıdaki kodu kullanın.

    ```
    ERObjectsFactory::createMappingDestinationRunByImportFormatMappingId().run()
    ```

    SharePoint klasöründen bir dosya başarıyla içe aktarıldığı zaman o klasörden silinir.

5. Fiş kodunu (**V-00001** vb.) girin ve **Tamam**'ı seçin.

[![ER model eşlemesini çalıştırma](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. **Kaynaklar için dosya durumları** sayfasında **Yenile**'yi seçerek sayfayı yenileyin.

[![Seçili kaynaklar için ER dosya durumları sayfası](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. **Dosyalar** bölümünde, dosyalar listesini inceleyin. **İçe aktarma biçimi için kaynaklar günlüğü** bölümü, Excel dosyası içe aktarma geçmişini verir. Bu dosya başarıyla içe aktarıldığı için SharePoint klasöründe **Silindi** olarak işaretlenir.
8. **Dosya içe aktarma kaynağı (ana)** SharePoint klasörünü inceleyin. Başarıyla içe aktarılan Excel dosyaları bu klasörden silinmiştir.
9. Finance and Operations'ta, **Borç hesapları** \> **Periyodik görevler** \> **Vergi 1099** \> **1099 formlarına ilişkin satıcı kapatması**'nı seçin.
10. **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına ilgili değerleri girin. Bunun ardından **El ile 1099 hareketleri**.

    SharePoint'te **V-00001** kodlu fiş için Excel dosyasından içe aktarılan satıcı hareketleri sayfada gösterilir.

[![1099 satıcı hareketleri sayfası](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Excel dosyasını içe aktarmaya hazırlama
1. Daha önce kullandığınız Excel dosyasını açın. Satır 3 sütun 1'e, uygulamada bulunmayan bir satıcı kodu ekleyin. Satıra yanlış bir satıcı bilgisi ekleyin.

[![SharePoint'ten içe aktarmada kullanılacak Microsoft Excel dosyası örneği](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Satıcı hareketlerini içeren güncelleştirilmiş Excel dosyasını **Dosya içe aktarma kaynağı (ana)** SharePoint klasörüne yükleyin.
3. Finance and Operations'ta, ER yapılandırmaları ağacını açın,**1099 Ödeme modeli**'ni seçin ve ER modeli bileşenleri listesini genişletin.
4. İçe aktarma işlemi sırasında yanlış satıcı kodunun hata olarak değerlendirilmesi için, model eşlemenin adını seçerek model eşlemeyi güncelleştirin.
5. **Tasarımcı**’yı seçin.
6. **Doğrulamalar** sekmesinde, içe aktarılan satıcı hesabının uygulamada var olup olmadığını değerlendirmek amacıyla yapılandırılmış doğrulama kuralı için, doğrulama sonrası eylemi değiştirmeniz gerekir. **Doğrulama sonrası eylem** alanının değerini **Yürütmeyi durdur** olarak güncelleştirin, değişikliklerinizi kaydedin ve sayfayı kapatın.

[![ER model eşleme tasarımcısı sayfası](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Değişikliklerinizi kaydedin ve ER model eşleme tasarımcısını kapatın.
8. Değiştirilen ER model eşlemesini çalıştırmak için **Çalıştır**'ı seçin.
9. Fiş kodunu (**V-00002** vb.) girin ve **Tamam**'ı seçin.

    Bilgi günlüğünde, SharePoint klasöründe kalan dosyanın yanlış satıcı hesabı içerdiği ve içe aktarılamayacağını bildiriminin bulunduğuna dikkat edin.

[![ER model eşlemesini çalıştırma](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. **Kaynak için dosya durumları** sayfasında **Yenile**'yi seçin ve ardından **Dosyalar** bölümünde, dosyalar listesini inceleyin.

[![Seçili kaynaklar için ER dosya durumları sayfası](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

**İçe aktarma biçimi için kaynaklar günlüğü** bölümü, içe aktarma işleminin başarısız olduğunu ve dosyanın hala SharePoint klasöründe olduğunu (**Silindi** onay kutusu işaretli değildir) gösterir. Doğru satıcı kodunu ekleyerek bu dosyayı SharePoint'te düzeltir ve ardından **İçe aktarma biçimi için kaynaklar günlüğü** bölümünde **Başarısız** olan dosya durumunu **Hazır** olarak değiştirirseniz dosyayı yeniden içe aktarabilirsiniz.

11. **Dosya içe aktarma kaynağı (ana)** SharePoint klasörünü inceleyin. İçe aktarılmamış Excel dosyasının hala bu klasörde olduğuna dikkat edin.
12. Finance and Operations'ta, **Borç hesapları** \> **Periyodik görevler** \> **Vergi 1099** \> **1099 formlarına ilişkin satıcı kapatması**'nı seçin, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına uygun değerleri girin ve **El ile 1099 hareketleri**'ni seçin.

    Yalnızca V-00001 kodlu fişe ilişkin hareketler kullanılabilir. Excel dosyasında son içe aktarılan harekette hata bulunsa bile V-00002 kodlu fişe ilişkin hareketler kullanılamaz.

