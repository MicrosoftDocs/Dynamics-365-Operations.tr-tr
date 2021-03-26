---
title: Perakende hareketlerini düzenlemek için bir Excel çalışma kitabı oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta perakende hareketlerini düzenleyebilmek için nasıl Excel çalışma kitabı oluşturabileceğiniz açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a4bc0a91ee2215dcde2f18575d58ab1ef2f5581
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207955"
---
# <a name="create-an-excel-workbook-to-edit-retail-transactions"></a><span data-ttu-id="11a37-103">Perakende hareketlerini düzenlemek için bir Excel çalışma kitabı oluşturma</span><span class="sxs-lookup"><span data-stu-id="11a37-103">Create an Excel workbook to edit retail transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11a37-104">Bu konuda, Microsoft Dynamics 365 Commerce'ta perakende hareketlerini düzenleyebilmek için nasıl Excel çalışma kitabı oluşturabileceğiniz açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="11a37-104">This topic describes how to create an Excel workbook so that you can edit retail transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="11a37-105">Genel bakış</span><span class="sxs-lookup"><span data-stu-id="11a37-105">Overview</span></span>

<span data-ttu-id="11a37-106">Müşterilerin sistemin farklı bölümlerinden erişebilecekleri ve perakende hareketlerini düzenleyip denetlemek için kullanabilecekleri önceden tanımlanmış bir Excel şablonu bulunur.</span><span class="sxs-lookup"><span data-stu-id="11a37-106">There is a predefined Excel template that customers can access from different parts of the system and use to edit and audit retail transactions.</span></span> <span data-ttu-id="11a37-107">Ancak müşteriler bu amaçla özel bir Excel çalışma kitabı da oluşturabilirler.</span><span class="sxs-lookup"><span data-stu-id="11a37-107">However, customers can also create a custom Excel workbook for this purpose.</span></span>

## <a name="create-and-configure-an-excel-workbook"></a><span data-ttu-id="11a37-108">Excel çalışma kitabı oluşturma ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="11a37-108">Create and configure an Excel workbook</span></span>

<span data-ttu-id="11a37-109">Perakende hareketlerini düzenleyebileceğiniz bir Excel çalışma kitabı oluşturmak ve yapılandırmak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="11a37-109">To create and configure an Excel workbook so that you can edit retail transactions, follow these steps.</span></span>

1. <span data-ttu-id="11a37-110">Excel'i açın ve boş bir çalışma kitabı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="11a37-110">Open Excel, and create a blank workbook.</span></span>
1. <span data-ttu-id="11a37-111">**Ekle** sekmesinde, **Eklentilerim**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="11a37-111">On the **Insert** tab, select **My add-ins**.</span></span>
1. <span data-ttu-id="11a37-112">Sağ bölmede, **Sunucu bilgilerini ekle** bağlantısını seçin.</span><span class="sxs-lookup"><span data-stu-id="11a37-112">In the right pane, select the **Add server information** link.</span></span>
1. <span data-ttu-id="11a37-113">Sunucu URL'sini girin ve ardından **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="11a37-113">Enter the server URL, and then select **OK**.</span></span>
1. <span data-ttu-id="11a37-114">"Uygulama kaydı bulunamadı" hata iletisini alırsanız sorunu çözmek için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="11a37-114">If you receive a "No applet registrations found" error message, follow these steps to resolve the issue:</span></span>

    1. <span data-ttu-id="11a37-115">Commerce uygulamasında, **Sistem yönetimi \> Ayar \> Office uygulaması parametreleri** bölümüne gidin.</span><span class="sxs-lookup"><span data-stu-id="11a37-115">In Commerce, go to **System administration \> Setup \> Office app parameters**.</span></span>
    1. <span data-ttu-id="11a37-116">**Uygulama parametreleri** hızlı sekmesinde, **Uygulama parametrelerini başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="11a37-116">On the **App parameters** FastTab, select **Initialize app parameters**.</span></span>
    1. <span data-ttu-id="11a37-117">Onay iletisi kutusunda **Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="11a37-117">In the confirmation message box, select **OK**.</span></span>
    1. <span data-ttu-id="11a37-118">**Kayıtlı uygulamalar** hızlı sekmesinde, **Uygulama kaydını başlat**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="11a37-118">On the **Registered applets** FastTab, select **Initialize applet registration**.</span></span>
    1. <span data-ttu-id="11a37-119">Gerekirse önceki üç adımı tekrarlayın.</span><span class="sxs-lookup"><span data-stu-id="11a37-119">Repeat the previous three steps as required.</span></span>

