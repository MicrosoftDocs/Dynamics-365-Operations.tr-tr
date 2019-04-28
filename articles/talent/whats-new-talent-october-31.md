---
title: Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (31 Ekim 2018)
description: Bu konuda, Microsoft Dynamics 365 for Talent Core HR'daki yeni veya değişen özellikler açıklanmaktadır.
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
ms.openlocfilehash: d6942f8e4dc86f18a081b347df0567b1358a87ab
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/19/2019
ms.locfileid: "858802"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a><span data-ttu-id="57d9d-103">Dynamics 365 for Talent Core HR'deki yenilikler veya değişiklikler (31 Ekim 2018)</span><span class="sxs-lookup"><span data-stu-id="57d9d-103">What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57d9d-104">**Derleme 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="57d9d-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="57d9d-105">Bu konuda, Core HR'deki yeni veya değişen özellikler açıklanmaktadır.</span><span class="sxs-lookup"><span data-stu-id="57d9d-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance-and-operations"></a><span data-ttu-id="57d9d-106">Talent ile Finance and Operations arasında bağlantı oluştur</span><span class="sxs-lookup"><span data-stu-id="57d9d-106">Create links from Talent to Finance and Operations</span></span>
<span data-ttu-id="57d9d-107">Bu yeni gezinti işlevi Talent ile Finance and Operations arasında bağlantı kurmanızı sağlayarak Finance and Operations sayfalarına doğrudan ulaşım sunar.</span><span class="sxs-lookup"><span data-stu-id="57d9d-107">This new navigation functionality allows you to link from Talent to Finance and Operations, giving you direct navigation into Finance and Operations pages.</span></span> <span data-ttu-id="57d9d-108">Bağlantılar yapılandırıldığında bağlantının adını ve grubunu, Talent'ta bağlantının yerini ve Finance and Operations'ta açılacak hedef sayfayı belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57d9d-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance and Operations.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="57d9d-109">Çok yakında</span><span class="sxs-lookup"><span data-stu-id="57d9d-109">Coming soon</span></span>
<span data-ttu-id="57d9d-110">Bağlam alanı daha sonra Finance and Operations'ta karşılık gelen kayıtlara doğrudan gezintiye izin verecek şekilde eklenir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance and Operations.</span></span> <span data-ttu-id="57d9d-111">Örneğin, belirli bir personel veya Finance and Operations'ta konuma doğrudan gitmek için bağlam sağlamak için **Alana bağlantı** kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57d9d-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance and Operations.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="57d9d-112">Hedef sistemleri yapılandır</span><span class="sxs-lookup"><span data-stu-id="57d9d-112">Configure target systems</span></span>

<span data-ttu-id="57d9d-113">Talent'ta sistem yöneticileri, Sistem Yönetimi çalışma alanında ortaya konacak bağlantılar tanımlayabilir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="57d9d-114">Konfigürasyonun bir kısmı, bağlantının "hedefi" olarak gitmek istediğiniz Finance and Operations ortamlarıdır.</span><span class="sxs-lookup"><span data-stu-id="57d9d-114">Part of the configuration is the Finance and Operations environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="57d9d-115">Hedef sisteme ad vererek ve Finance and Operations ortamı URL'sini sağlayarak bunu yaparsınız.</span><span class="sxs-lookup"><span data-stu-id="57d9d-115">You do this by giving the target system a name and providing the URL of the Finance and Operations environment.</span></span> <span data-ttu-id="57d9d-116">İşte belirttiğiniz bir Finance and Operations URL'si örneği: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="57d9d-116">Here is an example of a Finance and Operations URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="57d9d-117">Hedef sistemlerinizi yapılandırdıktan sonra bağlantıları tanımlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57d9d-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="57d9d-118">Bağlantıları yapılandır</span><span class="sxs-lookup"><span data-stu-id="57d9d-118">Configure links</span></span>

