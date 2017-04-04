---
title: Excel eklentisini kullanma
description: "Bu konuda varlık verileri Microsoft Excel&quot;de açın ve ardından görüntülemek, güncelleştirmek ve Excel Microsoft Dynamics ofisini eklentisini kullanarak verileri düzenlemek nasıl açıklar. Varlık veri açmak için Excel veya Microsoft Dynamics 365 işlemleri başlatabilirsiniz."
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

Bu konuda varlık verileri Microsoft Excel'de açın ve ardından görüntülemek, güncelleştirmek ve Excel Microsoft Dynamics ofisini eklentisini kullanarak verileri düzenlemek nasıl açıklar. Varlık veri açmak için Excel veya Microsoft Dynamics 365 işlemleri başlatabilirsiniz.

Microsoft Excel'de varlık verileri açarak, hızla ve kolayca görüntüleyebilir ve Excel Microsoft Dynamics ofisini eklentisini kullanarak verileri düzenleyin. Bu eklenti Microsoft Excel 2016 gerektirir. **Not:**, Microsoft Azure Active Directory (AD Azure) Kiracı, Active Directory Federasyon Hizmetleri (AD FS) kullanmak üzere yapılandırılmışsa, böylece Excel eklentisi düzgün oturum açmak, Mayıs 2016 güncelleştirmenin uygulandığını emin olmanız gerekir.

## <a name="open-entity-data-in-excel-when-you-start-from-dynamics-365-for-operations"></a>Dynamics 365 işlemleri için başlangıç zaman varlık verileri Excel'de açın.
1.  Microsoft Dynamics 365 işlemleri için bir sayfa üzerinde tıklatın **açık Microsoft Office**. Sayfanın kök veri kaynağı (tablo) tüm varlıklar için kök veri kaynağı ile aynı ise, varsayılan **Excel'de Aç** seçenekleri sayfa için oluşturulur. **Excel'de Aç** seçenekleri bulunabilir, sık kullanılan sayfaları gibi **tüm satıcılar** ve **tüm müşterileri**.
2.  ' I bir **Excel'de açmak** seçeneğini ve oluşturulan çalışma kitabını açın. Bu çalışma kitabı Excel eklentisi için bir işaretçi varlığı ve ortamınız için bir işaretçi için bağlama bilgileri vardır.
3.  Excel'de,'ı **düzenlemeyi etkinleştirme** Excel çalıştırmak eklenti etkinleştirmek için. Excel eklentisi Excel penceresinin sağ tarafında bir bölmede çalışır.
4.  Tıklatın Excel eklentisi ilk kez çalıştırıyorsanız, **bu eklentiyle güven ilişkisi**.
5.  Oturum açmanız istendiğinde,'ı **oturum**ve sonra Dynamics 365 işlemleri için oturum açmak için kullandığınız kimlik bilgilerini kullanarak oturum açın. Excel eklentisi önceki oturum kapsamı Internet Explorer'dan kullanmak ve kullanılabiliyorsa oturumunuzu otomatik olarak. Bu nedenle, Excel eklentisi sağ üst köşesindeki kullanıcı adını doğrulayın.

Excel eklentisi otomatik olarak seçtiğiniz varlıkla ilgili verileri okur. Olacağını hiç veri çalışma kitabında Excel eklentisi içinde okur kadar unutmayın.

## <a name="open-entity-data-in-excel-when-you-start-from-excel"></a>Excel'den başlattığınızda varlık verileri Excel'de açın.
1.  Excel'de, üzerinde **Ekle** sekmesini **eklentileri** tıklatın, grup **deposu** Office mağaza açmak için.
2.  Office deposunda arama anahtar sözcüğü "Dynamics" öğesini tıklatıp **Ekle** yanında **Microsoft Dynamics Office eklenti** (Excel eklentisi).
3.  Tıklatın Excel eklentisi ilk kez çalıştırıyorsanız, **bu eklentiyle güven ilişkisi** Excel çalıştırmak eklenti etkinleştirmek için. Excel eklentisi Excel penceresinin sağ tarafında bir bölmede çalışır.
4.  ' I **sunucu bilgileri eklemek** açmak için **seçenekleri** bölmesi.
5.  Hedefiniz Dynamics 365 işlemleri örneği için tarayıcı URL kopyalamak, içine yapıştırın **sunucu URL'si** alanı ve ana bilgisayar adından sonra her şeyi silin (örnek: delete **/? cmp usmf & mi = CustTableListPage =**). Sonuçta elde edilen URL yalnızca ana bilgisayar adı olmalıdır (örneğin, **https://xxx.dynamics.com**).
6.  ' I **Tamam**ı **Evet** Değişikliği onaylamak için. Excel-yeniden ve meta veriler yükler. **Tasarım** düğmesini yayımlamıştır. Excel eklenti varsa, bir **uygulamalarını yükleme** düğmesi, doğru kullanıcı olarak büyük olasılıkla oturum değil. Daha fazla bilgi için "uygulamaları Yükle düğmesini gösterilen" Bu konuda "Sorun giderme" bölümüne bakın.
7.  ' I **tasarım**. Excel eklentisi varlık meta verileri alır.
8.  ' I **Tablo Ekle**. Varlıkların bir listesi görüntülenir. Varlıkları "– etiket adı" biçiminde listelenir.
9.  Bir varlık seçin listesinde, aşağıdaki gibi **müşteri - müşteriler**ı **İleri**.
10. Bir alan eklemek için **kullanılabilir alanlar** listelemek için **seçili alanlar** listesinde, alanı tıklatın ve ardından **Ekle**. Alternatif olarak, alanı çift tıklatın.
11. İstenen alanları ekledikten sonra **seçili alanlar** listesinde, imleç (örneğin, A1 hücresi) çalışma doğru yerde olduğundan emin olun ve sonra'ı **yapılan**. ' I **yapılan** Tasarımcısı'ndan çıkmak için.
12. ' I **yenileme** bir veri kümesi çıkarmak için.

