---
title: İş belgesi yönetiminde yeni belge kullanıcı arabirimi
description: Bu konu, Elektronik raporlamanın İş belge yönetimi özelliğindeki yeni belge kullanıcı arabiriminin nasıl kullanılacağı hakkında bilgi vermektedir.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 64ac52385ae6145f7428ebbc3cb77e395557bce2
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092237"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="2f566-103">İş belgesi yönetiminde yeni belge kullanıcı arabirimi</span><span class="sxs-lookup"><span data-stu-id="2f566-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f566-104">İş belgesi yönetimi iş kullanıcılarının Microsoft 365 hizmeti veya uygun Microsoft Office masaüstü uygulamasını kullanarak iş belgesi şablonlarını düzenlemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="2f566-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="2f566-105">Düzenlemeler tasarım değişiklikleri veya yeni dağıtımlar içerebilir ya da kullanıcılar kaynak kodunu değiştirmeden ek veri eklemek için yer tutucular ekleyebilirler.</span><span class="sxs-lookup"><span data-stu-id="2f566-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="2f566-106">İş belgesi yönetimiyle nasıl çalışılacağı hakkında daha fazla bilgi için bkz. [İş belgesi yönetimine genel bakış](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="2f566-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="2f566-107">Yeni belge kullanıcı arabirimi (UI) daha net ve kullanımı daha rahat.</span><span class="sxs-lookup"><span data-stu-id="2f566-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="2f566-108">**İş belgesi** alanı, yalnızca, geçerli sağlayıcı için kullanılabilen şablonları gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f566-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="2f566-109">**Yeni belge** düğmesi, kullanıcıların başka bir sağlayıcı tarafından sağlanan bir Elektronik raporlama (ER) biçimi yapılandırmasında şablon oluşturmalarına ve düzenlemelerine olanak sağlar.</span><span class="sxs-lookup"><span data-stu-id="2f566-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="2f566-110">Bu konudaki örnekte sağlayıcı Microsoft'tur.</span><span class="sxs-lookup"><span data-stu-id="2f566-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="2f566-111">İş belgesi yönetiminde yeni belge kullanıcı arabirimini kullanıma açma</span><span class="sxs-lookup"><span data-stu-id="2f566-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="2f566-112">İş belgesi yönetiminde yeni belge kullanıcı arabirimini kullanmaya başlamak için,**Özellik yönetimi** çalışma alanındaki **İş belgesi yönetimi için Office benzeri arabirim deneyimi** özelliğini açmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2f566-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="2f566-113">Bu özelliği tüm tüzel kişilikler için açmak üzere bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="2f566-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="2f566-114">**Özellik yönetimi** çalışma alanında, **Yeni** sekmesinde, listeden **İş belgesi yönetimi için Office benzeri arabirim deneyimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="2f566-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="2f566-115">Seçili özelliği açmak için **Şimdi etkinleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="2f566-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="2f566-116">Yeni özelliğe erişmek için sayfayı yenileyin.</span><span class="sxs-lookup"><span data-stu-id="2f566-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="2f566-117">Sahibi diğer sağlayıcılar olan düzenleme şablonları</span><span class="sxs-lookup"><span data-stu-id="2f566-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="2f566-118">**İş belgesi yönetimi** çalışma alanında **Yeni belge**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="2f566-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![İş belgesi yönetimi çalışma alanı](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="2f566-120">İletişim kutusunda, şablon olarak kullanılacak belgeyi ve ardından **Belge oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="2f566-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![İş belgeleri iletişim kutusu](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="2f566-122">Yeni iletişim kutusunda, **Başlık** alanında, başlığı gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2f566-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="2f566-123">Başlık metni, otomatik olarak oluşturulan yeni ER biçimi yapılandırmasını adlandırmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2f566-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="2f566-124">Bu yapılandırmanın taslak sürümü (**Müşteri FTI raporu (GER) kopyası**) düzenlenen şablonu içerir ve bu ER biçimini geçerli kullanıcı için çalıştırmak üzere kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2f566-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="2f566-125">Temel ER biçimi yapılandırmasındaki özgün şablon, diğer kullanıcıların tümü için bu ER biçimini çalıştırmada kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="2f566-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="2f566-126">**Ad** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak ilk revizyonunun adını değiştirin.</span><span class="sxs-lookup"><span data-stu-id="2f566-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="2f566-127">**Yorum** alanında, düzenlenebilir şablonun otomatik olarak oluşturulacak revizyonuna için yorumları güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="2f566-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="2f566-128">Düzenleme işleminin başlangıcını onaylamak için **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="2f566-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![Belge oluşturma iletişim kutusu](./media/BDM_overview_new_template3.png)

<span data-ttu-id="2f566-130">**Yeni belge** düğmesi, kullanıcıların başka bir sağlayıcı tarafından sağlanan bir ER biçimi yapılandırmasında şablon oluşturmak ve düzenlemek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="2f566-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="2f566-131">Bu örnekte sağlayıcı Microsoft'tur.</span><span class="sxs-lookup"><span data-stu-id="2f566-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="2f566-132">**Yeni belge**'yi seçtiğiniz zaman, sahibi geçerli ve diğer sağlayıcılar olan tüm şablonları görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2f566-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="2f566-133">Siz şablonu seçtikten sonra şablon düzenleme için açılır.</span><span class="sxs-lookup"><span data-stu-id="2f566-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="2f566-134">Düzenlenen şablon daha sonra otomatik olarak oluşturulan yeni bir ER biçim yapılandırması içinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="2f566-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="2f566-135">Daha fazla bilgi için bkz. [İş belgesi yönetimine genel bakış](er-business-document-management.md).</span><span class="sxs-lookup"><span data-stu-id="2f566-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>
