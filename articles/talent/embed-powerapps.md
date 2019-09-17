---
title: PowerApps uygulamalarını Core HR içine katıştırma
description: Bu konu,, PowerApps menü öğesinin Sistem yönetim modülünden kaybolduğu sorunu ortadan kaldırmayı açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7c0dcdd7e2f407267cf99906b4d0b317858710af
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742831"
---
# <a name="embed-powerapps-apps-in-core-hr"></a><span data-ttu-id="e6cb3-103">PowerApps uygulamalarını Core HR içine katıştırma</span><span class="sxs-lookup"><span data-stu-id="e6cb3-103">Embed PowerApps apps in Core HR</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e6cb3-104">**Stok çıkışı**</span><span class="sxs-lookup"><span data-stu-id="e6cb3-104">**Issue**</span></span>

<span data-ttu-id="e6cb3-105">**PowerApps** menü öğesi, **Sistem yönetimi** modülünden kayboldu.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-105">The **PowerApps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="e6cb3-106">**Nedeni**</span><span class="sxs-lookup"><span data-stu-id="e6cb3-106">**Cause**</span></span>

<span data-ttu-id="e6cb3-107">Kullanıcı arabirimi (UI) tasarımı değiştirildi ve Microsoft PowerApps, şimdi standart kişiselleştirme modeline dahildir.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-107">The user interface (UI) design has been changed, and Microsoft PowerApps is now included in the standard personalization model.</span></span>

<span data-ttu-id="e6cb3-108">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="e6cb3-108">**Resolution**</span></span>

<span data-ttu-id="e6cb3-109">PowerApps uygulamalarının katıştırılması değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-109">The way that PowerApps apps are embedded has been changed.</span></span> <span data-ttu-id="e6cb3-110">Artık PowerApps uygulamaları kişiselleştirme modeli aracılığıyla eklenir.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-110">PowerApps apps are now added through the personalization model.</span></span> <span data-ttu-id="e6cb3-111">PowerApps uygulamalarını Microsoft Dynamics 365 for Talent içindeki neredeyse her sayfaya ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-111">You can add PowerApps apps to almost all pages in Microsoft Dynamics 365 for Talent.</span></span>

<span data-ttu-id="e6cb3-112">Talent içerisinde PowerApps uygulamasının nasıl katıştırılacağı hakkında bilgi için bkz: [PowerApps katıştırma](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="e6cb3-112">For information about how to embed PowerApps apps in Talent, see [Embed PowerApps apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="e6cb3-113">Değişimden önce uygulamalarını katıştırmış olan her PowerApps kullanıcısının yeni modele yükseltilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-113">Any PowerApps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="e6cb3-114">**PowerApps** düğmesi, Talent içindeki neredeyse her sayfanın sağ üst kösesindedir.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-114">The **PowerApps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="e6cb3-115">Bir PowerApps uygulaması eklemek için bu düğmeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-115">You can use this button to insert a PowerApps app.</span></span>

<span data-ttu-id="e6cb3-116">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-116">Here is an example.</span></span>

1. <span data-ttu-id="e6cb3-117">**Personel yönetimi \> Bağlantılar \> Çalışanlar \> Personel**.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="e6cb3-118">**PowerApps** düğmesini seçin ve sonra **Bir PowerApp ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-118">Select the **PowerApps** button, and then select **Insert a PowerApp**.</span></span>

    ![PowerApps düğmesi](media/png.png)

3. <span data-ttu-id="e6cb3-120">**Bir PowerApp ekleyin** iletişim kutusundaki alanları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Bir PowerApp iletişim kutusu girin](media/insert-powerapp.png)

<span data-ttu-id="e6cb3-122">Alternatif olarak bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="e6cb3-123">Sayfanın Eylem Panosunda, **Seçenekler** sekmesinde, **Kişiselleştir** grubunda, **Bu formu kişiselleştirin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Seçenekler sekmesinde Kişiselleştir grubu](media/options.png)

    <span data-ttu-id="e6cb3-125">Kişiselleştirme araç çubuğu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="e6cb3-126">Araç çubuğunda **Ekle \> PowerApp**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e6cb3-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Kişiselleştirme araç çubuğunu kullanarak bir PowerApps uygulamasını](media/powerapp-bar.png)
