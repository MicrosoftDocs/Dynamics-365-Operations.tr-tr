---
title: Kanal kurulum önkoşulları
description: Bu konu, Microsoft Dynamics 365 Commerce'te kanalların kurulum önkoşulları hakkında genel bilgi vermektedir.
author: samjarawan
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 33fcead6c0b08db17f24b638376a23b8b6024a5b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800531"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="7f924-103">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="7f924-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7f924-104">Bu konu, Microsoft Dynamics 365 Commerce'te kanal kurulum önkoşulları hakkında genel bilgi vermektedir.</span><span class="sxs-lookup"><span data-stu-id="7f924-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7f924-105">Bir Dynamics 365 Commerce kanalı oluşturulmadan önce, önkoşul olan bazı görevlerin tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7f924-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="7f924-106">Aşağıdaki önkoşul görevleri listeleri kanal türüne göre düzenlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="7f924-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="7f924-107">Bazı belgeler hala yazılıyor ve yeni içerik yayımlandıkça bağlantılar güncelleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="7f924-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="7f924-108">Başlatma</span><span class="sxs-lookup"><span data-stu-id="7f924-108">Initialization</span></span>

- [<span data-ttu-id="7f924-109">Çekirdek verileri başlatma</span><span class="sxs-lookup"><span data-stu-id="7f924-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="7f924-110">Tüm kanal türleri için gereken global önkoşullar</span><span class="sxs-lookup"><span data-stu-id="7f924-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="7f924-111">Tüzel kişilik yapınızı tanımlama ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7f924-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="7f924-112">Organizasyon hiyerarşinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7f924-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="7f924-113">Ambar ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="7f924-114">Satış vergisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7f924-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="7f924-115">E-posta bildirimi profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="7f924-116">Numara serileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="7f924-117">Varsayılan müşteriyi ve adres defterini ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="7f924-118">Perakende kanalı önkoşulları</span><span class="sxs-lookup"><span data-stu-id="7f924-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="7f924-119">Bilgi kodları ve bilgi kodu grupları</span><span class="sxs-lookup"><span data-stu-id="7f924-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="7f924-120">Perakende işlevselliği profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="7f924-121">Çalışan adres defteri ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="7f924-122">Ekran düzeni ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="7f924-123">Donanım istasyonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="7f924-124">Çağrı Merkezi kanalı önkoşulları</span><span class="sxs-lookup"><span data-stu-id="7f924-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="7f924-125">Çağrı merkezi parametreleri</span><span class="sxs-lookup"><span data-stu-id="7f924-125">Call center parameters</span></span>
- [<span data-ttu-id="7f924-126">Çağrı merkezi sipariş ve iade ödeme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="7f924-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="7f924-127">Çağrı merkezi teslimat ve ücret modları</span><span class="sxs-lookup"><span data-stu-id="7f924-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="7f924-128">Çevrimiçi kanal önkoşulları</span><span class="sxs-lookup"><span data-stu-id="7f924-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="7f924-129">Çevrimiçi işlevsellik profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="7f924-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="7f924-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7f924-130">Additional resources</span></span>

[<span data-ttu-id="7f924-131">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="7f924-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7f924-132">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="7f924-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7f924-133">Kuruluş hiyerarşilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="7f924-134">Tüzel kişilik oluşturma</span><span class="sxs-lookup"><span data-stu-id="7f924-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="7f924-135">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="7f924-136">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="7f924-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
