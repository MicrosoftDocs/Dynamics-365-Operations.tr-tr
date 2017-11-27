---
title: "Satıcı iş birliği kullanıcılarını yönetme"
description: "Bu konu, yeni satıcı iş birliği kullanıcıları hazırlama talebinde bulunma ve yeni satıcı iş birliği kişileri ekleme konularını ele alır."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6e83f46df30d13a8bffa5c2b0bd05f456b67e6ec
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="manage-vendor-collaboration-users"></a><span data-ttu-id="6e3e6-103">Satıcı iş birliği kullanıcılarını yönetme</span><span class="sxs-lookup"><span data-stu-id="6e3e6-103">Manage vendor collaboration users</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6e3e6-104">Bu konu, yeni satıcı iş birliği kullanıcıları hazırlama talebinde bulunma ve yeni satıcı iş birliği kişileri ekleme konularını ele alır.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-104">This topic describes how you can request the provisioning of new vendor collaboration users, and how to add new vendor collaboration contacts.</span></span> 

<span data-ttu-id="6e3e6-105">Microsoft Dynamics 365 for Finance and Operations'taki satıcı iş birliği arabirimi; satınalma siparişleri, faturalar ve harici satıcılara konsinye stok hakkında bilgi sağlar.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-105">The vendor collaboration interface in Microsoft Dynamics 365 for Finance and Operations exposes information about purchase orders, invoices, and consignment stock to external vendors.</span></span> <span data-ttu-id="6e3e6-106">**Satıcı yöneticisi (harici)** güvenlik rolü ya da benzer izinlerle harici satıcı olarak çalışıyorsanız yeni kullanıcıların sağlandığı yeni satıcı iş birliği kişileri ve talepleri oluşturabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-106">You can create new vendor collaboration contacts and request that new users are provisioned if you're working as an external vendor with the **Vendor admin (external)** security role, or similar permissions.</span></span> <span data-ttu-id="6e3e6-107">Tedarik profesyoneli olarak çalışıyorsanız da bu görevleri gerçekleştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-107">You can also perform these tasks if you're working as a procurement professional.</span></span> <span data-ttu-id="6e3e6-108">Bu konuda, bu rol Finance and Operations kurulumuna sahip bir şirkette çalışan tedarik profesyoneli anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-108">In this topic, this role refers to a procurement professional who is working within the company that owns the instance of Finance and Operations.</span></span> <span data-ttu-id="6e3e6-109">Harici satıcı iseniz satıcı işbirliğini kullanma hakkında daha fazla bilgi için bkz. [Müşterili satıcı](vendor-collaboration-work-customers-dynamics-365-operations.md).</span><span class="sxs-lookup"><span data-stu-id="6e3e6-109">For more information about how to use vendor collaboration if you're an external vendor, see [Vendor with customers](vendor-collaboration-work-customers-dynamics-365-operations.md).</span></span>  

