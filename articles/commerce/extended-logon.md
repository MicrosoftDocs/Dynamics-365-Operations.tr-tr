---
title: MPOS ve Cloud POS için genişletilmiş oturum açma işlevini ayarlama
description: Bu konu Bulut POS ve Retail Modern POS (MPOS) için genişletilmiş oturum açma seçeneğini ayarlamada kullanabileceğiniz seçenekleri ele alır.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 79878e2ffbf219f77f378997c277ced8bb41598c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024367"
---
# <a name="set-up-extended-logon-functionality-for-mpos-and-cloud-pos"></a><span data-ttu-id="c78c1-103">MPOS ve Cloud POS için genişletilmiş oturum açma işlevini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c78c1-103">Set up extended logon functionality for MPOS and Cloud POS</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c78c1-104">Bu konu Bulut POS ve Retail Modern POS (MPOS) için genişletilmiş oturum açma seçeneğini ayarlamada kullanabileceğiniz seçenekleri ele alır.</span><span class="sxs-lookup"><span data-stu-id="c78c1-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

## <a name="setting-up-extended-logon"></a><span data-ttu-id="c78c1-105">Genişletilmiş oturum açma ayarlaması</span><span class="sxs-lookup"><span data-stu-id="c78c1-105">Setting up extended logon</span></span>

<span data-ttu-id="c78c1-106">Barkod maskeleri ayarını **Retail and Commerce** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS profilleri** &gt; **İşlevsellik profilleri**'nde bulabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c78c1-106">You can find the setup for bar code masks at **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="c78c1-107">**İşlevler** Hızlı Sekmesi genişletilmiş oturum açma ile ilgili aşağıdaki seçenekleri içerir.</span><span class="sxs-lookup"><span data-stu-id="c78c1-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="c78c1-108">Personel barkod oturum açma işlemi</span><span class="sxs-lookup"><span data-stu-id="c78c1-108">Staff bar code logon</span></span>

<span data-ttu-id="c78c1-109">**Personel barkodla oturum açma** seçeneği etkinleştirilmişse, kendi satış noktası (POS) kimlik bilgilerine bir genişletilmiş oturum açma atanmış çalışanlar bir barkod kullanarak oturum açabilir.</span><span class="sxs-lookup"><span data-stu-id="c78c1-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="c78c1-110">Personelin barkodla oturum açması parola gerektirir</span><span class="sxs-lookup"><span data-stu-id="c78c1-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="c78c1-111">**Personel barkodla oturum açma parola gerektiriyor** seçeneği etkinleştirilmişse, personel barkodla oturum açma yalnızca mevcut genişletilmiş oturum açmaya atanan çalışanı seçer.</span><span class="sxs-lookup"><span data-stu-id="c78c1-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="c78c1-112">Bu seçenek etkinleştirildiğinde, çalışanların gene de parolalarını girmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c78c1-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="c78c1-113">Personel kart oturum açma işlemi</span><span class="sxs-lookup"><span data-stu-id="c78c1-113">Staff card logon</span></span>

<span data-ttu-id="c78c1-114">**Personel kartla oturum açma** seçeneği etkinleştirilmişse, kendi POS kimlik bilgilerine bir genişletilmiş oturum açma atanmış çalışanlar bir manyetik bant kullanarak oturum açabilir.</span><span class="sxs-lookup"><span data-stu-id="c78c1-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="c78c1-115">Personelin kartla oturum açması parola gerektirir</span><span class="sxs-lookup"><span data-stu-id="c78c1-115">Staff card logon requires password</span></span>

<span data-ttu-id="c78c1-116">**Personel kartla oturum açma parola gerektiriyor** seçeneği etkinleştirilmişse, personel kartla oturum açma yalnızca mevcut genişletilmiş oturum açmaya atanan çalışanı seçer.</span><span class="sxs-lookup"><span data-stu-id="c78c1-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="c78c1-117">Bu seçenek etkinleştirildiğinde, çalışanların gene de parolalarını girmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c78c1-117">Workers must still enter their password when this option is enabled.</span></span>

