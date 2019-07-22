---
title: RCS ve ER için uygulamaya özel meta verileri hazırlama
description: Bu konu, Regulatory Configuration Service (RCS) ve Elektronik Raporlama (ER) için uygulamaya özel meta verilerin nasıl hazırlanacağını açıklamaktadır.
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 289f901501a68319c9d85e993d8dfbfc3838a8eb
ms.sourcegitcommit: d940c7892b6caa6141b3bda8abf1c56e9df4687a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726444"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a><span data-ttu-id="a0bd2-103">RCS için uygulamaya özel meta veriler hazırlama</span><span class="sxs-lookup"><span data-stu-id="a0bd2-103">Prepare application-specific metadata for RCS</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a0bd2-104">Bu konu, aşağıdaki görevlere örnekler konusunda size yol gösterecektir:</span><span class="sxs-lookup"><span data-stu-id="a0bd2-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="a0bd2-105">RCS'de kullanılabilecek uygulama meta verileri hazırlama</span><span class="sxs-lookup"><span data-stu-id="a0bd2-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="a0bd2-106">Bir ER yapılandırması kullanarak uygulama meta verilerine erişme</span><span class="sxs-lookup"><span data-stu-id="a0bd2-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="a0bd2-107">Bağlı uygulamalar kullanarak uygulama meta verilerine erişme</span><span class="sxs-lookup"><span data-stu-id="a0bd2-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="a0bd2-108">RCS'de kullanılabilecek uygulama meta verileri hazırlama</span><span class="sxs-lookup"><span data-stu-id="a0bd2-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="a0bd2-109">Aşağıdaki prosedürde **Sistem Yöneticisi** ya da **Elektronik Raporlama Geliştirici** rolüne sahip Finance and Operations kullanıcısının Microsoft Dynamics 365 for Finance and Operations uygulaması içeren meta verileri içeren Elektronik raporlama (ER) yapılandırması oluşturup oluşturamayacağını gösterir ve bu Regulatory Configuration Service (RCS)'deki ER model eşleme yapılandırmalarını tasarlamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-109">The following procedure shows how a user of Finance and Operations who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the Microsoft Dynamics 365 for Finance and Operations application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="a0bd2-110">Bu örnekte oluşturulan örnek ER model eşleme yapılandırması, dış ticaret hareketlerine erişmek için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="a0bd2-111">Bu örnek için, dış ticari işletme etki alanındaki bilgileri içeren elektronik belgeler oluşturmak amacıyla kullanılacak Finance and Operations'a bir ER çözümü tasarlamak için RCS'yi kullanmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-111">For this example, you want to use RCS to design an ER solution for Finance and Operations that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="a0bd2-112">ER veri modeliyle gerekli verilerin kaynakları arasındaki eşlemeyi belirtmek amacıyla RCS'de Finance and Operations için uygulama meta verilerine erişiminizin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata for Finance and Operations in RCS.</span></span> <span data-ttu-id="a0bd2-113">Bu nedenle, ER çözümünü tasarlama sürecinin bir parçası olarak, seçilen iş etki alanı için ER raporları oluşturmak üzere gerekli olan tüm meta verileri içeren yeni bir ER meta veri yapılandırması yapılandırmalısınız.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="a0bd2-114">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="a0bd2-115">**Organizasyon yönetimi \> Çalışma alanları \> Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a0bd2-116">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="a0bd2-117">Bu yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedürünü tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-117">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="a0bd2-118">**Meta veri yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="a0bd2-119">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="a0bd2-120">Açılır menüdeki iletişim kutusunda, **Ad** alanına bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="a0bd2-121">Bu örnek için, **Dış ticaret meta verileri** girin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="a0bd2-122">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="a0bd2-123">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-123">Select **Designer**.</span></span>
8. <span data-ttu-id="a0bd2-124">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0bd2-125">Tüm uygulama, seçili model ya da modüller için tüm meta verileri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="a0bd2-126">Her iki durumda da aşağıdaki meta verilerin otomatik olarak eklenebileceğine dikkat edin: kayıt tabloları, numaralandırmalar ve genişletilmiş veri türleri (EDTs).</span><span class="sxs-lookup"><span data-stu-id="a0bd2-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="a0bd2-127">Ek meta veri türleri gerektiğinde, bunların el ile eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-127">When additional types of metadata are required, they must be manually added.</span></span>

