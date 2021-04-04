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
ms.openlocfilehash: cb9d78a945132c913dcb8a5d5b41eaacd1a6db3b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477744"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="ef10b-103">Çevrimiçi işlevsellik profili oluştur</span><span class="sxs-lookup"><span data-stu-id="ef10b-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ef10b-104">Bu konu, Microsoft Dynamics 365 Commerce için bir çevrimiçi işlevsellik profili kurma işleminin genel görünümünü sunmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ef10b-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="ef10b-105">Çevrimiçi işlevsellik profili, çevrimiçi kanallarda çeşitli ayarlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="ef10b-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="ef10b-106">Her bir çevrimiçi kanalın bir çevrimiçi işlevsellik profili belirtmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ef10b-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="ef10b-107">Çevrimiçi işlevsellik profili oluştur</span><span class="sxs-lookup"><span data-stu-id="ef10b-107">Create an online functionality profile</span></span>

<span data-ttu-id="ef10b-108">Aşağıdaki yordamda, Commerce Headquarters uygulaması içinden bir çevrimiçi işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="ef10b-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="ef10b-109">Gezinti bölmesinde **modüller \> Kanal kurulumu \> çevrimiçi mağaza kurulumu \> işlevsellik profillerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="ef10b-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="ef10b-110">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ef10b-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ef10b-111">**Profil** alanına profil için bir kod girin.</span><span class="sxs-lookup"><span data-stu-id="ef10b-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="ef10b-112">**Açıklama** alanına, aşağıdaki örnek görüntüye bir değer ("Adventure Works profili") girin.</span><span class="sxs-lookup"><span data-stu-id="ef10b-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="ef10b-113">**İşlevler** bölümünde, **alışveriş sepetini**, **perakende müşterileri** veya **kullanıma alma** ayarlarını gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="ef10b-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="ef10b-114">Eylem bölmesinde, **Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ef10b-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ef10b-115">Aşağıdaki resimde örnek bir çevrimiçi işlevsellik profili gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="ef10b-115">The following image shows an example online functionality profile.</span></span>
  
![Çevrimiçi işlev profili örneği](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="ef10b-117">İşlevler</span><span class="sxs-lookup"><span data-stu-id="ef10b-117">Functions</span></span>

- <span data-ttu-id="ef10b-118">**Toplu ürünler**: etkinleştirildiğinde, bu işlev sepetin aynı madde birden çok kez eklendiğinde miktarın güncelleştirilmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="ef10b-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="ef10b-119">**Ödemeyle kullanıma alma işlemine izin ver**: etkinleştirildiğinde, alışveriş sepetine eklenen maddelerin fiyat $0,00 olduğunda bu işlev senaryoyu işler.</span><span class="sxs-lookup"><span data-stu-id="ef10b-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="ef10b-120">**Müşteriyi zaman uyumsuz modda oluştur**: Bu üçüncü taraf e-ticaret kanallarına uygulanabilen eski bir ayardır ve Dynamics 365 e-ticaret sitesine uygulanamaz.</span><span class="sxs-lookup"><span data-stu-id="ef10b-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef10b-121">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="ef10b-121">Additional resources</span></span>

[<span data-ttu-id="ef10b-122">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="ef10b-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ef10b-123">Kanal ayarlama önkoşulları</span><span class="sxs-lookup"><span data-stu-id="ef10b-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ef10b-124">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="ef10b-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="ef10b-125">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ef10b-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="ef10b-126">Çağrı merkezi kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ef10b-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
