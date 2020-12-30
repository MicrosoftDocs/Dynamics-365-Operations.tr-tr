---
title: Yinelenen veri dışarı aktarma uygulaması oluşturma
description: Bu makalede, Microsoft Dynamics 365 Human Resources'tan alınan verileri yinelenen bir düzende dışa aktaran bir Microsoft Azure mantık uygulamasının nasıl oluşturulacağı gösterilmektedir.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: edd4b999624a845fc145ed9ff348ae9cba782719
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4420978"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="d49f8-103">Yinelenen veri dışarı aktarma uygulaması oluşturma</span><span class="sxs-lookup"><span data-stu-id="d49f8-103">Create a recurring data export app</span></span>

<span data-ttu-id="d49f8-104">Bu makalede, Microsoft Dynamics 365 Human Resources'tan alınan verileri yinelenen bir düzende dışa aktaran bir Microsoft Azure mantık uygulamasının nasıl oluşturulacağı gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="d49f8-105">Öğretici, verileri dışa aktarmak için İnsan Kaynakları'nın DMF Paket REST uygulama programlama arabirimini (API) kullanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d49f8-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="d49f8-106">Veriler dışa aktarıldıktan sonra, mantık uygulaması, dışa aktarılan veri paketini bir Microsoft OneDrive İş klasörüne kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d49f8-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="d49f8-107">İş senaryosu</span><span class="sxs-lookup"><span data-stu-id="d49f8-107">Business scenario</span></span>

<span data-ttu-id="d49f8-108">Microsoft Dynamics 365 tümleştirmeler için tipik bir iş senaryosunda, veriler yinelenen bir zamanlamaya göre bir aşağı akış sistemine aktarılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d49f8-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="d49f8-109">Bu öğretici, Microsoft Dynamics 365 Human Resources'taki tüm çalışan kayıtlarının nasıl dışa aktarılacağını ve bir OneDrive İş klasöründeki çalışan listesinin nasıl kaydedileceğini göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="d49f8-110">Bu öğreticideki dışa aktarılmış belirli veriler ve dışa aktarılan verilerin hedefi yalnızca birer örnektir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="d49f8-111">Bunları iş gereksinimlerinizi karşılayacak şekilde kolayca değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d49f8-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="d49f8-112">Kullanılan teknolojiler</span><span class="sxs-lookup"><span data-stu-id="d49f8-112">Technologies used</span></span>

