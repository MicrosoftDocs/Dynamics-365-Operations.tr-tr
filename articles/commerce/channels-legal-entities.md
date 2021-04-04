---
title: Tüzel kişilik oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te kanallar oluşturulmadan önce oluşturulup yapılandırılması gereken tüzel kişiliklerin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 016b67631a53139d12d65dfaf594f49b030326b1
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478224"
---
# <a name="create-legal-entities"></a><span data-ttu-id="d0e78-103">Tüzel kişilik oluşturma</span><span class="sxs-lookup"><span data-stu-id="d0e78-103">Create legal entities</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d0e78-104">Bu konuda, Microsoft Dynamics 365 Commerce'te kanallar oluşturulmadan önce oluşturulup yapılandırılması gereken tüzel kişiliklerin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="d0e78-104">This topic describes how to create legal entities in Microsoft Dynamics 365 Commerce, which must be created and configured before creating channels.</span></span>

<span data-ttu-id="d0e78-105">Tüzel kişilik, kayıtlı veya asal bir yapıya sahip olan bir organizasyondur.</span><span class="sxs-lookup"><span data-stu-id="d0e78-105">A legal entity is an organization that has a registered or legislated legal structure.</span></span> <span data-ttu-id="d0e78-106">Tüzel kişilikler yasal sözleşmelere girebilir ve performanslarını raporlayacak bildirimler hazırlamaları gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0e78-106">Legal entities can enter into legal contracts and are required to prepare statements that report on their performance.</span></span>

<span data-ttu-id="d0e78-107">Bir şirket, tüzel kişilik türüdür.</span><span class="sxs-lookup"><span data-stu-id="d0e78-107">A company is a type of legal entity.</span></span> <span data-ttu-id="d0e78-108">Şu anda oluşturabileceğiniz tek tüzel kişilik türü şirketlerdir ve her bir tüzel kişilik, bir şirket kimliği ile ilişkilendirilir.</span><span class="sxs-lookup"><span data-stu-id="d0e78-108">Currently, companies are the only kind of legal entity that you can create, and every legal entity is associated with a company ID.</span></span> <span data-ttu-id="d0e78-109">Bu ilişkilendirmenin nedeni programdaki bazı işlevsel alanların şirket kimliğini veya *DataAreaId*'yi kendi veri modellerinde kullanmasıdır.</span><span class="sxs-lookup"><span data-stu-id="d0e78-109">This association exists because some functional areas in the program use a company ID, or *DataAreaId*, in their data models.</span></span> <span data-ttu-id="d0e78-110">Bu işlevsel alanlarda, şirketler veri güvenliği için bir sınır olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="d0e78-110">In these functional areas, companies are used as a boundary for data security.</span></span> <span data-ttu-id="d0e78-111">Kullanıcılar, yalnızca oturum açmış oldukları şirketin verilerine erişebilir.</span><span class="sxs-lookup"><span data-stu-id="d0e78-111">Users can access data only for the company that they are currently logged on to.</span></span> 

<span data-ttu-id="d0e78-112">Bir kanal oluştururken, o kanalın ait olduğu tüzel kişiliği belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d0e78-112">When creating a channel, you must specify which legal entity that channel belongs to.</span></span>

## <a name="create-a-new-legal-entity"></a><span data-ttu-id="d0e78-113">Yeni bir tüzel kişilik oluşturma</span><span class="sxs-lookup"><span data-stu-id="d0e78-113">Create a new legal entity</span></span>

<span data-ttu-id="d0e78-114">Dynamics 365 Commerce'te yeni bir tüzel kişilik oluşturmak için bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-114">To create a new legal entity in Dynamics 365 Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d0e78-115">Gezinti bölmesinde, **Modüller \> Headquarters kurulumu \> Tüzel kişilikler**'e gidin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-115">In the navigation pane, go to  **Modules \> Headquarters setup \> Legal entities**.</span></span>
1. <span data-ttu-id="d0e78-116">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-116">On the action pane, select **New**.</span></span> <span data-ttu-id="d0e78-117">**Yeni tüzel kişilik** bölmesi sağda görünür.</span><span class="sxs-lookup"><span data-stu-id="d0e78-117">The **New legal entity** pane appears on the right.</span></span>
1. <span data-ttu-id="d0e78-118">**Ad** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-118">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="d0e78-119">**Şirket** alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-119">In the **Company** field, enter a value.</span></span>
1. <span data-ttu-id="d0e78-120">**Ülke/bölge** alanına bir değer girin veya buradan bir değer seçin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-120">In the **Country/region** field, enter or select a value.</span></span>
1. <span data-ttu-id="d0e78-121">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-121">Select **OK**.</span></span> 

   ![Tüzel kişilik oluşturma](media/legal-entities.png)

