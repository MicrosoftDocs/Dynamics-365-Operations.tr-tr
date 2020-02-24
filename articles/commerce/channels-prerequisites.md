---
title: Kanal kurulum önkoşulları
description: Bu konu, Microsoft Dynamics 365 Commerce'te kanalların kurulum önkoşulları hakkında genel bilgi vermektedir.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b861d90f1333c8f6e61a83602ed74e30b65f3dc1
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002301"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="6225b-103">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="6225b-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6225b-104">Bu konu, Microsoft Dynamics 365 Commerce'te kanal kurulum önkoşulları hakkında genel bilgi vermektedir.</span><span class="sxs-lookup"><span data-stu-id="6225b-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6225b-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="6225b-105">Overview</span></span>

<span data-ttu-id="6225b-106">Bir Dynamics 365 Commerce kanalı oluşturulmadan önce, önkoşul olan bazı görevlerin tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6225b-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="6225b-107">Aşağıdaki önkoşul görevleri listeleri kanal türüne göre düzenlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="6225b-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="6225b-108">Bazı belgeler hala yazılıyor ve yeni içerik yayımlandıkça bağlantılar güncelleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="6225b-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="6225b-109">Başlatma</span><span class="sxs-lookup"><span data-stu-id="6225b-109">Initialization</span></span>

- [<span data-ttu-id="6225b-110">Çekirdek verileri başlatma</span><span class="sxs-lookup"><span data-stu-id="6225b-110">Initialize seed data</span></span>](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="6225b-111">Tüm kanal türleri için gereken global önkoşullar</span><span class="sxs-lookup"><span data-stu-id="6225b-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="6225b-112">Tüzel kişilik yapınızı tanımlama ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6225b-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="6225b-113">Organizasyon hiyerarşinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6225b-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="6225b-114">Ambar ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="6225b-115">Satış vergisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="6225b-115">Configure sales tax</span></span>](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="6225b-116">E-posta bildirimi profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="6225b-117">Numara serileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-117">Set up number sequences</span></span>](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="6225b-118">Varsayılan müşteriyi ve adres defterini ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="6225b-119">Perakende kanalı önkoşulları</span><span class="sxs-lookup"><span data-stu-id="6225b-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="6225b-120">Bilgi kodları ve bilgi kodu grupları</span><span class="sxs-lookup"><span data-stu-id="6225b-120">Info codes and info code groups</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="6225b-121">Perakende işlevselliği profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="6225b-122">Çalışan adres defteri ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="6225b-123">Ekran düzeni ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-123">Set up a screen layout</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="6225b-124">Donanım istasyonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-124">Set up a hardware station</span></span>](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="6225b-125">Çağrı Merkezi kanalı önkoşulları</span><span class="sxs-lookup"><span data-stu-id="6225b-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="6225b-126">Çağrı merkezi parametreleri</span><span class="sxs-lookup"><span data-stu-id="6225b-126">Call center parameters</span></span>
- <span data-ttu-id="6225b-127">Çağrı merkezi para iadesi yöntemleri</span><span class="sxs-lookup"><span data-stu-id="6225b-127">Call center refund methods</span></span>
- <span data-ttu-id="6225b-128">Kiralama türleri</span><span class="sxs-lookup"><span data-stu-id="6225b-128">Rental types</span></span>
- <span data-ttu-id="6225b-129">Ödeme hizmetleri</span><span class="sxs-lookup"><span data-stu-id="6225b-129">Payment services</span></span>
- <span data-ttu-id="6225b-130">Sipariş tutma kodları</span><span class="sxs-lookup"><span data-stu-id="6225b-130">Order hold codes</span></span>

## <a name="online-channel-prerequisites"></a><span data-ttu-id="6225b-131">Çevrimiçi kanal önkoşulları</span><span class="sxs-lookup"><span data-stu-id="6225b-131">Online channel prerequisites</span></span>

- [<span data-ttu-id="6225b-132">Çevrimiçi işlevsellik profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="6225b-132">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="6225b-133">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="6225b-133">Additional resources</span></span>

[<span data-ttu-id="6225b-134">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="6225b-134">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6225b-135">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="6225b-135">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="6225b-136">Kuruluş hiyerarşilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-136">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="6225b-137">Tüzel kişilik oluşturma</span><span class="sxs-lookup"><span data-stu-id="6225b-137">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="6225b-138">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-138">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="6225b-139">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="6225b-139">Set up an online channel</span></span>](channel-setup-online.md)
