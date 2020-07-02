---
title: Müşteri portalını yükleme, kurma ve güncelleştirme
description: Bu konu, Müşteri portalı için lisans ayrıntılarını ve kurulum yönergelerini sağlar.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0343100362c4d7bc3e09334fb7890919bdb84941
ms.sourcegitcommit: 7d943499f302298c6ff127f56cecc34af6cee289
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/08/2020
ms.locfileid: "3435621"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="b9cde-103">Müşteri portalını yükleme, kurma ve güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="b9cde-103">Install, set up, and update the Customer portal</span></span>

## <a name="licensing-requirements"></a><span data-ttu-id="b9cde-104">Lisanslama gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="b9cde-104">Licensing requirements</span></span>

<span data-ttu-id="b9cde-105">Müşteri portalını uygulamak için aşağıdaki lisanslara sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="b9cde-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="b9cde-106">**Power Apps portallar** – Bu lisansın müşteri portalını barındırması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="b9cde-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="b9cde-107">Portallar kullanıma göre lisanslıdır.</span><span class="sxs-lookup"><span data-stu-id="b9cde-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="b9cde-108">Daha fazla bilgi için, [Power Apps Portal lisans gereksinimlerine](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals) bakın.</span><span class="sxs-lookup"><span data-stu-id="b9cde-108">For more information, see the [Power Apps portals licensing requirements](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="b9cde-109">**İkili yazma** – Supply Chain Management varlıklarının çift-yazılabilir özelliğini etkinleştirmek için gerekli lisanslara sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b9cde-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management entities.</span></span> <span data-ttu-id="b9cde-110">Daha fazla bilgi için bkz: [çift yazma için sistem gereksinimleri.](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md)</span><span class="sxs-lookup"><span data-stu-id="b9cde-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="b9cde-111">Çift yazma ve Power Apps portallarda bağımlılıklar</span><span class="sxs-lookup"><span data-stu-id="b9cde-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="b9cde-112">Müşteri Portalı, Aşağıdaki çizimde gösterildiği gibi Power Apps portallara ve çift yazmaya bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="b9cde-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="b9cde-113">![Müşteri portalına bağımlılıklar](media/customer-portal-elements.png "Müşteri portalına bağımlılıklar")</span><span class="sxs-lookup"><span data-stu-id="b9cde-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="b9cde-114">Supply Chain Management'tan alınan diğer özelliklerden farklı olarak, Müşteri Portalı şablonu Power Apps portalları içinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="b9cde-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="b9cde-115">Bu nedenle, müşteri portalı Power Apps portalların ve varlıkların çift yazması tarafından sağlanan işlevler ve yetenekler ile sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="b9cde-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the entities in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="b9cde-116">Müşteri portalını etkinleştirmek için gerekli kurulum</span><span class="sxs-lookup"><span data-stu-id="b9cde-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="b9cde-117">Gerekli lisanslara sahip olduğunuzdan emin olduktan sonra, [Çift-yazılabilir başlangıç eşitleme yönergelerinde](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md) açıklandığı gibi çift-yazılabilir ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9cde-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).</span></span>

<span data-ttu-id="b9cde-118">Çift yazarken aşağıdaki varlık eşlemelerini etkinleştirdiğinizden emin olun:</span><span class="sxs-lookup"><span data-stu-id="b9cde-118">Be sure to enable the following entity mappings in dual-write:</span></span>

- <span data-ttu-id="b9cde-119">Satış siparişi başlığı</span><span class="sxs-lookup"><span data-stu-id="b9cde-119">Sales Order Header</span></span>
- <span data-ttu-id="b9cde-120">Satış siparişi ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="b9cde-120">Sales Order Details</span></span>
- <span data-ttu-id="b9cde-121">Hesaplar</span><span class="sxs-lookup"><span data-stu-id="b9cde-121">Accounts</span></span>
- <span data-ttu-id="b9cde-122">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="b9cde-122">Contacts</span></span>
- <span data-ttu-id="b9cde-123">Ürünler</span><span class="sxs-lookup"><span data-stu-id="b9cde-123">Products</span></span>