<span data-ttu-id="d49f8-113">Bu öğretici aşağıdaki teknolojileri kullanmaktadır:</span><span class="sxs-lookup"><span data-stu-id="d49f8-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="d49f8-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)**– Dışa aktarılacak çalışanlar için ana veri kaynağı.</span><span class="sxs-lookup"><span data-stu-id="d49f8-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="d49f8-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – Yinelenen dışa aktarmanın düzenleme ve zamanlamasını sağlayan teknoloji.</span><span class="sxs-lookup"><span data-stu-id="d49f8-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="d49f8-116">**[Bağlayıcılar](https://docs.microsoft.com/azure/connectors/apis-list)** – Mantık uygulamasını gerekli uç noktalara bağlamak için kullanılan teknoloji.</span><span class="sxs-lookup"><span data-stu-id="d49f8-116">**[Connectors](https://docs.microsoft.com/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="d49f8-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="d49f8-117">[HTTP with Azure AD](https://docs.microsoft.com/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="d49f8-118">[OneDrive İş](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) bağlayıcısı</span><span class="sxs-lookup"><span data-stu-id="d49f8-118">[OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="d49f8-119">**[DMF paket REST API'sı](../dev-itpro/data-entities/data-management-api.md)** – Dışa aktarma işlemini tetiklemek ve ilerlemesini izlemek için kullanılan teknoloji.</span><span class="sxs-lookup"><span data-stu-id="d49f8-119">**[DMF package REST API](../dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="d49f8-120">**[OneDrive İş](https://onedrive.live.com/about/business/)** – Dışa aktarılan çalışanlar için hedef.</span><span class="sxs-lookup"><span data-stu-id="d49f8-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d49f8-121">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="d49f8-121">Prerequisites</span></span>

<span data-ttu-id="d49f8-122">Bu öğreticideki alıştırmaya başlamadan önce aşağıdaki öğelere sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="d49f8-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="d49f8-123">Ortamda yönetici düzeyinde izinleri olan bir İnsan Kaynakları ortamı</span><span class="sxs-lookup"><span data-stu-id="d49f8-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="d49f8-124">Mantık uygulamasını barındıracak bir [Azure aboneliği](https://azure.microsoft.com/free/)</span><span class="sxs-lookup"><span data-stu-id="d49f8-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="d49f8-125">Alıştırma</span><span class="sxs-lookup"><span data-stu-id="d49f8-125">The exercise</span></span>

<span data-ttu-id="d49f8-126">Bu alıştırmanın sonunda, İnsan Kaynakları ortamınıza ve OneDrive İş hesabınıza bağlı bir mantık uygulamasına sahip olacaksınız.</span><span class="sxs-lookup"><span data-stu-id="d49f8-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="d49f8-127">Mantık uygulaması, İnsan Kaynakları'ndan bir veri paketini dışa aktarır, dışa aktarmanın tamamlanmasını bekler, dışa aktarılan veri paketini indirir ve veri paketini belirttiğiniz OneDrive İş klasörüne kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d49f8-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="d49f8-128">Tamamlanmış mantık uygulaması aşağıdaki çizime benzeyecektir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-128">The completed logic app will resemble the following illustration.</span></span>

![Mantık uygulamasına genel bakış](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="d49f8-130">Adım 1: İnsan Kaynakları'nda bir veri dışa aktarma projesi oluşturun</span><span class="sxs-lookup"><span data-stu-id="d49f8-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="d49f8-131">İnsan Kaynakları'nda çalışanları dışa aktaran bir veri dışa aktarma projesi oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d49f8-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="d49f8-132">Projeye **Çalışanları Dışa Aktar** adını verin ve **Veri paketi oluştur** seçeneğinin **Evet** olarak ayarlandığından emin olun.</span><span class="sxs-lookup"><span data-stu-id="d49f8-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="d49f8-133">Projeye tek bir varlık (**Çalışan**) ekleyin ve dışa aktarma biçimini seçin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="d49f8-134">(Bu öğreticide Microsoft Excel biçimi kullanılmaktadır.)</span><span class="sxs-lookup"><span data-stu-id="d49f8-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Çalışanları Dışa Aktar veri projesi](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="d49f8-136">Veri dışa aktarma projesinin adını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-136">Remember the name of the data export project.</span></span> <span data-ttu-id="d49f8-137">Sonraki adımda mantık uygulaması oluşturduğunuz zaman buna gereksiniminiz olacak.</span><span class="sxs-lookup"><span data-stu-id="d49f8-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="d49f8-138">Adım 2: Mantık uygulamasını oluşturun</span><span class="sxs-lookup"><span data-stu-id="d49f8-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="d49f8-139">Alıştırmanın büyük kısmı, mantık uygulamasını oluşturmayla ilgilidir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="d49f8-140">Azure portalında bir mantık uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="d49f8-140">In the Azure portal, create a logic app.</span></span>

    ![Mantık uygulaması oluşturma sayfası](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="d49f8-142">Logic Apps Designer'da boş bir mantık uygulamasıyla başlayın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="d49f8-143">Mantık uygulamasını 24 saatte bir çalıştırmak için (veya istediğiniz zaman çizelgesine göre) bir [Yineleme Çizelgesi tetikleyicisi](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-143">Add a [Recurrence Schedule trigger](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Yineleme iletişim kutusu](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="d49f8-145">Veri paketinizin dışa aktarılmasını zamanlamak için [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API'sını çağırın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-145">Call the [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="d49f8-146">HTTP with Azure AD bağlayıcısından **Bir HTTP isteği çağır** eylemini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="d49f8-147">**Temel Kaynak URL'si:** İnsan Kaynakları ortamınızın URL'si (yol/ad alanı bilgilerini eklemeyin.)</span><span class="sxs-lookup"><span data-stu-id="d49f8-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="d49f8-148">**Azure AD Kaynak URI'sı:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="d49f8-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="d49f8-149">İnsan Kaynakları hizmeti, DMF Paket REST API'sını oluşturan, **ExportToPackage** gibi tüm API'ları gösteren bir bağlayıcıyı henüz sağlamıyor.</span><span class="sxs-lookup"><span data-stu-id="d49f8-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="d49f8-150">Bunun yerine, HTTP with Azure AD bağlayıcısıyla ham HTTPS isteklerini kullanarak API'ları çağırmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="d49f8-151">Bu bağlayıcı İnsan Kaynakları'nda kimlik doğrulama ve yetkilendirme için Azure Active Directory (Azure AD) kullanır.</span><span class="sxs-lookup"><span data-stu-id="d49f8-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP with Azure AD bağlayıcısı](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="d49f8-153">HTTP with Azure AD bağlayıcısını kullanarak İnsan Kaynakları ortamınızda oturum açın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="d49f8-154">**ExportToPackage** DMF REST API'sını çağırmak için bir HTTP **POST** isteği ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="d49f8-155">**Yöntem:** POST</span><span class="sxs-lookup"><span data-stu-id="d49f8-155">**Method:** POST</span></span>
        - <span data-ttu-id="d49f8-156">**Talep Url'si:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="d49f8-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="d49f8-157">**İsteğin gövdesi:**</span><span class="sxs-lookup"><span data-stu-id="d49f8-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Bir HTTP isteği çağır eylemi](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="d49f8-159">Her adımı, varsayılan addan daha anlamlı olacak şekilde yeniden adlandırmak isteyebilirsiniz: **Bir HTTP isteği çağır**.</span><span class="sxs-lookup"><span data-stu-id="d49f8-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="d49f8-160">Örneğin bu adımı **ExportToPackage** olarak yeniden adlandırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d49f8-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="d49f8-161">**ExportToPackage** isteğinin yürütme durumunu depolamak için [bir değişken başlatın](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable).</span><span class="sxs-lookup"><span data-stu-id="d49f8-161">[Initialize a variable](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Değişken başlatma eylemi](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="d49f8-163">Veri dışa aktarmanın yürütme durumu **Başarılı** olana kadar bekleyin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="d49f8-164">**ExecutionStatus** değişkeninin değeri **Başarılı** olana kadar yinelenen bir [Until döngüsü](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-164">Add an [Until loop](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="d49f8-165">Dışa aktarmanın geçerli yürütme durumu için yoklamadan önce beş saniye bekleyen bir **Gecikme** eylemi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Until döngüsü kapsayıcısı](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="d49f8-167">Dışa aktarmanın tamamlanması için maksimum 75 saniye (15 yineleme × 5 saniye) beklenmesi için limit sayısını **15** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="d49f8-168">Dışa aktarma işleminiz daha uzun sürüyorsa, limit sayısını uygun şekilde ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="d49f8-169">[GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API'yı çağırmak için bir **HTTP isteği çağır** eylemi ekleyin ve **ExecutionStatus** değişkenini **GetExecutionSummaryStatus** yanıtının sonucuna ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="d49f8-170">Bu örnek hata denetimi yapmaz.</span><span class="sxs-lookup"><span data-stu-id="d49f8-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="d49f8-171">**GetExecutionSummaryStatus** API, başarılı olmayan nihai durumları (yani **Başarılı** dışındaki durumları) döndürebilir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="d49f8-172">Daha fazla bilgi için [API belgelerine](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) bakın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-172">For more information, see the [API documentation](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="d49f8-173">**Yöntem:** POST</span><span class="sxs-lookup"><span data-stu-id="d49f8-173">**Method:** POST</span></span>
        - <span data-ttu-id="d49f8-174">**Talep url'si:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="d49f8-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="d49f8-175">**İsteğin gövdesi:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="d49f8-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="d49f8-176">**İsteğin gövdesi** değerini kod görünümünde veya tasarımcıdaki işlev düzenleyicisinde girmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![Bir HTTP isteği çağır 2 eylemi](media/integration-logic-app-get-execution-status-step.png)

        ![Değişken ayarla eylemi](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="d49f8-179">**Değişken ayarla** eyleminin değeri (**body('Invoke\_an\_HTTP\_request\_2')?['value']**), tasarımcı değerleri aynı şekilde gösterse bile, **Bir HTTP isteği çağır 2** gövde değerinin değerinden farklı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d49f8-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="d49f8-180">Dışa aktarılan paketin indirme URL'sini alın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="d49f8-181">[GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API'yı çağırmak için bir **HTTP isteği çağır** eylemi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="d49f8-182">**Yöntem:** POST</span><span class="sxs-lookup"><span data-stu-id="d49f8-182">**Method:** POST</span></span>
        - <span data-ttu-id="d49f8-183">**Talep URL'si:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="d49f8-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="d49f8-184">**İsteğin gövdesi:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="d49f8-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![GetExportedPackageURL eylemi](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="d49f8-186">Dışa aktarılan paketi indirin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-186">Download the exported package.</span></span>

    - <span data-ttu-id="d49f8-187">Paketi önceki adımda döndürülen URL'den indirmek için bir HTTP **GET** isteği ([yerleşik bir HTTP bağlayıcı eylemi](https://docs.microsoft.com/azure/connectors/connectors-native-http)) ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-187">Add an HTTP **GET** request (a built-in [HTTP connector action](https://docs.microsoft.com/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="d49f8-188">**Yöntem:** GET</span><span class="sxs-lookup"><span data-stu-id="d49f8-188">**Method:** GET</span></span>
        - <span data-ttu-id="d49f8-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="d49f8-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="d49f8-190">**URI** değerini kod görünümünde veya tasarımcıdaki işlev düzenleyicisinde girmeniz gerekebilir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP GET eylemi](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="d49f8-192">Bu istek herhangi bir ek kimlik doğrulaması gerektirmez çünkü **GetExportedPackageUrl** API'nın döndürdüğü URL, dosyayı indirmek için erişim izni veren bir paylaşılan bir erişim imzaları belirteci içerir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="d49f8-193">İndirilen paketi [OneDrive İş](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) bağlayıcısı kullanarak kaydedin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-193">Save the downloaded package by using the [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="d49f8-194">Bir OneDrive İş [Dosya Oluştur](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) eylemi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-194">Add a OneDrive for Business [Create File](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="d49f8-195">Gerektiğinde OneDrive İş hesabınıza bağlanın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="d49f8-196">**Klasör Yolu:** Seçtiğiniz bir klasör</span><span class="sxs-lookup"><span data-stu-id="d49f8-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="d49f8-197">**Dosya Adı:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="d49f8-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="d49f8-198">**Dosya İçeriği:** Önceki adımdaki gövde (dinamik içerik)</span><span class="sxs-lookup"><span data-stu-id="d49f8-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Dosya oluştur eylemi](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="d49f8-200">Adım 3: Mantık uygulamasını test edin</span><span class="sxs-lookup"><span data-stu-id="d49f8-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="d49f8-201">Mantık uygulamanızı test etmek için tasarımcıda **Çalıştır** düğmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="d49f8-202">Mantık uygulaması adımlarının çalışmaya başladığını göreceksiniz.</span><span class="sxs-lookup"><span data-stu-id="d49f8-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="d49f8-203">30-40 saniye sonra mantık uygulamasının çalışması sona erecek ve OneDrive İş klasörünüzde, dışa aktarılan çalışanların bulunduğu yeni bir paket dosyası yer alacaktır.</span><span class="sxs-lookup"><span data-stu-id="d49f8-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="d49f8-204">Herhangi bir adım için hata bildirilirse, tasarımcıda hatalı adımı seçin ve **Girdiler** ve **Çıktılar** alanlarını inceleyin.</span><span class="sxs-lookup"><span data-stu-id="d49f8-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="d49f8-205">Hataları düzeltmek için adımda gerekli hata ayıklama ve düzeltme işlemlerini yapın.</span><span class="sxs-lookup"><span data-stu-id="d49f8-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="d49f8-206">Aşağıdaki çizim, mantık uygulamasının tüm adımları başarıyla çalıştırıldığı zaman Logic Apps Designer'ın nasıl göründüğünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="d49f8-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Başarılı mantık uygulaması çalışması](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="d49f8-208">Özet</span><span class="sxs-lookup"><span data-stu-id="d49f8-208">Summary</span></span>

<span data-ttu-id="d49f8-209">Bu öğreticide, İnsan Kaynakları'ndan alınan verileri dışa aktarmak ve dışa aktarılan verileri bir OneDrive İş klasörüne kaydetmek için bir mantık uygulamasının nasıl kullanılacağını öğrendiniz.</span><span class="sxs-lookup"><span data-stu-id="d49f8-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="d49f8-210">Bu öğreticinin adımlarını, iş gereksinimlerinize uygun şekilde değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d49f8-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>