## <a name="view-and-update-entity-data-in-excel"></a>Görüntüleme ve varlık verileri Excel'de güncelleştirme
Excel eklentisi varlık verileri çalışma kitabına okuduktan sonra verileri herhangi bir anda tıklatarak güncelleştirebilirsiniz **yenileme** Excel eklentisinde.

## <a name="edit-entity-data-in-excel"></a>Varlık verileri Excel'de Düzenle
Varlık veri gerektirir ve Geri'yi tıklatarak yayımlamak gibi değiştirebilirsiniz **Yayımla** Excel eklentisinde. Bir kaydı düzenlemek için çalışma sayfasında bir hücre seçin ve ardından hücre değeri değiştirin. Yeni bir kayıt eklemek için aşağıdaki adımlardan birini izleyin:

-   Çalışma sayfasında herhangi bir yeri tıklatın ve ardından **yeni** Excel eklentisinde.
-   Çalışma sayfasının son satırını tıklatın ve sonra yeni bir satır oluşturulur ve imleç satır son sütununun dışında gider kadar SEKME tuşuna basın.
-   Çalışma hemen altındaki satırı tıklatın ve bir hücreye veri girmek başlatın. Bu hücreden odağı taşıdığınızda, yeni satır eklemek için çalışma genişletir.

Bir kaydı silmek için aşağıdaki adımlardan birini izleyin:

-   Sil öğesini tıklatıp ardından çalışma sayfasında satırın yanındaki satır numarasını sağ tıklatın **Sil**.
-   Silmek için çalışma sayfası satırını sağ tıklatın ve ardından **Sil**&gt;**tablo satırları**.

## <a name="add-or-remove-columns"></a>Sütun ekle veya kaldır
Tasarımcı, otomatik olarak çalışma sayfasına eklenen sütunlar ayarlamak için kullanabilirsiniz.

1.  Tıklatarak veri kaynağı Tasarımcısı Excel eklentisini başlatın **seçenekleri** (çark simgesi) düğmesini ve sonra seçerek **tasarım etkinleştir** onay kutusu.
2.  ' I **tasarım** Excel eklentisinde. Tüm veri kaynakları listelenir.
3.  Veri kaynağını yanındaki tıklatın **düzenleme** düğmesini (Kurşun Kalem simgesi).
4.  Listede Ayarla **seçili alanlar** gereksinim duyduğunuz kadar liste:
    -   Bir alan eklemek için **kullanılabilir alanlar** listelemek için **seçili alanlar** listesinde, alanı tıklatın ve ardından **Ekle**. Alternatif olarak, alanı çift tıklatın.
    -   Bir alan kaldırmak için **seçili alanlar** listesinde, alanı tıklatın ve ardından **kaldırmak**. Alternatif olarak, alanı çift tıklatın.
    -   Alanların sırasını değiştirmek için alanı tıklatın **seçili alanlar** listesini ve ardından **yukarı** veya **aşağı**.

5.  Tıklatarak veri kaynağına değişiklikleri uygulamak **Update**. ' I **yapılan** Tasarımcısı'ndan çıkmak için. Bir alan (sütun) eklediyseniz,'ı **yenileme** güncelleştirilmiş bir veri kümesinde çıkarmak için.

## <a name="httpspowerappsmicrosoftcomenustutorialsdataplatforminteractiveexceltroubleshootingtroubleshooting"></a>[](https://powerapps.microsoft.com/enus/tutorials/dataplatforminteractiveexcel/#troubleshooting)Troubleshooting
Bazı kolay adımlar ile çözülebilir birkaç sorun vardır.

-   **Uygulamaları Yükle düğmesini gösterilir.** Excel eklenti varsa, bir **uygulamalarını yükleme** düğmesini oturumaçma sonra size büyük olasılıkla doğru kullanıcı olarak oturum. Bu sorunu çözmek için doğru kullanıcı adını sağ üst köşesinde Excel eklentisi göründüğünü doğrulayın. Yanlış kullanıcı adı görünürse, tıklatın, Oturumu Kapat ve sonra oturum açın.
-   **"Yasak" iletisi alırsınız.** Excel eklentisi meta veriler yükleniyor "Yasak" iletisi alırsanız, Excel eklentisi için oturum hesabı hedeflenen hizmet, kopya veya veritabanı kullanma izni yoktur. Bu sorunu çözmek için doğru kullanıcı adını sağ üst köşesinde Excel eklentisi göründüğünü doğrulayın. Yanlış kullanıcı adı görünürse, tıklatın, Oturumu Kapat ve sonra oturum açın.
-   **Boş bir Web sayfası Excel gösterilir.** Oturum açma işlemi sırasında boş bir Web sayfası açarsa, AD FS hesap gerektirir, ancak eklenti çalışmakta olan Excel sürümünü oturum aç iletişim kutusunu yüklemek için yeni değildir. Bu sorunu gidermek için kullandığınız Excel sürümüne güncelleştirin. Ertelenmiş bir kanalda bir kuruluştaki olduğunuzda Excel sürümünü güncelleştirmek için kullanın [Office dağıtım aracı](https://technet.microsoft.com/library/jj219422.aspx) için [ertelenmiş kanalından taşımak için geçerli kanal](https://technet.microsoft.com/library/mt455210.aspx).