<span data-ttu-id="57d9d-119">Oluşturulan her bağlantının aşağıdaki bilgileri tanımlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="57d9d-120">Bağlantı - Bağlantı adı, yalnızca kimlik saptama için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="57d9d-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="57d9d-121">Bu bağlantıyı etkinleştir - Bağlantıyı Talent kullanıcılara görüntülemek isterseniz **Evet** ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="57d9d-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="57d9d-122">Görünen ad - Finance and Operations bağlantısı olarak görünecek adı belirtin.</span><span class="sxs-lookup"><span data-stu-id="57d9d-122">Display name - Define the name that will appear as a link to Finance and Operations.</span></span> <span data-ttu-id="57d9d-123">Bu veri şu anda çevrilmemiş.</span><span class="sxs-lookup"><span data-stu-id="57d9d-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="57d9d-124">Formda yüzey bağlantı - Bağlantıyı görüntülemek istediğiniz sayfayı seçin.</span><span class="sxs-lookup"><span data-stu-id="57d9d-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="57d9d-125">Grup - Gruplar gerekli değildir, ancak bağlantılarınızı grupları kullanarak düzenlemek istiyorsanız, varolan bir grup seçin veya **Grup** alanını kullanarak yeni bir grup oluşturun.</span><span class="sxs-lookup"><span data-stu-id="57d9d-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="57d9d-126">Hedef sistem - **Hedef sistemi yapılandır** seçeneği kullanılarak oluşturulmuş olan hedef sistemi seçin.</span><span class="sxs-lookup"><span data-stu-id="57d9d-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="57d9d-127">Bağlantıyı kullanarak ziyaret edildiğinde kullanılacak Finance and Operations ortamı olacak.</span><span class="sxs-lookup"><span data-stu-id="57d9d-127">This will be the Finance and Operations environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="57d9d-128">Kullanıcının geçerli şirketini kullanın - Finance and Operations'a giderken kullanıcının geçerli şirket içeriğini kullanmak isterseniz **Evet**'i seçin.</span><span class="sxs-lookup"><span data-stu-id="57d9d-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance and Operations.</span></span> <span data-ttu-id="57d9d-129">**Hayır** seçilirse kullanılması gereken şirket seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="57d9d-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="57d9d-130">Hedef menü öğesi - Ziyaret ederken kullanılması gereken bağlantı için Finance and Operations'tan menü öğesini girin.</span><span class="sxs-lookup"><span data-stu-id="57d9d-130">Target menu item - Enter the menu item from Finance and Operation that the link should use when navigating.</span></span> <span data-ttu-id="57d9d-131">Doğrudan gidilecek menü öğeleri bulunur.</span><span class="sxs-lookup"><span data-stu-id="57d9d-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="57d9d-132">Gereken menü öğesini bulmak için Finance and Operations'ı açın ve gezintinin hedefi olan sayfayı açın.</span><span class="sxs-lookup"><span data-stu-id="57d9d-132">To find the menu item required, open Finance and Operations and open the page that is the target of the navigation.</span></span> <span data-ttu-id="57d9d-133">Menü öğesini URL'den kopyalayın.</span><span class="sxs-lookup"><span data-stu-id="57d9d-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="57d9d-134">Örneğin, bağlantının sizi Finance and Operations'ta personele götürmesini isterseniz URL'de "&mi" sonrasında görünen değeri girin.</span><span class="sxs-lookup"><span data-stu-id="57d9d-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="57d9d-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="57d9d-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="57d9d-136">Bu örnekte personel listesi sayfasına gitmek için menü öğesi: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="57d9d-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="57d9d-137">Veri kaynağına bağlantı - Bağlantı referansı olan veri kaynağını seçin.</span><span class="sxs-lookup"><span data-stu-id="57d9d-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="57d9d-138">En sık kullanılan kaynaklar, **Çalışan** ve **Konum** gibi, kullanılabilirdir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="57d9d-139">Alan bağlantısı - (Çok yakında) Bu alan seçimi, Talent'ta tek bir kayıttan Finance and Operations'a tek bir kayıt için doğrudan gezintiye izin verir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance and Operations.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="57d9d-140">Bağlantılara erişim</span><span class="sxs-lookup"><span data-stu-id="57d9d-140">Access to links</span></span>

