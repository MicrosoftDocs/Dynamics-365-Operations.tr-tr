---
title: Varlık verilerini Excel ile görüntüleme ve güncelleştirme
description: Bu makalede, Microsoft Excel'de varlık verilerinin nasıl açılacağı, ardından Microsoft Dynamics Excel eklentisini kullanarak bu verilerin nasıl görüntüleneceği, güncelleştirileceği ve düzenleneceği açıklanmaktadır.
author: jasongre
ms.date: 05/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a05c34454e27244bb08bfff84f2ada6ff498f23
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862169"
---
# <a name="view-and-update-entity-data-with-excel"></a>Varlık verilerini Excel ile görüntüleme ve güncelleştirme 

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]


Bu makalede, Microsoft Excel'de varlık verilerinin nasıl açılacağı, ardından Microsoft Dynamics Excel eklentisini kullanarak bu verilerin nasıl görüntüleneceği, güncelleştirileceği ve düzenleneceği açıklanmaktadır. Varlık verilerini açmak için Excel'den veya Finans ve Operasyon uygulamalarından başlayabilirsiniz.

Varlık verilerini Excel'de açarak, Excel eklentisiyle bu verileri hızlı ve kolay bir şekilde görüntüleyip düzenleyebilirsiniz. Bu eklenti Microsoft Excel 2016 veya sonraki bir sürümünü gerektirir.

> [!NOTE]
> Microsoft Azure Active Directory (Azure AD) kiracınız Active Directory Federasyon Hizmetleri (AD FS) kullanmak üzere yapılandırılmışsa, Excel eklentisinin oturumunuzu doğru açabilmesi için Office Mayıs 2016 güncelleştirmesinin uygulandığından emin olmanız gerekir.

