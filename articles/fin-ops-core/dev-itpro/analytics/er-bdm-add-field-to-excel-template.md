---
title: Microsoft Excel'de iş belgesi şablonuna yeni alanlar ekleme
description: Bu konuda, İş belgesi yönetimi özelliğini kullanarak Microsoft Excel'de iş belgesi şablonuna yeni alanlar ekleme hakkında bilgiler sağlanmaktadır.
author: NickSelin
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: af9f3dd81b0681579c14e0afb8281706e8aa534d
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351806"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Microsoft Excel'de iş belgesi şablonuna yeni alanlar ekleme

[!include[banner](../includes/banner.md)]

İş belgelerini Microsoft Excel biçiminde oluşturmak için kullanılan şablona yeni alanlar ekleyebilirsiniz. Bu alanlar, oluşturulan belgeleri uygulamadaki gerekli bilgilerle doldurmak için kullanılan yer tutucular olarak eklenebilir. Eklediğiniz alanlara yönelik olarak, şablon iş belgeleri oluşturmak üzere kullanıldığında alana hangi uygulama verilerinin girileceğini belirlemek için veri kaynaklarına bir bağlama belirtebilirsiniz.

Bu özellik hakkında daha fazla bilgi edinmek için bu konudaki örneği tamamlayın. Bu örnekte, oluşturulan serbest metin faturası formlarındaki alanları dolduracak şekilde bir şablonun nasıl güncelleştirileceği gösterilmektedir.

## <a name="configure-business-document-management-to-edit-templates"></a>Şablonları düzenlemek için İş belge yönetimini yapılandırma

İş belgesi yönetimi (BDM) [Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md) çerçevesi üzerine kurulu olduğundan BDM ile çalışmaya başlayabilmeniz için gerekli ER ve BDM parametrelerini yapılandırmanız gerekir.

1.  Microsoft Dynamics 365 Finance kurulumunda sistem yöneticisi olarak oturum açın.
2.  [İş belgesi yönetimine genel bakış](er-business-document-management.md) konusundaki örneğin aşağıdaki adımlarını tamamlayın:

    1.  ER parametrelerini yapılandırın.
    2.  BDM'yi açın.

Artık iş belgesi şablonlarını düzenlemek için BDM kullanmaya başlayabilirsiniz.

## <a name="import-er-solutions-that-contain-a-template"></a>Şablon içeren ER çözümlerini içe aktarma

Bu prosedürdeki örnekte, resmi olarak yayımlanan ER çözümü kullanılmaktadır. Bu çözümün ER yapılandırmalarını geçerli Finance kurulumunuza içe aktarmanız gerekir.

**Serbest metin faturası (Excel)** Bu çözümün ER biçim yapılandırması BDM kullanarak düzenlenebilen Excel biçiminde iş belgesi şablonu içerir. Bu ER biçim yapılandırmasının en son sürümünü Microsoft Dynamics Lifecycle Service'tan (LCS) içe aktarın. İlgili ER veri modeli ve ER model eşleme yapılandırmaları otomatik olarak içe aktarılır.

ER yapılandırmalarını içe aktarma hakkında daha fazla bilgi içi bkz. [ER yapılandırması yaşam döngüsünü yönetme](general-electronic-reporting-manage-configuration-lifecycle.md).

