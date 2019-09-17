---
title: Konum hiyerarşisi üzerinde metin kesmeden kaçının ve Visio'ya dışa aktarın
description: Bu konu adlarını ve pozisyonları kişiler müşteriler yetenek için Microsoft Dynamics 365 for Talent için hiyerarşi görüntülediğinizde nerede kesiliyor sorununu açıklar. Metin kesme, hiyerarşinin ekran görüntüsünün veya baskısının alınmasını zorlaştırabilir.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 07a972bc1c6dd4076932248edb314992cb7297e5
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741833"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a><span data-ttu-id="add02-104">Konum hiyerarşisi üzerinde metin kesmeden kaçının ve Visio'ya dışa aktarın</span><span class="sxs-lookup"><span data-stu-id="add02-104">Avoid text truncation on the position hierarchy and export to Visio</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="add02-105">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="add02-105">**Issue**</span></span>

<span data-ttu-id="add02-106">Bir müşteri, Microsoft Dynamics 365 for Talent içinde konum hiyerarşisini görüntülerse, bireylerin ve pozisyonların adları kesilir.</span><span class="sxs-lookup"><span data-stu-id="add02-106">When a customer views the position hierarchy in Microsoft Dynamics 365 for Talent, the names of individuals and positions are truncated.</span></span> <span data-ttu-id="add02-107">Bu nedenle, bir ekran görüntüsü almak veya hiyerarşiyi yazdırıp dağıtmak zor olabilir.</span><span class="sxs-lookup"><span data-stu-id="add02-107">Therefore, it can be difficult to take a screenshot, or to print and distribute the hierarchy.</span></span>

![Pozisyon hiyerarşisi](media/position-h.png)

<span data-ttu-id="add02-109">**Nedeni**</span><span class="sxs-lookup"><span data-stu-id="add02-109">**Cause**</span></span>

<span data-ttu-id="add02-110">Bu davranış tasarımdan kaynaklanır.</span><span class="sxs-lookup"><span data-stu-id="add02-110">This behavior is by design.</span></span>

<span data-ttu-id="add02-111">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="add02-111">**Resolution**</span></span>

