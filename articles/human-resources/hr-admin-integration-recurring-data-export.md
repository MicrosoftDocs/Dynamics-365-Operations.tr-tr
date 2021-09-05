---
title: Yinelenen veri dışarı aktarma uygulaması oluşturma
description: Bu konuda, verileri Microsoft Dynamics 365 Human Resources uygulamasından yinelenen bir zamanlamaya göre dışarı aktaran bir Microsoft Azure mantıksal uygulamasının nasıl oluşturulacağı açıklanmaktadır.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce9fe4e77fa968463052e037ca767ed38e72796
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414774"
---
# <a name="create-a-recurring-data-export-app"></a>Yinelenen veri dışarı aktarma uygulaması oluşturma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Bu konuda, verileri Microsoft Dynamics 365 Human Resources uygulamasından yinelenen bir zamanlamaya göre dışarı aktaran bir Microsoft Azure mantıksal uygulamasının nasıl oluşturulacağı açıklanmaktadır. Öğretici, verileri dışa aktarmak için İnsan Kaynakları'nın DMF Paket REST uygulama programlama arabirimini (API) kullanmaktadır. Veriler dışa aktarıldıktan sonra, mantık uygulaması, dışa aktarılan veri paketini bir Microsoft OneDrive İş klasörüne kaydeder.

## <a name="business-scenario"></a>İş senaryosu

Microsoft Dynamics 365 tümleştirmeler için tipik bir iş senaryosunda, veriler yinelenen bir zamanlamaya göre bir aşağı akış sistemine aktarılmalıdır. Bu öğretici, Microsoft Dynamics 365 Human Resources'taki tüm çalışan kayıtlarının nasıl dışa aktarılacağını ve bir OneDrive İş klasöründeki çalışan listesinin nasıl kaydedileceğini göstermektedir.

> [!TIP]
> Bu öğreticideki dışa aktarılmış belirli veriler ve dışa aktarılan verilerin hedefi yalnızca birer örnektir. Bunları iş gereksinimlerinizi karşılayacak şekilde kolayca değiştirebilirsiniz.

## <a name="technologies-used"></a>Kullanılan teknolojiler

Bu öğretici aşağıdaki teknolojileri kullanmaktadır:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)**– Dışa aktarılacak çalışanlar için ana veri kaynağı.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – Yinelenen dışa aktarmanın düzenleme ve zamanlamasını sağlayan teknoloji.

    - **[Bağlayıcılar](/azure/connectors/apis-list)** – Mantık uygulamasını gerekli uç noktalara bağlamak için kullanılan teknoloji.

        - [HTTP with Azure AD](/connectors/webcontents/) bağlayıcısı
        - [OneDrive İş](/azure/connectors/connectors-create-api-onedriveforbusiness) bağlayıcısı

