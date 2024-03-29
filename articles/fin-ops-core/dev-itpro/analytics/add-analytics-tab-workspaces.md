---
title: Power BI Embedded kullanarak çalışma alanlarına analiz ekleme
description: Bu makalede, bir Power BI raporunun bir çalışma alanının Analizler sekmesine nasıl ekleneceği gösterilmektedir.
author: RichdiMSFT
ms.date: 06/21/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b06821f02e6a80f2e15db7d0dd95ef6c9a30d5bc
ms.sourcegitcommit: 3c4dd125ed321af8a983e89bcb5bd6e5ed04a762
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/28/2022
ms.locfileid: "9206431"
---
# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>Power BI Embedded kullanarak çalışma alanlarına analiz ekleme

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Bu özellik finans ve operasyon uygulamaları (sürüm 7.2 ve sonrası) için desteklenir.

## <a name="introduction"></a>Giriş
Bu makalede, bir Microsoft Power BI raporunun bir çalışma alanının **Analizler** sekmesine nasıl ekleneceği gösterilmektedir. Burada verilen örnek için Filo Yönetimi uygulamasındaki **Rezervasyon yönetimi** çalışma alanını, bir **Analizler** sekmesinde bir analitik çalışma alanı katıştırmak üzere genişleteceğiz.

## <a name="prerequisites"></a>Ön koşullar
+ Platform güncelleştirmesi 8 veya sonraki bir sürümü çalıştıran bir geliştirici ortamına erişin.
+ Microsoft Power BI Desktop kullanarak oluşturulmuş ve kaynağı Varlık deposu veritabanı olan bir veri modeline sahip bir analitik rapor (.pbix dosyası).

## <a name="overview"></a>Özet
Mevcut bir uygulama çalışma alanını genişlettiğinizde veya kendinize ait yeni bir çalışma alanı kullandığınızda, iş verilerinize bilgilendirici ve etkileşimli görünümler sunan katıştırılmış analitik görünümler kullanabilirsiniz. Bir analitik çalışma alanı sekmesi eklemenin dört adımı vardır.

1. Dynamics 365 kaynağına bir .pbix dosyası ekleyin.
2. Bir analitik çalışma alanı sekmesi belirleyin.
3. .pbix kaynağını çalışma alanı sekmesine gömün.
4. İsteğe bağlı: Görünümü özelleştirmek için uzantılar ekleyin.

> [!NOTE]
> Analitik raporlar oluşturmak hakkında daha fazla bilgi için bkz. [Power BI Desktop ile çalışmaya başlamak](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/). Bu sayfa, ilgi çekici analitik raporlama çözümleri oluşturmanıza yardımcı olacak harika bir bilgi kaynağıdır.

