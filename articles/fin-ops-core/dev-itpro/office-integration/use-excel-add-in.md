---
title: Varlık verilerini Excel'de açma ve Excel eklentisini kullanarak güncelleştirme
description: Bu konuda, Microsoft Excel'de varlık verilerinin nasıl açılacağı, ardından Excel için Microsoft Dynamics Office eklentisini kullanarak bu verilerin nasıl görüntüleneceği, güncelleştirileceği ve düzenleneceği açıklanmaktadır.
author: ChrisGarty
manager: AnnBe
ms.date: 04/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 210231bb442928674b490d83f50bf787d7bfa60c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181025"
---
# <a name="open-entity-data-in-excel-and-update-it-by-using-the-excel-add-in"></a>Varlık verilerini Excel'de açma ve Excel eklentisini kullanarak güncelleştirme

[!include [banner](../includes/banner.md)]

Bu konuda, Microsoft Excel'de varlık verilerinin nasıl açılacağı, ardından Excel için Microsoft Dynamics Office eklentisini kullanarak bu verilerin nasıl görüntüleneceği, güncelleştirileceği ve düzenleneceği açıklanmaktadır. Varlık verilerini açmak için Excel'den veya Finance and Operations'tan başlayabilirsiniz.

Varlık verilerini Excel'de açarak, Excel eklentisiyle bu verileri hızlı ve kolay bir şekilde görüntüleyip düzenleyebilirsiniz. Bu eklenti Microsoft Excel 2016 gerektirir.

> [!NOTE]
> Microsoft Azure Active Directory (Azure AD) kiracınız Active Directory Federasyon Hizmetleri (AD FS) kullanmak üzere yapılandırılmışsa, Excel eklentisinin oturumunuzu doğru açabilmesi için Office Mayıs 2016 güncelleştirmesinin uygulandığından emin olmanız gerekir.