1. <span data-ttu-id="11a37-120">**Tasarım**'ı ve ardından **Tablo ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="11a37-120">Select **Design**, and then select **Add table**.</span></span>
1. <span data-ttu-id="11a37-121">Değiştirilmesi gereken verilere bağlı olarak, düzenlenmek üzere Excel çalışma kitabına eklenmesi gereken varlıkları seçin.</span><span class="sxs-lookup"><span data-stu-id="11a37-121">Based on the data that has to be modified, select the entities that must be added to the Excel workbook for editing.</span></span> <span data-ttu-id="11a37-122">Referans olarak aşağıdaki tabloyu kullanın.</span><span class="sxs-lookup"><span data-stu-id="11a37-122">Use the following table as a reference.</span></span>

    | <span data-ttu-id="11a37-123">Hareket türü</span><span class="sxs-lookup"><span data-stu-id="11a37-123">Transaction type</span></span> | <span data-ttu-id="11a37-124">Kullanılacak veri varlıkları</span><span class="sxs-lookup"><span data-stu-id="11a37-124">Data entities to use</span></span> |
    |------------------|----------------------|
    | <span data-ttu-id="11a37-125">Peşin hareketler, Çevrimiçi siparişler, Zaman uyumsuz müşteri siparişleri, Zaman uyumsuz müşteri teklifleri</span><span class="sxs-lookup"><span data-stu-id="11a37-125">Cash and carry transactions, Online orders, Async customer orders, Async customer quotes</span></span> | <span data-ttu-id="11a37-126">Hareket (denetlenebilir), Satış hareketi (denetlenebilir), Ödeme hareketleri (denetlenebilir), Vergi hareketleri (denetlenebilir), İskonto hareketleri (denetlenebilir), Masraf hareketleri (denetlenebilir)</span><span class="sxs-lookup"><span data-stu-id="11a37-126">Transaction (auditable), Sales transaction (auditable), Payment transactions (auditable), Tax transactions (auditable), Discount transactions (auditable), Charge transactions (auditable)</span></span> |
    | <span data-ttu-id="11a37-127">Bankaya para nakli</span><span class="sxs-lookup"><span data-stu-id="11a37-127">Bank drop</span></span> | <span data-ttu-id="11a37-128">Hareket (denetlenebilir), Bankaya nakledilen ödeme hareketleri (denetlenebilir)</span><span class="sxs-lookup"><span data-stu-id="11a37-128">Transaction (auditable), Banked tender transactions (auditable)</span></span> |
    | <span data-ttu-id="11a37-129">Kasaya para nakli</span><span class="sxs-lookup"><span data-stu-id="11a37-129">Safe drop</span></span> | <span data-ttu-id="11a37-130">Hareket (denetlenebilir), Kasa ödemesi hareketleri (denetlenebilir)</span><span class="sxs-lookup"><span data-stu-id="11a37-130">Transaction (auditable), Safe tender transactions (auditable)</span></span> |
    | <span data-ttu-id="11a37-131">Kasa sayımı</span><span class="sxs-lookup"><span data-stu-id="11a37-131">Tender declaration</span></span> | <span data-ttu-id="11a37-132">Hareket (denetlenebilir), Kasa sayımı hareketleri (denetlenebilir)</span><span class="sxs-lookup"><span data-stu-id="11a37-132">Transaction (auditable), Tender declaration transactions (auditable)</span></span> |
    | <span data-ttu-id="11a37-133">Gelir, Gider</span><span class="sxs-lookup"><span data-stu-id="11a37-133">Income, Expense</span></span> | <span data-ttu-id="11a37-134">Hareket (denetlenebilir), Gelir/Gider hareketleri (denetlenebilir), Ödeme hareketleri (denetlenebilir)</span><span class="sxs-lookup"><span data-stu-id="11a37-134">Transaction (auditable), Income/Expense transactions (auditable), Payment transactions (auditable)</span></span> |
    | <span data-ttu-id="11a37-135">Başlangıç tutarını beyan etme, Ödeme kaldırma, Kasa devri girişi, Para üstü ödeme, Fatura ödeme, Müşteri havalesi</span><span class="sxs-lookup"><span data-stu-id="11a37-135">Declare starting amount, Tender removal, Float entry, Change tender, Invoice payment, Customer deposit</span></span> | <span data-ttu-id="11a37-136">Hareket (denetlenebilir), Ödeme hareketleri (denetlenebilir)</span><span class="sxs-lookup"><span data-stu-id="11a37-136">Transaction (auditable), Payment transactions (auditable)</span></span> |

    > [!NOTE]
    > <span data-ttu-id="11a37-137">Her Excel çalışma kitabına yalnızca bir veri varlığı eklemeniz önemlidir.</span><span class="sxs-lookup"><span data-stu-id="11a37-137">It's important that you add only one data entity to each Excel workbook.</span></span> <span data-ttu-id="11a37-138">Ek olarak, bir anahtar simgesiyle işaretlenmiş tüm alanlar ilgili çalışma kitabına eklenmelidir.</span><span class="sxs-lookup"><span data-stu-id="11a37-138">Additionally, all fields that are marked by a key symbol must be added to the relevant workbook.</span></span>

