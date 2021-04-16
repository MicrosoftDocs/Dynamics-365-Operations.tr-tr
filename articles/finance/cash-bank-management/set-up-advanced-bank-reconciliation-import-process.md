---
title: Gelişmiş banka mutabakatı içe aktarma sürecini ayarlama
description: Gelişmiş banka mutabakatı özelliği, elektronik banka ekstrelerini içe aktarmanıza ve bunların Microsoft Dynamics 365 Finance'teki banka hareketleriyle otomatik olarak mutabakat sağlamasına izin verir. Bu makalede banka ekstreleriniz için içe aktarma işlevinin nasıl ayarlanacağı açıklanmaktadır.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22d173f6ced2af3e8023bd40f70ca70728c3a0a7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834992"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Gelişmiş banka mutabakatı içe aktarma sürecini ayarlama

[!include [banner](../includes/banner.md)]

Gelişmiş banka mutabakatı özelliği, elektronik banka ekstrelerini içe aktarmanıza ve bunların Dynamics 365 Finance'teki banka hareketleriyle otomatik olarak mutabakat sağlamasına izin verir. Bu makalede banka ekstreleriniz için içe aktarma işlevinin nasıl ayarlanacağı açıklanmaktadır. 

Banka ekstresi içe aktarma işleminin kurulumu elektronik banka ekstrenizin biçimine bağlı olarak değişir. Finance kullanıma hazır üç banka ekstresi biçimini destekler: ISO20022, MT940 ve BAI2

## <a name="set-time-zone-preference"></a>Saat dilimi tercihini belirleme
Banka ekstresi içe aktarma ayarlarını konfigüre ettiğiniz zaman, içe aktarılacak banka ekstresi dosyalarındaki tarih-saat verilerinin saat dilimini göz önünde bulundurmanız önemli olabilir. Herhangi bir tarih ve saat değerinin zaten Eşgüdümlü Evrensel Saat (UTC) olduğu varsayıldığından, verileri içe aktardığınızda hiçbir saat dilimi dönüştürmesi uygulanmaz. 

Verileri içe aktarırken kullanılacak bir saat dilimi belirtmek için kullanılabilecek bir seçenek vardır. Bu seçenek her **Kaynak veri biçimi ayrıntıları** sayfasındaki **Saat dilimi tercihi** alanında kullanılabilir (**Veri yönetimi çalışma alanı > Veri kaynaklarını yapılandırın > Veri biçimi seçin > Bölgesel ayarlar** hızlı sekmesi). Girdiğiniz bu saat dilimi tercihi, o kaynak veri biçimini kullanan tüm içe aktarma işlemleri için geçerli olur. Birden çok saat diliminden veri içe aktarmak için gereken sayıda veri kaynağı biçimi oluşturabilirsiniz.  

Bu saat dilimi bir kullanıcının veya şirketin saat dilimiyle aynı olmayabileceği için, tarih ve saat verilerinin hangi saat dilimini kullandığını mutlaka netleştirin. Saat dilimi tercihini ayarlarken aşağıdaki hususları göz önünde bulundurmanızı öneririz. 

 - Saat dilimi tercihi, o kaynak veri biçimini kullanan tüm içe aktarma işlemleri için geçerli olur. Birden çok saat diliminden veri içe aktarma işlemini yürütmek için gereken sayıda veri kaynağı biçimi oluşturabilirsiniz. 
 
 - Saat dilimi tercihi, içe aktarma dosyasındaki tarih ve saat verilerinin yerel saat dilimi olmalıdır. 
 
 - Tarih ve saat verilerinin saat dilimi, kullanıcının veya şirketin saat dilimiyle aynı olmayabilir.
 
 - Kullanıcılar **Kullanıcı seçeneklerini** kullanarak kendi saat dilimlerini ayarlayabilirler.

Banka ekstrelerini içe aktardığınız zaman aşağıdaki eylemlerin olası tarih ve saat çakışmalarını en aza indirmeye yardımcı olabileceğini unutmayın. 

 - Ekstreleri zaten içe aktarılmış olan banka hesapları için saat dilimi tercihlerini değiştirmekten kaçının. Saat dilimi tercihinin değiştirilmesi, varolan ekstrelerle ilgili yeni ekstrelerin sıralamasını saat dilimi ayarından dolayı olumsuz etkileyebilir. 
 
 - Seçili veri kaynağı biçimini kullanan tüm içe aktarma işlemlerini inceleyin. Biçim için belirtilen saat dilimi tercihi, bu biçimi kullanan tüm içe aktarma projelerine uygulanır. Saat dilimi tercihinin bu biçimi kullanan tüm içe aktarma projeleri için uygun olduğunu doğrulayın.

