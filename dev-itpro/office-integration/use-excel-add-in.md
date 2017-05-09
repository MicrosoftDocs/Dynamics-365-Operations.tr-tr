---
title: Excel eklentisini kullanma
description: "Bu konuda, Microsoft Excel&quot;de varlık verilerinin nasıl açılacağı, ardından Excel için Microsoft Dynamics Office eklentisini kullanarak bu verilerin nasıl görüntüleneceği, güncelleştirileceği ve düzenleneceği açıklanmaktadır. Varlık verilerini açmak için Excel veya Microsoft Dynamics 365 for Operations&quot;tan başlatabilirsiniz."
author: ChrisGarty
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267914
ms.assetid: 4e6c7194-a059-4057-bd62-ec0c802c36fd
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: af7e7288f741b3c519227e2778c4c4311c3a2012
ms.openlocfilehash: 8af663b47117759ed3b2e2ed8eee85ae4df100d1
ms.lasthandoff: 03/31/2017


---

# <a name="use-the-excel-add-in"></a>Excel eklentisini kullanma

Bu konuda, Microsoft Excel'de varlık verilerinin nasıl açılacağı, ardından Excel için Microsoft Dynamics Office eklentisini kullanarak bu verilerin nasıl görüntüleneceği, güncelleştirileceği ve düzenleneceği açıklanmaktadır. Varlık verilerini açmak için Excel veya Microsoft Dynamics 365 for Operations'tan başlatabilirsiniz.

Varlık verilerini Microsoft Excel'de açarak, Excel için Microsoft Dynamics Office eklentisiyle bu verileri hızlı ve kolay bir şekilde görüntüleyip düzenleyebilirsiniz. Bu eklenti için Microsoft Excel 2016 gerekir. **Not:**, Microsoft Azure Active Directory (Azure AD) kiracınız Active Directory Federasyon Hizmetleri (AD FS) kullanmak üzere yapılandırılmışsa, Excel eklentisinin oturumunuzu doğru açabilmesi için Mayıs 2016 güncelleştirmesinin uygulandığından emin olmanız gerekir.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Dynamics 365 for Operations'tan başladığınız zaman varlık verilerini Excel'de açma
1.  Microsoft Dynamics 365 for Operations'ta bir sayfada **Microsoft Office'te aç**'a tıklayın. Sayfanın kök veri kaynağı (tablo) tüm varlıklar için kök veri kaynağı ile aynı ise, sayfa için, varsayılan **Excel'de aç** seçenekleri oluşturulur. **Excel'de aç** seçenekleri sık kullanılan sayfalarda (**Tüm satıcılar** ve **Tüm müşteriler** vb.) bulunabilir.
2.  Bir **Excel'de aç** seçeneğine tıklayın ve oluşturulan çalışma kitabını açın. Bu çalışma kitabı varlık için bağlayıcı bilgiler, ortamınız için bir işaretçi ve Excel eklentisi için bir işaretçi içerir.
3.  Excel'de,**Düzenlemeyi etkinleştir**'e tıklayarak Excel eklentisini etkinleştirin. Excel eklentisi Excel penceresinin sağ tarafındaki bir bölmede çalışır.
4.  Excel eklentisini ilk kez çalıştırıyorsanız **Bu eklentiyle güven**'e tıklayın.
5.  Oturum açmanız istendiğinde **Oturum aç**'a ve ardından Dynamics 365 for Operations'ta oturum açmak için kullandığınız kimlik bilgilerini kullanarak oturum açın. Excel eklentisi, yapabiliyorsa, Internet Explorer'dan aldığı önceki oturum bağlamını kullanır ve oturumunuzu otomatik olarak açar. Bu nedenle, Excel eklentisinin sağ üst köşesindeki kullanıcı adını doğrulayın.