<span data-ttu-id="a0bd2-128">Dış ticari hareketlerle ilgili bazı meta verileri eklemeniz ve meta veri öğelerini el ile seçmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="a0bd2-129">**Veri kaynağı ekle \> Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="a0bd2-130">**Ad** alanında **İntrastat** değerine filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="a0bd2-131">**Intrastat** tablosu kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="a0bd2-132">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-132">Select **OK**.</span></span>

<span data-ttu-id="a0bd2-133">Intrastat kayıt tablosu hakkında meta veri bilgileri eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="a0bd2-134">Ağaçta **Tablo kayıtları İntrastatı \> \>İlişkiler \> IntrastatCommodity (Tablo kayıtları EcoResCategory)**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="a0bd2-135">**Meta veri ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0bd2-136">Seçili kayıt tablosu için gerekli ilişkilerindeki meta veriler el ile eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="a0bd2-137">**Veri kaynağını ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="a0bd2-138">**Numaralandırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="a0bd2-139">**Ad** alanında **IntrastatDirection** değerine filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="a0bd2-140">**IntrastatDirection** numaralandırma kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="a0bd2-141">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-141">Select **OK**.</span></span>
20. <span data-ttu-id="a0bd2-142">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-142">Select **Save**.</span></span>
21. <span data-ttu-id="a0bd2-143">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-143">Close the page.</span></span>
22. <span data-ttu-id="a0bd2-144">Meta veri yapılandırmasının taslak sürümünü tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="a0bd2-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="a0bd2-145">**Durumu değiştir \> Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="a0bd2-146">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-146">Select **OK**.</span></span>
    3. <span data-ttu-id="a0bd2-147">Tamamlanmış sürüm 1'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="a0bd2-148">Meta veri yapılandırmasının tamamlanan sürümünü uygulamadan XML dosyası olarak dışarı aktarın:</span><span class="sxs-lookup"><span data-stu-id="a0bd2-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="a0bd2-149">**Değiştir \> XML dosyasını dışa aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="a0bd2-150">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-150">Select **OK**.</span></span>