## <a name="assigning-an-extended-logon"></a><span data-ttu-id="c78c1-118">Genişletilmiş oturum açma ataması</span><span class="sxs-lookup"><span data-stu-id="c78c1-118">Assigning an extended logon</span></span>

<span data-ttu-id="c78c1-119">Varsayılan olarak, yalnızca yöneticiler çalışanlara genişletilmiş oturum açma atayabilir.</span><span class="sxs-lookup"><span data-stu-id="c78c1-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="c78c1-120">Genişletilmiş oturum atamak için POS içinde **Genişletilmiş oturum açma**'ya gidin.</span><span class="sxs-lookup"><span data-stu-id="c78c1-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="c78c1-121">Daha sonra, operatör kimliğini arama alanına girerek çalışanı arayın.</span><span class="sxs-lookup"><span data-stu-id="c78c1-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="c78c1-122">Çalışanı seçip **Ata** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78c1-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="c78c1-123">Bir sonraki sayfada, çalışana atamak için genişletilmiş oturum açma kartını geçirin veya taratın.</span><span class="sxs-lookup"><span data-stu-id="c78c1-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="c78c1-124">Kart geçirme veya tarama başarıyla okunursa, **Tamam** düğmesi kullanılabilir olur.</span><span class="sxs-lookup"><span data-stu-id="c78c1-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="c78c1-125">O çalışan için genişletilmiş oturum açmayı kaydetmek için **Tamam** düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78c1-125">Click **OK** to save the extended logon for that worker.</span></span>

## <a name="deleting-an-extended-logon"></a><span data-ttu-id="c78c1-126">Genişletilmiş oturum açmanın silinmesi</span><span class="sxs-lookup"><span data-stu-id="c78c1-126">Deleting an extended logon</span></span>

<span data-ttu-id="c78c1-127">Bir çalışana atanan genişletilmiş oturum açmayı silmek için, **Genişletilmiş oturum açma** işlemini kullanarak o çalışanı arayın.</span><span class="sxs-lookup"><span data-stu-id="c78c1-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="c78c1-128">Çalışanı seçip **Atamayı Kaldır** öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c78c1-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="c78c1-129">Bu çalışan ile ilişkili olan tüm genişletilmiş oturum açma kimlik bilgileri kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="c78c1-129">All extended logon credentials that are associated with that worker are removed.</span></span>

## <a name="extending-extended-logon"></a><span data-ttu-id="c78c1-130">Genişletilmiş oturum açmanın genişletilmesi</span><span class="sxs-lookup"><span data-stu-id="c78c1-130">Extending extended logon</span></span>

<span data-ttu-id="c78c1-131">Oturum açma hizmeti, avuç içi tarayıcılar gibi ek genişletilmiş oturum açma cihazları desteklenecek şekilde genişletilebilir.</span><span class="sxs-lookup"><span data-stu-id="c78c1-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="c78c1-132">Daha fazla bilgi için, POS genişletilebilirlik belgelerine bakın.</span><span class="sxs-lookup"><span data-stu-id="c78c1-132">For more information, see the POS extensibility documentation.</span></span>

## <a name="using-extended-logon"></a><span data-ttu-id="c78c1-133">Genişletilmiş oturum açmanın kullanılması</span><span class="sxs-lookup"><span data-stu-id="c78c1-133">Using extended logon</span></span>

<span data-ttu-id="c78c1-134">Genişletilmiş oturum açma yapılandırıldığında ve bir çalışana barkod ya da manyetik bant atandığında, o çalışanın sadece POS oturum açma sayfası ekrana geldiğinde kartını geçirmesi veya taratması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c78c1-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="c78c1-135">Oturum açma işlemine devam edebilmesi için önce bir parola da gerekliyse, çalışandan parolasını girmesi istenir.</span><span class="sxs-lookup"><span data-stu-id="c78c1-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>