## <a name="add-a-pbix-file-as-a-resource"></a>Bir .pbix dosyasını bir kaynak olarak ekleyin.
Başlamadan önce, çalışma alanına katıştıracağınız Power BI raporunu oluşturun veya alın. Analitik raporlar oluşturmak hakkında daha fazla bilgi için bkz. [Power BI Desktop ile çalışmaya başlamak](https://powerbi.microsoft.com/documentation/powerbi-desktop-getting-started/).

Bir .pbix doyasını bir Visual Studio yapıtı olarak eklemek için şu adımları izleyin.

1. Uygun modelde yeni bir proje oluşturun.
2. Çözüm Gezgini'nde projeyi seçip sağ tıklayın ve ardından **Ekle** \> **Yeni Öğe**'yi seçin.
3. **Yeni Madde Ekle** iletişim kutusunda, **Operasyonlar Yapıları** altında **Kaynak** şablonunu seçin.
4. X++ meta verisindeki raporu referans olarak kullanacak bir ad girin ve **Ekle**'yi tıklatın.

    ![Yeni Madde Ekle iletişim kutusu.](media/analytical-workspace-add.png)

5. Analitik raporun tanımını içeren .pbix dosyasını bulun ve **Aç**'ı tıklatın.

    ![Bir Kaynak dosya iletişim kutusu seçin.](media/analytical-workspace-select-resource.png)

Şimdi .pbix dosyasını bir Dynamics 365 kaynağı olarak ekledikten sonra, raporları çalışma alanlarına katıştırabilir ve menü öğelerini kullanarak doğrudan bağlantılar ekleyebilirsiniz.

## <a name="add-a-tab-control-to-an-application-workspace"></a>Bir uygulama çalışma alanına bir sekme denetimi ekleyin
Bu örnekte Filo Yönetimi modelinde, **Analizler** sekmesini **FMClerkWorkspace** formuna ekleyerek **Rezervasyon yönetimi** çalışma alanını genişleteceğiz.

Aşağıdaki görsel, **FMClerkWorkspace** formunun Microsoft Visual Studio tasarımcısında nasıl görüneceğini gösterir.

![Değişikliklerden önce FMClerkWorkspace formu.](media/analytical-workspace-definition-before.png)

**Rezervasyon yönetimi** çalışma alanının form tanımını genişletmek için şu adımları izleyin.

1. Tasarım tanımını genişletmek için form tasarımcısını açın.
2. Tasarım tanımında, **Tasarım | Desen: Çalışma Alanı Operasyonel** olarak etiketlenmiş üst öğeyi seçin.
3. Sağ tıklayın ve ardından **FormTabControl1** adında yeni bir denetim eklemek için **Yeni** \> **Sekme**'yi seçin.
4. Form tasarımcısında **FormTabControl1**'i seçin.
5. Sağ tıklayın ve daha sonra yeni bir sekme sayfası eklemek için **Yeni Sekme Sayfası**'nı seçin.
6. Sekme sayfasının adını **Çalışma alanı** gibi anlamlı bir şeye değiştirin.
7. Form tasarımcısında **FormTabControl1**'i seçin.
8. Sağ tıklayın ve daha sonra **Yeni Sekme Sayfası**'nı seçin.
9. Sekme sayfasının adını **Analizler** gibi anlamlı bir şeye değiştirin.
10. Form tasarımcısında **Analizler (Sekme Sayfası)**'nı seçin.
11. **Açıklama yazısı** özelliğini **Analiz** olarak ayarlayın ve **Otomatik Beyaz** özelliğini **Evet** olarak ayarlayın.
12. Denetime sağ tıklayın ve ardından yeni bir form grubu denetimi eklemek için **Yeni** \> **Grup**'u seçin.
13. Form grubunun adını **powerBIReportGroup** gibi anlamlı bir şeye değiştirin.
14. Form tasarımcısında **PanoramaBody (Sekme)** seçin. ve denetimi **Çalışma alanı** sekmesine sürükleyin.
15. Tasarım tanımında, **Tasarım | Desen: Çalışma Alanı Operasyonel** olarak etiketlenmiş üst öğeyi seçin.
16. Sağ tıklayın ve daha sonra **Deseni sil**'i seçin.
17. Yeniden sağ tıklayın ve ardından **Desen ekle** \> **Sekmeli Çalışma Alanı**'nı seçin.
18. Yaptığınız değişiklikleri doğrulamak için bir yapı gerçekleştirin.

Aşağıdaki görsel, bu değişiklikler uygulandıktan sonra tasarımın nasıl görüneceğini gösterir.

![Değişikliklerden sonra FMClerkWorkspace.](media/analytical-workspace-definition-after.png)

Çalışma alanı raporunu katıştırmak için kullanılacak form denetimlerini ekledikten sonra, düzeni bulunduracak üst denetimin boyutunu tanımlamalısınız. Varsayılan olarak hem **Filtrelre Bölmesi** sayfası hem de **Sekmeler** sayfası raporda görünür olur. Bunula birlikte, bu denetimlerin görünürlüğünü raporun hedef tüketicisi için uygun şekilde değiştirebilirsiniz.

> [!NOTE]
> Katıştırılmış çalışma alanları için tutarlılık amacıyla hem **Filtrelre Bölmesi** hem de **Sekme** sayfasını gizleyecek uzantılar kullanmanızı öneririz.

Şimdi uygulama form tanımını genişletme görevini tamamladınız. Uzantıların nasıl kullanılacağı ve özelleştirmelerin nasıl yapılacağıyla ilgili daha fazla bilgi için bkz. [Uzantı ve katmanlamayla özelleştirme](../extensibility/customization-overlayering-extensions.md).

## <a name="add-x-business-logic-to-embed-a-viewer-control"></a>Bir görüntüleyici denetimi katıştırmak için X++ iş mantığı ekleyin
**Rezervasyon yönetimi** çalışma alanına katıştırılmış olan rapor görüntüleyici denetimini başlatan bir iş mantığı eklemek için bu adımları izleyin.

1. Tasarım tanımını genişletmek için **FMClerkWorkspace** form tasarımcısını açın.
2. Kod tanımının arkasındaki koda erişmek için F7'ye basın.
3. Aşağıdaki X++ kodunu ekleyin.

    ```xpp
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                // initialize the PBI report control using shared helper
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
        }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. Yaptığınız değişiklikleri doğrulamak için bir yapı gerçekleştirin.

Katıştırılmış rapor görüntüleme denetimini başlatmak için iş mantığı ekleme görevini şimdi tamamladınız. Aşağıdaki görsel, bu değişiklikler uygulandıktan sonra çalışma alanının nasıl görüneceğini gösterir.

![Çalışma alanına katıştırılmış rapor.](media/analytical-workspace-final.png)

> [!NOTE]
> Sayfa başlığının altındaki çalışma alanı sekmelerini kullanarak mevcut operasyonel görünümlere erişebilirsiniz.

## <a name="reference"></a>Referans

### <a name="pbireporthelperinitializereportcontrol-method"></a>PBIReportHelper.initializeReportControl yöntemi
Bu bölüm, bir Power BI raporunu (.pbix kaynağı) bir form grubu denetimine eklemek için kullanılan yardımcı sınıf hakkında bilgi sağlar.

#### <a name="syntax"></a>Sözdizimi
```xpp
public static void initializeReportControl(
    str                 _resourceName,
    FormGroupControl    _formGroupControl,
    str                 _defaultPageName = '',
    boolean             _showFilterPane = false,
    boolean             _showNavPane = false,
    List                _defaultFilters = new List(Types::Class))
```

#### <a name="parameters"></a>Parametreler

| Dosya Adı             | Açıklama                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------|
| resourceName     | .pbix kaynağının adı.                                                                              |
| formGroupControl | Power BI rapor denetiminin uygulanacağı form grup denetimi.                                              |
| defaultPageName  | Varsayılan sayfa adı.                                                                                       |
| showFilterPane   | Bir Boole değeri, filtre panosunun gösterilip (**doğru**) gösterilmeyeceğini (**yanlış**) belirtir.     |
| showNavPane      | Bir Boole değeri, gezinti panosunun gösterilip (**doğru**) gösterilmeyeceğini (**yanlış**) belirtir. |
| defaultFilters   | Power BI raporu için varsayılan filtreler.                                                                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
