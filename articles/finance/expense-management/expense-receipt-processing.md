---
title: Gider makbuzu işleme
description: Bu konu, makbuzlar için optik karakter tanıma (OCR) işlemi hakkında bilgi vermektedir. Bu özellik, Microsoft Dynamics 365 Finance'te gider raporları oluşturulurken kullanıcı deneyiminin geliştirilmesi için tasarlanmıştır.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 31c08ea264e6caec3217f4b424275495f39123e3
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378243"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="72b0d-104">Gider makbuzu işleme</span><span class="sxs-lookup"><span data-stu-id="72b0d-104">Expense receipt processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72b0d-105">Gider girişi, makbuzlar için optik karakter tanıma (OCR) işleminin devreye girmesiyle gelişim kaydetmiştir.</span><span class="sxs-lookup"><span data-stu-id="72b0d-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="72b0d-106">Bu özellik, gider raporları oluşturulurken kullanıcı deneyiminin geliştirilmesi için tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="72b0d-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="72b0d-107">Önemli özellikler</span><span class="sxs-lookup"><span data-stu-id="72b0d-107">Key features</span></span>

- <span data-ttu-id="72b0d-108">Satıcı adı, tarih ve toplam tutar makbuzlardan ayıklanır.</span><span class="sxs-lookup"><span data-stu-id="72b0d-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="72b0d-109">Özellik, iliştirilmemiş makbuzları iliştirilmemiş gider hareketlerine eşlemeyi dener.</span><span class="sxs-lookup"><span data-stu-id="72b0d-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="72b0d-110">Kullanıcılar, makbuzlardan el ile girilmiş gider hareketleri oluşturabilirler.</span><span class="sxs-lookup"><span data-stu-id="72b0d-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="72b0d-111">Kullanım örnekleri</span><span class="sxs-lookup"><span data-stu-id="72b0d-111">Usage examples</span></span>

<span data-ttu-id="72b0d-112">Gider raporu oluşturulurken kredi kartı hareketleri içeren makbuzları otomatik olarak iliştirmek için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="72b0d-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="72b0d-113">**Gider yönetimi** çalışma alanını açın.</span><span class="sxs-lookup"><span data-stu-id="72b0d-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="72b0d-114">**Makbuzlar** sekmesinde, iliştirilmemiş makbuzların olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="72b0d-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="72b0d-115">Makbuzları **Makbuzlar** sekmesinde de yükleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72b0d-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="72b0d-116">**Giderler** sekmesinde, iliştirilmemiş giderlerin olduğunu doğrulayın.</span><span class="sxs-lookup"><span data-stu-id="72b0d-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="72b0d-117">Genel olarak, gider yöneticisi bu giderleri kredi kartı sağlayıcısından içe aktarır.</span><span class="sxs-lookup"><span data-stu-id="72b0d-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="72b0d-118">**Yeni gider raporu**'nu seçin.</span><span class="sxs-lookup"><span data-stu-id="72b0d-118">Select **New expense report**.</span></span> <span data-ttu-id="72b0d-119">Artık, gider raporu oluştururken giderleri ve makbuzları da ekleyebildiğinizi bildirelim.</span><span class="sxs-lookup"><span data-stu-id="72b0d-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="72b0d-120">Hem giderler hem de makbuzlar eklerseniz, makbuzların giderlere karşı otomatik eşleşmesi tetiklenir.</span><span class="sxs-lookup"><span data-stu-id="72b0d-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="72b0d-121">Gider oluşturmak veya makbuzdan bir gideri eşlemek için aşağıdakileri yapın:</span><span class="sxs-lookup"><span data-stu-id="72b0d-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="72b0d-122">Bir gider raporunda, **Makbuzlar** sekmesinde, **Giriş ekle**'yi seçerek bir makbuz iliştirin.</span><span class="sxs-lookup"><span data-stu-id="72b0d-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="72b0d-123">Makbuzun karşıya yüklenen resminin altındaki **Oluştur** ve **Eşleştir** seçeneklerine dikkat edin.</span><span class="sxs-lookup"><span data-stu-id="72b0d-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="72b0d-124">El ile girilmiş bir gider hareketi oluşturmak ve makbuzdan ayıklanan değerleri doldurmak için **Oluştur**'u seçin.</span><span class="sxs-lookup"><span data-stu-id="72b0d-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="72b0d-125">**Eşleştir**'i seçerseniz, sistem varolan bir gideri makbuza eşleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="72b0d-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="72b0d-126">Yükleme</span><span class="sxs-lookup"><span data-stu-id="72b0d-126">Installation</span></span>

