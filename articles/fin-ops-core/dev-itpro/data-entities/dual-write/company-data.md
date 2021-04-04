---
title: Dataverse'da şirket kavramı
description: Bu konu, Finance and Operations ve Dataverse arasındaki şirket verileri tümleştirmesini açıklar.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 189d1b8a68f8457d32d656fefeb6cc2a332a3b22
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560261"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="7cffc-103">Dataverse'da şirket kavramı</span><span class="sxs-lookup"><span data-stu-id="7cffc-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="7cffc-104">Finance and Operations'da *şirket* kavramı hem yasal bir yapı hem de bir işletme yapısıdır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="7cffc-105">Ayrıca veriler için bir güvenlik ve görünürlük sınırıdır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="7cffc-106">Kullanıcılar her zaman tek bir şirket bağlamında çalışır ve verilerin çoğu şirket tarafından çıkarılır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="7cffc-107">Dataverse'da eşdeğer bir kavram yoktur.</span><span class="sxs-lookup"><span data-stu-id="7cffc-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="7cffc-108">En yakın kavram, birincil olarak kullanıcı verileri için bir güvenlik ve görünürlük sınırı olan *iş birimidir*.</span><span class="sxs-lookup"><span data-stu-id="7cffc-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="7cffc-109">Bu kavram, şirket kavramıyla aynı yasal veya iş etkilerine sahip değildir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="7cffc-110">İş birimi ve şirket eşdeğer kavramlar olmadığından, Dataverse tümleştirmesi amacıyla aralarında bire bir (1:1) eşlemesini zorlamak mümkün değildir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="7cffc-111">Ancak, kullanıcılar varsayılan olarak, uygulamada ve Dataverse'te aynı satırları görebilmelidir; bu nedenle Microsoft, Dataverse'te cdm\_Company adlı yeni bir tabloyu kullanıma sundu.</span><span class="sxs-lookup"><span data-stu-id="7cffc-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new table in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="7cffc-112">Bu tablo uygulamadaki Şirket tablosuna eşdeğerdir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-112">This table is equivalent to the Company table in the application.</span></span> <span data-ttu-id="7cffc-113">Satır görünürlüğünün uygulama ve Dataverse'te başlangıçtan itibaren eşdeğer olmasını sağlamaya yardımcı olmak için Dataverse'te veriler için aşağıdaki kurulumu öneriyoruz:</span><span class="sxs-lookup"><span data-stu-id="7cffc-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="7cffc-114">Çift yazma için etkinleştirilmiş her bir Finance and Operations Şirket satırı için, ilişkili bir cdm\_Company satırı oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7cffc-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="7cffc-115">cdm\_Company satırı oluşturulduğunda ve çift yazma için etkinleştirildiğinde, aynı ada sahip bir varsayılan iş birimi oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7cffc-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="7cffc-116">Bu iş birimi için otomatik olarak varsayılan bir ekip oluşturulsa da, iş birimi kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="7cffc-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="7cffc-117">Aynı ada sahip ayrı bir sahip olan takım oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7cffc-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="7cffc-118">Ayrıca iş birimi ile de ilişkilidir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="7cffc-119">Varsayılan olarak, oluşturulan ve Dataverse'e çift yazılan herhangi bir satırın sahibi, ilişkili iş birimine bağlı "DW Sahibi" ekibine ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="7cffc-120">Aşağıdaki şekilde, Dataverse'daki bu veri ayarının bir örneğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![Dataverse'da veri ayarı](media/dual-write-company-1.png)

<span data-ttu-id="7cffc-122">Bu yapılandırma nedeniyle, USMF şirketiyle ilgili herhangi bir satır, Dataverse'teki USMF iş birimine bağlı olan bir takıma ait olacaktır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="7cffc-123">Bu nedenle, iş birimi düzeyinde görünürlük için ayarlanan bir güvenlik rolü aracılığıyla bu iş birimine erişimi olan herhangi bir kullanıcı artık bu satırları görebilir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="7cffc-124">Aşağıdaki örnekte, bu satırlara doğru erişimi sağlamak amacıyla takımların nasıl kullanılabileceği gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="7cffc-125">"Satış Yöneticisi" rolü "USMF Satış" takımı üyelerine atanır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="7cffc-126">"Satış Yöneticisi" rolüne sahip kullanıcılar, üye oldukları aynı işi birimine üye olan hesap satırlarına erişebilir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="7cffc-127">"USMF Satış" ekibi, daha önce bahsedilen USMF iş birimine bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="7cffc-128">Bu nedenle, "USMF Satış" ekibinin üyeleri Finance and Operations'taki USMF Şirket tablosundan gelen "USMF DW" kullanıcısı tarafından sahip olunan herhangi bir hesabı görebilir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company table in Finance and Operations.</span></span>

![Ekipler nasıl kullanılabilir](media/dual-write-company-2.png)

<span data-ttu-id="7cffc-130">Önceki örnekte gösterildiği gibi iş birimi, şirket ve ekip arasındaki bu 1:1 eşleme yalnızca bir başlangıç noktasıdır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="7cffc-131">Bu örnekte, yeni bir "Avrupa" iş birimi hem DEMF hem de ESMF için üst öğe olarak Dataverse'ta el ile ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="7cffc-132">Bu yeni kök iş birimi çift yazma ile ilgili değildir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="7cffc-133">Ancak, "EUR Satış" ekibinin üyelerine, ilgili güvenlik rolündeki **Üst/Alt İş Birimi** veri görünürlüğünü ayarlayarak hem DEMF hem de ESMF'deki hesap verilerine erişim vermek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="7cffc-134">Tartışılması gereken son bir konu da çift yazmanın satırları hangi sahip takıma atayacağını belirleme yöntemidir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="7cffc-135">Bu davranış, cdm\_Company satırındaki **Varsayılan sahibi olan takım** sütunu tarafından denetlenir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-135">This behavior is controlled by the **Default owning team** column on the cdm\_Company row.</span></span> <span data-ttu-id="7cffc-136">Bir cdm\_Company satırı çift yazma için etkinleştirildiğinde, bir eklenti otomatik olarak ilişkili iş birimi ve sahibi olan takımı (zaten yoksa) oluşturur ve **Varsayılan sahibi olan takım** sütununu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7cffc-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** column.</span></span> <span data-ttu-id="7cffc-137">Yönetici bu sütunu farklı bir değere değiştirebilir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-137">The admin can change this column to a different value.</span></span> <span data-ttu-id="7cffc-138">Ancak, tablo çift yazma için etkinleştirildiği sürece yönetici sütunu temizleyemez.</span><span class="sxs-lookup"><span data-stu-id="7cffc-138">However, the admin can't clear the column as long as the table is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="7cffc-139">![Varsayılan sahibi olan takım sütunu](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="7cffc-139">![Default owning team column](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="7cffc-140">Şirket bölümleme ve yeniden örnekleme</span><span class="sxs-lookup"><span data-stu-id="7cffc-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="7cffc-141">Dataverse tümleştirmesi verileri bölümlemek için şirket tanımlayıcısını kullanarak şirket eşliği getirir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="7cffc-142">Aşağıdaki çizimde gösterildiği gibi, tüm şirkete özgü tablolar, cdm\_Company tablosutka çok-bir (N:1) ilişkisine sahip olmaları için genişletilir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company table.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="7cffc-143">![Şirkete özgü tablo ile cdm_Company tablosu arasındaki N:1 ilişkisi](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="7cffc-143">![N:1 relationship between a company-specific table and the cdm_Company table](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="7cffc-144">Satırlar için, bir şirket eklendikten ve kaydedildikten sonra, değer salt okunur olur.</span><span class="sxs-lookup"><span data-stu-id="7cffc-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="7cffc-145">Bu nedenle, kullanıcılar doğru şirketi seçtiğinden emin olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="7cffc-146">Yalnızca şirket verilerine sahip satırlar uygulama ile Dataverse arasında çift yazma için uygundur.</span><span class="sxs-lookup"><span data-stu-id="7cffc-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="7cffc-147">Var olan Dataverse verileri için, yönetici tarafından yürütülen bir yeniden örnekleme deneyimi yakında kullanıma sunulacaktır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="7cffc-148">Müşteri etkileşimi uygulamalarında şirket adını otomatik olarak doldurma</span><span class="sxs-lookup"><span data-stu-id="7cffc-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="7cffc-149">Müşteri etkileşimi uygulamalarında şirket adını otomatik olarak doldurmanın birkaç yolu vardır.</span><span class="sxs-lookup"><span data-stu-id="7cffc-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="7cffc-150">Sistem yöneticisiyseniz **Gelişmiş Ayarlar > Sistem > Güvenlik > Kullanıcılar** seçeneğine giderek varsayılan şirketi ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cffc-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="7cffc-151">**Kullanıcı** formunu açın ve **Kuruluş Bilgileri** bölümünde **Formlarda varsayılan olarak kullanılacak şirket** değerini ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7cffc-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Kuruluş bilgileri bölümünde varsayılan şirketi ayarlayın.":::

+ <span data-ttu-id="7cffc-153">**İş Birimi** düzeyi için **SystemUser** tablosuna **Yazma** erişiminiz varsa **Şirket** açılır menüsünden bir şirket seçerek tüm formlardaki varsayılan şirketi değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cffc-153">If you have **Write** access to the **SystemUser** table for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Yeni bir hesaptaki şirket adını değiştirme.":::

+ <span data-ttu-id="7cffc-155">Birden fazla şirketteki verilere **Yazma** erişiminiz varsa farklı bir şirkete ait satırı seçerek varsayılan şirketi değiştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cffc-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Satır seçmek, varsayılan şirketi değiştirir.":::

+ <span data-ttu-id="7cffc-157">Sistem yapılandırıcısı veya yöneticisiyseniz ve özel bir formda şirket verilerini otomatik olarak doldurmak istiyorsanız [form olaylarını](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cffc-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="7cffc-158">**msdyn_/DefaultCompany.js** öğesine JavaScript başvurusu ekleyip aşağıdaki olayları kullanın.</span><span class="sxs-lookup"><span data-stu-id="7cffc-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="7cffc-159">İstediğiniz kullanıma hazır formu (ör. **Hesap** formu) kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7cffc-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="7cffc-160">Form için **OnLoad** olayı: **defaultCompany** sütununu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7cffc-160">**OnLoad** event for the form: Set the **defaultCompany** column.</span></span>
    + <span data-ttu-id="7cffc-161">**Şirket** sütunu için **OnChange** olayı: **updateDefaultCompany** sütununu ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="7cffc-161">**OnChange** event for the **Company** column: Set the **updateDefaultCompany** column.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="7cffc-162">Şirket bağlamına göre filtre uygulama</span><span class="sxs-lookup"><span data-stu-id="7cffc-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="7cffc-163">Özel formlarınızda veya standart formlara eklenmiş özel arama sütunlarınızda şirket bağlamına göre filtre uygulamak için formu açın ve **İlgili Kayıtlara Filtre Uygulama** bölümünü kullanarak şirket filtresi uygulayın.</span><span class="sxs-lookup"><span data-stu-id="7cffc-163">To apply filtering based on the company context on your custom forms or on custom lookup columns added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="7cffc-164">Belirli bir satırdaki temel şirkete dayalı olarak filtre gerektiren her arama sütunu için bunu ayarlamalısınız.</span><span class="sxs-lookup"><span data-stu-id="7cffc-164">You must set this for each lookup column that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="7cffc-165">Aşağıdaki resimde bu ayar **Hesap** için gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="7cffc-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="Şirket bağlamını uygulama":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]