- **[DMF paket REST API'sı](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – Dışa aktarma işlemini tetiklemek ve ilerlemesini izlemek için kullanılan teknoloji.
- **[OneDrive İş](https://onedrive.live.com/about/business/)** – Dışa aktarılan çalışanlar için hedef.

## <a name="prerequisites"></a>Önkoşullar

Bu öğreticideki alıştırmaya başlamadan önce aşağıdaki öğelere sahip olmanız gerekir:

- Ortamda yönetici düzeyinde izinleri olan bir İnsan Kaynakları ortamı
- Mantık uygulamasını barındıracak bir [Azure aboneliği](https://azure.microsoft.com/free/)

## <a name="the-exercise"></a>Alıştırma

Bu alıştırmanın sonunda, İnsan Kaynakları ortamınıza ve OneDrive İş hesabınıza bağlı bir mantık uygulamasına sahip olacaksınız. Mantık uygulaması, İnsan Kaynakları'ndan bir veri paketini dışa aktarır, dışa aktarmanın tamamlanmasını bekler, dışa aktarılan veri paketini indirir ve veri paketini belirttiğiniz OneDrive İş klasörüne kaydeder.

Tamamlanmış mantık uygulaması aşağıdaki çizime benzeyecektir.

![Mantık uygulamasına genel bakış.](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>Adım 1: İnsan Kaynakları'nda bir veri dışa aktarma projesi oluşturun

İnsan Kaynakları'nda çalışanları dışa aktaran bir veri dışa aktarma projesi oluşturun. Projeye **Çalışanları Dışa Aktar** adını verin ve **Veri paketi oluştur** seçeneğinin **Evet** olarak ayarlandığından emin olun. Projeye tek bir varlık (**Çalışan**) ekleyin ve dışa aktarma biçimini seçin. (Bu öğreticide Microsoft Excel biçimi kullanılmaktadır.)

![Çalışanları Dışa Aktar veri projesi.](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> Veri dışa aktarma projesinin adını unutmayın. Sonraki adımda mantık uygulaması oluşturduğunuz zaman buna gereksiniminiz olacak.

### <a name="step-2-create-the-logic-app"></a>Adım 2: Mantık uygulamasını oluşturun

Alıştırmanın büyük kısmı, mantık uygulamasını oluşturmayla ilgilidir.

1. Azure portalında bir mantık uygulaması oluşturun.

    ![Mantık uygulaması oluşturma sayfası.](media/integration-logic-app-creation-1.png)

2. Logic Apps Designer'da boş bir mantık uygulamasıyla başlayın.
3. Mantık uygulamasını 24 saatte bir çalıştırmak için (veya istediğiniz zaman çizelgesine göre) bir [Yineleme Çizelgesi tetikleyicisi](/azure/connectors/connectors-native-recurrence) ekleyin.

    ![Yineleme iletişim kutusu.](media/integration-logic-app-recurrence-step.png)

4. Veri paketinizin dışa aktarılmasını zamanlamak için [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API'sını çağırın.

    1. HTTP with Azure AD bağlayıcısından **Bir HTTP isteği çağır** eylemini kullanın.

        - **Temel Kaynak URL'si:** İnsan Kaynakları ortamınızın URL'si (yol/ad alanı bilgilerini eklemeyin.)
        - **Azure AD Kaynak URI'sı:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > İnsan Kaynakları hizmeti, DMF Paket REST API'sını oluşturan, **ExportToPackage** gibi tüm API'ları gösteren bir bağlayıcıyı henüz sağlamıyor. Bunun yerine, HTTP with Azure AD bağlayıcısıyla ham HTTPS isteklerini kullanarak API'ları çağırmanız gerekir. Bu bağlayıcı İnsan Kaynakları'nda kimlik doğrulama ve yetkilendirme için Azure Active Directory (Azure AD) kullanır.

        ![HTTP with Azure AD bağlayıcısı.](media/integration-logic-app-http-aad-connector-step.png)

    2. HTTP with Azure AD bağlayıcısını kullanarak İnsan Kaynakları ortamınızda oturum açın.
    3. **ExportToPackage** DMF REST API'sını çağırmak için bir HTTP **POST** isteği ayarlayın.

        - **Yöntem:** POST
        - **Talep Url'si:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **İsteğin gövdesi:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Bir HTTP isteği çağır eylemi.](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > Her adımı, varsayılan addan daha anlamlı olacak şekilde yeniden adlandırmak isteyebilirsiniz: **Bir HTTP isteği çağır**. Örneğin bu adımı **ExportToPackage** olarak yeniden adlandırabilirsiniz.

5. **ExportToPackage** isteğinin yürütme durumunu depolamak için [bir değişken başlatın](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable).

    ![Değişken başlatma eylemi.](media/integration-logic-app-initialize-variable-step.png)

6. Veri dışa aktarmanın yürütme durumu **Başarılı** olana kadar bekleyin.

    1. **ExecutionStatus** değişkeninin değeri **Başarılı** olana kadar yinelenen bir [Until döngüsü](/azure/logic-apps/logic-apps-control-flow-loops#until-loop) ekleyin.
    2. Dışa aktarmanın geçerli yürütme durumu için yoklamadan önce beş saniye bekleyen bir **Gecikme** eylemi ekleyin.

        ![Until döngüsü kapsayıcısı.](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > Dışa aktarmanın tamamlanması için maksimum 75 saniye (15 yineleme × 5 saniye) beklenmesi için limit sayısını **15** olarak ayarlayın. Dışa aktarma işleminiz daha uzun sürüyorsa, limit sayısını uygun şekilde ayarlayın.        

    3. [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API'yı çağırmak için bir **HTTP isteği çağır** eylemi ekleyin ve **ExecutionStatus** değişkenini **GetExecutionSummaryStatus** yanıtının sonucuna ayarlayın.

        > Bu örnek hata denetimi yapmaz. **GetExecutionSummaryStatus** API, başarılı olmayan nihai durumları (yani **Başarılı** dışındaki durumları) döndürebilir. Daha fazla bilgi için [API belgelerine](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) bakın.

        - **Yöntem:** POST
        - **Talep url'si:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **İsteğin gövdesi:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > **İsteğin gövdesi** değerini kod görünümünde veya tasarımcıdaki işlev düzenleyicisinde girmeniz gerekebilir.

        ![Bir HTTP isteği çağır 2 eylemi.](media/integration-logic-app-get-execution-status-step.png)

        ![Değişken ayarla eylemi.](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > **Değişken ayarla** eyleminin (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) değeri, tasarımcı değerleri aynı şekilde gösterse bile, **Bir HTTP isteği çağır 2** gövde değerinden farklı olacaktır.

7. Dışa aktarılan paketin indirme URL'sini alın.

    - [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API'yı çağırmak için bir **HTTP isteği çağır** eylemi ekleyin.

        - **Yöntem:** POST
        - **Talep URL'si:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **İsteğin gövdesi:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![GetExportedPackageURL eylemi.](media/integration-logic-app-get-exported-package-step.png)

8. Dışa aktarılan paketi indirin.

    - Paketi önceki adımda döndürülen URL'den indirmek için bir HTTP **GET** isteği ([yerleşik bir HTTP bağlayıcı eylemi](/azure/connectors/connectors-native-http)) ekleyin.

        - **Yöntem:** GET
        - **URI:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > **URI** değerini kod görünümünde veya tasarımcıdaki işlev düzenleyicisinde girmeniz gerekebilir.

        ![HTTP GET eylemi.](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > Bu istek herhangi bir ek kimlik doğrulaması gerektirmez çünkü **GetExportedPackageUrl** API'nın döndürdüğü URL, dosyayı indirmek için erişim izni veren bir paylaşılan bir erişim imzaları belirteci içerir.

9. İndirilen paketi [OneDrive İş](/azure/connectors/connectors-create-api-onedriveforbusiness) bağlayıcısı kullanarak kaydedin.

    - Bir OneDrive İş [Dosya Oluştur](/connectors/onedriveforbusinessconnector/#create-file) eylemi ekleyin.
    - Gerektiğinde OneDrive İş hesabınıza bağlanın.

        - **Klasör Yolu:** Seçtiğiniz bir klasör
        - **Dosya Adı:** worker\_package.zip
        - **Dosya İçeriği:** Önceki adımdaki gövde (dinamik içerik)

        ![Dosya oluştur eylemi.](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>Adım 3: Mantık uygulamasını test edin

Mantık uygulamanızı test etmek için tasarımcıda **Çalıştır** düğmesini seçin. Mantık uygulaması adımlarının çalışmaya başladığını göreceksiniz. 30-40 saniye sonra mantık uygulamasının çalışması sona erecek ve OneDrive İş klasörünüzde, dışa aktarılan çalışanların bulunduğu yeni bir paket dosyası yer alacaktır.

Herhangi bir adım için hata bildirilirse, tasarımcıda hatalı adımı seçin ve **Girdiler** ve **Çıktılar** alanlarını inceleyin. Hataları düzeltmek için adımda gerekli hata ayıklama ve düzeltme işlemlerini yapın.

Aşağıdaki çizim, mantık uygulamasının tüm adımları başarıyla çalıştırıldığı zaman Logic Apps Designer'ın nasıl göründüğünü gösterir.

![Başarılı mantık uygulaması çalışması.](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>Özet

Bu öğreticide, İnsan Kaynakları'ndan alınan verileri dışa aktarmak ve dışa aktarılan verileri bir OneDrive İş klasörüne kaydetmek için bir mantık uygulamasının nasıl kullanılacağını öğrendiniz. Bu öğreticinin adımlarını, iş gereksinimlerinize uygun şekilde değiştirebilirsiniz.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
