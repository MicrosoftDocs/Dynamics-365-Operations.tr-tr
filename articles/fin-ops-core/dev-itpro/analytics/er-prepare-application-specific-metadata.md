---
title: RCS ve ER için uygulamaya özel meta verileri hazırlama
description: Bu konu, Regulatory Configuration Service (RCS) ve Elektronik Raporlama (ER) için uygulamaya özel meta verilerin nasıl hazırlanacağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 37da06f4ba86594c6368dcd1049456c58bf87e3a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565477"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a>RCS ve ER için uygulamaya özel meta verileri hazırlama

[!include[banner](../includes/banner.md)]

Bu konu, aşağıdaki görevlere örnekler konusunda size yol gösterecektir:

- [RCS'de kullanılabilecek uygulama meta verileri hazırlama](#prepare-application-metadata-that-can-be-used-in-rcs)
- [Bir ER yapılandırması kullanarak uygulama meta verilerine erişme](#access-application-metadata-by-using-an-er-configuration)
- [Bağlı uygulamalar kullanarak uygulama meta verilerine erişme](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a>RCS'de kullanılabilecek uygulama meta verileri hazırlama

Aşağıdaki prosedürde **Sistem Yöneticisi** ya da **Elektronik Raporlama Geliştirici** rolüne sahip kullanıcının uygulama meta verileri içeren Elektronik raporlama (ER) yapılandırması oluşturup oluşturamayacağını gösterir ve bu Regulatory Configuration Service (RCS)'deki ER model eşleme yapılandırmalarını tasarlamak için kullanılır. Bu örnekte oluşturulan örnek ER model eşleme yapılandırması, dış ticaret hareketlerine erişmek için kullanılacaktır.

Bu örnek için, dış ticari işletme etki alanındaki bilgileri içeren elektronik belgeler oluşturmak amacıyla kullanılacak uygulamaya bir ER çözümü tasarlamak için RCS'yi kullanmak istiyorsunuz. ER veri modeliyle gerekli verilerin kaynakları arasındaki eşlemeyi belirtmek amacıyla RCS'de uygulama meta verilerine erişiminizin olması gerekir. Bu nedenle, ER çözümünü tasarlama sürecinin bir parçası olarak, seçilen iş etki alanı için ER raporları oluşturmak üzere gerekli olan tüm meta verileri içeren yeni bir ER meta veri yapılandırması yapılandırmalısınız.

> [!NOTE]
> Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, herhangi bir şirkette gerçekleştirilebilir.

1. **Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.
2. Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedürünü tamamlayın. 
3. **Meta veri yapılandırması**'nı seçin.
4. **Yapılandırma oluştur**'u seçin.
5. Açılır menüdeki iletişim kutusunda, **Ad** alanına bir ad girin. Bu örnek için, **Dış ticaret meta verileri** girin.
6. **Yapılandırma oluştur**'u seçin.
7. **Tasarımcı**’yı seçin.
8. **Ekle**'yi seçin.

    > [!NOTE]
    > Tüm uygulama, seçili model ya da modüller için tüm meta verileri seçebilirsiniz. Her iki durumda da aşağıdaki meta verilerin otomatik olarak eklenebileceğine dikkat edin: kayıt tabloları, numaralandırmalar ve genişletilmiş veri türleri (EDTs). Ek meta veri türleri gerektiğinde, bunların el ile eklenmesi gerekir.

    Dış ticari hareketlerle ilgili bazı meta verileri eklemeniz ve meta veri öğelerini el ile seçmeniz gerekir.

9. **Veri kaynağı ekle \> Tablo kayıtları**'nı seçin.
10. **Ad** alanında **İntrastat** değerine filtre uygulayın.
11. **Intrastat** tablosu kaydını seçin.
12. **Tamam**'ı seçin.

    Intrastat kayıt tablosu hakkında meta veri bilgileri eklemeniz gerekir.

13. Ağaçta **Tablo kayıtları İntrastatı \> \>İlişkiler \> IntrastatCommodity (Tablo kayıtları EcoResCategory)**'yi seçin.
14. **Meta veri ekle**'yi seçin.

    > [!NOTE]
    > Seçili kayıt tablosu için gerekli ilişkilerindeki meta veriler el ile eklenmelidir.

15. **Veri kaynağını ekle**'yi seçin.
16. **Numaralandırma**'yı seçin.
17. **Ad** alanında **IntrastatDirection** değerine filtre uygulayın.
18. **IntrastatDirection** numaralandırma kaydını seçin.
19. **Tamam**'ı seçin.
20. **Kaydet**'i seçin.
21. Sayfayı kapatın.
22. Meta veri yapılandırmasının taslak sürümünü tamamlayın:

    1. **Durumu değiştir \> Tamamla**'yı seçin.
    2. **Tamam**'ı seçin.
    3. Tamamlanmış sürüm 1'i seçin.

23. Meta veri yapılandırmasının tamamlanan sürümünü uygulamadan XML dosyası olarak dışarı aktarın:

    1. **Değiştir \> XML dosyasını dışa aktar**'ı seçin.
    2. **Tamam**'ı seçin.

Oluşturduğunuz ER meta veri yapılandırması, **Dış ticaret meta verileri.xml** dosyası olarak kaydedilir. Dış ticari iş etki alanı için meta veri kaynağı olarak kullanılabilmesi amacıyla bunu RCS'de içe aktarabilirsiniz. Bu bilgiye dayanarak uygulama meta verileri ve ER veri modeli arasındaki eşlemeyi belirtebilirsiniz.

## <a name="access-application-metadata-by-using-an-er-configuration"></a>Bir ER yapılandırması kullanarak uygulama meta verilerine erişme

Aşağıdaki prosedürde **Sistem Yöneticisi** ya da **Elektronik Raporlama Geliştirici** rolüne sahip bir RCS kullanıcısının uygulamadan meta verileri kullanarak yeni bir ER model eşlemesi tasarlayabileceği gösterilmiştir. Uygulama meta verilerine, dış ticari hareketlere erişmek için örnek bir meta veri kümesi içeren ER meta veri yapılandırması kullanılarak erişilir.

Bu prosedürü tamamlamadan önce aşağıdaki prosedürleri tamamlamanız gerekir:

- [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [RCS'de kullanılabilecek uygulama meta verileri hazırlama](#prepare-application-metadata-that-can-be-used-in-rcs)

1. **Tüm çalışma alanları \> Elektronik raporlama**'ya gidin.
2. Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun. Bu yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedürünü tamamlayın. 
3. Dış ticari etki alanı elektronik belge oluşturmak üzere yapılandırılmış olan uygulama için meta veriler içeren ER meta veri yapılandırmasını içe aktarın. Bu ER meta veri yapılandırmasını daha önce bu konuda oluşturdunuz ve[RCS'de kullanılabilecek uygulama meta verileri hazırlama](#prepare-application-metadata-that-can-be-used-in-rcs) prosedüründe XML dosyası olarak dışa aktardınız.

    1. **Meta veri yapılandırması**'nı seçin.
    2. **Döviz**'i seçin.
    3. **XML dosyasından yükle**'yi seçin.
    4. **Dış ticaret meta verileri.xml** dosyasını seçmek için gözatın.
    5. **Tamam**'ı seçin.
    6. Sayfayı kapatın.

4. Bir veri modeli yapılandırması oluşturun:

    1. **Raporlama yapılandırmaları**'nı seçin.
    2. **Yapılandırma oluştur**'u seçin.
    3. Açılır menüdeki iletişim kutusunda, **Ad** alanına **Dış ticaret modeli** girin.
    4. **Yapılandırma oluştur**'u seçin.
    5. **Tasarımcı**’yı seçin.
    6. Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.

        1. **Ad** alanına **Kök** yazın.
        2. **Ekle**'yi seçin.
    
    7. Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.

        1. **Ad** alanına **Hareket** yazın.
        2. **Madde türü** alanında **Kayıt listesi**'ni seçin.
        3. **Ekle**'yi seçin.
 
    8. Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.

        1. **Ad** alanına **Emtia kodu** yazın.
        2. **Madde türü** alanında **Dize**'yi seçin.
        3. **Ekle**'yi seçin.

    9. Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.

        1. Ad alanına **Faturalanan tutar**.
        2. **Madde türü** alanında **Gerçek**'i seçin.
        3. **Ekle**'yi seçin.

    10. Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.

        1. **Ad** alanına **Tarih** yazın.
        2. **Madde türü** alanında **Tarih**'i seçin.
        3. **Ekle**'yi seçin.
 
    11. **Ekle \> Kök referansı**'nı seçin.
    12. **Tamam**'ı seçin.
    13. **Kaydet**'i seçin.
    14. Sayfayı kapatın.
    15. **Durumu değiştir \> Tamamla**'yı seçin.
    16. **Tamam**'ı seçin.

5. Model eşleme yapılandırması oluşturma

    1. **Yapılandırma oluştur**'u seçin.
    2. Açılır menüdeki iletişim kutusunda **Yeni** alanında **Dış ticaret modeli veri modelini temel alan Model Eşleme** girin.
    3. **Ad** alanına **Dış ticaret eşlemesi** girin.
    4. **Yapılandırma oluştur**'u seçin.
    5. **Önkoşullar** hızlı sekmesinde **Düzenle**'yi seçin.
    6. **Yeni**'yi seçin.
    7. **Önkoşul bileşen türü** alanında **Yapılandırma**'yı seçin.
    8. **Dış ticaret meta veri** yapılandırılmasını seçin.
    9. **Kaydet**'i seçin. **Dış ticaret meta verileri** yapılandırmasındaki sürüm 1'e referans eklendiğini unutmayın. Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verisi sunulacaktır.
    10. Sayfayı kapatın.
    11. **Tasarımcı**’yı seçin.
    12. **Tasarımcı**’yı seçin.
    13. Ağaçta **Dynamics 365 for Operations \> Tablo kayıtları**'nı seçin.
    14. **Kök ekle**'yi seçin.
    15. **Ad** alanına, **İntrastat** girin.
    16. **Intrastat** tablosu kayıtlarını seçin.
    17. **Tamam**'ı seçin.

        > [!NOTE]
        > Şu anda kullanılmakta olan meta veri kümesine sadece iki tablo eklendiğinden sadece iki tablo kullanıldı

    18. **Bağla**'yı seçin.
    19. Ağaçta **İntrastat \> AmountMST**'yi seçin.
    20. Ağaçta **Hareket = İntrastat \> Faturalanan tutar**'ı seçin.
    21. **Bağla**'yı seçin.
    22. Ağaçta **İntrastat \> TransDate**'i seçin.
    23. Ağaçta **Hareket = İntrastat \> Tarih**'i seçin.
    24. **Bağla**'yı seçin.
    25. Ağaçta **İntrastat \> \>İlişkiler \> IntrastatCommodity \> Kod**'u seçin.
    26. Ağaçta **Hareket = İntrastat \> Emtia kodu**'nu seçin.
    27. **Bağla**'yı seçin.
    28. **Doğrula**'yı seçin.

        > [!NOTE]
        > Doğrulama tamamlandıktan sonra belirtilen veri kaynağı öğeleriyle, başvurulan ER meta veri yapılandırmasından uygulama meta verilerinin ayrıntılarını kullanarak tanımlanan veri modeli öğelerini başarıyla bağladınız.

    29. **Kaydet**'i seçin.

Var olan meta veri kümesini genişletmek istediğinizde bunu uygulamadan yapabilirsiniz. ER meta veri yapılandırmasının yeni sürümünü içe aktarabilir, bunları RCS 'ye aktarabilir ve alınan meta veri yapılandırmasının yeni sürümüne başvuran yapılandırılmış model eşleme yapılandırmasının önkoşullarını güncelleştirebilirsiniz.

> [!NOTE]
> Uygulama meta verileri hakkında bilgi elde etmenin bu yolu, yerel işletme verileri (LBD) veya yerel olarak dağıtılmış uygulamalar için kullanılabilecek tek yoldur (yerel işletme verileri \[LBD\], ya da or şirket içi dağıtım modeli uygulama için kullanılır).

## <a name="access-application-metadata-by-using-connected-applications"></a>Bağlı uygulamalar kullanarak uygulama meta verilerine erişme

Aşağıdaki prosedürde **Sistem Yöneticisi** ya da **Elektronik Raporlama Geliştirici** rolüne sahip bir RCS kullanıcısının uygulama meta verilerini kullanarak yeni bir ER model eşlemesi tasarlayabileceği gösterilmiştir. RCS bağlantılı uygulama kullanılarak uygulama meta verilerine çevrimiçi olarak erişilir. Örnek ER model eşlemesi, dış ticari hareketlere erişmek üzere yapılandırılacak.

Bu prosedürdeki adımları tamamlamak için öncelikle RCS'deki [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedürünü tamamlamanız gerekir. Bu prosedürdeki [Bir ER yapılandırması kullanarak uygulama meta verilerine erişme](#access-application-metadata-by-using-an-er-configuration)'yi tamamlamadıysanız aşağıdaki ER yapılandırma dosyalarını önceden indirmek ve yerel olarak kaydetmek için [Dynamics 365 for Finance and Operations 8.1 için Elektronik Raporlama Görev Kılavuzu](https://go.microsoft.com/fwlink/?linkid=2082739) sayfasına gidin: **Foreign trade metadata.xml**, **Foreign trade model.xml**, ve **Foreign trade mapping.xml**.


### <a name="get-required-er-configurations"></a>Gerekli ER yapılandırmalarını alma

[(RCS) Access application metadata by using ER configuration](#access-application-metadata-by-using-an-er-configuration) prosedüründeki adımları daha önce bu konuda tamamladıysanız mevcut RCS örneğinde gerekli tüm ER yapılandırmalarına (dış ticaret meta verileri, model ve harita yapılandırmaları) zaten sahipsiniz. Bu durumda, bu prosedürü atlayabilirsiniz.

1. **Tüm çalışma alanları \> Elektronik raporlama**'ya gidin.
2. **Raporlama yapılandırmaları**'nı seçin.
3. **Dış ticaret meta verileri.xml**, **Dış ticaret modeli.xml**, and **Dış ticaret eşleme.xml** yapılandırma dosyaları için aşağıdaki adımlar zincirini tamamlayarak yükleyin:

    1. **Döviz**'i seçin.
    2. **XML dosyasından yükle**'yi seçin.
    3. **Gözat**'ı seçin ve bir dosya seçin.
    4. **Tamam**'ı seçin.

### <a name="register-the-connection-with-the-application"></a>Uygulamayla bağlantıyı kaydetme

1. **Tüm çalışma alanları \> Elektronik raporlama**'ya gidin.
2. **Bağlı uygulamalar** ı seçin.
3. Yapılandırılan uygulamanın Microsoft Azure'e bağlı olduğundan ve genel RCS kullanıcıları tarafından erişilebilir olduğundan emin olun. Ayrıca geçerli RCS kullanıcısının seçilen yapılandırılmış uygulamaya erişimi olması ve uygulamanın meta verilerine erişim ayrıcalıkları sunan bir rolde uygulama kullanıcısı olarak kayıtlı olması gerekir.
4. **Yeni**'yi seçin.
5. **Ad** alanına, bağlı uygulamanın adı olarak **MyConnectedApp** girin.
6. **Uygulama** alanında, uygulamanın URL'sini belirtin.
7. **Kiracı** alanında, uygulamanın sağlayıcısını belirtin.
8. **Kaydet**'i seçin. 
9. Yapılandırılmış uygulamaya olan bağlantıyı denetlediğinizde **Uzak uygulamaya bağlan** sayfasında **Seçilen uzak uygulama bağlantısına bağlanmak için buraya tıklayın**'ı seçin. 
10. Yapılandırılan uygulamaya erişimi doğrulamak için **Bağlantıyı kontrol et**'e tıklayın.
11. **Kapat**'ı seçin.

Bu prosedürü ve bağlantı doğrulaması başarılıyla tamamladığınızda geçerli kılavuzda yapılandırılan uygulama için sürüm ve kiracı ayrıntıları güncelleştirilir.

### <a name="review-the-existing-model-mapping-configuration"></a>Mevcut ER model eşleme yapılandırmasını inceleyin

1. **Tüm çalışma alanları \> Elektronik raporlama**'ya gidin.
2. **Raporlama yapılandırmaları**'nı seçin.
3. Ağaçta  **Dış ticaret modeli \> Dış ticaret eşlemesi**'ni seçin.
4. **Önkoşullar** hızlı sekmesini seçin.

    > [!NOTE]
    > Şu anda bu eşleme meta veri yapılandırmasına başvuruyor. Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verisi sunulacaktır.

4. **Tasarımcı**’yı seçin.
5. **Tasarımcı**’yı seçin.
6. Ağaçta **Dynamics 365 for Operations \> Tablo kayıtları**'nı seçin.
7. **Kök ekle**'yi seçin.
8. **Tablo** alanında bir değer girin veya bir değer seçin.

    > [!NOTE]
    > Şu anda bu eşleme meta veri yapılandırmasına başvuruyor. Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verisi sunulacaktır.

9. **İptal**'i seçin.

### <a name="assign-the-connected-application-to-a-model-mapping"></a>Bağlantılı uygulamayı bir model eşlemeye atayın

1. **Düzenle** öğesini seçin.
2. **Bağlı uygulama alanı**'nda, **MyConnectedApp** uygulamasını seçin.

    > [!NOTE]
    > Bu eşleme, seçilen bağlı uygulamanın meta verilerine başvuruda bulunuyor. Aynı eşleme aynı anda meta veri yapılandırmasına ve bağlı uygulamaya başvurursa bağlı uygulamanın meta verileri kullanılır.

3. **Tasarımcı**’yı seçin.
4. **Tasarımcı**’yı seçin.
5. Ağaçta **Dynamics 365 for Operations \> Tablo kayıtları**'nı seçin.
6. **Kök ekle**'yi seçin.
7. **Tablo** alanında bir değer girin veya bir değer seçin.

    > [!NOTE]
    > O zaman bu eşleme için atanmış olan bağlı uygulamanın tüm meta verileri kullandığından ikiden fazla uygulama tablosu sunulur.

8. **İptal**'i seçin.
9. **Doğrula**'yı seçin.

Belirtilen veri kaynağı öğeleriyle, bu eşleme için atanmış bağlı uygulamanın ayrıntılarını kullanarak tanımlanan veri modeli öğelerini başarıyla bağladınız.

Bu model eşlemesini farklı bir sürüm uygulamasının meta verilerini kullanarak değerlendirmeniz gerektiğinde, bağlı başka bir uygulamayı kaydedin, bu model eşlemesine atayın ve yeni meta verilere göre doğrulayın.

## <a name="additional-resources"></a>Ek kaynaklar

Alternatif olarak hem uygulamadaki **RCS'de kullanılabilecek uygulama meta verileri hazırlama** görev kılavuzlarını hem **Bir ER yapılandırması kullanarak uygulama meta verilerine erişme** ve RCS'deki **Bağlı uygulamalar kullanarak uygulama meta verilerine erişme** görev kılavuzlarını yürütebilirsiniz. Bu göre kılavuzları [Dynamics 365 for Finance and Operations 8.1 için Elektronil Raporlama Görev Kılavuzu](https://go.microsoft.com/fwlink/?linkid=2082739) sayfasından indirilebilir.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]