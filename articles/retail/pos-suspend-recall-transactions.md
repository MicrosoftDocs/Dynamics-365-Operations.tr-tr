---
title: Satış noktasında (POS) bir hareketi askıya alıp devam ettirmek
description: Bu konu, kullanıcıların Dynamics 365 Retail kullanarak sürmekte olan bir hareketi nasıl askıya alabileceklerini ve sonra başka bir kayıtta nasıl devam ettirebileceklerini açıklar.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: efab3b793eb15e7feffb569492b5c36a2e9d6ec0
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025299"
---
# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a><span data-ttu-id="7bfb3-103">Satış noktasında (POS) hareketleri askıya alıp devam ettirmek</span><span class="sxs-lookup"><span data-stu-id="7bfb3-103">Suspend and resume transactions in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7bfb3-104">Satış noktası (POS) kullanıcıları, sürmekte olan hareketleri askıya alabilir ve onları daha sonra farklı bir kayıtta devam ettirebilirler.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="7bfb3-105">Hareketler çoğunlukla bir hareketi, geçerli hareket üzerindeki ilerlemeyi kaybetmeden başka bir görev için serbest bırakmakta kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="7bfb3-106">Örneğin, bir mağaza çalışanı bir müşterinin işlemini bir mobil cihazda işlemeye başlıyor ancak bunu bir nakit çekmecesi olan bir kasadan tamamlamak zorunda.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="7bfb3-107">Bu durumda, mağaza çalışanı hareketi askıya almak mobil aygıtta ve daha sonra geri alıp onu bir kayıt üzerinde devam edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="7bfb3-108">Askıya alma ve devam ettirme özelliğini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7bfb3-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="7bfb3-109">POS işlemleri</span><span class="sxs-lookup"><span data-stu-id="7bfb3-109">POS operations</span></span>

<span data-ttu-id="7bfb3-110">İki [POS işlemi](pos-operations.md), POS'un askıya alma ve devam ettirme senaryolarını desteklemesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="7bfb3-111">Bu işlemleri [düğme kılavuzlarına](pos-screen-layouts.md) hareket sayfası üzerinde veya hoş geldiniz sayfasında atayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="7bfb3-112">503: Hareketi askıya al</span><span class="sxs-lookup"><span data-stu-id="7bfb3-112">503: Suspend transaction</span></span>
- <span data-ttu-id="7bfb3-113">504: Hareketi geri çağır</span><span class="sxs-lookup"><span data-stu-id="7bfb3-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="7bfb3-114">Giriş şablonu</span><span class="sxs-lookup"><span data-stu-id="7bfb3-114">Receipt template</span></span>

<span data-ttu-id="7bfb3-115">POS, hareket askıya alındığında bir yazılı slip oluşturmak üzere yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="7bfb3-116">Bu slip daha sonra hareketi hızlıca tespit etmek ve geri çağırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="7bfb3-117">POS'un bir slip yazdırmasını etkinleştirmek için **Askıya alınmış hareket** giriş biçimini mağazanın giriş profiline eklemeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="7bfb3-118">Giriş biçimini, hareket hakkında belirli ayrıntıları dahil etmesi veya dışarıda bırakması üzerine tasarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="7bfb3-119">Örneğin, biçim taramayı desteklemek için bir barkod içerebilir.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="7bfb3-120">Makbuz numaralandırma</span><span class="sxs-lookup"><span data-stu-id="7bfb3-120">Receipt numbering</span></span>

<span data-ttu-id="7bfb3-121">Yazdırılmış giriş oluşturan diğer POS hareketi türleri gibi, mağazanın işlev profilindeki askıya alınmış **Giriş numaralandırma** bölümünde bir numara serisi tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="7bfb3-122">Vardiya kapanışında hükümsüz kıl</span><span class="sxs-lookup"><span data-stu-id="7bfb3-122">Void when closing shift</span></span>

<span data-ttu-id="7bfb3-123">**Vardiya kapanırken geçersiz** seçeneğini, kullanıcıların askıya alınmış hareketleri vardiyaları bitmeden önce tamamlamalarını veya hükümsüz kılmalarını gerektirmek için kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="7bfb3-124">**Vardiya kapatma** operasyonu sırasında POS, kullanıcıların kalan askıya alınmış hareketleri görüntülemesini veya hükümsüz kılmasını isteyebilir.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="7bfb3-125">Bir hareketi askıya almak ve devam ettirmek</span><span class="sxs-lookup"><span data-stu-id="7bfb3-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="7bfb3-126">Bir hareketi askıya al</span><span class="sxs-lookup"><span data-stu-id="7bfb3-126">Suspend a transaction</span></span>

