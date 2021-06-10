---
title: Adres değişikliklerini görüntüleme ve yönetme
description: Bu konu adres değişikliklerini Dynamics 365 Human Resources'ta nasıl görüntüleyebileceğinizi ve yöneteceğinizi açıklamaktadır.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 751e903b011b74fad584a1a22b574134610aa3d2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051773"
---
# <a name="view-and-manage-address-changes"></a><span data-ttu-id="27b41-103">Adres değişikliklerini görüntüleme ve yönetme</span><span class="sxs-lookup"><span data-stu-id="27b41-103">View and manage address changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="27b41-104">Bu konu, adres değişikliklerini Personel self servisi **Kişisel ayrıntıları düzenle** sayfasında veya Dynamics 365 Human Resources'taki **Çalışan** ayrıntıları sayfasında nasıl görüntüleyip yönetebileceğinizi açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="27b41-104">This topic explains how you can view and manage address changes in the Employee self-service **Edit personal details** page or the **Worker** details page in Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="27b41-105">Birçok kuruluş, çalışanların kendi kişisel ayrıntılarını self servis deneyimiyle yönetmesini ister.</span><span class="sxs-lookup"><span data-stu-id="27b41-105">Many organizations want employees to manage their own personal details through a self-service experience.</span></span> <span data-ttu-id="27b41-106">Kullanıcıların adreslerini **Personel self servis** çalışma alanında güncelleştirmelerine olanak tanıyabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27b41-106">You can allow users to update their address in the **Employee self service** workspace.</span></span> <span data-ttu-id="27b41-107">Daha sonra, bu değişiklikleri **Personel yönetimi** çalışma alanında izleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27b41-107">You can then monitor these changes in the **Personnel management** workspace.</span></span> <span data-ttu-id="27b41-108">Bu özelliği kullanmak için, değişiklikleri **İnsan kaynakları parametreleri** sayfasında görüntülemek istediğiniz gün sayısını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="27b41-108">To use this feature, you must specify the number of days that you want to view changes in the **Human resources parameters** page.</span></span>

## <a name="configure-address-change-parameters"></a><span data-ttu-id="27b41-109">Adres değişikliği parametrelerini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="27b41-109">Configure address change parameters</span></span>

<span data-ttu-id="27b41-110">**Personel yönetimi** çalışma alanında adres değişikliklerinin görünmesini istediğiniz gün sayısını yapılandırmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="27b41-110">To configure the number of days that you want address changes to appear in the **Personnel management** workspace, follow these steps:</span></span>

1. <span data-ttu-id="27b41-111">Gezinti bölmesinde **Personel yönetimi**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-111">On the navigation pane, select **Personnel management**.</span></span>

2. <span data-ttu-id="27b41-112">**Bağlantılar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-112">Select **Links**.</span></span>

3. <span data-ttu-id="27b41-113">**İnsan kaynakları parametreleri**'ni seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-113">Select **Human resources parameters**.</span></span>

4. <span data-ttu-id="27b41-114">**Adres değişikliği** altındaki **Gün sayısı** alanına adres değişikliklerinin **Personel yönetimi** çalışma alanında görünmesini istediğiniz gün sayısını girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-114">In the **Number of days** field under **Address change**, enter the number of days that you want address changes to appear in the **Personnel management** workspace.</span></span>

5. <span data-ttu-id="27b41-115">Sayfayı kapatın.</span><span class="sxs-lookup"><span data-stu-id="27b41-115">Close the page.</span></span>

## <a name="create-or-change-an-employee-address"></a><span data-ttu-id="27b41-116">Çalışan adresi oluşturma veya değiştirme</span><span class="sxs-lookup"><span data-stu-id="27b41-116">Create or change an employee address</span></span>