1. <span data-ttu-id="11a37-139">Çalışma kitabı yapılandırıldıktan sonra gerekli filtreleri uygulayın.</span><span class="sxs-lookup"><span data-stu-id="11a37-139">After the workbook is configured, apply the required filters.</span></span> <span data-ttu-id="11a37-140">Dosyadaki tüm çalışma sayfalarına aynı filtreleri uyguladığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="11a37-140">Be sure to apply the same filters to all the worksheets in the file.</span></span> <span data-ttu-id="11a37-141">Excel dosyasına çok büyük miktarlarda veri yüklemekten kaçının.</span><span class="sxs-lookup"><span data-stu-id="11a37-141">Avoid loading very large amounts of data into the Excel file.</span></span> <span data-ttu-id="11a37-142">Aksi takdirde performans etkilenebilir, Excel ve sisteminiz yavaşlayabilir.</span><span class="sxs-lookup"><span data-stu-id="11a37-142">Otherwise, performance might be affected, and Excel and your system might slow down.</span></span> <span data-ttu-id="11a37-143">Dosyanızda her zaman "Şirket" ile "Ekstre Numarası" veya "Hareket Numarası" filtrelerini kullanmanızı öneririz.</span><span class="sxs-lookup"><span data-stu-id="11a37-143">We recommend that you always use "Company" and either "Statement Number" or "Transaction Number" as filters for your file.</span></span>
1. <span data-ttu-id="11a37-144">Filtreler yapılandırıldıktan sonra verileri yüklemek için **Yenile**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="11a37-144">After the filters are configured, select **Refresh** to load the data.</span></span>
1. <span data-ttu-id="11a37-145">Gerekli verileri düzenleyin ve ardından yayımlayın.</span><span class="sxs-lookup"><span data-stu-id="11a37-145">Edit the required data, and then publish it.</span></span> <span data-ttu-id="11a37-146">**Yayımla** düğmesi kullanılamıyorsa bazı önemli alanlar Excel çalışma kitabına eklenmemiş olabilir.</span><span class="sxs-lookup"><span data-stu-id="11a37-146">If the **Publish** button is unavailable, some key fields probably weren't added to the Excel workbook.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="11a37-147">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="11a37-147">Additional resources</span></span>

[<span data-ttu-id="11a37-148">Peşin ve nakit yönetimi hareketlerini düzenleme ve denetleme</span><span class="sxs-lookup"><span data-stu-id="11a37-148">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="11a37-149">Çevrimiçi siparişi ve zaman uyumsuz müşteri siparişi hareketlerini düzenleme ve denetleme</span><span class="sxs-lookup"><span data-stu-id="11a37-149">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="11a37-150">Perakende hareketlerinin mali boyutlarını düzenleme</span><span class="sxs-lookup"><span data-stu-id="11a37-150">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="11a37-151">Perakende hareketlerini düzenlemek için Excel çalışma kitabına alanlar ekleme</span><span class="sxs-lookup"><span data-stu-id="11a37-151">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]