---
title: "Gelişmiş banka mutabakatı içe aktarma sürecini ayarlama"
description: "Gelişmiş banka mutabakatı özelliği, elektronik banka ekstrelerini içe aktarmanıza ve bunların Microsoft Dynamics 365 for Finance and Operations Enterprise sürümündeki banka hareketleriyle otomatik olarak mutabakat sağlamasına izin verir. Bu makalede banka ekstreleriniz için içe aktarma işlevinin nasıl ayarlanacağı açıklanmaktadır."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4d7bb0fc5abedcce973632434a5cc174449cdc22
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Gelişmiş banka mutabakatı içe aktarma sürecini ayarlama

[!include[banner](../includes/banner.md)]


Gelişmiş banka mutabakatı özelliği, elektronik banka ekstrelerini içe aktarmanıza ve bunların Microsoft Dynamics 365 for Finance and Operations Enterprise sürümündeki banka hareketleriyle otomatik olarak mutabakat sağlamasına izin verir. Bu makalede banka ekstreleriniz için içe aktarma işlevinin nasıl ayarlanacağı açıklanmaktadır. 

Banka ekstresi içe aktarma işleminin kurulumu elektronik banka ekstrenizin biçimine bağlı olarak değişir. Finance and Operations ISO20022, MT940 ve BAI2 olmak üzere, kullanıma hazır üç banka ekstresi biçimini destekler.

## <a name="sample-files"></a>Örnek dosyalar
Bu üç biçim için, elektronik banka ekstresini orijinal biçimden Finance and Operations uygulamasının kullanabileceği bir biçime çeviren dosyalara sahip olmanız gerekir. Gerekli kaynak dosyaları Microsoft Visual Studio içindeki Uygulama Gezgini'nde **Kaynaklar** düğümü altında bulabilirsiniz. Dosyaları bulduktan sonra kurulum sürecinde daha kolay bir şekilde yükleyebilmeniz için dosyaları bilinen tek bir konuma kopyalayın.

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
Aşağıda gelişmiş banka mutabakatı içe aktarma dosyası teknik düzen tanımları örnekleri ve üç ilgili banka ekstresi örnek dosyası verilmektedir: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Teknik düzen tanımı                             | Banka ekstresi örnek dosya          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |

 

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
10. Sıra numarası 1 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **ISO20022XML-to-Reconciliation.xslt** dosyasını seçin. **Not:** Finance and Operations dönüşüm dosyaları standart biçim için oluşturulmuştur. Bankalar genellikle bu biçimden ayrıldıkları için dönüşüm dosyasını banka ekstresi biçiminizle eşleşecek şekilde güncelleştirmeniz gerekebilir. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
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
12. Sıra numarası 2 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **MT940XML-to-Reconciliation.xslt** dosyasını seçin. **Not:** Finance and Operations dönüşüm dosyaları standart biçim için oluşturulmuştur. Bankalar genellikle bu biçimden ayrıldıkları için dönüşüm dosyasını banka ekstresi biçiminizle eşleşecek şekilde güncelleştirmeniz gerekebilir. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
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
12. Sıra numarası 2 için **Dosyayı karşıya yükle** öğesine tıklayın ve daha önce kaydettiğiniz **BAI2XML-to-Reconciliation.xslt** dosyasını seçin. **Not:** Finance and Operations dönüşüm dosyaları standart biçim için oluşturulmuştur. Bankalar genellikle bu biçimden ayrıldıkları için dönüşüm dosyasını banka ekstresi biçiminizle eşleşecek şekilde güncelleştirmeniz gerekebilir. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
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