<span data-ttu-id="7bfb3-127">Yeterli ayrıcalıklara sahip kullanıcılar ve **Hareketi askıya al** operasyonunu ekran düzenlerinde bulunduranlar, daha sonra başka bir kayıtta geri çağrılmak üzere bir hareketi askıya alabilirler.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="7bfb3-128">Hareketler, yalnızca aşağıdaki türde satırları **içermiyorlarsa** askıya alınabilirler:</span><span class="sxs-lookup"><span data-stu-id="7bfb3-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="7bfb3-129">Etkin ödeme satırları</span><span class="sxs-lookup"><span data-stu-id="7bfb3-129">Active payment lines</span></span>
- <span data-ttu-id="7bfb3-130">Hediye kartı satırları (bir hediye kartı vermek veya hediye kartı bakiyesine eklemek için)</span><span class="sxs-lookup"><span data-stu-id="7bfb3-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="7bfb3-131">Askıya alınmış bir hareke, mağaza için satış bilgisini veya stok kullanılabilirlik bilgisini etkilemez.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="7bfb3-132">Askıya alınmış bir hareketi devam ettirmek</span><span class="sxs-lookup"><span data-stu-id="7bfb3-132">Resume a suspended transaction</span></span>

<span data-ttu-id="7bfb3-133">Askıya alınmış hareketler, aynı mağazada yeterli ayrıcalıklara sahip herhangi bir kullanıcı ve **Hareketi geri çağır** operasyonunu içeren bir düzene sahip bir kullanıcı tarafından geri çağrılabilir ve devam ettirebilir.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="7bfb3-134">Askıya alınmış bir hareketi hızlı ve kolay şekilde geri çağırmak için **Hareketi geri çağır** operasyonunda hareketlerin listesini görüntülerken yazdırılmış slip üzerindeki barkodu taratın.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="7bfb3-135">Çevrimdışı mod için değerlendirmeler</span><span class="sxs-lookup"><span data-stu-id="7bfb3-135">Considerations for offline mode</span></span>

- <span data-ttu-id="7bfb3-136">POS çevrim içi moddayken askıya alınmış herhangi bir hareket, çevrimdışı modda devam ettirilemez çünkü veri, çevirmdışı veritabanına eşitlenmemiştir.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="7bfb3-137">Bir hareketi, POS çevrimdışı moddayken askıya alırsanız, siz hareketi askıya aldıktan sonraki herhangi bir zamanda POS'un tekrar çevrimiçi moda döndürülmemiş olması şartıyla onu çevrimdışı modda geri çağırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="7bfb3-138">POS çevrimiçi moda geri geçtiğinde, askıya alınmış hareketler çevrimiçi veritabanına taşınır ve çevrimdışı veritabanından kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="7bfb3-139">Bu nedenle, hareketler yalnızca çevrimiçi modda devam ettirilebilir.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="7bfb3-140">POS'u çevrimdışı moda geri çevirirseniz, askıya alınmış bu hareketi devam ettiremezsiniz çünkü çevrimdışı veritabanından halihazırda kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="7bfb3-141">Askıya alınmış bir hareketi hükümsüz kılmak</span><span class="sxs-lookup"><span data-stu-id="7bfb3-141">Void a suspended transaction</span></span>

<span data-ttu-id="7bfb3-142">Askıya alınmış hareketleri, hareketi geri çağırarak ve sonra **Hareketi hükümsüz kıl** operasyonunu gerçekleştirerek veya hareketi **Hareketi geri çağır** listesinde seçerek ve uygulama çubuğunda **Hükümsüz kıl** seçeneğini işaretleyerek hükümsüz kılabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="7bfb3-143">Alternatif olarak, mağaza, kullanıcıları askıya alınmış hareketleri vardiyaları bittiklerinde hükümsüz kılmaları konusunda uyarmak üzere yapılandırılabilir.</span><span class="sxs-lookup"><span data-stu-id="7bfb3-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
