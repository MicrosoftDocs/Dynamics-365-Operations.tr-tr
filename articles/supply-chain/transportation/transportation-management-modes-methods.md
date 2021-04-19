---
title: Taşımacılık yönetimi modları ve yöntemleri
description: Bu konuda, Taşımacılık yönetimi modlarının ve yöntemlerinin nasıl ayarlanacağını gösterilmektedir.
author: Henrikan
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 71e37dcd4509813f930906ae3bb3d3b98c9100a0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828325"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="ace3d-103">Taşımacılık yönetimi modları ve yöntemleri</span><span class="sxs-lookup"><span data-stu-id="ace3d-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ace3d-104">Taşımacılık yönetimi modu; yükten az (LTL), kamyon yükü (TL) veya paket gibi taşıyıcının navlun teslimatları için kullandığı taşıma türünü temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ace3d-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="ace3d-105">Taşımacılık yöntemi; hava yolu, kara yolu, deniz yolu veya demir yolu gibi taşıyıcının navlun teslimatları için kullandığı taşıma biçimini temsil eder.</span><span class="sxs-lookup"><span data-stu-id="ace3d-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="ace3d-106">Modlar ve taşıma yöntemleri birçok bağlamda kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ace3d-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="ace3d-107">Rota planlarında yalnızca modlar kullanılırken sevkiyat taşıyıcıları ve taşıyıcı hizmetlerini ayarlanırken hem modlar hem de taşıma yöntemleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="ace3d-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="ace3d-108">Modlar ve taşıma yöntemleri arasında açık ilişki veya hiyerarşi yok.</span><span class="sxs-lookup"><span data-stu-id="ace3d-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="ace3d-109">Mod oluşturma</span><span class="sxs-lookup"><span data-stu-id="ace3d-109">Create a mode</span></span>

<span data-ttu-id="ace3d-110">Mod oluşturmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="ace3d-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="ace3d-111">**Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Mod** öğesine gidin.</span><span class="sxs-lookup"><span data-stu-id="ace3d-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="ace3d-112">Yeni mod oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ace3d-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="ace3d-113">Mod için benzersiz bir kimlik ve açıklayıcı ad girin.</span><span class="sxs-lookup"><span data-stu-id="ace3d-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="ace3d-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ace3d-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="ace3d-115">Taşıma yöntemi oluşturma</span><span class="sxs-lookup"><span data-stu-id="ace3d-115">Create a transportation method</span></span>

<span data-ttu-id="ace3d-116">Taşıma yöntemi oluşturmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="ace3d-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="ace3d-117">**Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Taşıma yöntemleri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="ace3d-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="ace3d-118">Yeni taşıma yöntemi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ace3d-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="ace3d-119">Taşıma modu için benzersiz bir kimlik ve açıklayıcı ad girin.</span><span class="sxs-lookup"><span data-stu-id="ace3d-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="ace3d-120">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="ace3d-120">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]