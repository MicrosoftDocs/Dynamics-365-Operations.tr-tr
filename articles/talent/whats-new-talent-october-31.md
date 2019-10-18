---
title: Dynamics 365 Talent - Core HR'daki yenilikler veya değişiklikler (31 Ekim 2018)
description: Bu konuda, Microsoft Dynamics 365 Talent - Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d2ad9be740d917a760815718a1473d7bcba97968
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025944"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-31-2018"></a><span data-ttu-id="e8d61-103">Dynamics 365 Talent: Core HR'daki yenilikler veya değişiklikler (31 Ekim 2018)</span><span class="sxs-lookup"><span data-stu-id="e8d61-103">What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e8d61-104">**Derleme 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="e8d61-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="e8d61-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="e8d61-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance"></a><span data-ttu-id="e8d61-106">Talent'tan Finance'e bağlantılar oluşturma</span><span class="sxs-lookup"><span data-stu-id="e8d61-106">Create links from Talent to Finance</span></span>
<span data-ttu-id="e8d61-107">Bu yeni gezinti işlevi Talent ile Finance arasında bağlantı kurmanızı sağlayarak Finance sayfalarına doğrudan ulaşım sunar.</span><span class="sxs-lookup"><span data-stu-id="e8d61-107">This new navigation functionality allows you to link from Talent to Finance, giving you direct navigation into Finance pages.</span></span> <span data-ttu-id="e8d61-108">Bağlantılar yapılandırıldığında bağlantının adını ve grubunu, Talent'ta bağlantının yerini ve Finance'te açılacak hedef sayfayı belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e8d61-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="e8d61-109">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="e8d61-109">Coming soon</span></span>
<span data-ttu-id="e8d61-110">Bağlam alanı daha sonra Finance'te karşılık gelen kayıtlara doğrudan gezintiye izin verecek şekilde eklenir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance.</span></span> <span data-ttu-id="e8d61-111">Örneğin, Finance'te belirli bir personele veya konuma doğrudan götürecek bağlam sağlamak için **Alana bağlantı** kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e8d61-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="e8d61-112">Hedef sistemleri yapılandır</span><span class="sxs-lookup"><span data-stu-id="e8d61-112">Configure target systems</span></span>

<span data-ttu-id="e8d61-113">Talent'ta sistem yöneticileri, Sistem Yönetimi çalışma alanında ortaya konacak bağlantılar tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="e8d61-114">Konfigürasyonun bir kısmı, bağlantının "hedefi" olarak gitmek istediğiniz Finance ortamlarıdır.</span><span class="sxs-lookup"><span data-stu-id="e8d61-114">Part of the configuration is the Finance environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="e8d61-115">Bunu hedef sisteme ad vererek ve Finance ortamının URL'sini girerek yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="e8d61-115">You do this by giving the target system a name and providing the URL of the Finance environment.</span></span> <span data-ttu-id="e8d61-116">Gireceğiniz Finance URL'sine bir örnek: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="e8d61-116">Here is an example of a Finance URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="e8d61-117">Hedef sistemlerinizi yapılandırdıktan sonra bağlantıları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e8d61-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="e8d61-118">Bağlantıları yapılandır</span><span class="sxs-lookup"><span data-stu-id="e8d61-118">Configure links</span></span>

<span data-ttu-id="e8d61-119">Oluşturulan her bağlantının aşağıdaki bilgileri tanımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="e8d61-120">Bağlantı - Bağlantı adı, yalnızca kimlik saptama için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="e8d61-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="e8d61-121">Bu bağlantıyı etkinleştir - Bağlantıyı Talent kullanıcılara görüntülemek isterseniz **Evet** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e8d61-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="e8d61-122">Görünen ad - Finance bağlantısı olarak görünecek adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="e8d61-122">Display name - Define the name that will appear as a link to Finance.</span></span> <span data-ttu-id="e8d61-123">Bu veri şu anda çevrilmemiş.</span><span class="sxs-lookup"><span data-stu-id="e8d61-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="e8d61-124">Formda yüzey bağlantı - Bağlantıyı görüntülemek istediğiniz sayfayı seçin.</span><span class="sxs-lookup"><span data-stu-id="e8d61-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="e8d61-125">Grup - Gruplar gerekli değildir, ancak bağlantılarınızı grupları kullanarak düzenlemek istiyorsanız, varolan bir grup seçin veya **Grup** alanını kullanarak yeni bir grup oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e8d61-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="e8d61-126">Hedef sistem - **Hedef sistemi yapılandır** seçeneği kullanılarak oluşturulmuş olan hedef sistemi seçin.</span><span class="sxs-lookup"><span data-stu-id="e8d61-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="e8d61-127">Bağlantıyı kullanarak ziyaret edildiğinde kullanılacak Finance ortamı olacak.</span><span class="sxs-lookup"><span data-stu-id="e8d61-127">This will be the Finance environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="e8d61-128">Kullanıcının geçerli şirketini kullanın - Finance'e giderken kullanıcının geçerli şirket içeriğini kullanmak isterseniz **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="e8d61-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance.</span></span> <span data-ttu-id="e8d61-129">**Hayır** seçilirse kullanılması gereken şirket seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e8d61-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="e8d61-130">Hedef menü öğesi - Ziyaret ederken kullanılması gereken bağlantı için Finance'ten menü öğesini girin.</span><span class="sxs-lookup"><span data-stu-id="e8d61-130">Target menu item - Enter the menu item from Finance that the link should use when navigating.</span></span> <span data-ttu-id="e8d61-131">Doğrudan gidilecek menü öğeleri bulunur.</span><span class="sxs-lookup"><span data-stu-id="e8d61-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="e8d61-132">Gereken menü öğesini bulmak için Finance'i açın ve gezintinin hedefi olan sayfayı açın.</span><span class="sxs-lookup"><span data-stu-id="e8d61-132">To find the menu item required, open Finance and open the page that is the target of the navigation.</span></span> <span data-ttu-id="e8d61-133">Menü öğesini URL'den kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="e8d61-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="e8d61-134">Örneğin, bağlantının sizi Finance and Operations'ta personele götürmesini isterseniz URL'de "&mi" sonrasında görünen değeri girin.</span><span class="sxs-lookup"><span data-stu-id="e8d61-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="e8d61-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="e8d61-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="e8d61-136">Bu örnekte personel listesi sayfasına gitmek için menü öğesi: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="e8d61-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="e8d61-137">Veri kaynağına bağlantı - Bağlantı referansı olan veri kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="e8d61-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="e8d61-138">En sık kullanılan kaynaklar, **Çalışan** ve **Konum** gibi, kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="e8d61-139">Alan bağlantısı - (Çok yakında) Bu alan seçimi, Talent'ta tek bir kayıttan Finance'e tek bir kayıt için doğrudan gezintiye izin verir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="e8d61-140">Bağlantılara erişim</span><span class="sxs-lookup"><span data-stu-id="e8d61-140">Access to links</span></span>