<span data-ttu-id="6e3e6-110">Tedarik uzmanıysanız satıcı işbirliğini kullanma hakkında daha fazla bilgi için bkz. [Harici satıcılarla satıcı iş birliği](vendor-collaboration-work-external-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="6e3e6-110">For more information about how to use vendor collaboration if you're a procurement professional, see [Vendor collaboration to with external vendors](vendor-collaboration-work-external-vendors.md).</span></span>

## <a name="add-new-vendor-collaboration-contacts"></a><span data-ttu-id="6e3e6-111">Yeni satıcı iş birliği kişileri ekleme</span><span class="sxs-lookup"><span data-stu-id="6e3e6-111">Add new vendor collaboration contacts</span></span>
<span data-ttu-id="6e3e6-112">Bir kullanıcının satıcı iş birliğine erişimi olmasını istiyorsanız ilk olarak satıcı iş birliği ilgili kişisi olarak eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-112">If you want someone to have access to vendor collaboration they first have to be added as a vendor collaboration contact.</span></span> <span data-ttu-id="6e3e6-113">Şirketinizdeki satıcı iş birliğini kullanmayan çalışanlar için de kişi eklemek isteyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-113">You may also want to add contacts for employees in your company who won't use vendor collaboration.</span></span> <span data-ttu-id="6e3e6-114">Örneğin, diğer tedarik bilgisi türleri için iletişim noktası olabilirler.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-114">For example, they could be the point of contact for other kinds of procurement information.</span></span> <span data-ttu-id="6e3e6-115">Yeni kişiler, **Satıcı işbirliği** &gt; **Kişiler** menüsünden erişilebilen **Tüm kişiler** sayfasından eklenir.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-115">New contacts are added on the **All contacts** page, which is accessed from the **Vendor collaboration** &gt; **Contacts** menu.</span></span> <span data-ttu-id="6e3e6-116">Yeni bir ilgili kişi eklemek için:</span><span class="sxs-lookup"><span data-stu-id="6e3e6-116">To add a new contact:</span></span>

1.  <span data-ttu-id="6e3e6-117">**Yeni**'ye tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-117">Click **New.**</span></span>
2.  <span data-ttu-id="6e3e6-118">İlgili kişi ayrıntılarını girin.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-118">Enter the contact person details.</span></span>
3.  <span data-ttu-id="6e3e6-119">Şirketinizde temsil ettikleri tüzel kişiliği ve iş birliği yapacakları şirkette birlikte çalışacakları tüzel kişiliği seçin.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-119">Choose which legal entity they're representing in your company, and which legal entity they'll work with in the company that they'll collaborate with.</span></span> <span data-ttu-id="6e3e6-120">Bunun için, **Benim şirketimdeki tüzel kişilik**/**Müşterinin şirketindeki tüzel kişilik**  çiftini seçmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-120">You do this by selecting a **Legal entity in my company**/**Legal entity in customer company** pair.</span></span>
4.  <span data-ttu-id="6e3e6-121">**Oluştur**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-121">Click **Create.**</span></span>

<span data-ttu-id="6e3e6-122">Yalnızca kendi oluşturduğunuz ilgili kişileri silebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-122">If you want to delete a contact, it's only possible to delete the ones that you've created.</span></span>

## <a name="vendor-collaboration-user-requests"></a><span data-ttu-id="6e3e6-123">Satıcı işbirliği kullanıcısı istekleri</span><span class="sxs-lookup"><span data-stu-id="6e3e6-123">Vendor collaboration user requests</span></span>
<span data-ttu-id="6e3e6-124">Satıcı iş birliği kullanıcısı istekleri bir tedarik profesyoneli veya harici satıcı yöneticisi tarafından yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-124">Vendor collaboration user requests can be raised by a procurement professional, or by an external vendor administrator.</span></span>

-   <span data-ttu-id="6e3e6-125">Harici satıcı iseniz **Satıcı işbirliği** modülündeki **Tüm kişiler** sayfasından istekleri gönderirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-125">If you're an external vendor, you submit requests from the **All contacts** page within the **Vendor collaboration** module.</span></span>
-   <span data-ttu-id="6e3e6-126">Tedarik profesyoneli iseniz **İlgili kişileri görüntüle** sayfasından istekleri gönderirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-126">If you're a procurement professional, you submit requests from the **View contacts** page.</span></span> <span data-ttu-id="6e3e6-127">Bunu yapmak için satıcı kaydının Eylem bölmesindeki **Kurulum** bölümünde **Kişiler** &gt; **İlgili kişileri görüntüle**'yi seçin.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-127">To do this, on the vendor record, in the **Setup** section in the Action pane, select **Contacts** &gt; **View contacts**.</span></span>

<span data-ttu-id="6e3e6-128">Kullanıcıyı hazırlamak, devre dışı bırakmak veya güvenlik rollerini değiştirmek için de istek gönderebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-128">You can make a request to provision a user, to inactivate a user, or to modify security roles.</span></span> <span data-ttu-id="6e3e6-129">Harici satıcı yöneticisi iseniz kullanıcı istekleri göndermek istediğiniz satıcı hesaplarında ilgili kişi olarak kayıtlı olmanız gerekir ve bu satıcı hesapları için satıcı iş birliği arabirimine erişiminiz olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-129">If you're an external vendor administrator, you must be registered as a contact person for the vendor accounts that you want to make user requests for, and you must have access to the vendor collaboration interface for those vendor accounts.</span></span>  

<span data-ttu-id="6e3e6-130">İstek gönderildiğinde **Satıcı işbirliği** modülündeki **Satıcı işbirliği kullanıcısı istekleri** ve **Tedarik ve kaynak atama** modülündeki **Satıcı işbirliği kullanıcısı isteği** listelerine eklenir. (Tedarik ve kaynak atama modülüne harici kullanıcılar erişemez.)</span><span class="sxs-lookup"><span data-stu-id="6e3e6-130">When a request is submitted it is added to the **Vendor collaboration user requests** list in the **Vendor collaboration** module, and to the **Vendor collaboration user request** list in the **Procurement and sourcing** module (the Procurement and sourcing module is not accessible to external users).</span></span>

### <a name="provision-a-user"></a><span data-ttu-id="6e3e6-131">Kullanıcıyı hazırlama</span><span class="sxs-lookup"><span data-stu-id="6e3e6-131">Provision a user</span></span>

<span data-ttu-id="6e3e6-132">Yeni bir kullanıcı hazırlanması için istekte bulunmadan önce ilgili kişinin bir veya daha fazla satıcı hesabında kayıtlı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-132">Before you can request that a new user is provisioned, that person must be set up as a contact for one or more vendor accounts.</span></span> <span data-ttu-id="6e3e6-133">Yeni bir satıcı iş birliği kullanıcısı isteği oluşturmak için:</span><span class="sxs-lookup"><span data-stu-id="6e3e6-133">To create a request for a new vendor collaboration user:</span></span>

1.  <span data-ttu-id="6e3e6-134">**Tüm kişiler** sayfasındaki **Provizyon satıcı kullanıcısı**'na tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-134">On the **All contacts** page, click **Provision vendor user**.</span></span>
2.  <span data-ttu-id="6e3e6-135">Kullanıcının e-posta adresini girin.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-135">Enter an email address for the user.</span></span> <span data-ttu-id="6e3e6-136">Bu adres kullanıcı tarafından Finance and Operations'ta oturum açmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-136">This address will be used by the user to log onto Finance and Operations.</span></span> <span data-ttu-id="6e3e6-137">E-posta adresi, Microsoft Azure'da kiracı olarak kayıtlı bir etki alanına aitse hazırlama işleminin başarıyla tamamlanması için e-posta adresi mevcut bir Azure Active Directory (ADD) hesabı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-137">If the email address belongs to a domain registered as a tenant with Microsoft Azure, then the email address has to be an existing Azure Active Directory (ADD) account in order for the provisioning process to complete successfully.</span></span> <span data-ttu-id="6e3e6-138">E-posta adresi Microsoft Azure'da kayıtlı bir etki alanına ait değilse hazırlama işleminin bir parçası olarak EKLE hesabı oluşturulur ve yeni kullanıcı bir davet e-postası alır.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-138">If the email address does not belong to a domain registered with Microsoft Azure, an ADD account will be created as part of the provisioning process and the new user will receive an invitation mail.</span></span> <span data-ttu-id="6e3e6-139">Finance and Operations kullanıcı kaydı için  @hotmail.com, @gmail.com veya @comcast.net gibi etki alanları olan tüketici e-posta adresleri kullanılamaz.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-139">Consumer email addresses with domains such as @hotmail.com, @gmail.com, or @comcast.net cannot be used to register a Finance and Operations user.</span></span>
3.  <span data-ttu-id="6e3e6-140">Kullanıcının erişimi olması gereken tüm tüzel kişilikler için **Satıcı işbirliği erişimine izin verildi** seçeneğini **Evet** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-140">Set the **Vendor collaboration access allowed** option to **Yes** for all the legal entities that the user needs access to.</span></span>
4.  <span data-ttu-id="6e3e6-141">**Kullanıcı rolleri ata** bölümünde, yeni kullanıcının sahip olması gereken güvenlik rolleri için **Ata** onay kutusunu işaretleyin.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-141">In the **Assign user roles** section, select the **Assign** check box for the security roles that the new user should have.</span></span>
5.  <span data-ttu-id="6e3e6-142">**Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-142">Click **Submit**.</span></span>

<span data-ttu-id="6e3e6-143">Satıcı kullanıcısı talebi gönderildiğinde, **Satıcı işbirliği erişimine izin verildi** alanı seçilen satıcı hesabı için **Evet** olarak ayarlanır ve kullanıcı talebi iş akışı başlatılır.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-143">When the vendor user request is submitted, the **Vendor collaboration access allowed** field is set to **Yes** for the selected vendor account and a user request workflow is started.</span></span> <span data-ttu-id="6e3e6-144">İş akışının bir parçası olarak, Finance and Operations'ta yeni bir kullanıcı oluşturulur ve güvenlik rolleri atanır.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-144">As part of the workflow, a new user is created in Finance and Operations, and security roles are assigned.</span></span> <span data-ttu-id="6e3e6-145">Buna ek olarak, Azure portalı ile etkileşim başlatan ve yeni veya mevcut bir AAD hesabını Finance and Operations kullanıcı hesabı ile ilişkilendiren bir Azure B2B hizmeti etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-145">In addition, an Azure B2B service is activated which initiates interaction with Azure portal and associates a new or existing AAD account with the Finance and Operations user account.</span></span>

### <a name="inactivate-a-user"></a><span data-ttu-id="6e3e6-146">Kullanıcıyı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="6e3e6-146">Inactivate a user</span></span>

<span data-ttu-id="6e3e6-147">İlgili kullanıcının satıcı iş birliğine olan erişimini kaldırmanın iki yolu bulunmaktadır:</span><span class="sxs-lookup"><span data-stu-id="6e3e6-147">There are two ways to remove access to vendor collaboration for a user:</span></span>

-   <span data-ttu-id="6e3e6-148">Satıcının **İlgili kişiler** sayfasındaki **Satıcı işbirliği erişimine izin verildi** seçeneğini ilgili kişi için **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-148">On the **Contacts** page for the vendor, set the **Vendor collaboration access allowed** option to **No** for the contact.</span></span> <span data-ttu-id="6e3e6-149">Bu, ilgili kişinin bağlantıda olduğu her bir tüzel kişilik için tek tek yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-149">This can be done individually per legal entity that the person is a contact for.</span></span> <span data-ttu-id="6e3e6-150">Bu seçenek yalnızca tedarik profesyonelleri tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-150">This option can only be used by procurement professionals.</span></span>
-   <span data-ttu-id="6e3e6-151">Tüm kullanıcı hesabını **Satıcı kullanıcısını devre dışı bırak** isteği göndererek devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-151">Inactivate the entire user account, by submitting an **Inactivate vendor user** request.</span></span>

<span data-ttu-id="6e3e6-152">Bir kullanıcının devre dışı bırakılmasını talep etmek için:</span><span class="sxs-lookup"><span data-stu-id="6e3e6-152">To request that a user is inactivated:</span></span>

1.  <span data-ttu-id="6e3e6-153"> **Tüm kişiler** sayfasındaki **Satıcı kullanıcısını** **devre dışı bırak**'a tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-153">On the **All contacts** page, click **Inactivate** **vendor user**.</span></span>
2.  <span data-ttu-id="6e3e6-154">**İş gerekçesi** alanına bir yorum yazın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-154">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="6e3e6-155">**Gönder**'e tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-155">Click **Submit**.</span></span>

### <a name="modify-security-roles"></a><span data-ttu-id="6e3e6-156">Güvenlik rollerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="6e3e6-156">Modify security roles</span></span>

<span data-ttu-id="6e3e6-157">**Satıcı kullanıcısı rollerini koru** sayfası, güvenlik rolleri listesinin düzenlenebilmesi dışında **Provizyon satıcı kullanıcısı** sayfası ile aynıdır.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-157">The **Maintain vendor user roles** page is the same as the **Provision vendor user** page except that the list of security roles can be edited.</span></span>  

<span data-ttu-id="6e3e6-158">İlgili kullanıcının güvenlik rollerinin değiştirilmesini talep etmek için:</span><span class="sxs-lookup"><span data-stu-id="6e3e6-158">To request that the security roles are modified for a user:</span></span>

1.  <span data-ttu-id="6e3e6-159">**Tüm kişiler** sayfasındaki **Satıcı kullanıcısı** **rollerini koru**'ya tıklayın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-159">On the **All contacts** page, click **Maintain** **vendor user roles**.</span></span>
2.  <span data-ttu-id="6e3e6-160">**İş gerekçesi** alanına bir yorum yazın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-160">Write a comment in the **Business justification** field.</span></span>
3.  <span data-ttu-id="6e3e6-161">**Kullanıcı rollerini koru** bölümünde, atamak istediğiniz güvenlik rollerini seçin veya kaldırmak istediklerinizin seçimini kaldırın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-161">In the **Maintain user roles** section, select the security roles that you want to assign, or clear the ones that you want to remove.</span></span>
4.  <span data-ttu-id="6e3e6-162">**Gönder**'i tıklatın.</span><span class="sxs-lookup"><span data-stu-id="6e3e6-162">Click **Submit**.</span></span>





