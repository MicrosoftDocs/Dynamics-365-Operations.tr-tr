---
title: Attract'te Broadbean tümleştirmesini etkinleştirme
description: Bu konu, Microsoft Dynamics 365 Talent - Attract'i işleri Broadbean gibi harici iş panolarına gönderecek şekilde yapılandırma yöntemini açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 10b612711e81b2b368ed23fdd95ab6a66451f0ca
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/25/2019
ms.locfileid: "2833220"
---
# <a name="enable-broadbean-integration-in-attract"></a><span data-ttu-id="e12db-103">Attract'te Broadbean tümleştirmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e12db-103">Enable Broadbean integration in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e12db-104">Açık pozisyonlarınızı olabildiğince fazla kalifiye adayın önüne sunmak istersiniz.</span><span class="sxs-lookup"><span data-stu-id="e12db-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="e12db-105">Broadbean gibi işe alma siteleri bu hedefinizi gerçekleştirmeye yardımcı olur.</span><span class="sxs-lookup"><span data-stu-id="e12db-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="e12db-106">Microsoft Dynamics 365 Talent: Attract, şimdi Broadbean'e iş ilanları vermenize olanak sağlıyor ve Microsoft düzenli olarak bu alanda yeni olanaklar sunuyor.</span><span class="sxs-lookup"><span data-stu-id="e12db-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="e12db-107">Harici sitelere iş ilanı verebilmek için [Kapsamlı işe alma eklentisine](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e12db-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="e12db-108">Attract üzerinden Broadbean'a iş göndermek için bir Broadbean aboneliğine sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="e12db-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="e12db-109">Bu özellik şu anda önizlemededir.</span><span class="sxs-lookup"><span data-stu-id="e12db-109">This feature is currently in preview.</span></span> <span data-ttu-id="e12db-110">Denemek isterseniz, [Attract yönetici ayarlarında açmanız gerekir](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="e12db-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="e12db-111">Broadbean tümleştirmesini yapılandırın</span><span class="sxs-lookup"><span data-stu-id="e12db-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="e12db-112">Attract'e bir yönetici olarak oturum açın.</span><span class="sxs-lookup"><span data-stu-id="e12db-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="e12db-113">**Ayarlar** düğmesini (çark simgesi) sayfanın sağ üst köşesinde seçin ve sonra **Yönetici merkezini** seçin.</span><span class="sxs-lookup"><span data-stu-id="e12db-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="e12db-114">Broadbean ile iletişime geçin ve **Kullanıcı adı**, **İstemci Kimliği** ve **Şifreleme Belirteci** alanlarına bilgilerinizi girin.</span><span class="sxs-lookup"><span data-stu-id="e12db-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="e12db-115">**Kaydet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e12db-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="e12db-116">Broadbean kimlik bilgileriniz hassas ve gizlidir.</span><span class="sxs-lookup"><span data-stu-id="e12db-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="e12db-117">Bu nedenle, bunları dikkatli bir biçimde depolayın ve paylaşın.</span><span class="sxs-lookup"><span data-stu-id="e12db-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="e12db-118">Attract içinde Yönetici rolüne sahip herkes bu kimlik bilgilerini görebilir.</span><span class="sxs-lookup"><span data-stu-id="e12db-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="e12db-119">Microsoft ve Attract, bu değerleri oluşturmak ve saklanmakta söz sahibi değildir.</span><span class="sxs-lookup"><span data-stu-id="e12db-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="e12db-120">Attract için bunları güncel tutmak ve kimlik bilgileriniz içeren herhangi bir sorunu Broadbean ile iş birliği yaparak çözmek sizin sorumluluğunuzdur.</span><span class="sxs-lookup"><span data-stu-id="e12db-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
