---
title: Taşımacılık yönetimi modları ve yöntemleri
description: Bu konuda, Taşımacılık yönetimi modlarının ve yöntemlerinin nasıl ayarlanacağını gösterilmektedir.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: ceb3930cdb7764f846e88edfff6906b902a7f5fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/29/2020
ms.locfileid: "4439763"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="54897-103">Taşımacılık yönetimi modları ve yöntemleri</span><span class="sxs-lookup"><span data-stu-id="54897-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54897-104">Taşımacılık yönetimi modu; yükten az (LTL), kamyon yükü (TL) veya paket gibi taşıyıcının navlun teslimatları için kullandığı taşıma türünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="54897-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="54897-105">Taşımacılık yöntemi; hava yolu, kara yolu, deniz yolu veya demir yolu gibi taşıyıcının navlun teslimatları için kullandığı taşıma biçimini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="54897-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="54897-106">Modlar ve taşıma yöntemleri birçok bağlamda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="54897-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="54897-107">Rota planlarında yalnızca modlar kullanılırken sevkiyat taşıyıcıları ve taşıyıcı hizmetlerini ayarlanırken hem modlar hem de taşıma yöntemleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="54897-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="54897-108">Modlar ve taşıma yöntemleri arasında açık ilişki veya hiyerarşi yok.</span><span class="sxs-lookup"><span data-stu-id="54897-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="54897-109">Mod oluşturma</span><span class="sxs-lookup"><span data-stu-id="54897-109">Create a mode</span></span>

<span data-ttu-id="54897-110">Mod oluşturmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="54897-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="54897-111">**Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Mod** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="54897-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="54897-112">Yeni mod oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="54897-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="54897-113">Mod için benzersiz bir kimlik ve açıklayıcı ad girin.</span><span class="sxs-lookup"><span data-stu-id="54897-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="54897-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="54897-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="54897-115">Taşıma yöntemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="54897-115">Create a transportation method</span></span>

<span data-ttu-id="54897-116">Taşıma yöntemi oluşturmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="54897-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="54897-117">**Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Taşıma yöntemleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="54897-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="54897-118">Yeni taşıma yöntemi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="54897-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="54897-119">Taşıma modu için benzersiz bir kimlik ve açıklayıcı ad girin.</span><span class="sxs-lookup"><span data-stu-id="54897-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="54897-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="54897-120">Close the page.</span></span>
