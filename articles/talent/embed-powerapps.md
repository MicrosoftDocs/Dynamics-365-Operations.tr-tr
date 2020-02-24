---
title: Power Apps uygulamalarını Dynamics 365 Human Resources'de katıştırma
description: Bu konu, Microsoft Power Apps menü öğesinin Sistem yönetim modülünden kaybolduğu sorunu ortadan kaldırmayı açıklamaktadır.
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
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/04/2020
ms.locfileid: "3017885"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a><span data-ttu-id="ca70a-103">Power Apps uygulamalarını Dynamics 365 Human Resources'de katıştırma</span><span class="sxs-lookup"><span data-stu-id="ca70a-103">Embed Power Apps apps in Dynamics 365 Human Resources</span></span>

<span data-ttu-id="ca70a-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="ca70a-104">**Issue**</span></span>

<span data-ttu-id="ca70a-105">**Power Apps** menü öğesi, **Sistem yönetimi** modülünden kayboldu.</span><span class="sxs-lookup"><span data-stu-id="ca70a-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="ca70a-106">**Nedeni**</span><span class="sxs-lookup"><span data-stu-id="ca70a-106">**Cause**</span></span>

<span data-ttu-id="ca70a-107">Kullanıcı arabirimi (UI) tasarımı değiştirildi ve Microsoft Power Apps, şimdi standart kişiselleştirme modeline dahildir.</span><span class="sxs-lookup"><span data-stu-id="ca70a-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="ca70a-108">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="ca70a-108">**Resolution**</span></span>

<span data-ttu-id="ca70a-109">Power Apps'ın katıştırılma şekli değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="ca70a-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="ca70a-110">Artık Power Apps kişiselleştirme modeli aracılığıyla eklenir.</span><span class="sxs-lookup"><span data-stu-id="ca70a-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="ca70a-111">Power Apps'i Microsoft Dynamics 365 Talent içinde neredeyse her sayfaya ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca70a-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="ca70a-112">Talent içerisinde Power Apps'in nasıl katıştırılacağı hakkında bilgi için bkz. [Power Apps'i katıştırma](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="ca70a-112">For information about how to embed Power Apps in Talent, see [Embed Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="ca70a-113">Değişimden önce uygulamalarını katıştırmış olan her Power Apps kullanıcısının yeni modele yükseltilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="ca70a-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="ca70a-114">**Power Apps** düğmesi, Talent içindeki neredeyse her sayfanın sağ üst kösesindedir.</span><span class="sxs-lookup"><span data-stu-id="ca70a-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="ca70a-115">Uygulamaları eklemek için bu düğmeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="ca70a-115">You can use this button to insert apps.</span></span>

<span data-ttu-id="ca70a-116">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="ca70a-116">Here is an example.</span></span>

1. <span data-ttu-id="ca70a-117">**Personel yönetimi \> Bağlantılar \> Çalışanlar \> Personel**.</span><span class="sxs-lookup"><span data-stu-id="ca70a-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="ca70a-118">**Power Apps** düğmesini ve ardından **Power Apps'ten uygulama ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ca70a-118">Select the **Power Apps** button, and then select **Add an app from Power Apps**.</span></span>

    ![Power Apps düğmesi](media/png.png)

3. <span data-ttu-id="ca70a-120">**Power Apps'ten uygulama ekle** iletişim kutusundaki alanları doldurun.</span><span class="sxs-lookup"><span data-stu-id="ca70a-120">Complete the fields in the **Add an app from Power Apps** dialog box.</span></span>

    ![Power Apps'ten uygulama ekle iletişim kutusu](media/insert-powerapp.png)

<span data-ttu-id="ca70a-122">Alternatif olarak bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="ca70a-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="ca70a-123">Sayfanın eylem bölmesinde, **Seçenekler** sekmesinde, **Kişiselleştir** grubunda **Bu sayfayı kişiselleştir**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="ca70a-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this page**.</span></span>

    ![Seçenekler sekmesinde Kişiselleştir grubu](media/options.png)

    <span data-ttu-id="ca70a-125">Kişiselleştirme araç çubuğu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="ca70a-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="ca70a-126">Araç çubuğunda, **Power Apps'tenuygulama ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="ca70a-126">On the toolbar, select **Add an app from Power Apps**.</span></span>

    ![Kişiselleştirme araç çubuğunu kullanarak Power Apps'ten uygulama ekleme](media/powerapp-bar.png)