Excel eklentisi kullanma hakkında daha fazla bilgi için [Dynamics 365 for Finance and Operations'ta başlık ve satır düzenleri için bir Excel şablonu oluşturma](https://youtu.be/RTicLb-6dbI) kısa videosunu izleyin.

## <a name="open-entity-data-in-excel-when-you-start-from-finance-and-operations"></a>Finance and Operations'tan başlattığınızda varlık verilerini Excel'de açma
1. Finance and Operations'taki bir sayfada **Microsoft Office'te aç**'ı seçin.

    Sayfanın kök veri kaynağı (tablo) tüm varlıklar için kök veri kaynağı ile aynı ise, sayfa için, varsayılan **Excel'de aç** seçenekleri oluşturulur. **Excel'de aç** seçenekleri sık kullanılan sayfalarda (**Tüm satıcılar** ve **Tüm müşteriler** vb.) bulunabilir.
 
2. Bir **Excel'de aç** seçeneğini belirleyin ve oluşturulan çalışma kitabını açın. Bu çalışma kitabı varlık için bağlayıcı bilgiler, ortamınız için bir işaretçi ve Excel eklentisi için bir işaretçi içerir.
3. Excel'de,**Düzenlemeyi etkinleştir**'i seçerek Excel eklentisini etkinleştirin. Excel eklentisi Excel penceresinin sağ tarafındaki bir bölmede çalışır.
4. Excel eklentisini ilk kez çalıştırıyorsanız **Bu eklentiyle güven**'i seçin.
5. Oturum açmanız istendiğinde **Oturum aç**'ı seçin ve ardından Finance and Operations'ta oturum açmak için kullandığınız kimlik bilgilerini kullanarak oturum açın. Excel eklentisi, yapabiliyorsa, Internet Explorer'dan aldığı önceki oturum bağlamını kullanır ve oturumunuzu otomatik olarak açar. Bu nedenle, Excel eklentisinin sağ üst köşesindeki kullanıcı adını doğrulayın.

Excel eklentisi, seçtiğiniz varlıkla ilgili verileri otomatik olarak okur. Excel eklentisi okuyana kadar çalışma kitabında veri olmayacağını unutmayın.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Excel'den başlattığınızda varlık verilerini Excel'de açma
1. Excel'de, **Ekle** sekmesinde, **Eklentiler** grubunda **Mağaza**'yı seçerek Office Mağazası'nı açın.
2. Office Mağazası'nda **Dynamics** anahtar sözcüğünü arayıp **Microsoft Dynamics Office Eklentisi** (Excel eklentisi) yanındaki **Ekle**'yi seçin.
3. Excel eklentisini ilk kez çalıştırıyorsanız **Bu eklentiyle güven**'i seçerek Excel eklentisini etkinleştirin. Excel eklentisi Excel penceresinin sağ tarafındaki bir bölmede çalışır.
4. **Sunucu bilgilerini ekle**'yi seçerek **Seçenekler** bölmesini açın.
5. Tarayıcınızda, hedef Finance and Operations örneğinizin URL'sini kopyalayıp **Sunucu URL**'si alanına yapıştırın ve ana bilgisayar adından sonraki her şeyi silin. Ortaya çıkan URL yalnızca ana bilgisayar adına sahip olmalıdır.

    Örneğin, URL `https://xxx.dynamics.com/?cmp=usmf&amp;mi=CustTableListPage` ise `https://xxx.dynamics.com` dışındaki her şeyi silin.

6. **Tamam**'ı ve ardından **Evet**'i seçerek değişikliği onaylayın. Excel eklentisi yeniden başlar ve meta verileri yükler.

    **Tasarım** düğmesi kullanılabilir hale gelir. Excel eklentisinde bir **Uygulamaları yükle** düğmesi varsa, büyük olasılıkla doğru kullanıcı olarak oturum açmamışsınızdır. Daha fazla bilgi için bu konunun [Sorun giderme](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#troubleshooting) bölümündeki "Uygulamaları yükle düğmesi görünüyor" konusuna bakın.

7. **Tasarım**'ı seçin. Excel eklentisi varlık meta verilerini alır.
8. **Tablo ekle**'yi seçin. Varlıkların listesi görüntülenir. Varlıklar "Ad - Etiket" biçiminde listelenir.
9. Listeden **Müşteri - Müşteriler** gibi bir varlık seçin ve **İleri**'yi seçin.
10. **Kullanılabilir alanlar** listesinden **Seçili alanlar** listesine bir alan eklemek için o alanı ve ardından **Ekle**'yi seçin. Alternatif olarak, alanı **Kullanılabilir alanlar** listesinden alana çift tıklayın.
11. Alanları **Seçili alanlar** listesine eklemeyi bitirdikten sonra, çalışma sayfasında imlecin doğru yerde bulunduğundan emin olun (örneğin A1 hücresi) ve **Bitti**'yi seçin. Ardından **Bitti**'yi seçerek tasarımcıdan çıkın.
12. Veri kümesi almak için **Yenile**'yi seçin.

## <a name="view-and-update-entity-data-in-excel"></a>Varlık verilerini Excel'de görüntüleme ve güncelleştirme
Excel eklentisi varlık verilerini okuyup çalışma kitabına aktardıktan sonra verileri Excel'deki **Yenile**'yi seçerek istediğiniz zaman güncelleştirebilirsiniz.

## <a name="edit-entity-data-in-excel"></a>Varlık verilerini Excel'de düzenleme
Varlık verilerini gerektiği gibi değiştirebilir ve Excel eklentisindeki **Yayımla**'yı seçerek yeniden yayımlayabilirsiniz. Bir kaydı düzenlemek için çalışma sayfasında bir hücre seçin ve hücre değerini değiştirin. Yeni bir kayıt eklemek için aşağıdaki adımlardan birini izleyin:

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

## <a name="copy-environment-data"></a>Ortam verilerini kopyala

Bir ortamdaki çalışma kitabından okunan veriler başka bir ortama kopyalanabilir. Bununla birlikte, çalışma kitabındaki veri önbelleği veriyi mevcut veri gibi ele almaya devam edeceğinden bağlantı URL'sini değiştiremezsiniz. Bunun yerine, verileri yeni ortama yeni veri olarak yayımlamak için Ortam Verilerini Kopyala işlevini kullanmanız gerekir.

1. **Seçenekler** düğmesini (çark simgesi) ve daha sonra **Veri Bağlayıcısı** hızlı sekmesinde **Ortam Verilerini Kopyala**'yı seçin. 
2. Yeni ortamın sunucu URL'sini girin. 
3. **Tamam**'ı ve ardından **Evet**'i seçerek eylemi onaylayın. Excel eklentisi yeniden başlatılır ve yeni ortama bağlanır. Çalışma kitabında varolan veriler yeni veri olarak kabul edilir.

    Excel eklentisi yeniden başlatıldıktan sonra bir ileti kutusu çalışma kitabının Ortam kopyalama modunda olduğunu belirtir.

4. Veriyi yeni ortama yeni veri olarak kopyalamak için **Yayımla**'yı seçin. Ortam kopyalama işlemi iptal etmek ve yeni ortamdaki mevcut verileri incelemek için **Yenile**'yi seçin.

## <a name="troubleshooting"></a>Sorun Giderme
Bazı kolay adımlarla çözülebilecek birkaç sorun var.

- **Uygulamaları yükle düğmesi görünüyor** – Oturum açıldıktan sonra Excel eklentisinde bir **Uygulamaları** yükle düğmesi varsa, büyük olasılıkla doğru kullanıcı olarak oturum açmamışsınızdır. Bu sorunu çözmek için, Excel eklentisinin sağ üst köşesinde doğru kullanıcı adının göründüğünü doğrulayın. Yanlış kullanıcı adı görünüyorsa, adı seçin, oturumu kapatın ve yeniden oturum açın.
- **"Yasak" iletisi alıyorsunuz** – Excel eklentisi meta verileri yüklerken "Yasak" iletisi alırsanız, Excel eklentisinde oturum açan hesabın, hedeflenen hizmeti, örneği veya veritabanını kullanma izni yoktur. Bu sorunu çözmek için, Excel eklentisinin sağ üst köşesinde doğru kullanıcı adının göründüğünü doğrulayın. Yanlış kullanıcı adı görünüyorsa, adı seçin, oturumu kapatın ve yeniden oturum açın.
- **Excel'de boş bir web sayfası görünüyor** - Oturum açma işlemi sırasında boş bir web sayfası açılıyorsa, hesap için AD FS gerekiyordur ancak Excel eklentisini çalıştıran Excel'in sürümü, oturum aç iletişim kutusunu yükleyecek kadar yeni değildir. Bu sorunu çözmek için, kullandığınız Excel sürümünü güncelleştirin. Gecikmeli bir kanalda bulunan bir kuruluştayken Excel sürümünü güncelleştirmek için [Office dağıtım aracını](https://technet.microsoft.com/library/jj219422.aspx) kullanarak [gecikmeli kanaldan geçerli kanala geçin](https://technet.microsoft.com/library/mt455210.aspx).