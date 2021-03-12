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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1b0afeabfecb60672156692f3cd809445624020c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969988"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="da062-103">Çevrimiçi işlevsellik profili oluştur</span><span class="sxs-lookup"><span data-stu-id="da062-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="da062-104">Bu konu, Microsoft Dynamics 365 Commerce için bir çevrimiçi işlevsellik profili kurma işleminin genel görünümünü sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="da062-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="da062-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="da062-105">Overview</span></span>

<span data-ttu-id="da062-106">Çevrimiçi işlevsellik profili, çevrimiçi kanallarda çeşitli ayarlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="da062-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="da062-107">Her bir çevrimiçi kanalın bir çevrimiçi işlevsellik profili belirtmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="da062-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="da062-108">Çevrimiçi işlevsellik profili oluştur</span><span class="sxs-lookup"><span data-stu-id="da062-108">Create an online functionality profile</span></span>

<span data-ttu-id="da062-109">Aşağıdaki yordamda, Commerce Headquarters uygulaması içinden bir çevrimiçi işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="da062-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="da062-110">Gezinti bölmesinde **modüller \> Kanal kurulumu \> çevrimiçi mağaza kurulumu \> işlevsellik profillerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="da062-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="da062-111">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="da062-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="da062-112">**Profil** alanına profil için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="da062-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="da062-113">**Açıklama** alanına, aşağıdaki örnek görüntüye bir değer ("Adventure Works profili") girin.</span><span class="sxs-lookup"><span data-stu-id="da062-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="da062-114">**İşlevler** bölümünde, **alışveriş sepetini**, **perakende müşterileri** veya **kullanıma alma** ayarlarını gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="da062-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="da062-115">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="da062-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="da062-116">Aşağıdaki resimde örnek bir çevrimiçi işlevsellik profili gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="da062-116">The following image shows an example online functionality profile.</span></span>
  
![Çevrimiçi işlev profili örneği](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="da062-118">İşlevler</span><span class="sxs-lookup"><span data-stu-id="da062-118">Functions</span></span>

- <span data-ttu-id="da062-119">**Toplu ürünler**: etkinleştirildiğinde, bu işlev sepetin aynı madde birden çok kez eklendiğinde miktarın güncelleştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="da062-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="da062-120">**Ödemeyle kullanıma alma işlemine izin ver**: etkinleştirildiğinde, alışveriş sepetine eklenen maddelerin fiyat $0,00 olduğunda bu işlev senaryoyu işler.</span><span class="sxs-lookup"><span data-stu-id="da062-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="da062-121">**Müşteriyi zaman uyumsuz modda oluştur**: Bu üçüncü taraf e-ticaret kanallarına uygulanabilen eski bir ayardır ve Dynamics 365 e-ticaret sitesine uygulanamaz.</span><span class="sxs-lookup"><span data-stu-id="da062-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da062-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="da062-122">Additional resources</span></span>

[<span data-ttu-id="da062-123">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="da062-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="da062-124">Kanal ayarlama önkoşulları</span><span class="sxs-lookup"><span data-stu-id="da062-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="da062-125">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="da062-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="da062-126">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="da062-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="da062-127">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="da062-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
