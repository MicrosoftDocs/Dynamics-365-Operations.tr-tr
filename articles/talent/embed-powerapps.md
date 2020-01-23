---
title: Power Apps uygulamalarını Dynamics 365 - Core HR içine katıştırma
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
ms.openlocfilehash: b1dd1756be349d85af8e6d7159623a2a95e75526
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898724"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a><span data-ttu-id="bbd4a-103">Power Apps uygulamalarını Dynamics 365 - Core HR içine katıştırma</span><span class="sxs-lookup"><span data-stu-id="bbd4a-103">Embed Power Apps apps in Dynamics 365 - Core HR</span></span>

<span data-ttu-id="bbd4a-104">**Çıkış**</span><span class="sxs-lookup"><span data-stu-id="bbd4a-104">**Issue**</span></span>

<span data-ttu-id="bbd4a-105">**Power Apps** menü öğesi, **Sistem yönetimi** modülünden kayboldu.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-105">The **Power Apps** menu item has disappeared from the **System administration** module.</span></span>

<span data-ttu-id="bbd4a-106">**Nedeni**</span><span class="sxs-lookup"><span data-stu-id="bbd4a-106">**Cause**</span></span>

<span data-ttu-id="bbd4a-107">Kullanıcı arabirimi (UI) tasarımı değiştirildi ve Microsoft Power Apps, şimdi standart kişiselleştirme modeline dahildir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-107">The user interface (UI) design has been changed, and Microsoft Power Apps is now included in the standard personalization model.</span></span>

<span data-ttu-id="bbd4a-108">**Çözünürlük**</span><span class="sxs-lookup"><span data-stu-id="bbd4a-108">**Resolution**</span></span>

<span data-ttu-id="bbd4a-109">Power Apps'ın katıştırılma şekli değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-109">The way that Power Apps are embedded has been changed.</span></span> <span data-ttu-id="bbd4a-110">Artık Power Apps kişiselleştirme modeli aracılığıyla eklenir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-110">Power Apps are now added through the personalization model.</span></span> <span data-ttu-id="bbd4a-111">Power Apps'i Microsoft Dynamics 365 Talent içinde neredeyse her sayfaya ekleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-111">You can add Power Apps to almost all pages in Microsoft Dynamics 365 Talent.</span></span>

<span data-ttu-id="bbd4a-112">Talent içerisinde Power Apps'in nasıl katıştırılacağı hakkında bilgi için bkz. [Microsoft Power Apps'i katıştırma](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span><span class="sxs-lookup"><span data-stu-id="bbd4a-112">For information about how to embed Power Apps in Talent, see [Embed Microsoft Power Apps](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span>

<span data-ttu-id="bbd4a-113">Değişimden önce uygulamalarını katıştırmış olan her Power Apps kullanıcısının yeni modele yükseltilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-113">Any Power Apps customer who embedded apps before the change should have been upgraded to the new model.</span></span>

<span data-ttu-id="bbd4a-114">**Power Apps** düğmesi, Talent içindeki neredeyse her sayfanın sağ üst kösesindedir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-114">The **Power Apps** button is in the upper-right corner of almost every page in Talent.</span></span> <span data-ttu-id="bbd4a-115">Power Apps'i eklemek için bu düğmeyi kullanın.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-115">You can use this button to insert Power Apps.</span></span>

<span data-ttu-id="bbd4a-116">Aşağıda bir örnek verilmiştir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-116">Here is an example.</span></span>

1. <span data-ttu-id="bbd4a-117">**Personel yönetimi \> Bağlantılar \> Çalışanlar \> Personel**.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-117">Go to **Personnel management \> Links \> Workers \> Employees**.</span></span>
2. <span data-ttu-id="bbd4a-118">**Power Apps** düğmesini seçin ve sonra **Bir PowerApp ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-118">Select the **Power Apps** button, and then select **Insert a PowerApp**.</span></span>

    ![Power Apps düğmesi](media/png.png)

3. <span data-ttu-id="bbd4a-120">**Bir PowerApp ekleyin** iletişim kutusundaki alanları tamamlayın.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-120">Complete the fields in the **Insert a PowerApp** dialog box.</span></span>

    ![Bir PowerApp iletişim kutusu girin](media/insert-powerapp.png)

<span data-ttu-id="bbd4a-122">Alternatif olarak bu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-122">Alternatively, follow these steps.</span></span>

1. <span data-ttu-id="bbd4a-123">Sayfanın Eylem Panosunda, **Seçenekler** sekmesinde, **Kişiselleştir** grubunda, **Bu formu kişiselleştirin**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-123">On the page's Action Pane, on the **Options** tab, in the **Personalize** group, select **Personalize this form**.</span></span>

    ![Seçenekler sekmesinde Kişiselleştir grubu](media/options.png)

    <span data-ttu-id="bbd4a-125">Kişiselleştirme araç çubuğu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-125">The personalization toolbar appears.</span></span>

2. <span data-ttu-id="bbd4a-126">Araç çubuğunda **Ekle \> PowerApp**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="bbd4a-126">On the toolbar, select **Insert \> PowerApp**.</span></span>

    ![Kişiselleştirme araç çubuğunu kullanarak bir Power Apps uygulaması ekleme](media/powerapp-bar.png)