<span data-ttu-id="a0bd2-151">Oluşturduğunuz ER meta veri yapılandırması, **Dış ticaret meta verileri.xml** dosyası olarak kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="a0bd2-152">Finance and Operations dış ticari iş etki alanı için meta veri kaynağı olarak kullanılabilmesi amacıyla bunu RCS'de içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain in Finance and Operations.</span></span> <span data-ttu-id="a0bd2-153">Bu bilgiye dayanarak uygulama meta verileri ve ER veri modeli arasındaki eşlemeyi belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="a0bd2-154">Bir ER yapılandırması kullanarak uygulama meta verilerine erişme</span><span class="sxs-lookup"><span data-stu-id="a0bd2-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="a0bd2-155">Aşağıdaki prosedürde **Sistem Yöneticisi** ya da **Elektronik Raporlama Geliştirici** rolüne sahip bir RCS kullanıcısının Finance and Operations uygulamasından meta verileri kullanarak yeni bir ER model eşlemesi tasarlayabileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the Finance and Operations application.</span></span> <span data-ttu-id="a0bd2-156">Uygulama meta verilerine, dış ticari hareketlere erişmek için örnek bir meta veri kümesi içeren ER meta veri yapılandırması kullanılarak erişilir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="a0bd2-157">Bu prosedürü tamamlamadan önce aşağıdaki prosedürleri tamamlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="a0bd2-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="a0bd2-158">Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme</span><span class="sxs-lookup"><span data-stu-id="a0bd2-158">Create a configuration provider and mark it as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="a0bd2-159">RCS'de kullanılabilecek uygulama meta verileri hazırlama</span><span class="sxs-lookup"><span data-stu-id="a0bd2-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="a0bd2-160">**Tüm çalışma alanları \> Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a0bd2-161">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="a0bd2-162">Bu yapılandırma sağlayıcısını göremiyorsanız [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedürünü tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-162">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="a0bd2-163">Dış ticari etki alanı elektronik belge oluşturmak üzere yapılandırılmış olan Finance and Operations uygulaması için meta veriler içeren ER meta veri yapılandırmasını içe aktarın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-163">Import the ER metadata configuration that contains metadata for the Finance and Operations application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="a0bd2-164">Bu ER meta veri yapılandırmasını daha önce bu konuda oluşturdunuz ve[RCS'de kullanılabilecek uygulama meta verileri hazırlama](#prepare-application-metadata-that-can-be-used-in-rcs) prosedüründe XML dosyası olarak dışa aktardınız.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="a0bd2-165">**Meta veri yapılandırması**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="a0bd2-166">**Döviz**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="a0bd2-167">**XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="a0bd2-168">**Dış ticaret meta verileri.xml** dosyasını seçmek için gözatın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="a0bd2-169">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-169">Select **OK**.</span></span>
    6. <span data-ttu-id="a0bd2-170">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-170">Close the page.</span></span>

4. <span data-ttu-id="a0bd2-171">Bir veri modeli yapılandırması oluşturun:</span><span class="sxs-lookup"><span data-stu-id="a0bd2-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="a0bd2-172">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="a0bd2-173">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="a0bd2-174">Açılır menüdeki iletişim kutusunda, **Ad** alanına **Dış ticaret modeli** girin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="a0bd2-175">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="a0bd2-176">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="a0bd2-177">Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="a0bd2-178">**Ad** alanına **Kök** yazın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="a0bd2-179">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="a0bd2-180">Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="a0bd2-181">**Ad** alanına **Hareket** yazın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="a0bd2-182">**Madde türü** alanında **Kayıt listesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="a0bd2-183">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="a0bd2-184">Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="a0bd2-185">**Ad** alanına **Emtia kodu** yazın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="a0bd2-186">**Madde türü** alanında **Dize**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="a0bd2-187">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-187">Select **Add**.</span></span>

    9. <span data-ttu-id="a0bd2-188">Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="a0bd2-189">Ad alanına **Faturalanan tutar**.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="a0bd2-190">**Madde türü** alanında **Gerçek**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="a0bd2-191">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-191">Select **Add**.</span></span>

    10. <span data-ttu-id="a0bd2-192">Açılır iletişim kutusunu açmak için **Yeni** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="a0bd2-193">**Ad** alanına **Tarih** yazın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="a0bd2-194">**Madde türü** alanında **Tarih**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="a0bd2-195">**Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="a0bd2-196">**Ekle \> Kök referansı**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="a0bd2-197">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-197">Select **OK**.</span></span>
    13. <span data-ttu-id="a0bd2-198">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-198">Select **Save**.</span></span>
    14. <span data-ttu-id="a0bd2-199">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-199">Close the page.</span></span>
    15. <span data-ttu-id="a0bd2-200">**Durumu değiştir \> Tamamla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="a0bd2-201">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-201">Select **OK**.</span></span>

5. <span data-ttu-id="a0bd2-202">Model eşleme yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="a0bd2-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="a0bd2-203">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="a0bd2-204">Açılır menüdeki iletişim kutusunda **Yeni** alanında **Dış ticaret modeli veri modelini temel alan Model Eşleme** girin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="a0bd2-205">**Ad** alanına **Dış ticaret eşlemesi** girin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="a0bd2-206">**Yapılandırma oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="a0bd2-207">**Önkoşullar** hızlı sekmesinde **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="a0bd2-208">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-208">Select **New**.</span></span>
    7. <span data-ttu-id="a0bd2-209">**Önkoşul bileşen türü** alanında **Yapılandırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="a0bd2-210">**Dış ticaret meta veri** yapılandırılmasını seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="a0bd2-211">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-211">Select **Save**.</span></span> <span data-ttu-id="a0bd2-212">**Dış ticaret meta verileri** yapılandırmasındaki sürüm 1'e referans eklendiğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="a0bd2-213">Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verisi sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="a0bd2-214">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-214">Close the page.</span></span>
    11. <span data-ttu-id="a0bd2-215">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="a0bd2-216">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="a0bd2-217">Ağaçta**Dynamics 365 for Operations \> Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="a0bd2-218">**Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="a0bd2-219">**Ad** alanına, **İntrastat** girin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="a0bd2-220">**Intrastat** tablosu kayıtlarını seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="a0bd2-221">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a0bd2-222">Şu anda kullanılmakta olan meta veri kümesine sadece iki tablo eklendiğinden sadece iki tablo kullanıldı</span><span class="sxs-lookup"><span data-stu-id="a0bd2-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="a0bd2-223">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="a0bd2-224">Ağaçta **İntrastat \> AmountMST**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="a0bd2-225">Ağaçta **Hareket = İntrastat \> Faturalanan tutar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="a0bd2-226">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="a0bd2-227">Ağaçta **İntrastat \> TransDate**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="a0bd2-228">Ağaçta **Hareket = İntrastat \> Tarih**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="a0bd2-229">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="a0bd2-230">Ağaçta **İntrastat \> \>İlişkiler \> IntrastatCommodity \> Kod**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="a0bd2-231">Ağaçta **Hareket = İntrastat \> Emtia kodu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="a0bd2-232">**Bağla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="a0bd2-233">**Doğrula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a0bd2-234">Doğrulama tamamlandıktan sonra belirtilen veri kaynağı öğeleriyle, başvurulan ER meta veri yapılandırmasından uygulama meta verilerinin ayrıntılarını kullanarak tanımlanan veri modeli öğelerini başarıyla bağladınız.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="a0bd2-235">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-235">Select **Save**.</span></span>

<span data-ttu-id="a0bd2-236">Varolan meta veri kümesini genişletmek istediğinizde bunu Finance and Operations'tan yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-236">As you require, you can extend the existing set of metadata in Finance and Operations.</span></span> <span data-ttu-id="a0bd2-237">ER meta veri yapılandırmasının yeni sürümünü Finance and Operations'tan içe aktarabilir, bunları RCS 'ye aktarabilir ve alınan meta veri yapılandırmasının yeni sürümüne başvuran yapılandırılmış model eşleme yapılandırmasının önkoşullarını güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-237">You can then export the new completed version of the ER metadata configuration from Finance and Operations, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="a0bd2-238">Uygulama meta verileri hakkında bilgi elde etmenin bu yolu, yerel işletme verileri (LBD) veya yerel olarak dağıtılmış uygulamalar için kullanılabilecek tek yoldur (yerel işletme verileri \[LBD\], ya da or şirket içi dağıtım modeli Finance and Operations için kullanılır).</span><span class="sxs-lookup"><span data-stu-id="a0bd2-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for Finance and Operations).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="a0bd2-239">Bağlı uygulamalar kullanarak uygulama meta verilerine erişme</span><span class="sxs-lookup"><span data-stu-id="a0bd2-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="a0bd2-240">Aşağıdaki prosedürde **Sistem Yöneticisi** ya da **Elektronik Raporlama Geliştirici** rolüne sahip bir RCS kullanıcısının Finance and Operations uygulamasından meta verileri kullanarak yeni bir ER model eşlemesi tasarlayabileceği gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the Finance and Operations application.</span></span> <span data-ttu-id="a0bd2-241">RCS bağlantılı uygulama kullanılarak uygulama meta verilerine çevrimiçi olarak erişilir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="a0bd2-242">Örnek ER model eşlemesi, dış ticari hareketlere erişmek üzere yapılandırılacak.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="a0bd2-243">Bu prosedürdeki adımları tamamlamak için öncelikle RCS'deki [Yapılandırma sağlayıcısı oluşturma ve etkin olarak işaretleme](tasks/er-configuration-provider-mark-it-active-2016-11.md) prosedürünü tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-243">To complete this procedure, you must first complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="a0bd2-244">Bu prosedürdeki [Bir ER yapılandırması kullanarak uygulama meta verilerine erişme](#access-application-metadata-by-using-an-er-configuration)'yi tamamlamadıysanız aşağıdaki ER yapılandırma dosyalarını önceden indirmek ve yerel olarak kaydetmek için [Dynamics 365 for Finance and Operations 8.1 için Elektronik Raporlama Görev Kılavuzu](https://go.microsoft.com/fwlink/?linkid=2082739) sayfasına gidin: **Foreign trade metadata.xml**, **Foreign trade model.xml**, ve **Foreign trade mapping.xml**.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="a0bd2-245">Gerekli ER yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="a0bd2-245">Get required ER configurations</span></span>

<span data-ttu-id="a0bd2-246">[(RCS) Access application metadata by using ER configuration](#access-application-metadata-by-using-an-er-configuration) prosedüründeki adımları daha önce bu konuda tamamladıysanız mevcut RCS örneğinde gerekli tüm ER yapılandırmalarına (dış ticaret meta verileri, model ve harita yapılandırmaları) zaten sahipsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="a0bd2-247">Bu durumda, bu prosedürü atlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="a0bd2-248">**Tüm çalışma alanları \> Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a0bd2-249">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="a0bd2-250">**Dış ticaret meta verileri.xml**, **Dış ticaret modeli.xml**, and **Dış ticaret eşleme.xml** yapılandırma dosyaları için aşağıdaki adımlar zincirini tamamlayarak yükleyin:</span><span class="sxs-lookup"><span data-stu-id="a0bd2-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="a0bd2-251">**Döviz**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="a0bd2-252">**XML dosyasından yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="a0bd2-253">**Gözat**'ı seçin ve bir dosya seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="a0bd2-254">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-finance-and-operations"></a><span data-ttu-id="a0bd2-255">Finance and Operations ile bağlantıyı kaydetme</span><span class="sxs-lookup"><span data-stu-id="a0bd2-255">Register the connection with Finance and Operations</span></span>

1. <span data-ttu-id="a0bd2-256">**Tüm çalışma alanları \> Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a0bd2-257">**Bağlı uygulamalar**ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="a0bd2-258">Yapılandırılan uygulamanın Microsoft Azure'e bağlı olduğundan ve genel RCS kullanıcıları tarafından erişilebilir olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="a0bd2-259">Ayrıca geçerli RCS kullanıcısının seçilen yapılandırılmış uygulamaya erişimi olması ve uygulamanın meta verilerine erişim ayrıcalıkları veren bu uygulamanın bir kullanıcı olarak kayıtlı olması da gerekir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="a0bd2-260">**Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-260">Select **New**.</span></span>
5. <span data-ttu-id="a0bd2-261">**Ad** alanına, bağlı uygulamanın adı olarak **MyConnectedApp** girin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="a0bd2-262">**Uygulama** alanında, uygulamanın URL'sini belirtin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="a0bd2-263">**Kiracı** alanında, uygulamanın sağlayıcısını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="a0bd2-264">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-264">Select **Save**.</span></span> 
9. <span data-ttu-id="a0bd2-265">Yapılandırılmış uygulamaya olan bağlantıyı denetlediğinizde **Uzak uygulamaya bağlan** sayfasında **Seçilen uzak uygulama bağlantısına bağlanmak için buraya tıklayın**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="a0bd2-266">Yapılandırılan uygulamaya erişimi doğrulamak için **Bağlantıyı kontrol et**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="a0bd2-267">**Kapat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-267">Select **Close**.</span></span>

<span data-ttu-id="a0bd2-268">Bu prosedürü ve bağlantı doğrulaması başarılıyla tamamladığınızda geçerli kılavuzda yapılandırılan uygulama için sürüm ve kiracı ayrıntıları güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="a0bd2-269">Mevcut ER model eşleme yapılandırmasını inceleyin</span><span class="sxs-lookup"><span data-stu-id="a0bd2-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="a0bd2-270">**Tüm çalışma alanları \> Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="a0bd2-271">**Raporlama yapılandırmaları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="a0bd2-272">Ağaçta  **Dış ticaret modeli \> Dış ticaret eşlemesi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="a0bd2-273">**Önkoşullar** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0bd2-274">Şu anda bu eşleme meta veri yapılandırmasına başvuruyor.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="a0bd2-275">Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verisi sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="a0bd2-276">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-276">Select **Designer**.</span></span>
5. <span data-ttu-id="a0bd2-277">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-277">Select **Designer**.</span></span>
6. <span data-ttu-id="a0bd2-278">Ağaçta**Dynamics 365 for Operations \> Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="a0bd2-279">**Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-279">Select **Add root**.</span></span>
8. <span data-ttu-id="a0bd2-280">**Tablo** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0bd2-281">Şu anda bu eşleme meta veri yapılandırmasına başvuruyor.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="a0bd2-282">Bu model eşlemesi tasarlanırken bu yapılandırmadan gelen uygulama meta verisi sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="a0bd2-283">**İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="a0bd2-284">Bağlantılı uygulamayı bir model eşlemeye atayın</span><span class="sxs-lookup"><span data-stu-id="a0bd2-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="a0bd2-285">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-285">Select **Edit**.</span></span>
2. <span data-ttu-id="a0bd2-286">**Bağlı uygulama alanı**'nda, **MyConnectedApp** uygulamasını seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0bd2-287">Bu eşleme, seçilen bağlı uygulamanın meta verilerine başvuruda bulunuyor.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="a0bd2-288">Aynı eşleme aynı anda meta veri yapılandırmasına ve bağlı uygulamaya başvurursa bağlı uygulamanın meta verileri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="a0bd2-289">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-289">Select **Designer**.</span></span>
4. <span data-ttu-id="a0bd2-290">**Tasarımcı**’yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-290">Select **Designer**.</span></span>
5. <span data-ttu-id="a0bd2-291">Ağaçta**Dynamics 365 for Operations \> Tablo kayıtları**'nı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="a0bd2-292">**Kök ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-292">Select **Add root**.</span></span>
7. <span data-ttu-id="a0bd2-293">**Tablo** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a0bd2-294">O zaman bu eşleme için atanmış olan bağlı uygulamanın tüm meta verileri kullandığından ikiden fazla uygulama tablosu sunulur.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="a0bd2-295">**İptal**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="a0bd2-296">**Doğrula**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-296">Select **Validate**.</span></span>

<span data-ttu-id="a0bd2-297">Belirtilen veri kaynağı öğeleriyle, bu eşleme için atanmış bağlı uygulamanın ayrıntılarını kullanarak tanımlanan veri modeli öğelerini başarıyla bağladınız.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="a0bd2-298">Bu model eşlemesini farklı bir sürüm uygulamasının meta verilerini kullanarak değerlendirmeniz gerektiğinde, bağlı başka bir uygulamayı kaydedin, bu model eşlemesine atayın ve yeni meta verilere göre doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0bd2-299">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="a0bd2-299">Additional resources</span></span>

<span data-ttu-id="a0bd2-300">Alternatif olarak hem Finance and Operations'taki **RCS'de kullanılabilecek uygulama meta verileri hazırlama** görev kılavuzlarını hem **Bir ER yapılandırması kullanarak uygulama meta verilerine erişme** ve RCS'deki **Bağlı uygulamalar kullanarak uygulama meta verilerine erişme** görev kılavuzlarını yürütebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in Finance and Operationsas as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="a0bd2-301">Bu göre kılavuzları [Dynamics 365 for Finance and Operations 8.1 için Elektronil Raporlama Görev Kılavuzu](https://go.microsoft.com/fwlink/?linkid=2082739) sayfasından indirilebilir.</span><span class="sxs-lookup"><span data-stu-id="a0bd2-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