<span data-ttu-id="add02-112">Ne yazık ki, kullanıcılar kolayca metin boyutunu değiştiremezler.</span><span class="sxs-lookup"><span data-stu-id="add02-112">Unfortunately, users can't easily change the size of the text.</span></span> <span data-ttu-id="add02-113">Ancak, konum hiyerarşisini Talent'in dışına aktarabilir ve daha sonra Microsoft Visio'ya içe aktarabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="add02-113">However, you can export the position hierarchy out of Talent and then import it into Microsoft Visio.</span></span> <span data-ttu-id="add02-114">Aşağıdaki makale Microsoft Dynamics AX 2012 için yazılmıştır, ancak prosedür halen Talent için geçerlidir: [Microsoft Visio'ya bir konum hiyerarşisi dışa aktarmak](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span><span class="sxs-lookup"><span data-stu-id="add02-114">Although the following article was written for Microsoft Dynamics AX 2012, the process still applies to Talent: [Export a position hierarchy to Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).</span></span>

<span data-ttu-id="add02-115">Visio'ya dışa aktarmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="add02-115">Follow these steps to export to Visio.</span></span>

1. <span data-ttu-id="add02-116">Talent içerisinde **Konumlar** liste sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="add02-116">In Talent, open the **Positions** list page.</span></span>

    <span data-ttu-id="add02-117">Kuruluş yapısı diyagramına daha fazla bilgi eklemek için **Konumlar** listesine alanlar ekleyin, böylece bu prosedürdeki sihirbazı kullandığınızda kullanılabilir olurlar.</span><span class="sxs-lookup"><span data-stu-id="add02-117">To include more information in the organization structure diagram, add fields to the **Positions** list, so that they are available when you use the wizard later in this procedure.</span></span>

2. <span data-ttu-id="add02-118">Eylem Panosu üzerinde **Microsoft Office içinde aç** düğmesini seçin ve sonra **Excel'e dışa aktar** altında, **Konumlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-118">On the Action Pane, select the **Open in Microsoft Office** button, and then, under **Export to Excel**, select **Positions**.</span></span> <span data-ttu-id="add02-119">Bunun yerine, Ctrl+T tuşlarına basın.</span><span class="sxs-lookup"><span data-stu-id="add02-119">Alternatively, press Ctrl+T.</span></span>

    ![Konumlar listesi sayfasını Excel'e dışa aktarın](media/org-admin.png)

3. <span data-ttu-id="add02-121">Dışa aktarılan Excel dosyasını kaydedin.</span><span class="sxs-lookup"><span data-stu-id="add02-121">Save the Excel file that is exported.</span></span>

    ![Excel iletişim kutusuna dışa aktarmak](media/export-excel.png)

4. <span data-ttu-id="add02-123">Visio içinde **Visio - Yeni oluştur** öğesini seçin ve **İş** şablon kategorisini seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-123">In Visio, select **Visio - Create New**, and select the **Business** template category.</span></span>

    ![Yeni diyagram](media/new.png)

5. <span data-ttu-id="add02-125">**Kuruluş Şeması Sihirbazı**'nı seçin ve sonra **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-125">Select **Organization Chart Wizard**, and then select **Create**.</span></span>

    ![Kuruluş Şeması Sihirbazı iletişim kutusu](media/orgchart-wizard.png)

6. <span data-ttu-id="add02-127">**Halihazırda bir dosya veya veri tabanında depolanmış olan bilgi**'yi seçin ve sonra **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-127">Select **Information that's already stored in a file or database**, and then select **Next**.</span></span>

    ![Kuruluş Şeması Sihirbazı 1](media/orgchart-wizard7.png)

7. <span data-ttu-id="add02-129">**Bir metin, Org Plus (\*.txt), veya Excel dosyası** öğesini seçin ve sonra **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-129">Choose **A text, Org Plus (\*.txt), or Excel file**, and then select **Next**.</span></span>

    ![Kuruluş şeması sihirbazı 2](media/orgchart-wizard3.png)

8. <span data-ttu-id="add02-131">Konum hiyerarşisini içeren seçilen dışa aktarılan Excel dosyasını seçmek için tarayın ve sonra **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-131">Browse to select the exported Excel file that contains the position hierarchy, and then select **Next**.</span></span>

    ![Kuruluş Şeması Sihirbazı 3](media/orgchart-wizard2.png)

9. <span data-ttu-id="add02-133">**Adı** alanında **Konum** olarak ayarlayın, **Raporlar için** alanını **Konuma raporlar** olarak ayarlayın ve sonra **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-133">Set the **Name** field to **Position**, set the **Reports to** field to **Reports to position**, and then select **Next**.</span></span>

    ![Kuruluş Şeması Sihirbazı 4](media/orgchart-wizard1.png)

10. <span data-ttu-id="add02-135">Her bir düğümde gösterilecek alanları seçin ve sonra **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-135">Select the fields that should be shown on each node, and then select **Next**.</span></span>

    ![Kuruluş Şeması Sihirbazı 5](media/orgchart-wizard5.png)

11. <span data-ttu-id="add02-137">**Konum** sütununu **Veri alanlarını şekillendir** listesine ekleyin ve sonra **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-137">Add the **Position** column to the **Shape Data fields** list, and then select **Next**.</span></span>

    ![Kuruluş Şeması Sihirbazı 6](media/orgchart-wizard6.png)

12. <span data-ttu-id="add02-139">Resimler şu anda kullanılamıyor.</span><span class="sxs-lookup"><span data-stu-id="add02-139">Pictures aren't currently available.</span></span> <span data-ttu-id="add02-140">Bu nedenle, bir sonraki sayfada **İleri**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-140">Therefore, on the next page, select **Next**.</span></span>
13. <span data-ttu-id="add02-141">**Sihirbazın kuruluş şemamı sayfalar arasında otomatik olarak kesmesini istiyorum**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-141">Select **I want the wizard to automatically break my organization chart across pages**.</span></span>

    ![Kuruluş Şeması Sihirbazı 7](media/orgchart-wizard4.png)

14. <span data-ttu-id="add02-143">**Bitir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="add02-143">Select **Finish**.</span></span>

    <span data-ttu-id="add02-144">Yapı içerisinde bulunmayan herhangi bir konum varsa, onları diyagrama eklemeniz istenir.</span><span class="sxs-lookup"><span data-stu-id="add02-144">If there are any positions that aren't in the structure, you're asked to include them in the diagram.</span></span>

<span data-ttu-id="add02-145">Visio içinde oluşturulan diyagram, her bir yöneticiyi farklı bir çalışma sayfasında gösterir.</span><span class="sxs-lookup"><span data-stu-id="add02-145">The diagram that is generated in Visio shows each manager on a separate worksheet.</span></span>

<span data-ttu-id="add02-146">Diyagrama dahil etmeyi seçtiğiniz alanlara dayalı olarak, her bir düğüm Visio dosyası oluşturulduğunda uygun bilgiyi gösterir.</span><span class="sxs-lookup"><span data-stu-id="add02-146">Based on the fields that you selected to include in the diagram, each node shows the appropriate information when the Visio file is generated.</span></span>

![Hiyerarşi diyagramı](media/hierarchy.png)

<span data-ttu-id="add02-148">**Ek seçenek**</span><span class="sxs-lookup"><span data-stu-id="add02-148">**Additional option**</span></span>

<span data-ttu-id="add02-149">Talen içerisinde, **Kişiler** çalışma alanını hiyerarşiye dayalı bazı bilgileri görmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="add02-149">In Talent, you might also be able to use the **People** workspace to view some hierarchy-related information.</span></span>