<span data-ttu-id="27b41-117">Çalışanlar kendi adreslerini **Personel self servis** çalışma alanında güncelleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="27b41-117">Employees can update their own address in the **Employee self service** workspace.</span></span> <span data-ttu-id="27b41-118">Adres oluşturmak veya değiştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="27b41-118">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="27b41-119">Giriş sayfanızda **Personel self servisi** kutucuğunu seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-119">Select the **Employee self-service** tile on your home page.</span></span>

2. <span data-ttu-id="27b41-120">**Kişisel ayrıntıları düzenle** seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-120">Select **Edit personal details**.</span></span>

3. <span data-ttu-id="27b41-121">Adres eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-121">To add an address, select **Add**.</span></span> <span data-ttu-id="27b41-122">Varolan bir adresi güncelleştirmek için, listeden adresi seçin ve **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-122">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="27b41-123">**Ad veya açıklama** girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-123">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="27b41-124">**Amaç** açılan kutusunu seçin ve sonra adres türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-124">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="27b41-125">**Ülke/bölge** girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-125">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="27b41-126">**Posta kodu** girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-126">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="27b41-127">**Cadde** girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-127">Enter the **Street**.</span></span>

9. <span data-ttu-id="27b41-128">**Şehir**, **İl** ve **İlçe** girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-128">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="27b41-129">Bu alanlar genellikle **posta kodu** alanına göre otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="27b41-129">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="27b41-130">İsteğe bağlı olarak, birincil adres belirtmek için **Birincil** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-130">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="27b41-131">Yalnızca tek bir adres birincil olarak işaretlenebilir.</span><span class="sxs-lookup"><span data-stu-id="27b41-131">Only one address can be marked as the primary.</span></span> <span data-ttu-id="27b41-132">Zaten birincil adres olarak işaretlenmiş başka bir adres varsa, bu adresi birincil olarak kullanmak istediğinizi onaylamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="27b41-132">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="27b41-133">İsteğe bağlı olarak, adresin özel olduğunu belirtmek için **Özel** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-133">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="27b41-134">Yalnızca özel adres bilgilerini görüntülemek için açıkça izni olan kullanıcılar bu adresi görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="27b41-134">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="27b41-135">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-135">Select **OK**.</span></span>

## <a name="create-or-change-a-worker-address"></a><span data-ttu-id="27b41-136">Çalışan adresi oluşturma veya değiştirme</span><span class="sxs-lookup"><span data-stu-id="27b41-136">Create or change a worker address</span></span>

<span data-ttu-id="27b41-137">Bir adresi, **Personel yönetimi** çalışma alanında güncelleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27b41-137">You can update an address in the **Personnel management** workspace.</span></span> <span data-ttu-id="27b41-138">Adres oluşturmak veya değiştirmek için şu adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="27b41-138">Follow these steps to create or change an address:</span></span>

1. <span data-ttu-id="27b41-139">**Personel yönetimi** çalışma alanında, **Bağlantılar**'ı seçin ve sonra **Çalışanlar**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-139">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>

3. <span data-ttu-id="27b41-140">Çalışanı seçip **Adresler** öğesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-140">Select the worker, and then select **Addresses**.</span></span>

3. <span data-ttu-id="27b41-141">Adres eklemek için **Ekle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-141">To add an address, select **Add**.</span></span> <span data-ttu-id="27b41-142">Varolan bir adresi güncelleştirmek için, listeden adresi seçin ve **Düzenle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-142">To update an existing address, select the address from the list and then select **Edit**.</span></span>

4. <span data-ttu-id="27b41-143">**Ad veya açıklama** girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-143">Enter the **Name or description**.</span></span>

5. <span data-ttu-id="27b41-144">**Amaç** açılan kutusunu seçin ve sonra adres türünü seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-144">Select the **Purpose** drop-down box and then select the type of address.</span></span>

6. <span data-ttu-id="27b41-145">**Ülke/bölge** girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-145">Enter the **Country/region**.</span></span>

7. <span data-ttu-id="27b41-146">**Posta kodu** girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-146">Enter the **ZIP/postal code**.</span></span>