1. <span data-ttu-id="d0e78-123">**Genel** bölümünde, tüzel kişilik hakkında aşağıdaki genel bilgileri girin:</span><span class="sxs-lookup"><span data-stu-id="d0e78-123">In the **General** section, provide the following general information about the legal entity:</span></span> 
   1. <span data-ttu-id="d0e78-124">Arama adı gerekiyorsa bir arama adı girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-124">Enter a search name, if a search name is required.</span></span> <span data-ttu-id="d0e78-125">Arama adı, bu tüzel kişilik için arama yapılmasında kullanılabilecek alternatif bir addır.</span><span class="sxs-lookup"><span data-stu-id="d0e78-125">A search name is an alternate name that can be used to search for this legal entity.</span></span> 
   1. <span data-ttu-id="d0e78-126">Bu tüzel kişiliğin bir konsolidasyon şirketi olarak kullanılıp kullanılmadığını seçin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-126">Select whether this legal entity is being used as a consolidation company.</span></span>
   1. <span data-ttu-id="d0e78-127">Bu tüzel kişiliğin bir eliminasyon şirketi olarak kullanılıp kullanılmadığını seçin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-127">Select whether this legal entity is being used as an elimination company.</span></span> 
   1. <span data-ttu-id="d0e78-128">Kişilik için **varsayılan dili** seçin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-128">Select the **default language** for the entity.</span></span> 
   1. <span data-ttu-id="d0e78-129">Kişilik için **saat dilimini** seçin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-129">Select the **time zone** for the entity.</span></span>
1. <span data-ttu-id="d0e78-130">**Adresler** bölümünde, sokak adı ve numarası, posta kodu ve şehir gibi adres bilgilerini girmek için **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-130">In the **Addresses** section, select **Edit** to enter address information, such as the street name and number, postal code, and city.</span></span>
1. <span data-ttu-id="d0e78-131">**İletişim bilgileri** bölümünde e-posta adresleri, URL'ler ve telefon numaraları gibi iletişim yöntemleri hakkında bilgi girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-131">In the **Contact information** section, enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span>
1. <span data-ttu-id="d0e78-132">**Yasal raporlama** bölümünde, yasal raporlama için kullanılan kayıt numaralarını girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-132">In the **Statutory reporting** section, enter the registration numbers that are used for statutory reporting.</span></span>
1. <span data-ttu-id="d0e78-133">**Kayıt numaraları** bölümünde, tüzel kişilik tarafından istenen bilgileri girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-133">In the **Registration numbers** section, enter any information required by the legal entity.</span></span>
1. <span data-ttu-id="d0e78-134">**Banka hesabı bilgileri** bölümünde, tüzel kişilik için banka hesaplarını ve rota numaralarını girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-134">In the **Bank account information** section, enter bank accounts and routing numbers for the legal entity.</span></span>
1. <span data-ttu-id="d0e78-135">**Dış Ticaret ve lojistik** bölümünde, tüzel kişilik sevkiyat bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-135">In the **Foreign trade and logistics** section, enter shipping information for the legal entity.</span></span>
1. <span data-ttu-id="d0e78-136">**Numara serileri** bölümünde, tüzel kişilikle ilişkili numara serilerini görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d0e78-136">In the **Number sequences** section, you can view the number sequences that are associated with the legal entity.</span></span> <span data-ttu-id="d0e78-137">Bu, başlangıçta boş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="d0e78-137">This will be empty to start with.</span></span>
1. <span data-ttu-id="d0e78-138">**Pano resmi** bölümünde, tüzel kişilikle ilişkili logoyu ve pano görüntüsünü görüntüleyin veya değiştirin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-138">In the **Dashboard image** section, view or change the logo and dashboard image associated with the legal entity.</span></span>
1. <span data-ttu-id="d0e78-139">**Vergi kaydı** bölümünde, vergi kurumlarına bildirilirken kullanılacak kayıt numaralarını girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-139">In the **Tax registration** section, enter the registration numbers that are used to report to tax authorities.</span></span>
1. <span data-ttu-id="d0e78-140">**Vergi 1099** bölümüne tüzel kişilik için 1099 bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-140">In the **Tax 1099** section, enter 1099 information for the legal entity.</span></span>
1. <span data-ttu-id="d0e78-141">**Vergi bilgileri** bölümünde, tüzel kişilik için vergi bilgilerini girin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-141">In the **Tax invormation** section, enter tax information for the legal entity.</span></span>
1. <span data-ttu-id="d0e78-142">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="d0e78-142">Select **Save**.</span></span>

<span data-ttu-id="d0e78-143">Aşağıdaki resimde örnek bir tüzel kişiliğin ayrıntıları gösteriliyor.</span><span class="sxs-lookup"><span data-stu-id="d0e78-143">The following image shows details of an example legal entity.</span></span>

![Tüzel kişilik genel bölümü](media/legal-entities-general.png)
   
## <a name="additional-resources"></a><span data-ttu-id="d0e78-145">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d0e78-145">Additional resources</span></span>

[<span data-ttu-id="d0e78-146">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="d0e78-146">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d0e78-147">Kuruluş hiyerarşinizi planlama</span><span class="sxs-lookup"><span data-stu-id="d0e78-147">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d0e78-148">Kuruluş hiyerarşileri</span><span class="sxs-lookup"><span data-stu-id="d0e78-148">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="d0e78-149">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="d0e78-149">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="d0e78-150">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="d0e78-150">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
