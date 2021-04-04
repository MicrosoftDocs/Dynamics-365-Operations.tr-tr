---
title: Kişisel bilgilerin düzenlenmesini kısıtlama
description: Çalışanların Dynamics 365 Human Resources'daki iletişim bilgilerini düzenlemelerini kısıtlayın.
author: andreabichsel
manager: tfehr
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d4785232dbb21c5f8a800497fb0cfd3c64dea2d8
ms.sourcegitcommit: 45d10d0c25b3ec585323709bb97ba1895b500429
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2021
ms.locfileid: "5503048"
---
# <a name="restrict-editing-of-personal-information"></a><span data-ttu-id="bb6cf-103">Kişisel bilgilerin düzenlenmesini kısıtlama</span><span class="sxs-lookup"><span data-stu-id="bb6cf-103">Restrict editing of personal information</span></span>

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

<span data-ttu-id="bb6cf-104">Bu konuda, çalışanların Dynamics 365 Human Resources'da iletişim bilgilerini düzenlemesinin nasıl kısıtlanacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-104">This topic describes how to restrict employees from editing contact details in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="bb6cf-105">Çalışanların iş konumları veya e-posta adresleri gibi belirli iletişim bilgilerini düzenlemelerini engellemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-105">You might want to prevent employees from editing certain contact details, such as their business location or email address.</span></span>

> [!NOTE]
> <span data-ttu-id="bb6cf-106">Bu özelliği kullanmak için önce Özellik yönetiminde **(Önizleme) Belirli amaçlar için çalışanların adres ve iletişim bilgilerini eklemesini veya düzenlemesini kısıtlama** özelliğini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-106">To use this feature, you must first enable **(Preview) Restrict employees from adding or editing address and contact information for select purposes** in Feature management.</span></span> <span data-ttu-id="bb6cf-107">Önizleme özelliklerini etkinleştirmeyle ilgili daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="bb6cf-107">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span><br><br><span data-ttu-id="bb6cf-108">![Önizleme özelliğini etkinleştir](./media/hr-employee-self-service-restrict-enable.png)</span><span class="sxs-lookup"><span data-stu-id="bb6cf-108">![Enable preview feature](./media/hr-employee-self-service-restrict-enable.png)</span></span>

## <a name="choose-the-information-an-employee-can-add-or-edit"></a><span data-ttu-id="bb6cf-109">Bir çalışanın ekleyebileceği veya düzenleyebileceği bilgileri seçme</span><span class="sxs-lookup"><span data-stu-id="bb6cf-109">Choose the information an employee can add or edit</span></span>

1. <span data-ttu-id="bb6cf-110">Human Resources'ta **Personel yönetimi**'ni, **Bağlantılar**'ı ve sonra **İnsan kaynakları parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-110">In Human Resources, select **Personnel management**, select **Links**, and then select **Human resources parameters**.</span></span>

   ![Human Resources parametrelerini yapılandır'a gidin](./media/hr-employee-self-service-human-resources-parameters.png)

2. <span data-ttu-id="bb6cf-112">**Human Resources parametreleri** sayfasında **Çalışan self servisi** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-112">On the **Human resources parameters** page, select the **Employee self service** tab.</span></span>

   ![Employee Self Service'i seçme](./media/hr-employee-self-service-tab.png)

3. <span data-ttu-id="bb6cf-114">**Çalışan self servisi** sekmesinde, **Adres ve iletişim bilgileri** bölümünde çalışanların eklemesini veya düzenlemesini istemediğiniz tüm bilgilerin işaretini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-114">On the **Employee self service** tab, uncheck all information in the **Address and contact information** section that you don't want employees to add or edit.</span></span> <span data-ttu-id="bb6cf-115">Bu örnekte, **İş** iletişim bilgilerinin işaretini kaldırdık.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-115">In this example, we've unchecked **Business** contact information.</span></span>

   ![İş iletişim bilgileri için düzenlemeyi kısıtlama](./media/hr-employee-self-service-restrict-business.png)

4. <span data-ttu-id="bb6cf-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-117">Select **Save**.</span></span>

   ![Değişiklikleri kaydet](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a><span data-ttu-id="bb6cf-119">Çalışan deneyimi</span><span class="sxs-lookup"><span data-stu-id="bb6cf-119">Employee experience</span></span>

<span data-ttu-id="bb6cf-120">Çalışanların iletişim bilgilerini eklemesini veya düzenlemesini kısıtladıktan sonra çalışanlar bilgileri görebilir ancak değiştiremez.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-120">After you've restricted employees from adding or editing contact details, they can see the information, but can't change it.</span></span>

<span data-ttu-id="bb6cf-121">Bu örnekte, çalışanların **İş** iletişim bilgilerini düzenlemelerinin kısıtlandı ancak Çalışan self servisi'ndeki bilgileri görmeye devam edebilir:</span><span class="sxs-lookup"><span data-stu-id="bb6cf-121">In this example, where employees are restricted from editing **Business** contact details, they can still see the information in Employee self service:</span></span>

![İş iletişim bilgilerini görüntüleme](./media/hr-employee-self-service-restrict-view.png)

<span data-ttu-id="bb6cf-123">Ancak iş iletişim bilgilerini seçtiklerinde, **Adresi düzenle** bölmesi salt okunur olarak görünür ve alanların hiçbirini değiştiremezler.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-123">However, when they select the business contact details, the **Edit address** pane appears as read-only, and they can't change any of the fields.</span></span>

![İş iletişim bilgileri salt okunur olarak görüntülenir](./media/hr-employee-self-service-restrict-read-only.png)

<span data-ttu-id="bb6cf-125">Ayrıca, yeni adres eklemek için **Ekle**'yi seçerlerse **Amaç** açılan kutusundan **İş**'i seçemezler.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-125">In addition, if they select **Add** to add a new address, they can't select **Business** from the **Purpose** dropdown box.</span></span>

![Çalışan İş adresi ekleyemiyor](./media/hr-employee-self-service-restrict-add.png)

<span data-ttu-id="bb6cf-127">Çalışanlar, **Kişisel bilgiler** sayfasında **İletişim bilgileri**'ni seçip yeni bir adres eklediklerinde de aynı deneyimi yaşarlar.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-127">Employees get the same experience when they select **Contact details** on the **Personal information** page and add a new address.</span></span> <span data-ttu-id="bb6cf-128">**Amaç** açılan kutusu yalnızca ekleyebilecekleri bilgi türlerini görüntüler.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-128">The **Purpose** dropdown box only displays the types of information they can add.</span></span> 

![Çalışan Amaç açılan menüsünde İş'i seçemiyor](./media/hr-employee-self-service-restrict-purpose.png)

<span data-ttu-id="bb6cf-130">**İletişim bilgileri** artık kılavuzda **Amaç**'ı gösterir.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-130">**Contact details** now shows **Purpose** in the grid.</span></span>

![İletişim bilgileri kılavuzunda Amaç gösteriliyor](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a><span data-ttu-id="bb6cf-132">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="bb6cf-132">See also</span></span>

[<span data-ttu-id="bb6cf-133">Personel ve Yönetici self servisine genel bakış</span><span class="sxs-lookup"><span data-stu-id="bb6cf-133">Employee and Manager self service overview</span></span>](hr-employee-manager-self-service-overview.md)<br>
[<span data-ttu-id="bb6cf-134">Human Resources parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="bb6cf-134">Configure Human resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="bb6cf-135">Kişisel bilgileri düzenle</span><span class="sxs-lookup"><span data-stu-id="bb6cf-135">Edit personal information</span></span>](hr-employee-manager-self-service-edit-personal-information.md)