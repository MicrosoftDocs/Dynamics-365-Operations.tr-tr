---
title: Satıcı portal kullanıcı güvenliği
description: Bu makale, Satıcı portalını kullanan dış satıcılar için güvenliğin nasıl ayarlanacağını açıklamaktadır. Bu bilgiler, Dynamics AX'in yalnızca Şubat 2016 &amp; Mayıs 2016 sürümleri için geçerlidir.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72f353448f3b5d1f816bb240a230e26529c9cec3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207138"
---
# <a name="vendor-portal-user-security"></a><span data-ttu-id="d336f-104">Satıcı portalı kullanıcı güvenliği</span><span class="sxs-lookup"><span data-stu-id="d336f-104">Vendor portal user security</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d336f-105">Bu makale, Satıcı portalını kullanan dış satıcılar için güvenliğin nasıl ayarlanacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="d336f-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="d336f-106">Bu bilgiler, Dynamics AX'in yalnızca Şubat 2016 &amp; Mayıs 2016 sürümleri için geçerlidir.</span><span class="sxs-lookup"><span data-stu-id="d336f-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="d336f-107">Satıcı portal işlevi, Dynamics 365 for Operations sürüm 1611'de genişletilmiş satıcı iş birliği işlevleri ile değiştirilmiştir.</span><span class="sxs-lookup"><span data-stu-id="d336f-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="d336f-108">Satıcı iş birliğini için satıcıların güvenliğinin yapılandırması hakkında daha fazla bilgi için bkz. [Satıcı iş birliğini kurulumu ve bakımı](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="d336f-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="d336f-109">Satıcı portal dış satıcı için satın alma siparişleri (PO'lar) hakkında sınırlı bir bilgi kümesini sunar.</span><span class="sxs-lookup"><span data-stu-id="d336f-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="d336f-110">Satıcılar Dynamics AX yüklemenizdeki ek bilgilere erişimi olmasın diye, Microsoft Dynamics AX'te satıcı portalı için kullanıcı izinlerini doğru ayarlamanız önemlidir.</span><span class="sxs-lookup"><span data-stu-id="d336f-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="d336f-111">**Önemli:** diğer kullanıcılardan farklı olarak, harici satıcılarda **SystemUser** rolü olmamalıdır.</span><span class="sxs-lookup"><span data-stu-id="d336f-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="d336f-112">**SystemUser** rolü dış kullanıcılar için uygun olmayan ayrıcalıklar kümesine erişim verir.</span><span class="sxs-lookup"><span data-stu-id="d336f-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="d336f-113">Bir tedarikçi portalı kullanıcısı kurma</span><span class="sxs-lookup"><span data-stu-id="d336f-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="d336f-114">Tedarikçi portalı kullanan birisi için bir kullanıcı hesabı oluşturmadan önce satıcıyı satıcı portal iş birliği için izin verecek şekilde ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="d336f-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="d336f-115">**satıcılar** sayfasında **genel** sekmesinde **satın alma siparişi iş birliği** alanını seçin.</span><span class="sxs-lookup"><span data-stu-id="d336f-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="d336f-116">Tedarikçi portalı kullanan harici satıcılarda aşağıdaki Kurulum olması gerekir:</span><span class="sxs-lookup"><span data-stu-id="d336f-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="d336f-117">Microsoft Azure Active Directory (AAD) kullanıcı hesabı Dynamics AX'de **Kullanıcılar** sayfasında satıcı üzerinde kayıtlı olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d336f-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="d336f-118">Satıcı **(Dış) satıcı** güvenlik rolüne sahip olması gerekir, **SystemUser** rolü değil.</span><span class="sxs-lookup"><span data-stu-id="d336f-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="d336f-119">**Not:** **SystemUser** rolü Dynamics AX uygulamasında yeni bir kullanıcı hesabı oluşturduğunuzda otomatik olarak verilir.</span><span class="sxs-lookup"><span data-stu-id="d336f-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="d336f-120">Bu nedenle, bu rolü kaldırmanız ve aldığınız uyarı iletisini kabul etmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="d336f-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="d336f-121">Satıcı kullanıcıya kendi PO görünümüne PO tablolardan ek alanlar eklemek için izni verilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="d336f-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="d336f-122">**kişiselleştirme** sekmesinde, **kullanıcılar** sekmesinde, kullanıcı için **açık kişiselleştirme izinli** seçeneğini **Hayır** olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="d336f-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="d336f-123">Kullanıcı hesabı kayıtlı bir ilgili kişi ile ilişkilendirilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d336f-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="d336f-124">**kullanıcı** sayfasında, **Ad** alanında bir kişiyi seçin.</span><span class="sxs-lookup"><span data-stu-id="d336f-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="d336f-125">Seçtiğiniz kişinin ilgili satıcı için **kişi** rolüne sahip olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d336f-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="d336f-126">Aynı kişi için birden çok satıcı hesapları satıcı portal erişimi gerektiriyorsa (farklı tüzel kişilikler için belki de), o kişinin kullanıcı hesaplarının her birini aynı kayıtlı ilgili kişi ile ilişkilendirilmiş olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="d336f-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="d336f-127">**(Dış) satıcı** rolü satıcı Portal'da kullanılabilir işlevleri kullanmak için gerekli olan temel özellikleri içerir.</span><span class="sxs-lookup"><span data-stu-id="d336f-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="d336f-128">Bu kurulum yalnızca amaçlanan senaryoda dış kullanıcının gördüğü kullanıcı arayüzüne odaklanmasına garantilemeye yarar.</span><span class="sxs-lookup"><span data-stu-id="d336f-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="additional-resources"></a><span data-ttu-id="d336f-129">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="d336f-129">Additional resources</span></span>
--------

[<span data-ttu-id="d336f-130">Satıcılarla Satıcı portalını kullanarak iş birliği yapın</span><span class="sxs-lookup"><span data-stu-id="d336f-130">Collaborate with vendors by using the Vendor portal</span></span>](collaborate-vendors-vendor-portal.md)



