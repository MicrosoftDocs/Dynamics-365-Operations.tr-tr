---
title: Çevrimiçi işlevsellik profili oluştur
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta bir çevrimiçi işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003384"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="ceadd-103">Çevrimiçi işlevsellik profili oluştur</span><span class="sxs-lookup"><span data-stu-id="ceadd-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ceadd-104">Bu konu, Microsoft Dynamics 365 Commerce için bir çevrimiçi işlevsellik profili kurma işleminin genel görünümünü sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ceadd-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ceadd-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="ceadd-105">Overview</span></span>

<span data-ttu-id="ceadd-106">Çevrimiçi işlevsellik profili, çevrimiçi kanallarda çeşitli ayarlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="ceadd-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="ceadd-107">Her bir çevrimiçi kanalın bir çevrimiçi işlevsellik profili belirtmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ceadd-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="ceadd-108">Çevrimiçi işlevsellik profili oluştur</span><span class="sxs-lookup"><span data-stu-id="ceadd-108">Create an online functionality profile</span></span>

<span data-ttu-id="ceadd-109">Aşağıdaki yordamda, Commerce Headquarters uygulaması içinden bir çevrimiçi işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ceadd-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="ceadd-110">Gezinti bölmesinde **modüller \> Kanal kurulumu \> çevrimiçi mağaza kurulumu \> işlevsellik profillerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="ceadd-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="ceadd-111">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ceadd-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ceadd-112">**Profil** alanına profil için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="ceadd-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="ceadd-113">**Açıklama** alanına, aşağıdaki örnek görüntüye bir değer ("Adventure Works profili") girin.</span><span class="sxs-lookup"><span data-stu-id="ceadd-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="ceadd-114">**İşlevler** bölümünde, **alışveriş sepetini**, **perakende müşterileri** veya **kullanıma alma** ayarlarını gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ceadd-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="ceadd-115">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ceadd-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ceadd-116">Aşağıdaki resimde örnek bir çevrimiçi işlevsellik profili gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ceadd-116">The following image shows an example online functionality profile.</span></span>
  
![Çevrimiçi işlev profili örneği](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="ceadd-118">İşlevler</span><span class="sxs-lookup"><span data-stu-id="ceadd-118">Functions</span></span>

- <span data-ttu-id="ceadd-119">**Toplu ürünler**: etkinleştirildiğinde, bu işlev sepetin aynı madde birden çok kez eklendiğinde miktarın güncelleştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ceadd-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="ceadd-120">**Ödemeyle kullanıma alma işlemine izin ver**: etkinleştirildiğinde, alışveriş sepetine eklenen maddelerin fiyat $0,00 olduğunda bu işlev senaryoyu işler.</span><span class="sxs-lookup"><span data-stu-id="ceadd-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="ceadd-121">**Müşteriyi zaman uyumsuz modda oluştur**: Bu üçüncü taraf e-ticaret kanallarına uygulanabilen eski bir ayardır ve Dynamics 365 e-ticaret sitesine uygulanamaz.</span><span class="sxs-lookup"><span data-stu-id="ceadd-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ceadd-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ceadd-122">Additional resources</span></span>

[<span data-ttu-id="ceadd-123">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="ceadd-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ceadd-124">Kanal ayarlama önkoşulları</span><span class="sxs-lookup"><span data-stu-id="ceadd-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ceadd-125">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="ceadd-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="ceadd-126">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ceadd-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="ceadd-127">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ceadd-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
