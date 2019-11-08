---
title: SharePoint'ten veri aktarımını yapılandırma
description: Bu konu, Microsoft SharePoint'ten nasıl veri aktarılacağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 11/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: b40f9a5677fd5375d7a19a75400d4305a8850392
ms.sourcegitcommit: 399e861ca6f2bdcd4fe84d89fedc04b60d9f43e6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/07/2019
ms.locfileid: "2564949"
---
# <a name="configure-data-import-from-sharepoint"></a>SharePoint'ten veri aktarımını yapılandırma

[!include[banner](../includes/banner.md)]

Elektronik raporlama (ER) çerçevesini kullanarak bir gelen dosyadan verileri içe aktarmak için, içe aktarmayı destekleyen bir ER biçimi yapılandırmanız ve ardından bu biçimi veri kaynağı olarak kullanan **Hedefe** türünün bir model eşlemesini çalıştırmanız gerekir. Verileri içe aktarmak için, içe aktarmak istediğiniz dosyaya gitmeniz gerekir. Kullanıcı gelen dosyayı el ile seçebilir. Microsoft SharePoint'ten veri içe aktarmayı destekleyen yeni ER özelliği sayesinde bu işlem müdahalesiz yürüyecek şekilde yapılandırılabilir. Microsoft SharePoint klasörlerinde depolanan dosyalardan veri içe aktarmak için ER yapılandırmalarını kullanabilirsiniz. Bu konu SharePoint'den içe aktarma işleminin nasıl tamamlanacağını açıklar. Örneklerde iş verisi olarak satıcı hareketleri kullanılmaktadır.

## <a name="prerequisites"></a>Önkoşullar
Bu konudaki örnekleri tamamlamak için şu erişimlere sahip olmanız gerekir:

- Aşağıdaki rollerden birine erişim:

    - Elektronik raporlama geliştirici
    - Elektronik raporlama işlev danışmanı
    - Sistem yöneticisi

- Uygulama ile kullanılmak için yapılandırılmış Microsoft SharePoint Server örneğine erişim.
- 1099 ödemeleri için ER biçimi ve model yapılandırmaları.

### <a name="create-required-er-configurations"></a>Gerekli ER yapılandırmalarını oluşturma
**7.5.4.3 BT hizmeti/çözüm bileşenleri Al/Geliştir (10677)** iş sürecinin parçası olan **Bir Microsoft Excel dosyasından ER veri içe aktarma** görev kılavuzlarını oynatın. Bu görev kılavuzları, Microsoft Excel dosyalarından satıcı hareketlerini etkileşimli olarak içe aktarmak için ER yapılandırmalarını tasarlama ve kullanma sürecinde size yol gösterir. Daha fazla bilgi için bkz. [Microsoft Excel biçiminde gelen belgeleri ayrıştırma](parse-incoming-documents-excel.md). Görev Kılavuzlarını tamamladıktan sonra aşağıdaki kuruluma sahip olursunuz.

#### <a name="er-configurations"></a>ER yapılandırmaları

- ER model yapılandırması, **1099 Ödemeleri modeli**
- ER biçim yapılandırması, **Satıcıların hareketlerini Excel'den içe aktarma biçimi**

