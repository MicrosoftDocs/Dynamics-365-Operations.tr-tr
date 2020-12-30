---
title: Dynamics 365 Talent'daki yenilikler veya değişiklikler (7 Ocak 2020)
description: Bu makalede, Microsoft Dynamics 365 Talent'taki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462835"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="1402e-103">Dynamics 365 Talent'daki yenilikler veya değişiklikler (7 Ocak 2020)</span><span class="sxs-lookup"><span data-stu-id="1402e-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="1402e-104">Bu makalede Dynamics 365 Talent'te yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="1402e-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="1402e-105">Attract'te değişiklikler</span><span class="sxs-lookup"><span data-stu-id="1402e-105">Changes in Attract</span></span>

<span data-ttu-id="1402e-106">Bu sürüm, Dynamics 365 Talent: Attract için küçük hata düzeltmeleri içeriyor.</span><span class="sxs-lookup"><span data-stu-id="1402e-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="1402e-107">Onboard'taki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="1402e-107">Changes in Onboard</span></span>

<span data-ttu-id="1402e-108">Bu sürüm, Dynamics 365 Talent: Onboard için küçük hata düzeltmeleri içeriyor.</span><span class="sxs-lookup"><span data-stu-id="1402e-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="1402e-109">Core HR içindeki değişiklikler</span><span class="sxs-lookup"><span data-stu-id="1402e-109">Changes in Core HR</span></span>

<span data-ttu-id="1402e-110">Bu bölümde açıklanan değişiklikler sürüm numarası 8.1.2697 için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="1402e-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="1402e-111">Bazı başlıklardaki parantez içindeki numaralar Microsoft Dynamics Lifecycle Services (LCS) destek numaralarına referans verir.</span><span class="sxs-lookup"><span data-stu-id="1402e-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="1402e-112">İşe alma kayıtları olmayan çalışanlar silinemez-(386157)</span><span class="sxs-lookup"><span data-stu-id="1402e-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="1402e-113">Bu değişiklik, **çalışmayan işçiler** formuna bir silme seçeneği ekler.</span><span class="sxs-lookup"><span data-stu-id="1402e-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="1402e-114">Çalışan için hiçbir ileri, etkin veya geçmiş istihdam mevcut olduğunda çalışanlar bu formda görünür.</span><span class="sxs-lookup"><span data-stu-id="1402e-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="1402e-115">Bu sürümde, silme işlemi yalnızca sistem yöneticileri için etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="1402e-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="1402e-116">Ancak, gelecek haftaki sürümde, güvenlik güncelleştirmesi, HR yardımcısı rolüne sahip tüm kullanıcıların istihdam içermeyen çalışanları kaldırmasına olanak verecek şekilde güncelleştirilecektir.</span><span class="sxs-lookup"><span data-stu-id="1402e-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="1402e-117">Bu değişiklikleri aşağıdaki adımları izleyerek de el ile yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1402e-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="1402e-118">**Güvenlik konfigürasyonu**'na gidin.</span><span class="sxs-lookup"><span data-stu-id="1402e-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="1402e-119">**Ayrıcalıklar** sekmesinde , **çalışanları korumak** için **ayrıcalıklar** listesine filtre uygulayın.</span><span class="sxs-lookup"><span data-stu-id="1402e-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="1402e-120">**Başvurular** sütununda, **menü öğelerini görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1402e-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="1402e-121">**menü öğelerini görüntüle** sütununda, **HcmWOrkersWithoutEmployment**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="1402e-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="1402e-122">Izin vermek için **Silme** iznini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="1402e-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="1402e-123">**Yayımlanmamış nesneler** sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="1402e-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="1402e-124">**Tümünü yayımla**'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="1402e-124">Select **Publish all**.</span></span>