![LCS Paylaşılan varlık kitaplığı sayfası.](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>ER çözüm şablonunu düzenleme

1.  **İş belgesi yönetimi** çalışma alanına erişimi olan bir kullanıcı olarak oturum açın.
2.  **İş belgesi yönetimi** çalışma alanı sayfasını açın.

    ![İş belgesi yönetimi çalışma alanı.](./media/BDM-AddFldExcel-Workspace.png)

3.  Kılavuzda, **Serbest metin faturası (Excel)** şablonunu seçin.
4.  Sağ bölmede, seçili şablona dayalı yeni bir şablon oluşturmak için **Yeni şablon**'u seçin.
5.  **Başlık** alanına, yeni şablonun başlığı olarak **Serbest metin faturası (Excel) Contoso** girin.
6.  Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.

BDM şablon düzenleyici sayfası görüntülenir. Microsoft 365 kullanarak, katıştırılmış denetimde seçili şablonu çevrimiçi olarak düzenleyebilirsiniz.

![BDM şablon düzenleyicisi sayfası.](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Şablona yeni alan etiketini ekleme

1.  BDM şablon düzenleyicisi sayfasında Excel şeridindeki **Görünüm** sekmesinde düzenlenebilir Excel şablonu için **Başlıklar ve Kılavuz Çizgileri** onay kutularını seçin.

    ![Seçili Başlıklar ve Kılavuz Çizgileri onay kutuları.](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  **E8:F8** hücrelerini seçin.
3.  Excel şeridindeki **Giriş** sekmesinde, seçilen hücreleri yeni birleştirilen **E8:F8** hücresinde birleştirmek için **Birleştir ve Ortala**'yı seçin.
4.  Birleştirilen **E8:F8** hücresine **URL**'yi girin.
5.  Birleştirilen **E7:F7** hücresini seçin, **Biçim boyacısı** seçeneğini belirleyin ve ardından birleştirilen **E8:F8** hücresini seçerek bunu birleştirilen **E7:F7** hücresiyle aynı şekilde biçimlendirin.

    ![Şablona eklenen yeni alan etiketi.](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>Şablonu yeni alan için alan rezerve edecek şekilde biçimlendirme

1.  BDM şablon düzenleyicisi sayfasında, birleştirilen **G8:H8** hücresini seçin.
2.  Excel şeridindeki **Giriş** sekmesinde, seçilen hücreleri yeni birleştirilen **G8:H8** hücresinde birleştirmek için **Birleştir ve Ortala**'yı seçin.
3.  Birleştirilen **G7:H7** hücresini seçin, **Biçim boyacısı** seçeneğini belirleyin ve ardından birleştirilen **G8:H8** hücresini seçerek bunu birleştirilen **G7:H7** hücresiyle aynı şekilde biçimlendirin.

    ![Yeni alan için rezerve edilen alan.](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  **Ad** kutu alanında, **CompanyInfo**'yu seçin.

    Geçerli Excel şablonunun **CompanyInfo** aralığı, satıcı taraf olarak geçerli şirketin ayrıntılarıyla oluşturulan raporun başlığını doldurmak için kullanılan tüm alanları içerir.

    ![Seçili CompanyInfo aralığı.](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Şablona yeni alan ekleme

1.  **BDM şablon düzenleyicisi** sayfasındaki Eylem Bölmesi'nde **Biçimlendirmeyi göster**'i seçin.
2.  **Şablon yapısı** bölmesinde **Ekle**'yi seçin.

    > [!NOTE]
    > Yeni alan olarak kullanmak istediğiniz şablonun bölümünü ayarlamanız gerekir. Bu ayarlamayı birleştirilen **G8:H8** hücresini biçimlendirerek zaten yaptınız.

    ![Şablona yeni alan ekleme.](./media/BDM-AddFldExcel-AddCell.png)

3.  **Excel\Hücre**'yi seçerek yeni alanı şablondaki bir hücre olarak ekleyin.

    Şablona yeni aralık eklemek isterseniz **Excel\Aralık**'ı seçebilirsiniz. Girilen aralık birden fazla hücre içerebilir. Bu hücreleri daha sonra ekleyebilirsiniz.
    
    Eklediğiniz alan için geçerli şablon yapısındaki en uygun ana bileşen olduğundan **CompanyInfo** şablon bileşeninin **Şablon yapısı** bölmesinde otomatik olarak seçildiğini unutmayın.
    
4.  **Excel aralığı** alanına **CompanyURL_Value** girin.
5.  **Tamam**'ı seçin.

    ![Şablon yapısına eklenen CompanyURL_Value alanı.](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  **Şablon yapısı** bölmesinde, üç nokta düğmesini (...) seçin ve ardından **Bağlamaları göster** seçeneğini belirleyin.

    ![Seçili bağlamaları göster.](./media/BDM-AddFldExcel-ShowBindings.png)

    **Şablon yapısı** bölmesi artık temel alınan ER biçiminde kullanılabilen veri kaynaklarını gösterir.

7.  Temel alınan ER biçiminin veri kaynağına bağlamayı planladığınız alan olarak **CompanyInfo_Value**'yu seçin.
8.  **Şablon yapısı** bölmesinin **Veri kaynakları** bölümünde **Model \> InvoiceBase \> CompanyInfo**'yu genişletin.
9.  **CompanyInfo** altında **WebsiteURI** öğesini seçin.

    ![Seçili WebsiteURI öğesi.](./media/BDM-AddFldExcel-BindURL.png)

10. **Bağla**'yı seçin.
11. **Şablon yapısı** bölmesinde **Kaydet**'i seçin ve ardından BDM şablon düzenleyicisi sayfasını kapatın.

**İş belgesi yönetimi** çalışma alanında sağ bölmedeki **Şablon** sekmesi, güncelleştirilen şablonu gösterir. Kılavuzda, düzenlenen şablonun **Durum** alanının **Taslak** olarak değiştirildiğini ve **Revizyon** alanının artık boş olmadığına dikkat edin. Bu değişiklikler, bu şablonu düzenleme işleminin başlatıldığını gösterir.

![İş belgesi yönetimi çalışma alanında düzenlenen şablon.](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Şirket ayarlarını inceleme

1.  **Kuruluş yönetimi \> Kuruluşlar \> Tüzel kişilikler**'e gidin.
2.  **İletişim bilgileri** hızlı sekmesinde, şirket URL'sinin girildiğini doğrulayın.

![Tüzel kişilikler sayfasına girilen şirket URL'si.](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Güncelleştirilen şablonu test etmek için iş belgeleri oluşturma

1.  Uygulamada, şirketi **USMF** olarak değiştirin ve **Alacak hesapları \> Faturalar \> Tüm serbest metin faturaları**'na gidin.
2.  **FTI-00000002** faturasını seçin ve ardından **Yazdırma yönetimi** seçeneğini belirleyin.
3.  Sol bölmede, **Modül - alacak hesapları \> Belgeler \> Serbest metin faturası**'nı genişletin.
4.  **Serbest metin faturası** altında, **Özgün belge** düzeyini seçerek işlenecek faturaların kapsamını belirleyin.
5.  Sağ bölmedeki **Rapor biçimi** alanında, belirtilen belge düzeyi için **Serbest metin faturası (Excel) Contoso** şablonunu seçin.

    ![Seçili serbest metin faturası (Excel) Contoso şablonu.](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Geçerli sayfayı kapatmak için **Esc** tuşuna basın.
7.  **Yazdır \> Seçilen**'i belirleyin.
8.  Oluşturulan belgeyi indirin ve Excel'de açın.

    ![Excel'de serbest metin faturası.](./media/BDM-AddFldExcel-PreviewReport.png)

Değiştirilen şablon, seçili madde için serbest metin faturası raporu oluşturmak amacıyla kullanılır. Bu raporun şablonda yaptığınız değişikliklerden nasıl etkilendiğini analiz etmek için başka bir uygulama oturumunda şablonu değiştirdikten sonra raporu hemen bir uygulama oturumunda çalıştırın.

## <a name="related-links"></a>İlgili bağlantılar

[Elektronik raporlamaya (ER) genel bakış](general-electronic-reporting.md)

[İş belgesi yönetimine genel bakış](er-business-document-management.md)

[OPENXML formatında raporların oluşturulması için bir yapılandırma tasarlama](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]