![SharePoint'ten veri içe aktarmak için ER yapılandırmaları](./media/GERImportFromSharePoint-01-Configurations.PNG)

#### <a name="sample-of-the-incoming-file-for-data-import"></a>Veri içe aktarmada kullanılacak gelen dosya örneği

- Excel dosyası **1099import-data.xlsx**: Aktarılması gereken satıcı hareketlerinin bulunduğu dosya.

![SharePoint'ten içe aktarma için örnek Microsoft Excel dosyası](./media/GERImportFromSharePoint-02-Excel.PNG)
    
> [!NOTE]
> Satıcı hareketlerini içe aktarmak için kullanılan biçim, varsayılan model eşleme olarak seçilidir. Bu nedenle, bir model eşlemesi çalıştırıyorsanız, **1099 Ödemeleri modeli** çalıştırıyorsanız ve söz konusu model eşleme **Hedefe** türündeyse, model eşleme, harici dosyalardan içe veri aktarmak için bu biçimi çalıştırır. Ardından bu verileri, uygulama tablolarını güncelleştirmek için kullanır.

## <a name="configure-access-to-sharepoint-for-file-storage"></a>Dosya depolama için SharePoint erişimini yapılandırma
Bir SharePoint konumuna elektronik rapor dosyaları depolamak için geçerli şirket tarafından kullanılacak olan SharePoint sunucusu örneği erişimini yapılandırmanız gerekir. Bu örnekte şirket USMF'dir. Yönergeler için bkz: [SharePoint depolama yapılandırma](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).

1. Şuradaki adımları tamamlayın [SharePoint depolamayı yapılandırma](../../fin-ops/organization-administration/configure-document-management.md#configure-sharepoint-storage).
2. Yapılandırılmış SharePoint sitesini açın.
3. Gelen elektronik raporlama dosyalarının depolanabileceği aşağıdaki klasörleri oluşturun:

     - Dosyalar içe aktarma kaynağı (ana) (Örnek aşağıdaki ekran görüntüsünde gösterilmektedir)
     - Dosya içe aktarma kaynağı (alternatif)

    ![Dosya içe aktarma kaynağı (ana)](./media/GERImportFromSharePoint-04-SharePointFolder1.png)

4. (İsteğe bağlı) Dosyaların içe aktarmadan depolanabileceği klasörleri oluşturun. 

    - Dosyalar arşiv klasörü - Bu klasör, başarıyla içe aktarılan klasörler için olacaktır.
    - Dosyalar uyarı klasörü - Bu klasör, bir uyarıyla içe aktarılan dosyalar için olacaktır.
    - Dosya hata klasörü - Bu klasör, içe aktarması başarısız olan dosyalar için olacaktır.

4. **Kuruluş yönetimi > Belge yönetimi > Belge türleri**'ne gidin.
5. Oluşturmuş olduğunuz SharePoint klasörlerine erişimde kullanılacak aşağıdaki belge türlerini oluşturun. Yönergeler için bkz: [Belge türlerini yapılandırma](../../fin-ops/organization-administration/configure-document-management.md#configure-document-types).

|Belge türü       | Grup              | Yer      | SharePoint klasörü      |
|--------------------|--------------------|---------------|------------------------|
|SP Ana             |Dosya                |SharePoint     |Dosya içe aktarma kaynağı (ana)|
|SP Alternatif             |Dosya                |SharePoint     |Dosya içe aktarma kaynağı (alternatif)|
|SP Arşivi:             |Dosya                |SharePoint     |Dosyalar arşivi klasörü|
|SP Uyarı             |Dosya                |SharePoint     |Dosyalar uyarı klasörü|
|SP Hatası             |Dosya                |SharePoint     |Dosyalar hata klasörü|

![SharePoint ayarı - yeni belge türü](./media/GERImportFromSharePoint-06-SharePointDocumentTypesSetup.png)

## <a name="configure-er-sources-for-the-er-format"></a>ER biçimi için ER kaynaklarını yapılandırma
1. **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Elektronik raporlama kaynağı**'na tıklayın.
2. **Elektronik raporlama kaynağı** sayfasında, yapılandırılmış ER biçimini kullanarak, veri içe aktarma işlemi için kullanılacak kaynak dosyalarını yapılandırın.
3. Yalnızca .xlsx uzantılı dosyaların içe aktarılması için bir dosya adı maskesi tanımlayın. Dosya adı maskesi isteğe bağlıdır ve ancak tanımlandığı zaman kullanılır. Her bir ER biçimi için yalnızca bir maske tanımlayabilirsiniz.
4. İçe aktarılma için çok fazla dosya varsa ve sıralaması önemli değilse, **Dosyaları içe aktarmadan önce sırala**'yı **Sıralama** olarak değiştirin.
5. Daha önce oluşturduğunuz tüm SharePoint klasörlerini seçin.

    [![ER dosyaları kaynak ayarı](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)](./media/GERImportFromSharePoint-07-FormatSourceSetup.PNG)

> [!NOTE]
> - ER *kaynağı* her bir uygulama şirketi için ayrı ayrı tanımlanır. Bunun aksine, ER *yapılandırmaları* şirketler arasında paylaşılır.
> - Bir ER biçimine ait bir ER kaynağı ayarını sildiğiniz zaman, tüm bağlantılı dosya durumları da (aşağıya bakın) onay ile silinir.

## <a name="review-the-files-states-for-the-er-format"></a>ER biçimi için dosya durumlarını inceleme
1. Mevcut ER biçimi için yapılandırılmış dosya kaynaklarının içeriğini incelemek için **Elektronik raporlama kaynağı** sayfasında **Kaynaklar için dosya durumları**'nı seçin.
2. **Dosyalar** bölümünde, dosyalar listesini inceleyin. Bu listede aşağıdakiler sunulur:

    - Dosya adı maskesine göre (bir dosya adı maskesi tanımlandıysa) uygun ve veri içe aktarmaya hazır kaynak dosyalar. Bu dosyalar için, **İçe aktarma için kaynaklar günlüğü** bölümü boştur.
    - Daha önce içe aktarılan dosyalar. Bu dosyaların her biri için, **İçe aktarma biçimi için kaynaklar günlüğü** bölümünde, bu dosyanın içe aktarma geçmişini inceleyebilirsiniz.

**Kaynaklar için dosya durumları** sayfasını **Kuruluş yönetimi** \> **Elektronik raporlama** \> **Kaynaklar için dosya durumları**'nı seçerek de açabilirsiniz. Bu durumda, sayfada, oturum açtığınız şirkette dosya kaynaklarının yapılandırıldığı tüm ER biçimlerinin dosya kaynakları hakkında bilgiler verilir.

## <a name="import-data-from-excel-files-that-are-in-a-sharepoint-folder"></a>Bir SharePoint klasöründeki Excel dosyalarından verileri içe aktarma
1. SharePoint'te, satıcı hareketlerini içeren Microsoft Excel, **dosyasını 1099import-data.xlsx**, daha önce oluşturduğunuz **Dosya içe aktarma kaynağı (ana)** SharePoint klasörüne yükleyin.

    [![SharePoint içeriği – İçe aktarma için Microsoft Excel dosyası](./media/GERImportFromSharePoint-08-UploadFile.png)](./media/GERImportFromSharePoint-08-UploadFile.png)

2. **Kaynaklar için dosya durumları** sayfasında **Yenile**'yi seçerek sayfayı yenileyin. SharePoint'e yüklenen Excel dosyasının bu sayfadaki **Hazır** durumda görüneceğine dikkat edin. Şu anda aşağıdaki durumlar desteklenmektedir:

    - **Hazır** - SharePoint klasöründeki her yeni dosyaya otomatik olarak atanır. Bu durum, dosyanın içe aktarılmaya hazır olduğu anlamına gelir.
    - **İçe Aktarılıyor**: Dosya, başka işlemler (çok sayıda işlem aynı anda çalışıyorsa) tarafından kullanılmasını önlemek için içe aktarma işlemi tarafından kilitleneceği zaman bir ER raporu tarafından otomatik olarak atanır.
    - **İçe Aktarıldı**: Dosyayı içeri aktarma işlemi başarıyla tamamlandığında bir ER raporu tarafından otomatik olarak atanır. Bu durum, içe aktarılan dosyanın, yapılandırılan dosya kaynağından (SharePoint klasörü) silindiği anlamına gelir.
    - **Başarısız**: Dosyayı içeri aktarma işlemi hatalarla veya özel durumlarla tamamlandığında ER raporu tarafından otomatik olarak atanır.
    - **Beklemede**: Bu sayfada kullanıcı tarafından el ile atanır. Bu durum, dosyanın şimdilik içe aktarılmayacağı anlamına gelir. Bu durum, bazı dosyaları içe aktarma işlemini ertelemek için kullanılabilir.

    [![Seçili kaynaklar için ER dosya durumları sayfası](./media/GERImportFromSharePoint-09-FileStatesForm.png)](./media/GERImportFromSharePoint-09-FileStatesForm.png)

## <a name="import-data-from-sharepoint-files"></a>SharePoint dosyalardan içe aktarma
1. ER yapılandırmaları ağacını açın, **1099 Ödeme modeli**'ni seçin ve ER modeli bileşenleri listesini genişletin.
2. Seçili ER model yapılandırmasının model eşlemeleri listesini açmak için model eşlemenin adını seçin.

    [![Seçili kaynaklar için ER dosya durumları sayfası](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)](./media/GERImportFromSharePoint-10-SelectModelMapping.PNG)

3. Seçili model eşlemeyi çalıştırmak için **Çalıştır**'ı seçin. ER biçimi için dosya kaynaklarını siz yapılandırdığınız için, **Dosya kaynağı** seçeneğinin ayarını gerekli olduğu gibi değiştirebilirsiniz. Bu seçeneğin ayarını korursanız, .xslx dosyaları, yapılandırılmış kaynaklardan (bu örnekte SharePoint klasörleri) içe aktarılır.

    Bu örnekte tek bir dosya içe aktarıyorsunuz. Ancak birden çok dosya varsa, bu dosyalar SharePoint klasörüne eklendikleri sırayla içe aktarma işlemine seçilir. Her ER biçimi çalıştırılışında, seçilen dosyalardan biri içe aktarılır.

    [![ER model eşlemesini çalıştırma](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)](./media/GERImportFromSharePoint-11-RunModelMapping.PNG)

4. Model eşleme, toplu iş modunda müdahalesiz çalıştırılabilir. Bu durumda, bu ER biçimi bir toplu iş tarafından her çalıştırıldığında, yapılandırılan dosya kaynaklarından tek bir dosya içe aktarılır.

    Bir dosya SharePoint klasöründen başarıyla içe aktarıldıktan sonra, bu klasörden silinir ve başarıyla içe aktarılan veya uyarılar ile içe aktarılan dosyalar klasörüne taşınır. Aksi taktirde başarısız dosyalar klasörüne taşınır veya bu ayarlanmadıysa, bu klasörde kalır. 

5. Fiş kodunu (**V-00001** vb.) girin ve **Tamam**'ı seçin.

    [![ER model eşlemesini çalıştırma](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-12-ModelMappingRunFinished.PNG)

6. **Kaynaklar için dosya durumları** sayfasında **Yenile**'yi seçerek sayfayı yenileyin.

    [![Seçili kaynaklar için ER dosya durumları sayfası](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)](./media/GERImportFromSharePoint-13-FileStatesForm.PNG)

7. **Dosyalar** bölümünde, dosyalar listesini inceleyin. **İçe aktarma biçimi için kaynaklar günlüğü** bölümü, Excel dosyası içe aktarma geçmişini verir. Bu dosya başarıyla içe aktarıldığı için SharePoint klasöründe **Silindi** olarak işaretlenir.
8. **Dosya içe aktarma kaynağı (ana)** SharePoint klasörünü inceleyin. Başarıyla içe aktarılan Excel dosyaları bu klasörden silinmiştir.
9. **Borç hesapları** \> **Periyodik görevler** \> **Vergi 1099** \> **1099 formlarına ilişkin satıcı kapatması**'na gidin.
10. **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına ilgili değerleri girin. Bunun ardından **El ile 1099 hareketleri**.

    SharePoint'te **V-00001** kodlu fiş için Excel dosyasından içe aktarılan satıcı hareketleri sayfada gösterilir.

    [![1099 satıcı hareketleri sayfası](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)](./media/GERImportFromSharePoint-14-ImportedTransactions.PNG)

## <a name="prepare-an-excel-file-for-import"></a>Excel dosyasını içe aktarmaya hazırlama
1. Daha önce kullandığınız Excel dosyasını açın. Satır 3 sütun 1'e, uygulamada bulunmayan bir satıcı kodu ekleyin. Satıra yanlış bir satıcı bilgisi ekleyin.

    [![SharePoint'ten içe aktarma için örnek Microsoft Excel dosyası](./media/GERImportFromSharePoint-15-Excel.PNG)](./media/GERImportFromSharePoint-15-Excel.PNG)

2. Satıcı hareketlerini içeren güncelleştirilmiş Excel dosyasını **Dosya içe aktarma kaynağı (ana)** SharePoint klasörüne yükleyin.
3. ER yapılandırmaları ağacını açın, **1099 Ödeme modeli**'ni seçin ve ER modeli bileşenleri listesini genişletin.
4. İçe aktarma işlemi sırasında yanlış satıcı kodunun hata olarak değerlendirilmesi için, model eşlemenin adını seçerek model eşlemeyi güncelleştirin.
5. **Tasarımcı**’yı seçin.
6. **Doğrulamalar** sekmesinde, içe aktarılan satıcı hesabının uygulamada var olup olmadığını değerlendirmek amacıyla yapılandırılmış doğrulama kuralı için, doğrulama sonrası eylemi değiştirmeniz gerekir. **Doğrulama sonrası eylem** alanının değerini **Yürütmeyi durdur** olarak güncelleştirin, değişikliklerinizi kaydedin ve sayfayı kapatın.

    [![ER model eşleme tasarımcısı sayfası](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)](./media/GERImportFromSharePoint-16-UpdateModelMapping.PNG)

7. Değişikliklerinizi kaydedin ve ER model eşleme tasarımcısını kapatın.
8. Değiştirilen ER model eşlemesini çalıştırmak için **Çalıştır**'ı seçin.
9. Fiş kodunu (**V-00002** vb.) girin ve **Tamam**'ı seçin.

    Bilgi günlüğünde, SharePoint klasöründe bir dosyanın yanlış satıcı hesabı içerdiği ve içe aktarılamayacağını bildiriminin bulunduğuna dikkat edin.

    [![ER model eşlemesini çalıştırma](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)](./media/GERImportFromSharePoint-17-ModelMappingRunFinished.PNG)

10. **Kaynak için dosya durumları** sayfasında **Yenile**'yi seçin ve ardından **Dosyalar** bölümünde, dosyalar listesini inceleyin.

    [![Seçili kaynaklar için ER dosya durumları sayfası](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)](./media/GERImportFromSharePoint-18-FileStatesForm.PNG)

   **İçe aktarma biçimi için kaynaklar günlüğü** bölümü, içe aktarma işleminin başarısız olduğunu ve dosyanın hala Dosya hatalı SharePoint klasöründe olduğunu (**Silindi** onay kutusu işaretli değildir) gösterir. SharePoint üzerinde bu dosyayı doğru satıcı kodunu ekleyerek düzeltirseniz ve sonra Dosya içe aktarma kaynak (ana) SharePoint klasörüne taşırsanız, dosyayı yeniden içe aktarabilirsiniz.

11. **Borç hesapları** \> **Periyodik görevler** \> **Vergi 1099** \> **1099 formlarına ilişkin satıcı kapatması**'nı seçin, **Başlangıç tarihi** ve **Bitiş tarihi** alanlarına uygun değerleri girin ve **El ile 1099 hareketleri**'ni seçin.

    Yalnızca V-00001 kodlu fişe ilişkin hareketler kullanılabilir. Excel dosyasında son içe aktarılan harekette hata bulunsa bile V-00002 kodlu fişe ilişkin hareketler kullanılamaz.
