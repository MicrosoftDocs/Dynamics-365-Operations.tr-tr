---
title: Taraf veri modeli ile Power Portal'ı kullanma
description: Bu konu, Çift yazma taraf veri modeli nedeniyle Power Portal Web rollerine yapılan değişiklikleri açıklamaktadır.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833102"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="92e42-103">Taraf veri modeli ile Power Portal'ı kullanma</span><span class="sxs-lookup"><span data-stu-id="92e42-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="92e42-104">Çift yazma uygulama düzenleme çözümü sürüm 2.0.999.0 ve sonraki sürümleri, Hesap ve İlgili kişi tabloları için tarafta ve genel adres defterindeki veri modeli değişikliklerini içerir.</span><span class="sxs-lookup"><span data-stu-id="92e42-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="92e42-105">Değişiklikler, gelişmiş iş senaryolarını destekleyen çok-çok ilişkisi sağlar.</span><span class="sxs-lookup"><span data-stu-id="92e42-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="92e42-106">Bu değişiklikler, müşteri portalı dahil, kullanıma hazır veya çift yazma yüklenmeden önce ortamınızda varolan portal web rolleri tarafından desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="92e42-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="92e42-107">Web rollerinin beklendiği gibi çalışması için yeni veri modelini kullanarak yeni Web rolleri oluşturmanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="92e42-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="92e42-108">Özetle, tabloların etkileşim şekli değişti, ancak müşteri portalındaki tablo izinleri değişmedi.</span><span class="sxs-lookup"><span data-stu-id="92e42-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="92e42-109">Bu konu, yeni gelişmiş veri modeliyle çalışan yeni Web rollerinin nasıl oluşturulacağını açıklamaktadır.</span><span class="sxs-lookup"><span data-stu-id="92e42-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="92e42-110">Bu diyagram, taraf ve genel adres defteri veri modeli **olmadan** tablo ilişkisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="92e42-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![Taraf modeli olmadan](media/without-party-model.PNG)

<span data-ttu-id="92e42-112">Bu diyagram, taraf ve genel adres defteri veri modeli **ile birlikte** tablo ilişkisini gösterir:</span><span class="sxs-lookup"><span data-stu-id="92e42-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![Taraf modeli ile birlikte](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="92e42-114">Yeni tablo izni oluşturma</span><span class="sxs-lookup"><span data-stu-id="92e42-114">Create a new table permission</span></span>

<span data-ttu-id="92e42-115">Bu yeni tablo izinlerini oluşturmak için şu adımları izleyin:</span><span class="sxs-lookup"><span data-stu-id="92e42-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="92e42-116">[Power Apps](https://make.powerapps.com)'te oturum açın ve uygulamalarınıza gidin.</span><span class="sxs-lookup"><span data-stu-id="92e42-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="92e42-117">Portal yönetimi uygulamanızı seçin.</span><span class="sxs-lookup"><span data-stu-id="92e42-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="92e42-118">Yan çubukta **güvenlik > tablo izinlerini** seçin.</span><span class="sxs-lookup"><span data-stu-id="92e42-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="92e42-119">Üç yeni izin oluşturmalısınız:</span><span class="sxs-lookup"><span data-stu-id="92e42-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="92e42-120">İlgili kişi - Taraf bağlantısı</span><span class="sxs-lookup"><span data-stu-id="92e42-120">Contact to Party connection</span></span>
    + <span data-ttu-id="92e42-121">Taraf - Hesap bağlantısı</span><span class="sxs-lookup"><span data-stu-id="92e42-121">Party to Account connection</span></span>
    + <span data-ttu-id="92e42-122">Hesap - Sipariş bağlantısı</span><span class="sxs-lookup"><span data-stu-id="92e42-122">Account to Order connection</span></span>

4. <span data-ttu-id="92e42-123">Şu parameteleri ayarlayarak İlgili kişi - taraf bağlantısı için yeni bir izin oluştup Kaydedin:</span><span class="sxs-lookup"><span data-stu-id="92e42-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="92e42-124">**Ad**: Taraf - hesap bağlantısı (veya sizin seçiminiz)</span><span class="sxs-lookup"><span data-stu-id="92e42-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="92e42-125">**Tablo adı**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="92e42-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="92e42-126">**Web sitesi**: Müşteri Portalı</span><span class="sxs-lookup"><span data-stu-id="92e42-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="92e42-127">**Kapsam**: İlgili kişi</span><span class="sxs-lookup"><span data-stu-id="92e42-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="92e42-128">**Ayrıcalıklar**: Tümünü Seç</span><span class="sxs-lookup"><span data-stu-id="92e42-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="92e42-129">**Web rolleri**: Kimliği doğrulanmış kullanıcılar, müşteri temsilcisi (veya seçiminiz)</span><span class="sxs-lookup"><span data-stu-id="92e42-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="92e42-130">Şu parameteleri ayarlayarak Taraf - Hesap bağlantısı için yeni bir izin oluştup Kaydedin:</span><span class="sxs-lookup"><span data-stu-id="92e42-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="92e42-131">**Ad**: Taraf - hesap bağlantısı (veya sizin seçiminiz)</span><span class="sxs-lookup"><span data-stu-id="92e42-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="92e42-132">**Tablo adı**: hesap</span><span class="sxs-lookup"><span data-stu-id="92e42-132">**Table Name**: account</span></span>
    + <span data-ttu-id="92e42-133">**Web sitesi**: Müşteri Portalı</span><span class="sxs-lookup"><span data-stu-id="92e42-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="92e42-134">**Kapsam**: üst</span><span class="sxs-lookup"><span data-stu-id="92e42-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="92e42-135">**Ayrıcalıklar**: Tümünü Seç</span><span class="sxs-lookup"><span data-stu-id="92e42-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="92e42-136">**Üst tablo izni**: İlgili kişi - Taraf bağlantısı</span><span class="sxs-lookup"><span data-stu-id="92e42-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="92e42-137">Şu parameteleri ayarlayarak Hesap - Sipariş bağlantısı için yeni bir izin oluştup Kaydedin:</span><span class="sxs-lookup"><span data-stu-id="92e42-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="92e42-138">**Ad**: Hesap - Sipariş bağlantısı (veya sizin seçiminiz)</span><span class="sxs-lookup"><span data-stu-id="92e42-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="92e42-139">**Tablo adı**: salesorder</span><span class="sxs-lookup"><span data-stu-id="92e42-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="92e42-140">**Web sitesi**: Müşteri Portalı</span><span class="sxs-lookup"><span data-stu-id="92e42-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="92e42-141">**Kapsam**: üst</span><span class="sxs-lookup"><span data-stu-id="92e42-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="92e42-142">**Ayrıcalıklar**: Tümünü Seç</span><span class="sxs-lookup"><span data-stu-id="92e42-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="92e42-143">**Üst tablo izni**: Taraf - Hesap bağlantısı</span><span class="sxs-lookup"><span data-stu-id="92e42-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
