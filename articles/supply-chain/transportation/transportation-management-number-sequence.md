---
title: Taşıma yönetimi numara serisi
description: Bu konuda, taşıma yönetimi için numara serilerinin nasıl ayarlanacağı açıklanmaktadır.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b7bb6c9338808828a41801a85a1b93b420e9c75b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004761"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="74e6c-103">Taşıma yönetimi numara serisi</span><span class="sxs-lookup"><span data-stu-id="74e6c-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74e6c-104">Çeşitli profesyonel numaraları ayarlamak için, taşıma yönetimi modülündeki **Numara serileri** sayfasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="74e6c-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="74e6c-105">Profesyonel numaralar, her sevkiyatın ilerlemesini düzenlemek ve izlemek için taşıyıcılar tarafından kullanılır.</span><span class="sxs-lookup"><span data-stu-id="74e6c-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="74e6c-106">Profesyonel numaralar için numara serisi oluşturma</span><span class="sxs-lookup"><span data-stu-id="74e6c-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="74e6c-107">Profesyonel numaralara yönelik numara serisi oluşturmak için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="74e6c-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="74e6c-108">**Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Numara serileri** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="74e6c-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="74e6c-109">Yeni bir numara serisi oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="74e6c-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="74e6c-110">Numara serisi için benzersiz bir kimlik ve açıklayıcı ad girin.</span><span class="sxs-lookup"><span data-stu-id="74e6c-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="74e6c-111">**Numara serisi türü** alanındaki tek seçenek *Profesyonel numara* alanıdır.</span><span class="sxs-lookup"><span data-stu-id="74e6c-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="74e6c-112">**Denetleme basamağı** alanında, *Denetleme basamağı* tek seçenektir ve genel altyapı olarak ayarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="74e6c-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="74e6c-113">**Seri** hızlı sekmesinde, sırayla ilgili bilgileri sağlayın.</span><span class="sxs-lookup"><span data-stu-id="74e6c-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="74e6c-114">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="74e6c-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="74e6c-115">Numara serilerini sevkiyat taşıyıcısı ile ilişkilendirme</span><span class="sxs-lookup"><span data-stu-id="74e6c-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="74e6c-116">Numara serilerini bir taşıyıcıya bağlamak için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="74e6c-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="74e6c-117">**Taşımacılık yönetimi \> Kurulum \> Taşıyıcılar \> Sevkiyat taşıyıcıları** seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="74e6c-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="74e6c-118">Sevkiyat taşıyıcısı seçin.</span><span class="sxs-lookup"><span data-stu-id="74e6c-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="74e6c-119">**Düzenle** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="74e6c-119">Select **Edit**.</span></span>
1. <span data-ttu-id="74e6c-120">**Genel Bakış** hızlı sekmesinde, **Pro numara serisi** alanında bir seçenek belirleyin.</span><span class="sxs-lookup"><span data-stu-id="74e6c-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="74e6c-121">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="74e6c-121">Close the page.</span></span>
