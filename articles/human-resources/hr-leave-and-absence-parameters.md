---
title: Bırakma ve devamsızlık parametrelerini konfigüre et
description: Dynamics 365 Human Resources'ta izin ve devamsızlık için insan kaynakları parametrelerini tanımlayın.
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
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010845"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="4ed85-103">Bırakma ve devamsızlık parametrelerini konfigüre et</span><span class="sxs-lookup"><span data-stu-id="4ed85-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="4ed85-104">Dynamics 365 Human Resources'ta , izin ve devamsızlık planlarını ayarlamadan önce, aşağıdakiler dahil olmak üzere ilgili tüm insan kaynakları parametrelerinin ayarlarını doğrulamak iyi bir fikirdir.</span><span class="sxs-lookup"><span data-stu-id="4ed85-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="4ed85-105">İzin talepleri için numara serisi</span><span class="sxs-lookup"><span data-stu-id="4ed85-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="4ed85-106">Aile sağlık ve izin Yasası (FMLA) ayarları</span><span class="sxs-lookup"><span data-stu-id="4ed85-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="4ed85-107">İzin ve devamsızlık talepleri için çalışan self servis ayarları</span><span class="sxs-lookup"><span data-stu-id="4ed85-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="4ed85-108">İzin ve devamsızlık parametreleri</span><span class="sxs-lookup"><span data-stu-id="4ed85-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="4ed85-109">İnsan kaynakları parametrelerini görüntüle ve değiştir</span><span class="sxs-lookup"><span data-stu-id="4ed85-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="4ed85-110">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4ed85-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="4ed85-111">**Kurulum**'un altında, **İnsan kaynakları parametrelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="4ed85-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="4ed85-112">**Numara serileri** sekmesinde, **izin talebi kodunun** **numara serisi kodunu** doğrulayın ve gerekli değişiklikleri yapın.</span><span class="sxs-lookup"><span data-stu-id="4ed85-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="4ed85-113">Bu ayar, isteklere izin vermek üzere otomatik olarak kimlik atamak için kullanılan sırayı belirler.</span><span class="sxs-lookup"><span data-stu-id="4ed85-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="4ed85-114">**FMLA** sekmesinde, FMLA ayarlarını doğrulayın ve gerektiği şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4ed85-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="4ed85-115">**Çalışan self servis** sekmesinde, yöneticilerin çalışanlar adına bırakma ve devamsızlık talepleri girip giremeyeceğini belirtin.</span><span class="sxs-lookup"><span data-stu-id="4ed85-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="4ed85-116">**izin ve devamsızlık** sekmesinde, ayarlarını doğrulayın ve gerektiği şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4ed85-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="4ed85-117">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4ed85-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="4ed85-118">Takvim parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="4ed85-118">Configure calendar parameters</span></span>

<span data-ttu-id="4ed85-119">İzin ve devamsızlık takvimi önizleme özelliğini etkinleştirdiyseniz, ek parametreler konfigüre etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="4ed85-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="4ed85-120">3 Şubat 2020 ' de önizleme sürümü için yalnızca **bekleyen izin istekleri** etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="4ed85-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="4ed85-121">**İzin ve devamsızlık** sayfasında, **Bağlantılar** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="4ed85-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="4ed85-122">**Kurulum**'un altında, **İnsan kaynakları parametrelerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="4ed85-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="4ed85-123">**Takvim** sekmesinde, takvim ayarlarını gerektiği şekilde değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4ed85-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="4ed85-124">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="4ed85-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ed85-125">Ayrıca bkz.</span><span class="sxs-lookup"><span data-stu-id="4ed85-125">See also</span></span>

- [<span data-ttu-id="4ed85-126">İzin ve devamsızlığa genel bakış</span><span class="sxs-lookup"><span data-stu-id="4ed85-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