<span data-ttu-id="72b0d-127">Bu özellik, gider deneyimini basitleştirmeye yardımcı olmak için **Gider raporları yeniden tasarlandı** özelliğiyle birlikte çalışır.</span><span class="sxs-lookup"><span data-stu-id="72b0d-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="72b0d-128">Bu özellik yalnızca Katman 2+ ortamları, Korumalı Alan ve Üretim için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="72b0d-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="72b0d-129">Bu gelişmiş gider yeteneklerini kullanmak için, kurulumunuzda Microsoft Dynamics 365 Finance için Gider Yönetimi Hizmeti eklentisini yükleyin ve özellikleri etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="72b0d-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="72b0d-130">Eklentiye, Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72b0d-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="72b0d-131">LCS'de oturum açın ve istediğiniz ortamı açın.</span><span class="sxs-lookup"><span data-stu-id="72b0d-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="72b0d-132">**Tüm ayrıntılar**'a gidin.</span><span class="sxs-lookup"><span data-stu-id="72b0d-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="72b0d-133">**Bakım yap**'ı seçin veya **Ortam eklentileri** hızlı sekmesinde aşağı kaydırın.</span><span class="sxs-lookup"><span data-stu-id="72b0d-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="72b0d-134">**Yeni eklenti yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="72b0d-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="72b0d-135">**Gider Yönetimi Hizmeti**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="72b0d-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="72b0d-136">Yükleme kılavuzunu izleyin ve hüküm ve koşulları kabul edin.</span><span class="sxs-lookup"><span data-stu-id="72b0d-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="72b0d-137">**Yükle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="72b0d-137">Select **Install**.</span></span>

<span data-ttu-id="72b0d-138">**Özellik yönetimi** çalışma alanında aşağıdaki özellikleri açın:</span><span class="sxs-lookup"><span data-stu-id="72b0d-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="72b0d-139">Gider raporları yeniden tasarlandı</span><span class="sxs-lookup"><span data-stu-id="72b0d-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="72b0d-140">Otomatik eşleştir ve makbuzdan gider oluştur</span><span class="sxs-lookup"><span data-stu-id="72b0d-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="72b0d-141">Bu özellikleri açtığınız zaman aşağıdaki eylemler gerçekleşir:</span><span class="sxs-lookup"><span data-stu-id="72b0d-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="72b0d-142">Mevcut **Gider yönetimi** çalışma alanı yeni çalışma alanıyla değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="72b0d-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="72b0d-143">Gider alanı görünürlüğü için yeni bir menü öğesi eklenir.</span><span class="sxs-lookup"><span data-stu-id="72b0d-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="72b0d-144">Önceki **Gider raporları** sayfasını **Gider yönetimi > Giderlerim > Gider raporları**'na giderek açmaya devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="72b0d-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="72b0d-145">İş akışları ve onayların sizi varolan gider raporları sayfasına götürmeye devam eder.</span><span class="sxs-lookup"><span data-stu-id="72b0d-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="72b0d-146">Makbuzlar Microsoft Azure Cognitive Services üzerinden işlenir ve meta veriler ayıklanıp eklenir.</span><span class="sxs-lookup"><span data-stu-id="72b0d-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="72b0d-147">Eşleşen iliştirilmemiş makbuzları içeren bir gider raporu oluşturmanıza olanak sağlayan bir seçenek eklenmiştir.</span><span class="sxs-lookup"><span data-stu-id="72b0d-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="72b0d-148">Gider raporlarına eklenen bir seçenek, makbuzdan gider satırı oluşturmanıza olanak sağlar veya varolan bir makbuzu varolan bir gider satırıyla eşleştirmeye çalışır.</span><span class="sxs-lookup"><span data-stu-id="72b0d-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="72b0d-149">Gider raporları yeniden tasarlandı özelliği hakkında daha fazla bilgi için bkz. [Gider raporları yeniden tasarlandı](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="72b0d-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="72b0d-150">Sık sorulan sorular</span><span class="sxs-lookup"><span data-stu-id="72b0d-150">Frequently asked questions</span></span>

<span data-ttu-id="72b0d-151">**Microsoft, modelleri için verilerimi kullanıyor mu?**</span><span class="sxs-lookup"><span data-stu-id="72b0d-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="72b0d-152">Hayır, Microsoft makbuz işleme hizmeti için genel bir makine öğrenimi modeli oluşturdu.</span><span class="sxs-lookup"><span data-stu-id="72b0d-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="72b0d-153">Bu model, karşıya yüklediğiniz makbuzlara dayanmaz.</span><span class="sxs-lookup"><span data-stu-id="72b0d-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="72b0d-154">**Bu özellik nerede kullanılıyor ve işleniyor?**</span><span class="sxs-lookup"><span data-stu-id="72b0d-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="72b0d-155">Şu anda Amerika Birleşik Devletleri destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="72b0d-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="72b0d-156">**Makbuzlarım nereye gidiyor?**</span><span class="sxs-lookup"><span data-stu-id="72b0d-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="72b0d-157">Finance, alan verilerini ayıklamak için Cognitive Services ile bağlantı kuracaktır.</span><span class="sxs-lookup"><span data-stu-id="72b0d-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="72b0d-158">Cognitive Services, işlem yapılırken makbuzunuzun bir kopyasını 24 saate kadar koruyacaktır.</span><span class="sxs-lookup"><span data-stu-id="72b0d-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="72b0d-159">İşlem tamamlandıktan sonra, Cognitive Services makbuzu kaldırır.</span><span class="sxs-lookup"><span data-stu-id="72b0d-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="72b0d-160">Makbuzlar Finance'te depolanmaya devam eder.</span><span class="sxs-lookup"><span data-stu-id="72b0d-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="72b0d-161">Daha fazla bilgi için bkz. [Form Tanıma'nın yeni yeteneğiyle makbuz kavramayı etkinleştirme](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="72b0d-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
