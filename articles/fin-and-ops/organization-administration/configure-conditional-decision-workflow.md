---
title: "Bir iş akışında koşullu bir kararı yapılandırma"
description: "Koşullu kararın özelliklerini yapılandırmak için aşağıdaki yordamı kullanın."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 597a6a254dcd623f9e7c59a0309eeedee1b5adee
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a><span data-ttu-id="6e17d-103">Bir iş akışında koşullu bir kararı yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6e17d-103">Configure a conditional decision in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6e17d-104">Koşullu kararın özelliklerini yapılandırmak için aşağıdaki yordamı kullanın.</span><span class="sxs-lookup"><span data-stu-id="6e17d-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="6e17d-105">Koşullu karar, bir iş akışının iki dala ayrıldığı bir noktadır.</span><span class="sxs-lookup"><span data-stu-id="6e17d-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="6e17d-106">Koşullu bir kararı iş akışı düzenleyicisinde yapılandırmak için koşullu karara sağ tıklayın ve ardından **Özellikler** formunu açmak için **Özellikler**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e17d-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="6e17d-107">Karara ad verme</span><span class="sxs-lookup"><span data-stu-id="6e17d-107">Name a decision</span></span>
<span data-ttu-id="6e17d-108">Koşullu bir karara bir ad vermek için aşağıdaki adımları uygulayın.</span><span class="sxs-lookup"><span data-stu-id="6e17d-108">Follow these steps to enter a name for a conditional decision.</span></span>
1.  <span data-ttu-id="6e17d-109">Sol bölmede **Temel Ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e17d-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="6e17d-110">Koşullu karar için **Ad** alanına benzersiz bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="6e17d-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="6e17d-111"> Koşulları ayarlama</span><span class="sxs-lookup"><span data-stu-id="6e17d-111">Set conditions</span></span>
<span data-ttu-id="6e17d-112">Sistem, gönderilen belgeyi belirli koşulları karşılayıp karşılamadığını belirlemek için değerlendirerek hangi dalın kullanıldığını belirler.</span><span class="sxs-lookup"><span data-stu-id="6e17d-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>
1.  <span data-ttu-id="6e17d-113">Sol bölmede **Temel Ayarlar**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e17d-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="6e17d-114">**Koşul ekle** seçeneğini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6e17d-114">Click **Add condition**.</span></span>
3.  <span data-ttu-id="6e17d-115">Koşulu girin.</span><span class="sxs-lookup"><span data-stu-id="6e17d-115">Enter a condition.</span></span>
4.  <span data-ttu-id="6e17d-116">Gerekiyorsa ek koşulları girin.</span><span class="sxs-lookup"><span data-stu-id="6e17d-116">Enter additional conditions, if they are required.</span></span>
5.  <span data-ttu-id="6e17d-117">Girdiğiniz koşulların doğru biçimde yapılandırıldığını doğrulamak için aşağıdaki adımları tamamlayın:</span><span class="sxs-lookup"><span data-stu-id="6e17d-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="6e17d-118">**Sınama iş akışı koşulu** formunu açmak için **Sına**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e17d-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="6e17d-119">Formdaki **Koşulu doğrula** alanından bir kayıt seçin.</span><span class="sxs-lookup"><span data-stu-id="6e17d-119">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="6e17d-120">**Sına**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e17d-120">Click **Test**.</span></span> <span data-ttu-id="6e17d-121">Sistem, belirtmiş olduğunuz koşullarını yerine getirip getirmediğini belirlemek için kaydı değerlendirir.</span><span class="sxs-lookup"><span data-stu-id="6e17d-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="6e17d-122">**Özellikler** formuna geri dönmek için **Tamam** veya **İptal**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e17d-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>