Excel eklentisi, seçtiğiniz varlıkla ilgili verileri otomatik olarak okur. Excel eklentisi okuyana kadar çalışma kitabında veri olmayacağını unutmayın.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Excel'den başlattığınızda varlık verilerini Excel'de açma
1.  Excel'de, **Ekle** sekmesinde, **Eklentiler** grubunda **Mağaza**'yı tıklayarak Office Mağazası'nı açın.
2.  Office Mağazası'nda "Dynamics" anahtar sözcüğünü arayıp **Microsoft Dynamics Office Eklentisi** (Excel eklentisi) yanındaki **Ekle**'ye tıklayın.
3.  Excel eklentisini ilk kez çalıştırıyorsanız **Bu eklentiyle güven**'e tıklayarak Excel eklentisini etkinleştirin. Excel eklentisi Excel penceresinin sağ tarafındaki bir bölmede çalışır.
4.  **Sunucu bilgilerini ekle**'ye tıklayarak **Seçenekler** bölmesini açın.
5.  Hedef Dynamics 365 for Operations örneğinizden tarayıcı URL'sini kopyalayıp **Sunucu URL'si** alanına yapıştırın ve ana bilgisayar adından sonraki her şeyi (örneğin **/? cmp usmf & mi = CustTableListPage =** kısmını) silin. Elde edilen URL'de yalnızca ana bilgisayar adı olmalıdır (örneğin **https://xxx.dynamics.com**).
6.  **Tamam**'a ve ardından **Evet**'e tıklayarak değişikliği onaylayın. Excel eklentisi yeniden başlar ve meta verileri yükler. **Tasarım** düğmesi kullanılabilir hale gelir. Excel eklentisinde bir **Uygulamaları yükle** düğmesi varsa, büyük olasılıkla doğru kullanıcı olarak oturum açmamışsınızdır. Daha fazla bilgi için bu konunun "Sorun giderme" bölümündeki "Uygulamaları yükle düğmesi görünüyor" konusuna bakın.
7.  **Tasarım**'ı tıklayın. Excel eklentisi varlık meta verilerini alır.
8.  **Tablo ekle**'ye tıklayın. Varlıkların listesi görüntülenir. Varlıklar "Ad - Etiket" biçiminde listelenir.
9.  Listeden **Müşteri - Müşteriler** gibi bir varlık seçin ve **İleri**'ye tıklayın.
10. **Kullanılabilir alanlar** listesinden **Seçili alanlar** listesine bir alan eklemek için o alana ve ardından **Ekle**'ye tıklayın. Alternatif olarak, alana çift tıklayın.
11. İstediğiniz alanları **Seçili alanlar** listesine ekledikten sonra, çalışma sayfasında imlecin doğru yerde bulunduğundan emin olun (örneğin A1 hücresi) ve **Bitti**'ye tıklayın. Ardından **Bitti**'ye tıklayarak tasarımcıdan çıkın.
12. Veri kümesi almak için **Yenile**'ye tıklayın.

## <a name="view-and-update-entity-data-in-excel"></a>Varlık verilerini Excel'de görüntüleme ve güncelleştirme
Excel eklentisi varlık verilerini okuyup çalışma kitabına aktardıktan sonra verileri Excel'deki **Yenile**'ye tıklayarak istediğiniz zaman güncelleştirebilirsiniz.

## <a name="edit-entity-data-in-excel"></a>Varlık verilerini Excel'de düzenleme
Varlık verilerini gerektiği gibi değiştirebilir ve Excel eklentisindeki **Yayımla**'ya tıklayarak yeniden yayımlayabilirsiniz. Bir kaydı düzenlemek için çalışma sayfasında bir hücre seçin ve hücre değerini değiştirin. Yeni bir kayıt eklemek için aşağıdaki adımlardan birini izleyin:

-   Çalışma sayfasında herhangi bir yere tıklayın ve ardından Excel eklentisinde **Yeni**'ye tıklayın.
-   Çalışma sayfasının son satırına tıklayın ve sonra imleç satırın son sütununa gidip yeni bir satır oluşana kadar Tab tuşuna basın.
-   Çalışma sayfasının hemen altındaki satıra tıklayın ve bir hücreye veri girmeye başlayın. İmleci o hücreden çıkardığınızda çalışma sayfası genişleyerek yeni satırı kapsar.

