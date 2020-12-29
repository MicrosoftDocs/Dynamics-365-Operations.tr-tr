---
title: Perakende işlevselliği profili oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta bir işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.
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
ms.openlocfilehash: 6bee51eb25b04eb65e588dd4cf54a0cef587aa15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416296"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="9a50c-103">Perakende işlevselliği profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="9a50c-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="9a50c-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta bir işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="9a50c-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9a50c-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="9a50c-105">Overview</span></span>

<span data-ttu-id="9a50c-106">Ticaret işlevsellik profili, çevrimiçi kanallarda çeşitli ayarlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="9a50c-106">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="9a50c-107">Her bir kanalın bir işlevsellik profili belirtmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="9a50c-107">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="9a50c-108">İşlevsellik profili oluştur</span><span class="sxs-lookup"><span data-stu-id="9a50c-108">Create a functionality profile</span></span>

<span data-ttu-id="9a50c-109">İşlev profili oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-109">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="9a50c-110">Gezinti bölmesinde **modüller \> Kanal kurulumu \> POS profilleri \> işlevsellik profillerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="9a50c-111">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="9a50c-112">**Profil** alanına profil için bir kimlik girin (aşağıdaki örnek resme "FN006").</span><span class="sxs-lookup"><span data-stu-id="9a50c-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="9a50c-113">**Açıklama** alanına, aşağıdaki örnek görüntüye bir değer ("Adventure Works profili") girin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="9a50c-114">**Genel** bölümünde, **ISO** yerel ayarı için bir ülke seçin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="9a50c-115">**Genel** bölümünde, diğer ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="9a50c-116">**Genel** bölümünde, e-posta alındıları **için bir makbuz** profili kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="9a50c-117">**İşlevler** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="9a50c-118">**Tutar** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="9a50c-119">**Bilgi Kodları** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="9a50c-120">**Makbuz numaralandırması** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="9a50c-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="9a50c-121">Aşağıdaki resimde örnek bir işlevsellik profili gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9a50c-121">The following image shows an example functionality profile.</span></span>
  
![İşlev profili örneği](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="9a50c-123">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="9a50c-123">Additional resources</span></span>

[<span data-ttu-id="9a50c-124">Bilgi kodları ve bilgi kodu grupları</span><span class="sxs-lookup"><span data-stu-id="9a50c-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="9a50c-125">Yeni adres defteri oluşturun</span><span class="sxs-lookup"><span data-stu-id="9a50c-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="9a50c-126">Ekran düzenine genel bakış</span><span class="sxs-lookup"><span data-stu-id="9a50c-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="9a50c-127">Retail Hardware Station'ı yapılandırma ve yükleme</span><span class="sxs-lookup"><span data-stu-id="9a50c-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 
