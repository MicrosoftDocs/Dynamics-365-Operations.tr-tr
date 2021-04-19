---
title: Perakende işlevselliği profili oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta bir işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b8d481597485775796290f61de19ef7682cb9f43
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792010"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="667c7-103">Perakende işlevselliği profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="667c7-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="667c7-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta bir işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="667c7-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="667c7-105">Ticaret işlevsellik profili, çevrimiçi kanallarda çeşitli ayarlar sağlar.</span><span class="sxs-lookup"><span data-stu-id="667c7-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="667c7-106">Her bir kanalın bir işlevsellik profili belirtmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="667c7-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="667c7-107">İşlevsellik profili oluştur</span><span class="sxs-lookup"><span data-stu-id="667c7-107">Create a functionality profile</span></span>

<span data-ttu-id="667c7-108">İşlev profili oluşturmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="667c7-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="667c7-109">Gezinti bölmesinde **modüller \> Kanal kurulumu \> POS profilleri \> işlevsellik profillerine** gidin.</span><span class="sxs-lookup"><span data-stu-id="667c7-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="667c7-110">Eylem bölmesinde **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="667c7-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="667c7-111">**Profil** alanına profil için bir kimlik girin (aşağıdaki örnek resme "FN006").</span><span class="sxs-lookup"><span data-stu-id="667c7-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="667c7-112">**Açıklama** alanına, aşağıdaki örnek görüntüye bir değer ("Adventure Works profili") girin.</span><span class="sxs-lookup"><span data-stu-id="667c7-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="667c7-113">**Genel** bölümünde, **ISO** yerel ayarı için bir ülke seçin.</span><span class="sxs-lookup"><span data-stu-id="667c7-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="667c7-114">**Genel** bölümünde, diğer ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="667c7-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="667c7-115">**Genel** bölümünde, e-posta alındıları **için bir makbuz** profili kodu seçin.</span><span class="sxs-lookup"><span data-stu-id="667c7-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="667c7-116">**İşlevler** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="667c7-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="667c7-117">**Tutar** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="667c7-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="667c7-118">**Bilgi Kodları** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="667c7-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="667c7-119">**Makbuz numaralandırması** bölümünde, ayarları gerektiği gibi değiştirin.</span><span class="sxs-lookup"><span data-stu-id="667c7-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="667c7-120">Aşağıdaki resimde örnek bir işlevsellik profili gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="667c7-120">The following image shows an example functionality profile.</span></span>
  
![İşlev profili örneği](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="667c7-122">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="667c7-122">Additional resources</span></span>

[<span data-ttu-id="667c7-123">Bilgi kodları ve bilgi kodu grupları</span><span class="sxs-lookup"><span data-stu-id="667c7-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="667c7-124">Yeni adres defteri oluşturun</span><span class="sxs-lookup"><span data-stu-id="667c7-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="667c7-125">Ekran düzenine genel bakış</span><span class="sxs-lookup"><span data-stu-id="667c7-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="667c7-126">Retail Hardware Station'ı yapılandırma ve yükleme</span><span class="sxs-lookup"><span data-stu-id="667c7-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