<span data-ttu-id="57d9d-141">Sistem yöneticileri, **Bu bağlantıyı etkinleştir** seçeneği **Hayır** olarak ayarlanmış olsa bile yeni oluşturulan bağlantıları tanımlanan sayfalarda gösterir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="57d9d-142">Bu, bağlantıları diğer çalışanlara sunmadan önce test etmek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="57d9d-143">Tüm diğer roller yalnızca **Bu bağlantıyı etkinleştir** seçeneği **Evet** olarak ayarlandıktan sonra yapılandırılmış bağlantıları görür.</span><span class="sxs-lookup"><span data-stu-id="57d9d-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="57d9d-144">Bağlantıların yer aldığı sayfalara erişimi olan personeller, bağlantılara erişime sahiptir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="57d9d-145">Kullanıcılar, Finance and Operations'taki sayfalara erişmek için Finance and Operations'ta tanımlanmış güvenlik haklarına sahip olabilir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-145">Users can also have security rights within Finance and Operations defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="57d9d-146">Yoksa, bağlantıyı kullanırken güvenlik iletişim kutusu görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="57d9d-147">Diğer değişimler/düzeltmeler</span><span class="sxs-lookup"><span data-stu-id="57d9d-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="57d9d-148">İleride bir başlangıç tarihine sahip olan pozisyonlar yeni bir personele atanamaz</span><span class="sxs-lookup"><span data-stu-id="57d9d-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="57d9d-149">Gelecek tarihli pozisyonlara personel atamasına izin vermek için değişiklikler yapıldı.</span><span class="sxs-lookup"><span data-stu-id="57d9d-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="57d9d-150">Başlangıç tarihi gelecekte olan pozisyonlar seçilebilir ve personel ataması, kaydetmeden ya da iş akışının (iş akışı etkinse) tamamlanmasından sonra yapılır.</span><span class="sxs-lookup"><span data-stu-id="57d9d-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="57d9d-151">Yeni çalışan varolan konuma atanamaz</span><span class="sxs-lookup"><span data-stu-id="57d9d-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="57d9d-152">Yeni personel ataması artık varolan konumlara atanabilsin diye değişiklikler yapıldı.</span><span class="sxs-lookup"><span data-stu-id="57d9d-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="57d9d-153">Kıdem tarihi/Ofis konumu, çalışma başlangıç tarihi geçmişte olduğunda ve kayıt kaydedildiğinde kaybolur</span><span class="sxs-lookup"><span data-stu-id="57d9d-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="57d9d-154">Eski personeller için değişiklikleri kaydederken **Kıdem tarihi** ve **Ofis konumu** görünürlüğünü doğrulamak için değişiklikler yapıldı.</span><span class="sxs-lookup"><span data-stu-id="57d9d-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="57d9d-155">Çalışan sayfasına gelecek tarihli istihdamlar için veri girilemiyor</span><span class="sxs-lookup"><span data-stu-id="57d9d-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="57d9d-156">Gelecek tarihli istihdamlar için çalışma verileri ana çalışan sayfasında devre dışı bırakıldı.</span><span class="sxs-lookup"><span data-stu-id="57d9d-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="57d9d-157">İstihdam verileri, **Tarih Yöneticisi** sayfalarıyla girilebilir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="57d9d-158">Gelecekteki sürümlerde, iş akışı süreci sırasında doğrudan istihdam verilerini girebilmek için ilave değişiklikler yapılacak.</span><span class="sxs-lookup"><span data-stu-id="57d9d-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="57d9d-159">HcmPersonalContactPersonEntity'ye ValidFrom ve ValidTo ekleyin</span><span class="sxs-lookup"><span data-stu-id="57d9d-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="57d9d-160">Veri Yönetimi Çerçevesi (DMF) varlığı HcmPersonalContactPersonEntity, belirli kazanç entegrasyon senaryolarını etkinleştirmek için "geçerli başlangıç" ve "geçerli bitiş" tarihlerini içerecek şekilde güncelleştirildi.</span><span class="sxs-lookup"><span data-stu-id="57d9d-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="57d9d-161">Bilinen sorun</span><span class="sxs-lookup"><span data-stu-id="57d9d-161">Known issue</span></span>
- <span data-ttu-id="57d9d-162">**Sorun**: Bir çalışan için yeni bir eki eklerken **Yeni** ve **Düzenle** düğmeleri gridir.</span><span class="sxs-lookup"><span data-stu-id="57d9d-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="57d9d-163">**Çözüm:** Ek sayfasını açmadan önce **Çalışan** sayfasındaki bilgi kutularının kapalı olduğundan emin olun.</span><span class="sxs-lookup"><span data-stu-id="57d9d-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="57d9d-164">**Çalışan** sayfası yüklendiğinde bilgi kutuları kapalıysa, eklentiler düğmeleri etkinleştirilmiş olacaktır.</span><span class="sxs-lookup"><span data-stu-id="57d9d-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="57d9d-165">(Bu sorun sonraki platform güncelleştirmesinde giderilecektir.)</span><span class="sxs-lookup"><span data-stu-id="57d9d-165">(This issue will be fixed in the next platform update.)</span></span>
