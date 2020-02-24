---
title: Perakende işlevselliği profili oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta bir perakende işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.
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
ms.openlocfilehash: 9fb0fd63b11e55f2b153fc9c135f148a6e343057
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002855"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="6ada3-103">Perakende işlevselliği profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="6ada3-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6ada3-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta bir perakende işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="6ada3-104">This topic describes how to create a retail functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6ada3-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="6ada3-105">Overview</span></span>

<span data-ttu-id="6ada3-106">Perakende işlevsellik profili, çevrimiçi kanallarda çeşitli ayarlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="6ada3-106">The retail functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="6ada3-107">Her bir perakende kanalın bir perakende işlevsellik profili belirtmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6ada3-107">Each retail channel must specify a retail functionality profile.</span></span>

## <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="6ada3-108">Perakende işlevselliği profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="6ada3-108">Create a retail functionality profile</span></span>

<span data-ttu-id="6ada3-109">Perakende işlev profili oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-109">To create a retail functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="6ada3-110">Gezinti bölmesinde **modüller \> Kanal kurulumu \> POS profilleri \> işlevsellik profillerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="6ada3-111">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6ada3-112">**Profil** alanına profil için bir kimlik girin (aşağıdaki örnek resme "FN006").</span><span class="sxs-lookup"><span data-stu-id="6ada3-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="6ada3-113">**Açıklama** alanına, aşağıdaki örnek görüntüye bir değer ("Adventure Works profili") girin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="6ada3-114">**Genel** bölümünde, **ISO** yerel ayarı için bir ülke seçin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="6ada3-115">**Genel** bölümünde, diğer ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="6ada3-116">**Genel** bölümünde, e-posta alındıları **için bir makbuz** profili kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="6ada3-117">**İşlevler** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="6ada3-118">**Tutar** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="6ada3-119">**Bilgi Kodları** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="6ada3-120">**Makbuz numaralandırması** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="6ada3-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="6ada3-121">Aşağıdaki resimde örnek bir perakende işlevsellik profili gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="6ada3-121">The following image shows an example retail functionality profile.</span></span>
  
![Perakende işlev profili örneği](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="6ada3-123">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6ada3-123">Additional resources</span></span>

[<span data-ttu-id="6ada3-124">Bilgi kodları ve bilgi kodu grupları</span><span class="sxs-lookup"><span data-stu-id="6ada3-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="6ada3-125">Yeni adres defteri oluşturun</span><span class="sxs-lookup"><span data-stu-id="6ada3-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="6ada3-126">Ekran düzenine genel bakış</span><span class="sxs-lookup"><span data-stu-id="6ada3-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="6ada3-127">Retail Hardware Station'ı yapılandırma ve yükleme</span><span class="sxs-lookup"><span data-stu-id="6ada3-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