Excel eklentisini nasıl kullanacağınızı öğrenmek için [Üst bilgi ve satır düzenleri için Excel şablonu oluşturma](https://youtu.be/RTicLb-6dbI) kısa videosunu izleyin.

## <a name="open-entity-data-in-excel-when-you-start-from-a-finance-and-operations-app"></a>Finans ve Operasyon uygulamasından başlattığınızda varlık verilerini Excel'de açma
1. Finans ve Operasyon uygulamasındaki bir sayfada **Microsoft Office'te aç**'ı seçin.

    Sayfanın kök veri kaynağı (tablo) tüm varlıklar için kök veri kaynağı ile aynı ise, sayfa için, varsayılan **Excel'de aç** seçenekleri oluşturulur. **Excel'de aç** seçenekleri sık kullanılan sayfalarda (**Tüm satıcılar** ve **Tüm müşteriler** vb.) bulunabilir.
 
2. Bir **Excel'de aç** seçeneğini belirleyin ve oluşturulan çalışma kitabını açın. Bu çalışma kitabı varlık için bağlayıcı bilgiler, ortamınız için bir işaretçi ve Excel eklentisi için bir işaretçi içerir.
3. Excel'de,**Düzenlemeyi etkinleştir**'i seçerek Excel eklentisini etkinleştirin. Excel eklentisi Excel penceresinin sağ tarafındaki bir bölmede çalışır.
4. Excel eklentisini ilk kez çalıştırıyorsanız **Bu eklentiyle güven**'i seçin.
5. Oturum açmanız istendiğinde **Oturum aç**'ı seçin ve ardından Finans ve Operasyon uygulamasında oturum açmak için kullandığınız kimlik bilgilerini kullanarak oturum açın. Excel eklentisi, yapabiliyorsa, tarayıcıdan aldığı önceki oturum bağlamını kullanır ve oturumunuzu otomatik olarak açar. (İşletim sistemine göre kullanılan tarayıcı hakkında daha fazla bilgi için bkz. [Office eklentileri tarafından kullanılan tarayıcılar](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins). Oturum açma işleminin başarılı olması için Excel eklentisinin sağ üst köşesindeki kullanıcı adını doğrulayın. 

Excel eklentisi, seçtiğiniz varlıkla ilgili verileri otomatik olarak okur. Excel eklentisi okuyana kadar çalışma kitabında veri olmayacağını unutmayın.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Excel'den başlattığınızda varlık verilerini Excel'de açma
1. Excel'de, **Ekle** sekmesinde, **Eklentiler** grubunda **Mağaza**'yı seçerek Office Mağazası'nı açın.
2. Office Mağazası'nda **Dynamics** anahtar sözcüğünü arayıp **Microsoft Dynamics Office Eklentisi** (Excel eklentisi) yanındaki **Ekle**'yi seçin.
3. Excel eklentisini ilk kez çalıştırıyorsanız **Bu eklentiyle güven**'i seçerek Excel eklentisini etkinleştirin. Excel eklentisi Excel penceresinin sağ tarafındaki bir bölmede çalışır.
4. **Sunucu bilgilerini ekle**'yi seçerek **Seçenekler** bölmesini açın.
5. Tarayıcınızda, hedef Finans ve Operasyon uygulaması örneğinizin URL'sini kopyalayıp **Sunucu URL**'si alanına yapıştırın ve ana bilgisayar adından sonraki her şeyi silin. Ortaya çıkan URL yalnızca ana bilgisayar adına sahip olmalıdır.

    Örneğin, URL `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage` ise `https://xxx.dynamics.com` dışındaki her şeyi silin.

6. **Tamam**'ı ve ardından **Evet**'i seçerek değişikliği onaylayın. Excel eklentisi yeniden başlar ve meta verileri yükler.

    **Tasarım** düğmesi kullanılabilir hale gelir. Excel eklentisinde bir **Uygulamaları yükle** bağlantısı varsa büyük olasılıkla doğru kullanıcı olarak oturum açmamışsınızdır. Bu sorunu gidermeye yönelik daha fazla bilgi için [Uygulamaları yükle](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane) sorun giderme girişine bakın.

7. **Tasarım**'ı seçin. Excel eklentisi varlık meta verilerini alır.
8. **Tablo ekle**'yi seçin. Varlıkların listesi görüntülenir. Varlıklar "Ad - Etiket" biçiminde listelenir.
9. Listeden **Müşteri - Müşteriler** gibi bir varlık seçin ve **İleri**'yi seçin.
10. **Kullanılabilir alanlar** listesinden **Seçili alanlar** listesine bir alan eklemek için o alanı ve ardından **Ekle**'yi seçin. Alternatif olarak, alanı **Kullanılabilir alanlar** listesinden alana çift tıklayın.
11. Alanları **Seçili alanlar** listesine eklemeyi bitirdikten sonra, çalışma sayfasında imlecin doğru yerde bulunduğundan emin olun (örneğin A1 hücresi) ve **Bitti**'yi seçin. Ardından **Bitti**'yi seçerek tasarımcıdan çıkın.
12. Veri kümesi almak için **Yenile**'yi seçin.

## <a name="view-and-update-entity-data-in-excel"></a>Varlık verilerini Excel'de görüntüleme ve güncelleştirme
Excel eklentisi varlık verilerini okuyup çalışma kitabına aktardıktan sonra verileri Excel'deki **Yenile**'yi seçerek istediğiniz zaman güncelleştirebilirsiniz.

## <a name="edit-entity-data-in-excel"></a>Varlık verilerini Excel'de düzenleme
Varlık verilerini gerektiği gibi değiştirebilir ve Excel eklentisindeki **Yayımla**'yı seçerek Finans ve Operasyon uygulamalarında yeniden yayımlayabilirsiniz. Bir kaydı düzenlemek için çalışma sayfasında bir hücre seçin ve hücre değerini değiştirin. Yeni bir kayıt eklemek için aşağıdaki adımlardan birini izleyin:

- Veri kaynakları tablosunda herhangi bir yere tıklayın ve ardından Excel eklentisinde **Yeni**'yi seçin.
- Veri kaynakları tablosunun son satırında herhangi bir yere tıklayın ve sonra imleç satırın son sütununa gidip yeni bir satır oluşana kadar Sekme tuşuna basın.
- Veri kaynakları tablosunun hemen altındaki satırda herhangi bir yere tıklayın ve bir hücreye veri girmeye başlayın. İmleci o hücreden çıkardığınızda tablo genişleyerek yeni satırı kapsar.
- Başlık kayıtlarının alan bağlamaları için, alanlardan birini seçin ve daha sonra Excel eklentisinde **Yeni**'yi seçin.

Yeni kaydın yalnızca önemli ve gerekli alanların çalışma sayfasında bağlı olduğunda veya varsayılan değerlerin filtre koşulu kullanarak doldurulmuş olduğunda oluşturulabileceğini unutmayın.

Bir kaydı silmek için aşağıdaki adımlardan birini izleyin:

- Silinmesi gereken çalışma sayfası satırının yanındaki satır numarasına sağ tıklayın ve **Sil**'i seçin.
- Silinmesi gereken çalışma sayfası satırının herhangi bir yerine sağ tıklayın ve **Sil** &gt; **Tablo Satırları**'nı seçin.

Veri kaynakları ilişkili veri kaynakları olarak eklenmişse, başlık satırlardan önce yayımlanır. Diğer veri kaynakları arasında bağımlılıklar varsa, varsayılan yayımlanma sırasını değiştirmeniz gerekebilir. Yayımlama sırasını değiştirmek için Excel eklentisinde **Seçenekler** düğmesini (çark simgesi) seçin ve ardından **Veri Bağlayıcı** hızlı sekmesinde, **Yayımlama sırasını yapılandır**'ı seçin.

## <a name="add-or-remove-columns"></a>Sütun ekle veya kaldır
Çalışma sayfasına otomatik olarak eklenen sütunları ayarlamak için tasarımcıyı kullanabilirsiniz.

> [!NOTE]
> **Tasarla** düğmesi Excel eklentisindeki **Filtre** altında görünmezse veri kaynağı tasarımcısını etkinleştirmelisiniz. **Seçenekler** düğmesini (çark simgesi) seçin ve sonra **Tasarımı etkinleştir** onay kutusunu seçin.

1. Excel eklentisinde **Tasarım**'ı seçin. Tüm veri kaynakları listelenir.
2. Veri kaynağının yanındaki **Düzenle** düğmesini (kurşun kalem simgesi) tıklayın.
3. **Seçili alanlar** listesinde alan listesini gerektiği gibi ayarlayın:

    - **Kullanılabilir alanlar** listesinden **Seçili alanlar** listesine bir alan eklemek için o alanı ve ardından **Ekle**'yi seçin. Alternatif olarak, alanı **Kullanılabilir alanlar** listesinden alana çift tıklayın.
    - **Seçili alanlar** listesinden bir alan kaldırmak için alanı ve ardından **Kaldır**'ı seçin. Alternatif olarak, alana çift tıklayın.
    - **Seçili alanlar** listesindeki alanların sırasını değiştirmek için, bir alan seçin ve ardından **Yukarı**'ya veya **Aşağı**'ya tıklayın.

4. Veri kaynağına değişikliklerinizi uygulamak için **Güncelleştir**'i seçin. Ardından **Bitti**'yi seçerek tasarımcıdan çıkın.
5. Bir alan (sütun) eklediyseniz güncelleştirilmiş bir veri kümesini almak için **Yenile**'yi seçin.

## <a name="change-the-publish-batch-size"></a>Yayımlama toplu iş boyutunu değiştirme
Kullanıcılar Excel eklentisini kullanarak veri kayıtlarında yapılan değişiklikleri yayımladıkları zaman, güncelleştirmeler toplu işler halinde gönderilir. Varsayılan (ve maksimum) yayımlama toplu işi boyutunu 100 satırdır. Ancak, **Excel eklentisinde yayımlama toplu iş boyutunun yapılandırılmasına izin ver** özelliği, yayımlama toplu işi boyutunu azaltma esnekliği sunar. Bu, özellikle Excel'den yayımlama güncelleştirmeleri denediğinizde zaman aşımı hatalarıyla karşılaşmanız durumunda faydalıdır.

Sistem yöneticileri, **Office uygulaması parametreleri** sayfasının **Uygulama parametreleri** bölümünde **Yayımlama toplu işi sınırı** alanını ayarlayarak "Excel'de aç" çalışma kitapları için sistem genelinde bir sınır belirleyebilir.

Yayımlama toplu işi boyutu, Excel eklentisi kullanılarak tek bir çalışma kitabı için de değiştirilebilir.

1. Çalışma kitabını Excel'de açın.
2. Excel eklentisinin sağ üst kısmındaki **Seçenek** (dişli) düğmesini seçin.
3. **Yayımlama toplu işi boyutu** alanını istediğiniz şekilde ayarlayın. Ayarladığınız değerin, sistem geneli yayımlama toplu iş sınırından küçük olması gerekir.
4. **Tamam**'ı seçin.
5. Çalışma kitabını kaydedin. Eklenti ayarlarında değişiklik yaptıktan sonra çalışma kitabını kaydetmezseniz çalışma kitabı yeniden açıldığında bu değişiklikler korunmayacaktır.

Excel çalışma kitabı şablonu yazarları, sisteme yüklemeden önce şablonlar için yayımlama toplu işi boyutunu ayarlarken aynı yordamı kullanabilir.

## <a name="copy-environment-data"></a>Ortam verilerini kopyala

Bir ortamdaki çalışma kitabından okunan veriler başka bir ortama kopyalanabilir. Bununla birlikte, çalışma kitabındaki veri önbelleği veriyi mevcut veri gibi ele almaya devam edeceğinden bağlantı URL'sini değiştiremezsiniz. Bunun yerine, verileri yeni ortama yeni veri olarak yayımlamak için Ortam Verilerini Kopyala işlevini kullanmanız gerekir.

1. **Seçenekler** düğmesini (çark simgesi) ve daha sonra **Veri Bağlayıcısı** hızlı sekmesinde **Ortam Verilerini Kopyala**'yı seçin. 
2. Yeni ortamın sunucu URL'sini girin. 
3. **Tamam**'ı ve ardından **Evet**'i seçerek eylemi onaylayın. Excel eklentisi yeniden başlatılır ve yeni ortama bağlanır. Çalışma kitabında varolan veriler yeni veri olarak kabul edilir.

    Excel eklentisi yeniden başlatıldıktan sonra bir ileti kutusu çalışma kitabının Ortam kopyalama modunda olduğunu belirtir.

4. Veriyi yeni ortama yeni veri olarak kopyalamak için **Yayımla**'yı seçin. Ortam kopyalama işlemi iptal etmek ve yeni ortamdaki mevcut verileri incelemek için **Yenile**'yi seçin.

## <a name="troubleshooting"></a>Sorun Giderme
Bazı kolay adımlarla çözülebilecek birkaç sorun var.

- **"Uygulamaları yükle" bağlantısı görünüyor**: Bu sorunu gidermeye yönelik daha fazla bilgi için [Uygulamaları yükle](../office-integration/office-integration-troubleshooting.md#issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane) sorun giderme girişine bakın. 
- **"Yasak" iletisi alıyorsunuz** – Excel eklentisi meta verileri yüklerken "Yasak" iletisi alırsanız, Excel eklentisinde oturum açan hesabın, hedeflenen hizmeti, örneği veya veritabanını kullanma izni yoktur. Bu sorunu çözmek için, Excel eklentisinin sağ üst köşesinde doğru kullanıcı adının göründüğünü doğrulayın. Yanlış kullanıcı adı görünüyorsa, adı seçin, oturumu kapatın ve yeniden oturum açın.
- **Excel'de boş bir web sayfası görünüyor**: Oturum açma işlemi sırasında boş bir web sayfası açılıyorsa, hesap için AD FS gerekiyordur ancak Excel eklentisini çalıştıran Excel'in sürümü, oturum aç iletişim kutusunu yükleyecek kadar yeni değildir. Bu sorunu çözmek için, kullandığınız Excel sürümünü güncelleştirin. Gecikmeli bir kanalda bulunan bir kuruluştayken Excel sürümünü güncelleştirmek için [Office dağıtım aracını](/deployoffice/overview-office-deployment-tool) kullanarak [gecikmeli kanaldan geçerli kanala geçin](/deployoffice/overview-update-channels).
- **Veri değişiklikleri yayımladığınızda zaman aşımı iletisi alıyorsunuz**: Varlıkta yapılan veri değişikliklerini yayımlamaya çalışırken zaman aşımı iletileri alıyorsanız etkilenen çalışma kitabının yayımlama toplu işi boyutunu azaltabilirsiniz. Kayıt değişikliklerinde büyük boyutlarda mantık tetikleyen varlıklar, zaman aşımlarını önlemeye yardımcı olmak için güncelleştirmelerin daha küçük toplu işlerle gönderilmesini gerektirebilir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
