---
title: Azure Active Directory'den kullanıcıları içeri aktarma
description: Bu yordam, sistem yöneticisi tarafından Azure Active Directory'den seçili kullanıcıları el ile içeri aktarma veya çok sayıda kullanıcıyı içeri aktarma için kullanılabilir.
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571017"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="d27da-103">Azure Active Directory'den kullanıcıları içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="d27da-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="d27da-104">Seçili kullanıcıları içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="d27da-104">Import select users</span></span>

<span data-ttu-id="d27da-105">Bu yordam, sistem yöneticisi tarafından Azure Active Directory'den (Azure AD) seçili kullanıcıları içeri aktarmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d27da-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="d27da-106">Kullanıcı içeri aktarılırken geçerli oturum şirketi varsayılan şirketi olur.</span><span class="sxs-lookup"><span data-stu-id="d27da-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="d27da-107">Gerekirse kullanıcıları içeri aktarmadan önce geçerli şirketi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d27da-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="d27da-108">**Sistem yönetimi > Kullanıcılar > Kullanıcı** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d27da-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="d27da-109">**Kullanıcıları içe aktar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d27da-109">Click **Import users**.</span></span>
4. <span data-ttu-id="d27da-110">İçeri aktarılması gereken kullanıcıları seçin ve **Kullanıcıları içe aktar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d27da-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="d27da-111">İçeri aktarma işlemi tamamlandıktan sonra, kullanıcılara rol atanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d27da-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="d27da-112">Kullanıcıları topluca içe aktarma</span><span class="sxs-lookup"><span data-stu-id="d27da-112">Import users in bulk</span></span>

<span data-ttu-id="d27da-113">Bu yordam, sistem yöneticisi tarafından çok sayıda kullanıcıyı Azure Active Directory'den almak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="d27da-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="d27da-114">Toplu içeri aktarma seçeneğini kullanırken kullanıcı seçmek mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="d27da-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="d27da-115">İçeri aktarmayı toplu iş olarak çalıştırma</span><span class="sxs-lookup"><span data-stu-id="d27da-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="d27da-116">Kullanıcı içeri aktarılırken geçerli oturum şirketi varsayılan şirketi olur.</span><span class="sxs-lookup"><span data-stu-id="d27da-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="d27da-117">Gerekirse kullanıcıları içeri aktarmadan önce geçerli şirketi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d27da-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="d27da-118">**Sistem yönetimi > Kullanıcılar > Kullanıcılar** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="d27da-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="d27da-119">**Toplu içe aktarma**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d27da-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="d27da-120">**Arka planda çalıştır** bölümünü genişletin.</span><span class="sxs-lookup"><span data-stu-id="d27da-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="d27da-121">**Toplu işlem** alanında **Evet** seçeneğini seçin.</span><span class="sxs-lookup"><span data-stu-id="d27da-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="d27da-122">**Toplu iş grubu** alanında bir değer girin veya bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d27da-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="d27da-123">Bu isteğe bağlı bir adımdır.</span><span class="sxs-lookup"><span data-stu-id="d27da-123">This is an optional step.</span></span>  
7. <span data-ttu-id="d27da-124">**Özel** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d27da-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="d27da-125">Bu isteğe bağlı bir adımdır.</span><span class="sxs-lookup"><span data-stu-id="d27da-125">This is an optional step.</span></span>  
8. <span data-ttu-id="d27da-126">**Kritik iş** alanında **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d27da-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="d27da-127">Bu isteğe bağlı bir adımdır.</span><span class="sxs-lookup"><span data-stu-id="d27da-127">This is an optional step.</span></span>  
9. <span data-ttu-id="d27da-128">**İzleme kategorisi** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="d27da-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="d27da-129">**Tamam**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="d27da-129">Click **OK**.</span></span>

<span data-ttu-id="d27da-130">İçeri aktarma işlemi tamamlandıktan sonra, kullanıcılara rol atanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d27da-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="d27da-131">Bir korumalı alan ortamında çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d27da-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="d27da-132">**Toplu içeri aktarma**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="d27da-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="d27da-133">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d27da-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]