## <a name="sample-files"></a>Örnek dosyalar
Bu üç biçimin tümü için, elektronik banka ekstresini orijinal biçimden Finance uygulamasının kullanabileceği bir biçime çeviren dosyalara sahip olmanız gerekir. Gerekli kaynak dosyaları Microsoft Visual Studio içindeki Uygulama Gezgini'nde **Kaynaklar** düğümü altında bulabilirsiniz. Dosyaları bulduktan sonra kurulum sürecinde daha kolay bir şekilde yükleyebilmeniz için dosyaları bilinen tek bir konuma kopyalayın.

| Kaynak adı                                           | Dosya adı                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_to\_Composite\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Banka ekstresi biçimleri ve teknik düzenlerine örnekler
Aşağıda gelişmiş banka mutabakatını içe aktarma dosyası teknik düzen tanımları ve ilişkili üç banka ekstresi örnek dosyasına örnekler bulunmaktadır: [İçe aktarma dosyası örnekleri](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Teknik düzen tanımı                             | Banka ekstresi örnek dosya          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>ISO20022 banka ekstrelerinin içe aktarma işlemini ayarlama
İlk olarak, veri varlık çerçevesini kullanarak ISO20022 banka ekstreleri için banka ekstresi biçimi işlem grubu tanımlamanız gerekir.

1.  **Çalışma alanları** &gt; **Veri yönetimi**'ne gidin.
2.  **İçe aktar**'a tıklayın.
3.  Biçim için bir ad girin, örneğin **ISO20022**.
4.  **Kaynak veri biçimi** alanını **XML-Element** olarak ayarlayın.
5.  **Varlık adı** alanını **Banka ekstreleri** olarak ayarlayın.
6.  İçe aktarılan dosyaları karşıya yüklemek için **Karşıya yükle** öğesine tıklayın ve ardından daha önce kaydettiğiniz **SampleBankCompositeEntity.xml** dosyasını seçmek üzere dosya konumuna gidin.
7.  Banka ekstreleri varlığı karşıya yüklendikten ve eşleştirme işlemi tamamlandıktan sonra varlığın **Eşlemeyi görüntüle** eylemine tıklayın.
8.  Banka ekstreleri varlığı dört farklı varlıktan oluşan birleşik bir varlıktır. Listeden **BankStatementDocumentEntity** öğesini seçin ve **Eşlemeyi görüntüle** eylemine tıklayın.
9.  **Dönüşümler** sekmesinde **Yeni** öğesine tıklayın.
10. Sıra numarası 1 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **ISO20022XML-to-Reconciliation.xslt** dosyasını seçin. **Not:** Dönüşüm dosyaları standart biçim için oluşturulmuştur. Bankalar genellikle bu biçimden ayrıldıkları için dönüşüm dosyasını banka ekstresi biçiminizle eşleşecek şekilde güncelleştirmeniz gerekebilir. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. **Yeni**'ye tıklayın.
12. Sıra numarası 2 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **BankReconciliation-to-Composite.xslt** dosyasını seçin.
13. **Dönüşümleri uygula**'ya tıklayın.

Biçim işlem grubu ayarlandıktan sonraki adım ISO20022 banka ekstreleri için banka ekstresi biçim kurallarını tanımlamaktır.

1.  **Nakit ve banka yönetimi** &gt; **Kurulum** &gt; **Gelişmiş banka mutabakatı kurulumu** &gt; **Banka ekstresi biçimi**'ne gidin.
2.  **Yeni**'ye tıklayın.
3.  Bir ekstre biçimi belirtin, örneğin **ISO20022**.
4.  Biçim için bir ad girin.
5.  **İşlem grubu** alanını daha önce tanımladığınız grup olarak ayarlayın, örneğin **ISO20022**.
6.  **XML dosyası** onay kutusunu seçin.

Son adım Gelişmiş banka mutabakatını etkinleştirmek ve banka hesabındaki ekstre biçimini ayarlamaktır.

1.  **Nakit ve banka yönetimi** &gt; **Banka hesapları**'na gidin.
2.  Banka hesabını seçin ve ayrıntılarını görüntülemek için hesabı açın.
3.  **Mutabakat** sekmesinde, **Gelişmiş banka mutabakatı** seçeneğini **Evet** olarak ayarlayın.
4.  **Ekstre biçimi** alanını daha önce oluşturduğunuz biçime ayarlayın, örneğin **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>MT940 banka ekstrelerinin içe aktarma işlemini ayarlama
İlk olarak, veri varlık çerçevesini kullanarak MT940 banka ekstreleri için banka ekstresi biçimi işlem grubu tanımlamanız gerekir.

1.  **Çalışma alanları** &gt; **Veri yönetimi**'ne gidin.
2.  **İçe aktar**'a tıklayın.
3.  Biçim için bir ad girin, örneğin **MT940**.
4.  **Kaynak veri biçimi** alanını **XML-Element** olarak ayarlayın.
5.  **Varlık adı** alanını **Banka ekstreleri** olarak ayarlayın.
6.  İçe aktarılan dosyaları karşıya yüklemek için **Karşıya yükle** öğesine tıklayın ve ardından daha önce kaydettiğiniz **SampleBankCompositeEntity.xml** dosyasını seçmek üzere dosya konumuna gidin.
7.  Banka ekstreleri varlığı karşıya yüklendikten ve eşleştirme işlemi tamamlandıktan sonra varlığın **Eşlemeyi görüntüle** eylemine tıklayın.
8.  Banka ekstreleri varlığı dört farklı varlıktan oluşan birleşik bir varlıktır. Listeden **BankStatementDocumentEntity** öğesini seçin ve **Eşlemeyi görüntüle** eylemine tıklayın.
9.  **Dönüşümler** sekmesinde **Yeni** öğesine tıklayın.
10. Sıra numarası 1 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **MT940TXT-to-MT940XML.xslt** dosyasını seçin.
11. **Yeni**'yi tıklatın.
12. Sıra numarası 2 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **MT940XML-to-Reconciliation.xslt** dosyasını seçin. **Not:** Dönüşüm dosyaları standart biçim için oluşturulmuştur. Bankalar genellikle bu biçimden ayrıldıkları için dönüşüm dosyasını banka ekstresi biçiminizle eşleşecek şekilde güncelleştirmeniz gerekebilir. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. **Yeni**'ye tıklayın.
14. Sıra numarası 3 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **BankReconciliation-to-Composite.xslt** dosyasını seçin.
15. **Dönüşümleri uygula**'ya tıklayın.

Biçim işlem grubu ayarlandıktan sonraki adım MT940 banka ekstreleri için banka ekstresi biçim kurallarını tanımlamaktır.

1.  **Nakit ve banka yönetimi** &gt; **Kurulum** &gt; **Gelişmiş banka mutabakatı kurulumu** &gt; **Banka ekstresi biçimi**'ne gidin.
2.  **Yeni**'ye tıklayın.
3.  Bir ekstre biçimi belirtin, örneğin **MT940**.
4.  Biçim için bir ad girin.
5.  **İşlem grubu** alanını daha önce tanımladığınız grup olarak ayarlayın, örneğin **MT940**.
6.  **Dosya türü** alanını **txt** olarak ayarlayın.

Son adım Gelişmiş banka mutabakatını etkinleştirmek ve banka hesabındaki ekstre biçimini ayarlamaktır.

1.  **Nakit ve banka yönetimi** &gt; **Banka hesapları**'na gidin.
2.  Banka hesabını seçin ve ayrıntılarını görüntülemek için hesabı açın.
3.  **Mutabakat** sekmesinde, **Gelişmiş banka mutabakatı** seçeneğini **Evet** olarak ayarlayın.
4.  Seçiminizi onaylamanız ve Gelişmiş banka mutabakatı seçeneğini etkinleştirmeniz istendiğinde **Tamam**'a tıklayın.
5.  **Ekstre biçimi** alanını daha önce oluşturduğunuz biçime ayarlayın, örneğin **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>BAI2 banka ekstrelerinin içe aktarma işlemini ayarlama
İlk olarak, veri varlık çerçevesini kullanarak BAI2 banka ekstreleri için banka ekstresi biçimi işlem grubu tanımlamanız gerekir.

1.  **Çalışma alanları** &gt; **Veri yönetimi**'ne gidin.
2.  **İçe aktar**'a tıklayın.
3.  Biçim için bir ad girin, örneğin **BAI2**.
4.  **Kaynak veri biçimi** alanını **XML-Element** olarak ayarlayın.
5.  **Varlık adı** alanını **Banka ekstreleri** olarak ayarlayın.
6.  İçe aktarılan dosyaları karşıya yüklemek için **Karşıya yükle** öğesine tıklayın ve ardından daha önce kaydettiğiniz **SampleBankCompositeEntity.xml** dosyasını seçmek üzere dosya konumuna gidin.
7.  Banka ekstreleri varlığı karşıya yüklendikten ve eşleştirme işlemi tamamlandıktan sonra varlığın **Eşlemeyi görüntüle** eylemine tıklayın.
8.  Banka ekstreleri varlığı dört farklı varlıktan oluşan birleşik bir varlıktır. Listeden **BankStatementDocumentEntity** öğesini seçin ve **Eşlemeyi görüntüle** eylemine tıklayın.
9.  **Dönüşümler** sekmesinde **Yeni** öğesine tıklayın.
10. Sıra numarası 1 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **BAI2CSV-to-BAI2XML.xslt** dosyasını seçin.
11. **Yeni**'yi tıklatın.
12. Sıra numarası 2 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **BAI2XML-to-Reconciliation.xslt** dosyasını seçin. **Not:** Dönüşüm dosyaları standart biçim için oluşturulmuştur. Bankalar genellikle bu biçimden ayrıldıkları için dönüşüm dosyasını banka ekstresi biçiminizle eşleşecek şekilde güncelleştirmeniz gerekebilir. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. **Yeni**'ye tıklayın.
14. Sıra numarası 3 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **BankReconciliation-to-Composite.xslt** dosyasını seçin.
15. **Dönüşümleri uygula**'ya tıklayın.

Biçim işlem grubu ayarlandıktan sonraki adım BAI2 banka ekstreleri için banka ekstresi biçim kurallarını tanımlamaktır.

1.  **Nakit ve banka yönetimi** &gt; **Kurulum** &gt; **Gelişmiş banka mutabakatı kurulumu** &gt; **Banka ekstresi biçimi**'ne gidin.
2.  **Yeni**'ye tıklayın.
3.  Bir ekstre biçimi belirtin, örneğin **BAI2**.
4.  Biçim için bir ad girin.
5.  **İşlem grubu** alanını daha önce tanımladığınız grup olarak ayarlayın, örneğin **BAI2**.
6.  **Dosya türü** alanını **txt** olarak ayarlayın.

Son adım Gelişmiş banka mutabakatını etkinleştirmek ve banka hesabındaki ekstre biçimini ayarlamaktır.

1.  **Nakit ve banka yönetimi** &gt; **Banka hesapları**'na gidin.
2.  Banka hesabını seçin ve ayrıntılarını görüntülemek için hesabı açın.
3.  **Mutabakat** sekmesinde, **Gelişmiş banka mutabakatı** seçeneğini **Evet** olarak ayarlayın.
4.  Seçiminizi onaylamanız ve Gelişmiş banka mutabakatı seçeneğini etkinleştirmeniz istendiğinde **Tamam**'a tıklayın.
5.  **Ekstre biçimi** alanını daha önce oluşturduğunuz biçime ayarlayın, örneğin **BAI2**.

## <a name="test-the-bank-statement-import"></a>Banka ekstresi içe aktarma sınaması
Son adım banka ekstrenizi içe aktarıp aktaramadığınızı sınamaktır.

1.  **Nakit ve banka yönetimi** &gt; **Banka hesapları**'na gidin.
2.  Gelişmiş banka mutabakatı işlevinin etkinleştirildiği banka hesabını seçin.
3.  **Mutabakat** sekmesinde **Banka ekstreleri** seçeneğine tıklayın.
4.  **Banka ekstresi** sayfasında **Ekstreyi içe aktar** öğesine tıklayın.
5.  **Banka hesabı** alanını seçili banka hesabı olacak şekilde ayarlayın. **Ekstre biçimi** alanı banka hesabının ayarına göre otomatik olarak ayarlanır.
6.  **Gözat**'a tıklayın ve elektronik banka ekstresi dosyanızı seçin.
7.  **Karşıya yükle** seçeneğini tıklatın.
8.  **Tamam** düğmesini tıklatın.

İçe aktarma işlemi başarılı olduğunda ekstrenizin içe aktarıldığını belirten bir ileti alırsınız. İçe aktarma işlemi başarılı olmazsa, **Veri yönetimi** çalışma alanındaki **İş geçmişi** bölümünde işi bulun. İşin **Yürütme ayrıntıları**'na tıklayıp **Yürütme özeti** sayfasını açın ve içe aktarma hatalarını görüntülemek için **Yürütme günlüğünü görüntüle** seçeneğine tıklayın.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