8. <span data-ttu-id="27b41-147">**Cadde** girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-147">Enter the **Street**.</span></span>

9. <span data-ttu-id="27b41-148">**Şehir**, **İl** ve **İlçe** girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-148">Enter the **City**, **State**, and **County**.</span></span> <span data-ttu-id="27b41-149">Bu alanlar genellikle **posta kodu** alanına göre otomatik olarak ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="27b41-149">Typically, these fields are automatically set based on the **ZIP/postal code** field.</span></span>

10. <span data-ttu-id="27b41-150">İsteğe bağlı olarak, birincil adres belirtmek için **Birincil** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-150">Optionally, select the **Primary** field to indicate a primary address.</span></span> <span data-ttu-id="27b41-151">Yalnızca tek bir adres birincil olarak işaretlenebilir.</span><span class="sxs-lookup"><span data-stu-id="27b41-151">Only one address can be marked as the primary.</span></span> <span data-ttu-id="27b41-152">Zaten birincil adres olarak işaretlenmiş başka bir adres varsa, bu adresi birincil olarak kullanmak istediğinizi onaylamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="27b41-152">If another address is already marked as the primary address, you'll need to confirm that you want to use this address as the primary.</span></span>

11. <span data-ttu-id="27b41-153">İsteğe bağlı olarak, adresin özel olduğunu belirtmek için **Özel** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-153">Optionally, select the **Private** field to indicate that the address is private.</span></span> <span data-ttu-id="27b41-154">Yalnızca özel adres bilgilerini görüntülemek için açıkça izni olan kullanıcılar bu adresi görüntüleyebilir.</span><span class="sxs-lookup"><span data-stu-id="27b41-154">Only users with explicit permission to view private address information can view this address.</span></span>

12. <span data-ttu-id="27b41-155">**Tamam**'ı seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-155">Select **OK**.</span></span>
 
## <a name="create-a-future-change-for-an-address"></a><span data-ttu-id="27b41-156">Adres için gelecekte bir değişiklik oluşturma</span><span class="sxs-lookup"><span data-stu-id="27b41-156">Create a future change for an address</span></span>

<span data-ttu-id="27b41-157">Bazı durumlarda, gelecekte değiştirilecek bir adresi güncelleştirmek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27b41-157">In some cases, you might want to update an address to change in the future.</span></span> <span data-ttu-id="27b41-158">Örneğin, bir çalışan takip eden ayın 15'inde taşınacaksa bu kullanışlı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="27b41-158">For example, this would be useful if an employee is moving on the 15th of the following month.</span></span>

1. <span data-ttu-id="27b41-159">Herhangi bir adres kılavuzundan **Diğer seçenekler > Gelişmiş**'i seçerek **Adresleri yönet** sayfasını açın.</span><span class="sxs-lookup"><span data-stu-id="27b41-159">Open the **Manage addresses** page by selecting **More options > Advanced** from any address grid.</span></span>

2. <span data-ttu-id="27b41-160">Yeni bir adres oluşturmak için **Yeni**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-160">Select **New** to create a new address.</span></span>

3. <span data-ttu-id="27b41-161">Adres ayrıntılarını girin.</span><span class="sxs-lookup"><span data-stu-id="27b41-161">Enter the details of the address.</span></span>

4. <span data-ttu-id="27b41-162">**Genel** hızlı sekmesini seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-162">Select the **General** FastTab.</span></span>

5. <span data-ttu-id="27b41-163">**Geçerlilik tarihi** alanında, yeni adresin geçerli olacağı tarihi seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-163">In the **Effective date** field, select the date the new address will be effective.</span></span>

6. <span data-ttu-id="27b41-164">**Sona erme tarihi** alanında, isteğe bağlı olarak, adresin ne zaman geçerli olmayacağını seçin.</span><span class="sxs-lookup"><span data-stu-id="27b41-164">In the **Expiration date** field, optionally select when the address will no longer be effective.</span></span>

