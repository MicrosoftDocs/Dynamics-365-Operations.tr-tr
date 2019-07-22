---
title: RCS'de kullanılacak uygulama meta verileri hazırlama
description: Bu konudaki adımlarda, bir kullanıcının, Regulatory Configuration Service (RCS) içinde ER model eşleme yapılandırmaları tasarlamakta kullanılan Finance and Operations uygulama meta verilerini içeren yeni elektronik raporlama (ER) yapılandırmasını nasıl oluşturabileceğiniz açıklanmaktadır.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1bd2298240fa789762a350e90888201c5a7ce45
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726995"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="3a7b1-103">RCS'de kullanılacak uygulama meta verileri hazırlama</span><span class="sxs-lookup"><span data-stu-id="3a7b1-103">Prepare application metadata to be used in RCS</span></span>
[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a7b1-104">Aşağıdaki adımlar, Sistem Yöneticisi veya Elektronik Raporlama Geliştiricisi rolündeki bir kullanıcının, Regulatory Configuration Service (RCS) içinde ER model eşleme yapılandırmaları tasarlamakta kullanılan Microsoft Dynamics 365 for Finance and Operations uygulama meta verilerini içeren yeni elektronik raporlama (ER) yapılandırmasını nasıl oluşturabileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains Microsoft Dynamics 365 for Finance and Operations application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="3a7b1-105">Bu yapılandırma dış ticaret işlemlerine erişmek için örnek bir ER modeli eşlemesi yapılandırması tasarlamak için kullanılacaktır.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="3a7b1-106">Bu örnekte Litware, Inc. örnek şirketi için bir yapılandırma oluşturacaksınız. Bu adımlar, herhangi bir şirkette gerçekleştirilebilir.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="3a7b1-107">Bu adımları tamamlamak için öncelikle [Yapılandırma sağlayıcıları oluşturma ve bunları etkin olarak işaretleme](er-configuration-provider-mark-it-active-2016-11.md). adımlarını tamamlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3a7b1-108">Önkoşullar</span><span class="sxs-lookup"><span data-stu-id="3a7b1-108">Prerequisites</span></span>
1.  <span data-ttu-id="3a7b1-109">**Organizasyon yönetimi** > **Çalışma alanları** > **Elektronik raporlama**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.  <span data-ttu-id="3a7b1-110">Örnek şirket ‘Litware, Inc.’ için yapılandırma sağlayıcısının kullanılabilir olduğunu ve **Etkin** olarak işaretlemiş olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="3a7b1-111">Bu yapılandırma sağlayıcısını göremiyorsanız[Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md). prosedüründeki adımları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.  <span data-ttu-id="3a7b1-112">**Meta veri yapılandırması**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-112">Click **Metadata configurations**.</span></span> 
4.  <span data-ttu-id="3a7b1-113">Örnepin, dış ticari işletme etki alanındaki bilgileri içeren elektronik belgeler oluşturmak amacıyla kullanılacak Finance and Operations uygulamasına bir ER çözümü tasarlamak için RCS'yi kullanmak istiyorsunuz.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="3a7b1-114">ER veri modeliyle gerekli verilerin kaynakları arasındaki eşlemeyi belirtmek amacıyla RCS'de Finance and Operations uygulaması için uygulama meta verilerine erişiminizin olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="3a7b1-115">Bu nedenle, ER çözümünü tasarlama sürecinin bir parçası olarak, seçilen iş etki alanı için ER raporları oluşturmak üzere gerekli olan tüm meta verileri içeren yeni bir ER meta veri yapılandırması yapılandırıyoruz.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="3a7b1-116">Meta veri yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="3a7b1-116">Add metadata configuration</span></span> 
1.  <span data-ttu-id="3a7b1-117">İletişim kutusu formunu açmak için **Yapılandırma oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.  <span data-ttu-id="3a7b1-118">**Ad** alanına, "Dış ticaret meta verisi" yazın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.  <span data-ttu-id="3a7b1-119">**Konfigürasyon oluştur**'u tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-119">Click **Create configuration**.</span></span> 
4.  <span data-ttu-id="3a7b1-120">**Tasarımcı**'yı tıklatın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-120">Click **Designer**.</span></span> 
5.  <span data-ttu-id="3a7b1-121">**Ekle** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3a7b1-122">Tüm uygulama, seçili model ya da modüller için tüm meta verileri seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="3a7b1-123">Bu durumda aşağıdaki meta verilerin otomatik olarak eklenebileceğine dikkat edin: kayıt tabloları, numaralandırmalar ve genişletilmiş veri türleri.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="3a7b1-124">Ek meta veri türleri gerektiğinde, bunların el ile eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="3a7b1-125">El ile seçmeniz gereken dış ticari hareketlerle ilgili bazı meta verilerimiz ve meta veri öğelerimiz var.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.  <span data-ttu-id="3a7b1-126">**Veri kaynağı ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-126">Click **Add data source**.</span></span> 
7.  <span data-ttu-id="3a7b1-127">**Tablo kayıtları**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-127">Click **Table records**.</span></span> 
8.  <span data-ttu-id="3a7b1-128">**Ad** alanında bir "İntrastat" değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.  <span data-ttu-id="3a7b1-129">**Intrastat** tablosu kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-129">Select the **Intrastat** table record.</span></span> 
10. <span data-ttu-id="3a7b1-130">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-130">Click **OK**.</span></span>
  
<span data-ttu-id="3a7b1-131">Intrastat kayıt tablosu hakkında meta veri bilgileri ekledik.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11. <span data-ttu-id="3a7b1-132">Ağaçta **Tablo kayıtları Instrastat**\>**İlişkiler**'i genişletin.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12. <span data-ttu-id="3a7b1-133">Ağaçta **Tablo kayıtları İntrastatı**\>**İlişkiler\IntrastatCommodity (Tablo kayıtları EcoResCategory)**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>   
13. <span data-ttu-id="3a7b1-134">**Meta veri ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3a7b1-135">Seçili kayıt tablosu için gerekli ilişkilerindeki meta veriler el ile eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16. <span data-ttu-id="3a7b1-136">**Veri kaynağı ekle**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-136">Click **Add data source**.</span></span> 
17. <span data-ttu-id="3a7b1-137">**Numaralandırma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-137">Click **Enumeration**.</span></span> 
18. <span data-ttu-id="3a7b1-138">**Ad** alanında bir "IntrastatDirection" değeriyle filtreleme yapmak için Hızlı Filtre'yi kullanın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19. <span data-ttu-id="3a7b1-139">**IntrastatDirection numaralandırma** kaydını seçin.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20. <span data-ttu-id="3a7b1-140">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-140">Click **OK**.</span></span> 
21. <span data-ttu-id="3a7b1-141">**Kaydet**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-141">Click **Save**.</span></span>  
22. <span data-ttu-id="3a7b1-142">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="3a7b1-143">Meta veri yapılandırmasının taslak sürümünü tamamlama</span><span class="sxs-lookup"><span data-stu-id="3a7b1-143">Complete the draft version of metadata configuration</span></span>
1.  <span data-ttu-id="3a7b1-144">**Durumu değiştir** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-144">Click **Change status**.</span></span> 
2.  <span data-ttu-id="3a7b1-145">**Tamamla** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-145">Click **Complete**.</span></span> 
3.  <span data-ttu-id="3a7b1-146">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-146">Click **OK**.</span></span> 
4.  <span data-ttu-id="3a7b1-147">Tamamlanmış sürüm **1**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="3a7b1-148">Meta veri yapılandırmasının tamamlanan sürümünü uygulamadan XML dosyası olarak dışarı aktarın:</span><span class="sxs-lookup"><span data-stu-id="3a7b1-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.  <span data-ttu-id="3a7b1-149">**Değiştir**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-149">Click **Exchange**.</span></span> 
2.  <span data-ttu-id="3a7b1-150">**XML dosyası olarak dışa aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-150">Click **Export as XML file**.</span></span> 
3.  <span data-ttu-id="3a7b1-151">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-151">Click **OK**.</span></span> 
    
<span data-ttu-id="3a7b1-152">Oluşturulan ER meta veri yapılandırması, RCS'ye alınabilecek ve Finance and Operations'taki dış ticari işletme etki alanının meta verileri hakkında bilgi kaynağı olarak kullanılabilen bir XML dosyası olarak kaydedildi.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain in Finance and Operations.</span></span> <span data-ttu-id="3a7b1-153">Bu bilgiye dayanarak uygulama meta verileri ve ER veri modeli arasındaki eşlemeyi belirtebiliriz.</span><span class="sxs-lookup"><span data-stu-id="3a7b1-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