Bir kaydı silmek için aşağıdaki adımlardan birini izleyin:

-   Silinecek çalışma sayfası satırının yanındaki satır numarasına sağ tıklayın ve **Sil**'e tıklayın.
-   Silinecek çalışma sayfası satırına sağ tıklayın ve **Sil** &gt; **Tablo Satırları**'na tıklayın.

## <a name="add-or-remove-columns"></a>Sütun ekle veya kaldır
Çalışma sayfasına otomatik olarak eklenen sütunları ayarlamak için tasarımcıyı kullanabilirsiniz.

1.  **Seçenekler** düğmesine (dişli simgesi) tıklayıp **Tasarımı etkinleştir** onay kutusunu işaretleyerek Excel eklentisinin veri kaynağı tasarımcısını başlatın.
2.  Excel eklentisinde **Tasarım**'a tıklayın. Tüm veri kaynakları listelenir.
3.  Veri kaynağının yanındaki **Düzenle** düğmesine (kurşun kalem simgesi) tıklayın.
4.  **Seçili alanlar** listesinde listeyi gerektiği gibi ayarlayın:
    -   **Kullanılabilir alanlar** listesinden **Seçili alanlar** listesine bir alan eklemek için o alana ve ardından **Ekle**'ye tıklayın. Alternatif olarak, alana çift tıklayın.
    -   **Seçili alanlar** listesinden bir alan kaldırmak için alana ve ardından **Kaldır**'a tıklayın. Alternatif olarak, alana çift tıklayın.
    -   Alanların sırasını değiştirmek için, **Seçili alanlar** listesindeki alana ve ardından **Yukarı**'ya veya **Aşağı**'ya tıklayın.

5.  Veri kaynağındaki değişikliklerinizi **Güncelleştir**'e tıklayarak uygulayın. Ardından **Bitti**'ye tıklayarak tasarımcıdan çıkın. Bir alan (sütun) eklediyseniz güncelleştirilmiş bir veri kümesini almak için **Yenile**'ye tıklayın.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Sorun Giderme
Bazı kolay adımlarla çözülebilecek birkaç sorun var.

-   **Uygulamaları yükle düğmesi görünüyor.** Oturum açıldıktan sonra Excel eklentisinde bir **Uygulamaları yükle** düğmesi varsa, büyük olasılıkla doğru kullanıcı olarak oturum açmamışsınızdır. Bu sorunu çözmek için, Excel eklentisinin sağ üst köşesinde doğru kullanıcı adının göründüğünü doğrulayın. Yanlış kullanıcı adı görünüyorsa, ada tıklayın, oturumu kapatın ve yeniden oturum açın.
-   **"Yasak" iletisi alıyorsunuz.** Excel eklentisi meta verileri yüklerken "Yasak" iletisi alırsanız, Excel eklentisinde oturum açan hesabın, hedeflenen hizmeti, örneği veya veritabanını kullanma izni yoktur. Bu sorunu çözmek için, Excel eklentisinin sağ üst köşesinde doğru kullanıcı adının göründüğünü doğrulayın. Yanlış kullanıcı adı görünüyorsa, ada tıklayın, oturumu kapatın ve yeniden oturum açın.
-   **Excel'de boş bir web sayfası görünüyor.** Oturum açma işlemi sırasında boş bir web sayfası açılıyorsa, hesap için AD FS gerekiyordur ancak eklentiyi çalıştıran Excel'in sürümü, oturum aç iletişim kutusunu yükleyecek kadar yeni değildir. Bu sorunu çözmek için, kullandığınız Excel sürümünü güncelleştirin. Gecikmeli bir kanalda bulunan bir kuruluştayken Excel sürümünü güncelleştirmek için [Office dağıtım aracını](https://technet.microsoft.com/library/jj219422.aspx) kullanarak [gecikmeli kanaldan geçerli kanala geçin](https://technet.microsoft.com/library/mt455210.aspx).