<span data-ttu-id="e8d61-141">Sistem yöneticileri, **Bu bağlantıyı etkinleştir** seçeneği **Hayır** olarak ayarlanmış olsa bile yeni oluşturulan bağlantıları tanımlanan sayfalarda gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="e8d61-142">Bu, bağlantıları diğer çalışanlara sunmadan önce test etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="e8d61-143">Tüm diğer roller yalnızca **Bu bağlantıyı etkinleştir** seçeneği **Evet** olarak ayarlandıktan sonra yapılandırılmış bağlantıları görür.</span><span class="sxs-lookup"><span data-stu-id="e8d61-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="e8d61-144">Bağlantıların yer aldığı sayfalara erişimi olan personeller, bağlantılara erişime sahiptir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="e8d61-145">Kullanıcılar, Finance and Operations'taki sayfalara erişmek için Finance'te tanımlanmış güvenlik haklarına da sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-145">Users can also have security rights within Finance defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="e8d61-146">Yoksa, bağlantıyı kullanırken güvenlik iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="e8d61-147">Diğer değişimler/düzeltmeler</span><span class="sxs-lookup"><span data-stu-id="e8d61-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="e8d61-148">İleride bir başlangıç tarihine sahip olan pozisyonlar yeni bir personele atanamaz</span><span class="sxs-lookup"><span data-stu-id="e8d61-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="e8d61-149">Gelecek tarihli pozisyonlara personel atamasına izin vermek için değişiklikler yapıldı.</span><span class="sxs-lookup"><span data-stu-id="e8d61-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="e8d61-150">Başlangıç tarihi gelecekte olan pozisyonlar seçilebilir ve personel ataması, kaydetmeden ya da iş akışının (iş akışı etkinse) tamamlanmasından sonra yapılır.</span><span class="sxs-lookup"><span data-stu-id="e8d61-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="e8d61-151">Yeni çalışan varolan konuma atanamaz</span><span class="sxs-lookup"><span data-stu-id="e8d61-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="e8d61-152">Yeni personel ataması artık varolan konumlara atanabilsin diye değişiklikler yapıldı.</span><span class="sxs-lookup"><span data-stu-id="e8d61-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="e8d61-153">Kıdem tarihi/Ofis konumu, çalışma başlangıç tarihi geçmişte olduğunda ve kayıt kaydedildiğinde kaybolur</span><span class="sxs-lookup"><span data-stu-id="e8d61-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="e8d61-154">Eski personeller için değişiklikleri kaydederken **Kıdem tarihi** ve **Ofis konumu** görünürlüğünü doğrulamak için değişiklikler yapıldı.</span><span class="sxs-lookup"><span data-stu-id="e8d61-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="e8d61-155">Çalışan sayfasına gelecek tarihli istihdamlar için veri girilemiyor</span><span class="sxs-lookup"><span data-stu-id="e8d61-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="e8d61-156">Gelecek tarihli istihdamlar için çalışma verileri ana çalışan sayfasında devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="e8d61-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="e8d61-157">İstihdam verileri, **Tarih Yöneticisi** sayfalarıyla girilebilir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="e8d61-158">Gelecekteki sürümlerde, iş akışı süreci sırasında doğrudan istihdam verilerini girebilmek için ilave değişiklikler yapılacak.</span><span class="sxs-lookup"><span data-stu-id="e8d61-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="e8d61-159">HcmPersonalContactPersonEntity'ye ValidFrom ve ValidTo ekleyin</span><span class="sxs-lookup"><span data-stu-id="e8d61-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="e8d61-160">Veri Yönetimi Çerçevesi (DMF) varlığı HcmPersonalContactPersonEntity, belirli kazanç entegrasyon senaryolarını etkinleştirmek için "geçerli başlangıç" ve "geçerli bitiş" tarihlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="e8d61-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="e8d61-161">Bilinen sorun</span><span class="sxs-lookup"><span data-stu-id="e8d61-161">Known issue</span></span>
- <span data-ttu-id="e8d61-162">**Sorun**: Bir çalışan için yeni bir eki eklerken **Yeni** ve **Düzenle** düğmeleri gridir.</span><span class="sxs-lookup"><span data-stu-id="e8d61-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="e8d61-163">**Çözüm:** Ek sayfasını açmadan önce **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="e8d61-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="e8d61-164">**Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="e8d61-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="e8d61-165">(Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)</span><span class="sxs-lookup"><span data-stu-id="e8d61-165">(This issue will be fixed in the next platform update.)</span></span>