<span data-ttu-id="b9cde-124">Bu kurulum tamamlandıktan sonra, müşteri portalı şablonunu temin edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9cde-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="b9cde-125">Müşteri Portalı Hazırlama</span><span class="sxs-lookup"><span data-stu-id="b9cde-125">Provision the Customer portal</span></span>

<span data-ttu-id="b9cde-126">Başlamadan önce [gerekli kurulumu](#required-setup) tamamlamış olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b9cde-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="b9cde-127">Müşteri portalını sağlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="b9cde-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="b9cde-128">[make.powerapps.com](https://make.powerapps.com/) gidin.</span><span class="sxs-lookup"><span data-stu-id="b9cde-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="b9cde-129">Çift-yazmayı etkinleştirdiğiniz ortamı kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="b9cde-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="b9cde-130">**Oluştur** sekmesinde, **şablondan başlangıç şablonu** bölümüne gidin ve **Müşteri Portalı** olarak adlandırılan şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="b9cde-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="b9cde-131">Ekrandaki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="b9cde-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="b9cde-132">Sağlama tamamlandıktan sonra, **giriş** sayfasının **uygulamalarınız** bölümünde müşteri portalına erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b9cde-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="b9cde-133">Çift-yazılır çözüm, üzerinde çalışmakta olduğunuz ortamda kurulu değilse bir hata iletisi alırsınız ve müşteri portalı sağlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="b9cde-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="b9cde-134">Müşteri Portalı güncelleme</span><span class="sxs-lookup"><span data-stu-id="b9cde-134">Update the Customer portal</span></span>

<span data-ttu-id="b9cde-135">Daha sonra müşteri portalına daha fazla işlevsellik eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="b9cde-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="b9cde-136">Microsoft'un alttaki çözüm bileşenlerine yaptığı değişiklikler sizin ortamınızda otomatik olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="b9cde-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="b9cde-137">Ancak, ortamınızda sağlanan Web sitesi, yapılandırma verilerinde yapılan değişiklikleri otomatik olarak yansıtmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="b9cde-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="b9cde-138">Yeni şablondan kodu alarak ve bunu sağlanan Web sitesiyle birleştirerek bu değişiklikleri el ile uygulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b9cde-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9cde-139">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="b9cde-139">Additional resources</span></span>

<span data-ttu-id="b9cde-140">Müşteri portalını nasıl ayarlayabileceğinizi ve özelleştirebileceğinizi öğrenmek için, temeldeki teknolojiler için aşağıdaki belgeleri gözden geçirerek başlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="b9cde-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="b9cde-141">Power Apps portal belgeleri</span><span class="sxs-lookup"><span data-stu-id="b9cde-141">Power Apps portals documentation</span></span>](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [<span data-ttu-id="b9cde-142">Çift yazma belgeleri</span><span class="sxs-lookup"><span data-stu-id="b9cde-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="b9cde-143">Portallarınızı etkili şekilde yönetmek için Power Apps portalları ve Common Data Service yaşam döngüsünü anlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="b9cde-143">To effectively manage your portals, you must understand the Power Apps portals and Common Data Service lifecycle.</span></span> <span data-ttu-id="b9cde-144">Daha fazla bilgi edinmek için aşağıdaki kaynaklara bakın:</span><span class="sxs-lookup"><span data-stu-id="b9cde-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="b9cde-145">Portal yaşam döngüsü hakkında</span><span class="sxs-lookup"><span data-stu-id="b9cde-145">About portal lifecycle</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="b9cde-146">Bir portalı yükselt</span><span class="sxs-lookup"><span data-stu-id="b9cde-146">Upgrade a portal</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="b9cde-147">Portal konfigürasyonu geçir</span><span class="sxs-lookup"><span data-stu-id="b9cde-147">Migrate portal configuration</span></span>](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="b9cde-148">Çözüm yaşam döngüsü yönetimi: Customer Engagement için Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="b9cde-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)
