---
title: Kanal kurulum önkoşulları
description: Bu konu, Microsoft Dynamics 365 Commerce'te kanalların kurulum önkoşulları hakkında genel bilgi vermektedir.
author: samjarawan
manager: annbe
ms.date: 02/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 270f751e860e56a03e20df720c088f275d0298e7
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477936"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="7a8ab-103">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="7a8ab-103">Channel setup prerequisites</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7a8ab-104">Bu konu, Microsoft Dynamics 365 Commerce'te kanal kurulum önkoşulları hakkında genel bilgi vermektedir.</span><span class="sxs-lookup"><span data-stu-id="7a8ab-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7a8ab-105">Bir Dynamics 365 Commerce kanalı oluşturulmadan önce, önkoşul olan bazı görevlerin tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="7a8ab-105">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="7a8ab-106">Aşağıdaki önkoşul görevleri listeleri kanal türüne göre düzenlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="7a8ab-106">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="7a8ab-107">Bazı belgeler hala yazılıyor ve yeni içerik yayımlandıkça bağlantılar güncelleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="7a8ab-107">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="7a8ab-108">Başlatma</span><span class="sxs-lookup"><span data-stu-id="7a8ab-108">Initialization</span></span>

- [<span data-ttu-id="7a8ab-109">Çekirdek verileri başlatma</span><span class="sxs-lookup"><span data-stu-id="7a8ab-109">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="7a8ab-110">Tüm kanal türleri için gereken global önkoşullar</span><span class="sxs-lookup"><span data-stu-id="7a8ab-110">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="7a8ab-111">Tüzel kişilik yapınızı tanımlama ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7a8ab-111">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="7a8ab-112">Organizasyon hiyerarşinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7a8ab-112">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="7a8ab-113">Ambar ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-113">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="7a8ab-114">Satış vergisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="7a8ab-114">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="7a8ab-115">E-posta bildirimi profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-115">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="7a8ab-116">Numara serileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-116">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="7a8ab-117">Varsayılan müşteriyi ve adres defterini ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-117">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="7a8ab-118">Perakende kanalı önkoşulları</span><span class="sxs-lookup"><span data-stu-id="7a8ab-118">Retail channel prerequisites</span></span>

- [<span data-ttu-id="7a8ab-119">Bilgi kodları ve bilgi kodu grupları</span><span class="sxs-lookup"><span data-stu-id="7a8ab-119">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="7a8ab-120">Perakende işlevselliği profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-120">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="7a8ab-121">Çalışan adres defteri ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-121">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="7a8ab-122">Ekran düzeni ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-122">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="7a8ab-123">Donanım istasyonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-123">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="7a8ab-124">Çağrı Merkezi kanalı önkoşulları</span><span class="sxs-lookup"><span data-stu-id="7a8ab-124">Call Center channel prerequisites</span></span>

- <span data-ttu-id="7a8ab-125">Çağrı merkezi parametreleri</span><span class="sxs-lookup"><span data-stu-id="7a8ab-125">Call center parameters</span></span>
- [<span data-ttu-id="7a8ab-126">Çağrı merkezi sipariş ve iade ödeme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="7a8ab-126">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="7a8ab-127">Çağrı merkezi teslimat ve ücret modları</span><span class="sxs-lookup"><span data-stu-id="7a8ab-127">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="7a8ab-128">Çevrimiçi kanal önkoşulları</span><span class="sxs-lookup"><span data-stu-id="7a8ab-128">Online channel prerequisites</span></span>

- [<span data-ttu-id="7a8ab-129">Çevrimiçi işlevsellik profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a8ab-129">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="7a8ab-130">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="7a8ab-130">Additional resources</span></span>

[<span data-ttu-id="7a8ab-131">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="7a8ab-131">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="7a8ab-132">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="7a8ab-132">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="7a8ab-133">Kuruluş hiyerarşilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-133">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="7a8ab-134">Tüzel kişilik oluşturma</span><span class="sxs-lookup"><span data-stu-id="7a8ab-134">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="7a8ab-135">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-135">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="7a8ab-136">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a8ab-136">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
