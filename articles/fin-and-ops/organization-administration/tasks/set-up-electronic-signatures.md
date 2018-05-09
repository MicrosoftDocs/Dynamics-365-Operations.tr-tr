--- 
title: Elektronik imza ayarlama
description: "Bu yordamı kullanarak elektronik imzaları ayarların."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 95c1c750349feaa3bfe47385585989ef8f9fa3bc
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="c732f-103">Elektronik imza ayarlama</span><span class="sxs-lookup"><span data-stu-id="c732f-103">Set up electronic signatures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c732f-104">Bu yordamı kullanarak elektronik imzaları ayarların.</span><span class="sxs-lookup"><span data-stu-id="c732f-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="c732f-105">Elektronik imza bir hesaplama işlemi başlatmak veya onaylamak üzere olan kişinin kimliğini doğrular.</span><span class="sxs-lookup"><span data-stu-id="c732f-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="c732f-106">Bu yöntemi oluşturmak için kullanılan demo verisi şirketi DAT'dir.</span><span class="sxs-lookup"><span data-stu-id="c732f-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="c732f-107">Elektronik imza konfigürasyon anahtarını etkinleştirin</span><span class="sxs-lookup"><span data-stu-id="c732f-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="c732f-108">Sistem Yönetimi > Kurulum > Lisans yapılandırma seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="c732f-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="c732f-109">Ağaçta, 'Yönetim' öğesini genişletin veya daraltın.</span><span class="sxs-lookup"><span data-stu-id="c732f-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="c732f-110">Elektronik imza onay kutusunun işaretlendiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="c732f-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="c732f-111">Elektronik imza onay kutusu seçili değilse, bakım modunu etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="c732f-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="c732f-112">Bakım modu bu ortamda Lifecycle Services'den bir bakım işi çalıştırılarak ya da Deployment.Setup aracını yerel ortamda kullanarak etkin hale getirilebilir.</span><span class="sxs-lookup"><span data-stu-id="c732f-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="c732f-113">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c732f-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="c732f-114">Elektronik imza parametrelerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c732f-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="c732f-115">Kuruluş yönetimi > Kurulum > Elektronik imza > Elektronik imza parametreleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="c732f-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="c732f-116">Düzenle öğesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-116">Click Edit.</span></span>
3. <span data-ttu-id="c732f-117">Bildirim alanına bir değer yazın.</span><span class="sxs-lookup"><span data-stu-id="c732f-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="c732f-118">İmza istendiğinde imzalayanların alacağı bildirimi girin.</span><span class="sxs-lookup"><span data-stu-id="c732f-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="c732f-119">Herhangi bir metni girebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c732f-119">You can enter any text.</span></span> <span data-ttu-id="c732f-120">Genellikle bu metin kullanıcılara, bir belgenin imzalanmasının ne anlama geldiğini açıklar.</span><span class="sxs-lookup"><span data-stu-id="c732f-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="c732f-121">Bildirim metninin başka dillerde girmek isterseniz, çeviriler düğmesini tıklatın.</span><span class="sxs-lookup"><span data-stu-id="c732f-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="c732f-122">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-122">Click Save.</span></span>
5. <span data-ttu-id="c732f-123">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c732f-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="c732f-124">Elektronik imzalar için neden kodları ayarlama</span><span class="sxs-lookup"><span data-stu-id="c732f-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="c732f-125">Kuruluş yönetimi > Kurulum > Elektronik imza > Elektronik imza sebep kodları seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="c732f-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="c732f-126">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-126">Click New.</span></span>
    * <span data-ttu-id="c732f-127">Elektronik imzaları kullanmadan önce neden kodları ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="c732f-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="c732f-128">Bir belgeyi imzalarken geçerli bir neden kodu gerekir.</span><span class="sxs-lookup"><span data-stu-id="c732f-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="c732f-129">İmzalayan, bir elektronik imzanın amacını belirtmek üzere bir neden kodu seçer.</span><span class="sxs-lookup"><span data-stu-id="c732f-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="c732f-130">Örneği, yasal onayı belirtmek için bir neden kodu kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="c732f-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="c732f-131">Sebep kodu alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c732f-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="c732f-132">Açıklama alanına bir değer girin.</span><span class="sxs-lookup"><span data-stu-id="c732f-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c732f-133">Gerekirse ek neden kodlarını girin.</span><span class="sxs-lookup"><span data-stu-id="c732f-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="c732f-134">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-134">Click Save.</span></span>
6. <span data-ttu-id="c732f-135">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c732f-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="c732f-136">Varolan bir işlemler için elektronik imzayı gerekli kılın</span><span class="sxs-lookup"><span data-stu-id="c732f-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="c732f-137">Kuruluş yönetimi > Kurulum > Elektronik imza > Elektronik imza gereksinimleri seçeneğine gidin.</span><span class="sxs-lookup"><span data-stu-id="c732f-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="c732f-138">Listede, istenen kaydı bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c732f-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c732f-139">Elektronik imza gerektiren bir işlem seçme.</span><span class="sxs-lookup"><span data-stu-id="c732f-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="c732f-140">İmza gerekli onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="c732f-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="c732f-141">Elektronik imza gerektiren her işlem için bu adımları yineleyin.</span><span class="sxs-lookup"><span data-stu-id="c732f-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="c732f-142">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="c732f-143">Elektronik imzalar için özel bir gereksinim oluşturun</span><span class="sxs-lookup"><span data-stu-id="c732f-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="c732f-144">Yeni'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-144">Click New.</span></span>
2. <span data-ttu-id="c732f-145">İmza gerekli onay kutusunu seçin veya temizleyin.</span><span class="sxs-lookup"><span data-stu-id="c732f-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="c732f-146">Ad alanında, elektronik imza gerektiren bir işlem için bir ad girin.</span><span class="sxs-lookup"><span data-stu-id="c732f-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="c732f-147">Tablo adı alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c732f-148">Listeden, imzalanması gereken verilerin depolandığı tabloyu bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c732f-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="c732f-149">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="c732f-150">Alan ismi alanında, aramayı açmak için açılır menü düğmesine tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c732f-151">Listede, izlemek istediğiniz tabloyu bulun ve seçin.</span><span class="sxs-lookup"><span data-stu-id="c732f-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="c732f-152">Listede, seçili satırdaki bağlantıya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c732f-153">İmzanın ne zaman gerekli olacağını belirtin.</span><span class="sxs-lookup"><span data-stu-id="c732f-153">Specify when a signature is required.</span></span>     <span data-ttu-id="c732f-154">Alan içindeki veri değiştiğinde imza gerekliyse Her zaman'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="c732f-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="c732f-155">Yalnızca belirli koşullarda imza gerekliyse, Yalnızca'yı seçin.</span><span class="sxs-lookup"><span data-stu-id="c732f-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="c732f-156">Yalnızca'yı seçerseniz, ayrıca aşağıdaki seçeneklerden birini seçmelisiniz: bir kayıt silindiğinde, bir kayıt güncelleştirildiğinde veya bir kayıt eklendiğinde.</span><span class="sxs-lookup"><span data-stu-id="c732f-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="c732f-157">Kaydet'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="c732f-157">Click Save.</span></span>
11. <span data-ttu-id="c732f-158">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="c732f-158">Close the page.</span></span>