7. <span data-ttu-id="27b41-165">Sayfaları kapatın.</span><span class="sxs-lookup"><span data-stu-id="27b41-165">Close the pages.</span></span>

## <a name="view-and-monitor-address-changes"></a><span data-ttu-id="27b41-166">Adres değişikliklerini görüntüleme ve izleme</span><span class="sxs-lookup"><span data-stu-id="27b41-166">View and monitor address changes</span></span>

<span data-ttu-id="27b41-167">İK personeli **Personel yönetimi** çalışma alanından adres değişikliklerini görüntüleyebilir ve izleyebilir.</span><span class="sxs-lookup"><span data-stu-id="27b41-167">HR personnel can view and monitor address changes from the **Personnel management** workspace.</span></span> <span data-ttu-id="27b41-168">Adres değişikliklerini görüntülemek için **Giriş** sayfasından **Personel yönetimi** kutucuğunu açın.</span><span class="sxs-lookup"><span data-stu-id="27b41-168">To view the address changes, open the **Personnel management** tile from the **Home** page.</span></span> <span data-ttu-id="27b41-169">Adres değişiklikleri, sağ üst köşedeki bir kutucukta görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="27b41-169">The address changes display on a tile in the upper-right corner.</span></span> <span data-ttu-id="27b41-170">**Adres değişiklikleri** üzerindeki sayı **İnsan kaynakları parametreleri** sayfasında belirtilen gün sayısı içinde gerçekleşen adres değişikliklerinin sayısını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27b41-170">The number above **Address changes** shows how many address changes occurred in the number of days specified in the **Human resources parameters** page.</span></span> 

<span data-ttu-id="27b41-171">**Adres değişiklikleri** kutucuğunu seçtiğinizde, yeni bir sayfa, tüm adres değişikliklerinin ayrıntılarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="27b41-171">When you select the **Address changes** tile, a new page displays the details of any address changes.</span></span> <span data-ttu-id="27b41-172">Gelecek tarihteki adres değişikliklerini görüntülemek için, isteğe bağlı olarak, sağ üst köşedeki **Gelecek adres değişikliklerini dahil et**'i seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27b41-172">You can optionally select **Include future address changes** in the upper-right corner to display address changes with a future date.</span></span>

> [!NOTE]
> <span data-ttu-id="27b41-173">Bu adres değişiklikleriyle ilgili bir uyarı veya e-posta almak istiyorsanız, Eylem bölmesindeki **Seçenekler** sekmesinde yeni bir uyarı kuralı oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27b41-173">If you want to receive an alert or email about these address changes, you can create a new alert rule on the **Options** tab in the Action Pane.</span></span> <span data-ttu-id="27b41-174">Uyarı kuralları ile ilgili daha fazla bilgi için bkz. [Uyarı kuralları oluşturma](../fin-ops-core/fin-ops/get-started/create-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="27b41-174">For more information about alert rules, see [Create alert rules](../fin-ops-core/fin-ops/get-started/create-alerts.md).</span></span><br><br>

> <span data-ttu-id="27b41-175">Adres değişiklikleri için bir iş akışı yapılandırmak istiyorsanız, uyarı kuralınızda **Harici olarak gönder** seçeneğini seçebilir ve iş olayını tetikleyip bir iş akışı yapılandırmak için Power Automate kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27b41-175">If you want to configure a workflow for the address changes, you can select the **Send externally** option on your alert rule, and then use Power Automate to trigger the business event and configure a workflow.</span></span> <span data-ttu-id="27b41-176">Daha fazla bilgi için bkz. [İş olayları olarak uyarılar](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).</span><span class="sxs-lookup"><span data-stu-id="27b41-176">For more information, see [Alerts as business events](../fin-ops-core/fin-ops/get-started/create-alerts.md#alerts-as-business-events).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]