---
title: Müşteri portalını yükleme, kurma ve güncelleştirme
description: Bu konu, Müşteri portalı için lisans ayrıntılarını ve kurulum yönergelerini sağlar.
author: dasani-madipalli
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 5c4cad305e3d130b3283ca3424c84f60e2d13307
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907827"
---
# <a name="install-set-up-and-update-the-customer-portal"></a><span data-ttu-id="4dffd-103">Müşteri portalını yükleme, kurma ve güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="4dffd-103">Install, set up, and update the Customer portal</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a><span data-ttu-id="4dffd-104">Lisanslama gereksinimleri</span><span class="sxs-lookup"><span data-stu-id="4dffd-104">Licensing requirements</span></span>

<span data-ttu-id="4dffd-105">Müşteri portalını uygulamak için aşağıdaki lisanslara sahip olmanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="4dffd-105">To implement the Customer portal, you must have the following licenses:</span></span>

- <span data-ttu-id="4dffd-106">**Power Apps portallar** – Bu lisansın müşteri portalını barındırması gereklidir.</span><span class="sxs-lookup"><span data-stu-id="4dffd-106">**Power Apps portals** – This license is required to host the Customer portal.</span></span> <span data-ttu-id="4dffd-107">Portallar kullanıma göre lisanslıdır.</span><span class="sxs-lookup"><span data-stu-id="4dffd-107">Portals are licensed based on usage.</span></span> <span data-ttu-id="4dffd-108">Daha fazla bilgi için, [Power Apps Portal lisans gereksinimlerine](/power-platform/admin/powerapps-flow-licensing-faq#portals) bakın.</span><span class="sxs-lookup"><span data-stu-id="4dffd-108">For more information, see the [Power Apps portals licensing requirements](/power-platform/admin/powerapps-flow-licensing-faq#portals).</span></span>
- <span data-ttu-id="4dffd-109">**Çift yazma**: Supply Chain Management tablolarında çift yazma özelliğini etkinleştirmek için gerekli lisanslara sahip olmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4dffd-109">**Dual-write** – You must have the necessary licenses to enable dual-write for Supply Chain Management tables.</span></span> <span data-ttu-id="4dffd-110">Daha fazla bilgi için bkz: [çift yazma için sistem gereksinimleri.](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md)</span><span class="sxs-lookup"><span data-stu-id="4dffd-110">For more information, see the [system requirements for dual-write](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).</span></span>

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a><span data-ttu-id="4dffd-111">Çift yazma ve Power Apps portallarda bağımlılıklar</span><span class="sxs-lookup"><span data-stu-id="4dffd-111">Dependencies on dual-write and Power Apps portals</span></span>

<span data-ttu-id="4dffd-112">Müşteri Portalı, Aşağıdaki çizimde gösterildiği gibi Power Apps portallara ve çift yazmaya bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="4dffd-112">The Customer portal depends on Power Apps portals and dual-write, as shown in the following illustration.</span></span>

<span data-ttu-id="4dffd-113">![Müşteri portalına bağımlılıklar](media/customer-portal-elements.png "Müşteri portalına bağımlılıklar")</span><span class="sxs-lookup"><span data-stu-id="4dffd-113">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="4dffd-114">Supply Chain Management'tan alınan diğer özelliklerden farklı olarak, Müşteri Portalı şablonu Power Apps portalları içinde bulunur.</span><span class="sxs-lookup"><span data-stu-id="4dffd-114">Unlike other features from Supply Chain Management, the Customer portal template resides in Power Apps portals.</span></span> <span data-ttu-id="4dffd-115">Bu nedenle, Müşteri portalı çift yazmadaki Power Apps portalları ve tabloları tarafından sağlanan işlevler ve özelliklerle sınırlıdır.</span><span class="sxs-lookup"><span data-stu-id="4dffd-115">Therefore, the Customer portal is limited by the functionality and capabilities that are provided by Power Apps portals and the tables in dual-write.</span></span>

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a><span data-ttu-id="4dffd-116">Müşteri portalını etkinleştirmek için gerekli kurulum</span><span class="sxs-lookup"><span data-stu-id="4dffd-116">Required setup to enable the Customer portal</span></span>

<span data-ttu-id="4dffd-117">Gerekli lisanslara sahip olduğunuzdan emin olduktan sonra, [Çift-yazılabilir başlangıç eşitleme yönergelerinde](/dynamics365/supply-chain/sales-marketing/enable-entity-map) açıklandığı gibi çift-yazılabilir ayarlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4dffd-117">After you've made sure that you have the required licenses, you can set up dual-write as described in the [dual-write initial synchronization instructions](/dynamics365/supply-chain/sales-marketing/enable-entity-map).</span></span>

<span data-ttu-id="4dffd-118">Çift yazmada aşağıdaki tablo eşlemelerini etkinleştirdiğinizden emin olun:</span><span class="sxs-lookup"><span data-stu-id="4dffd-118">Be sure to enable the following table mappings in dual-write:</span></span>

- <span data-ttu-id="4dffd-119">Satış siparişi başlığı</span><span class="sxs-lookup"><span data-stu-id="4dffd-119">Sales Order Header</span></span>
- <span data-ttu-id="4dffd-120">Satış siparişi ayrıntıları</span><span class="sxs-lookup"><span data-stu-id="4dffd-120">Sales Order Details</span></span>
- <span data-ttu-id="4dffd-121">Hesaplar</span><span class="sxs-lookup"><span data-stu-id="4dffd-121">Accounts</span></span>
- <span data-ttu-id="4dffd-122">İlgili kişiler</span><span class="sxs-lookup"><span data-stu-id="4dffd-122">Contacts</span></span>
- <span data-ttu-id="4dffd-123">Ürünler</span><span class="sxs-lookup"><span data-stu-id="4dffd-123">Products</span></span>

<span data-ttu-id="4dffd-124">Bu kurulum tamamlandıktan sonra, müşteri portalı şablonunu temin edebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4dffd-124">After this setup is completed, you can provision the Customer portal template.</span></span>

## <a name="provision-the-customer-portal"></a><span data-ttu-id="4dffd-125">Müşteri Portalı Hazırlama</span><span class="sxs-lookup"><span data-stu-id="4dffd-125">Provision the Customer portal</span></span>

<span data-ttu-id="4dffd-126">Başlamadan önce [gerekli kurulumu](#required-setup) tamamlamış olduğunuzdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="4dffd-126">Before you begin, make sure that you've already completed the [required setup](#required-setup).</span></span> <span data-ttu-id="4dffd-127">Müşteri portalını sağlamak için aşağıdaki adımları izleyin.</span><span class="sxs-lookup"><span data-stu-id="4dffd-127">Then follow these steps to provision the Customer portal.</span></span>

1. <span data-ttu-id="4dffd-128">[make.powerapps.com](https://make.powerapps.com/) gidin.</span><span class="sxs-lookup"><span data-stu-id="4dffd-128">Go to [make.powerapps.com](https://make.powerapps.com/).</span></span>
2. <span data-ttu-id="4dffd-129">Çift-yazmayı etkinleştirdiğiniz ortamı kullandığınızdan emin olun.</span><span class="sxs-lookup"><span data-stu-id="4dffd-129">Make sure that you're using the environment where you enabled dual-write.</span></span>
3. <span data-ttu-id="4dffd-130">**Oluştur** sekmesinde, **şablondan başlangıç şablonu** bölümüne gidin ve **Müşteri Portalı** olarak adlandırılan şablonu seçin.</span><span class="sxs-lookup"><span data-stu-id="4dffd-130">On the **Create** tab, scroll down to the **Start from template** section, and select the template that is named **Customer Portal**.</span></span>
4. <span data-ttu-id="4dffd-131">Ekrandaki yönergeleri izleyin.</span><span class="sxs-lookup"><span data-stu-id="4dffd-131">Follow the on-screen instructions.</span></span>

<span data-ttu-id="4dffd-132">Sağlama tamamlandıktan sonra, **giriş** sayfasının **uygulamalarınız** bölümünde müşteri portalına erişebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4dffd-132">After provisioning is completed, you can access the Customer portal in the **Your apps** section of the **Home** page.</span></span>

> [!NOTE]
> <span data-ttu-id="4dffd-133">Çift-yazılır çözüm, üzerinde çalışmakta olduğunuz ortamda kurulu değilse bir hata iletisi alırsınız ve müşteri portalı sağlanmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="4dffd-133">If the dual-write solution isn't installed in the environment that you're working in, you will receive an error message, and the Customer portal won't be provisioned.</span></span>

## <a name="update-the-customer-portal"></a><span data-ttu-id="4dffd-134">Müşteri Portalı güncelleme</span><span class="sxs-lookup"><span data-stu-id="4dffd-134">Update the Customer portal</span></span>

<span data-ttu-id="4dffd-135">Daha sonra müşteri portalına daha fazla işlevsellik eklenebilir.</span><span class="sxs-lookup"><span data-stu-id="4dffd-135">More functionality might be added to the Customer portal later.</span></span> <span data-ttu-id="4dffd-136">Microsoft'un alttaki çözüm bileşenlerine yaptığı değişiklikler sizin ortamınızda otomatik olarak görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="4dffd-136">Any changes that Microsoft makes to the underlying solution components will automatically appear in your environment.</span></span> <span data-ttu-id="4dffd-137">Ancak, ortamınızda sağlanan Web sitesi, yapılandırma verilerinde yapılan değişiklikleri otomatik olarak yansıtmayacaktır.</span><span class="sxs-lookup"><span data-stu-id="4dffd-137">However, the website that is provisioned in your environment won't automatically reflect changes that are made to the configuration data.</span></span> <span data-ttu-id="4dffd-138">Yeni şablondan kodu alarak ve bunu sağlanan Web sitesiyle birleştirerek bu değişiklikleri el ile uygulamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4dffd-138">You will have to manually apply those changes by getting the code from the new template and merging it with the provisioned website.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4dffd-139">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="4dffd-139">Additional resources</span></span>

<span data-ttu-id="4dffd-140">Müşteri portalını nasıl ayarlayabileceğinizi ve özelleştirebileceğinizi öğrenmek için, temeldeki teknolojiler için aşağıdaki belgeleri gözden geçirerek başlamanız gerekir:</span><span class="sxs-lookup"><span data-stu-id="4dffd-140">To learn how you can set up and customize the Customer portal, you should start by reviewing the following documentation for the underlying technologies:</span></span>

- [<span data-ttu-id="4dffd-141">Power Apps portal belgeleri</span><span class="sxs-lookup"><span data-stu-id="4dffd-141">Power Apps portals documentation</span></span>](/powerapps/maker/portals/overview)
- [<span data-ttu-id="4dffd-142">Çift yazma belgeleri</span><span class="sxs-lookup"><span data-stu-id="4dffd-142">Dual-write documentation</span></span>](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

<span data-ttu-id="4dffd-143">Portallarınızı etkili şekilde yönetmek için Power Apps portalları ve Microsoft Dataverse yaşam döngüsünü anlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="4dffd-143">To effectively manage your portals, you must understand the Power Apps portals and Microsoft Dataverse lifecycle.</span></span> <span data-ttu-id="4dffd-144">Daha fazla bilgi edinmek için aşağıdaki kaynaklara bakın:</span><span class="sxs-lookup"><span data-stu-id="4dffd-144">For more information, see the following resources:</span></span>

- [<span data-ttu-id="4dffd-145">Portal yaşam döngüsü hakkında</span><span class="sxs-lookup"><span data-stu-id="4dffd-145">About portal lifecycle</span></span>](/powerapps/maker/portals/admin/portal-lifecycle)
- [<span data-ttu-id="4dffd-146">Bir portalı yükselt</span><span class="sxs-lookup"><span data-stu-id="4dffd-146">Upgrade a portal</span></span>](/powerapps/maker/portals/admin/upgrade-portal)
- [<span data-ttu-id="4dffd-147">Portal konfigürasyonu geçir</span><span class="sxs-lookup"><span data-stu-id="4dffd-147">Migrate portal configuration</span></span>](/powerapps/maker/portals/admin/migrate-portal-configuration)
- [<span data-ttu-id="4dffd-148">Çözüm yaşam döngüsü yönetimi: Customer Engagement için Dynamics 365 uygulamaları</span><span class="sxs-lookup"><span data-stu-id="4dffd-148">Solution Lifecycle Management: Dynamics 365 for Customer Engagement apps</span></span>](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]