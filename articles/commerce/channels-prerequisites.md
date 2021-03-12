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
ms.openlocfilehash: 0705efac4659f96ebca1c67f6f0ab8d23c99d81e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997712"
---
# <a name="channel-setup-prerequisites"></a><span data-ttu-id="afcbb-103">Kanal kurulum önkoşulları</span><span class="sxs-lookup"><span data-stu-id="afcbb-103">Channel setup prerequisites</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="afcbb-104">Bu konu, Microsoft Dynamics 365 Commerce'te kanal kurulum önkoşulları hakkında genel bilgi vermektedir.</span><span class="sxs-lookup"><span data-stu-id="afcbb-104">This topic presents an overview of channel setup prerequisites in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="afcbb-105">Genel Bakış</span><span class="sxs-lookup"><span data-stu-id="afcbb-105">Overview</span></span>

<span data-ttu-id="afcbb-106">Bir Dynamics 365 Commerce kanalı oluşturulmadan önce, önkoşul olan bazı görevlerin tamamlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="afcbb-106">Before a Dynamics 365 Commerce channel can be created, several prerequisite tasks must be completed.</span></span> <span data-ttu-id="afcbb-107">Aşağıdaki önkoşul görevleri listeleri kanal türüne göre düzenlenmiştir.</span><span class="sxs-lookup"><span data-stu-id="afcbb-107">The following lists of prerequisite tasks are organized by channel type.</span></span>

> [!NOTE]
> <span data-ttu-id="afcbb-108">Bazı belgeler hala yazılıyor ve yeni içerik yayımlandıkça bağlantılar güncelleştirilecek.</span><span class="sxs-lookup"><span data-stu-id="afcbb-108">Some documentation is still being written, and links will be updated as new content is published.</span></span>

## <a name="initialization"></a><span data-ttu-id="afcbb-109">Başlatma</span><span class="sxs-lookup"><span data-stu-id="afcbb-109">Initialization</span></span>

- [<span data-ttu-id="afcbb-110">Çekirdek verileri başlatma</span><span class="sxs-lookup"><span data-stu-id="afcbb-110">Initialize seed data</span></span>](enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a><span data-ttu-id="afcbb-111">Tüm kanal türleri için gereken global önkoşullar</span><span class="sxs-lookup"><span data-stu-id="afcbb-111">Global prerequisities required for all channel types</span></span>

- [<span data-ttu-id="afcbb-112">Tüzel kişilik yapınızı tanımlama ve yapılandırma</span><span class="sxs-lookup"><span data-stu-id="afcbb-112">Define and configure your legal entity structure</span></span>](channels-legal-entities.md) 
- [<span data-ttu-id="afcbb-113">Organizasyon hiyerarşinizi yapılandırma</span><span class="sxs-lookup"><span data-stu-id="afcbb-113">Configure your organizational hierarchy</span></span>](channels-org-hierarchies.md)
- [<span data-ttu-id="afcbb-114">Ambar ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-114">Set up a warehouse</span></span>](channels-setup-warehouse.md)
- [<span data-ttu-id="afcbb-115">Satış vergisini yapılandırma</span><span class="sxs-lookup"><span data-stu-id="afcbb-115">Configure sales tax</span></span>](../finance/general-ledger/indirect-taxes-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="afcbb-116">E-posta bildirimi profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-116">Set up an email notification profile</span></span>](email-notification-profiles.md)
- [<span data-ttu-id="afcbb-117">Numara serileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-117">Set up number sequences</span></span>](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=/dynamics365/commerce/toc.json)
- [<span data-ttu-id="afcbb-118">Varsayılan müşteriyi ve adres defterini ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-118">Set up a default customer and address book</span></span>](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a><span data-ttu-id="afcbb-119">Perakende kanalı önkoşulları</span><span class="sxs-lookup"><span data-stu-id="afcbb-119">Retail channel prerequisites</span></span>

- [<span data-ttu-id="afcbb-120">Bilgi kodları ve bilgi kodu grupları</span><span class="sxs-lookup"><span data-stu-id="afcbb-120">Info codes and info code groups</span></span>](info-codes-retail.md)
- [<span data-ttu-id="afcbb-121">Perakende işlevselliği profili ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-121">Set up a retail functionality profile</span></span>](retail-functionality-profile.md)
- [<span data-ttu-id="afcbb-122">Çalışan adres defteri ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-122">Set up an employee address book</span></span>](new-address-book.md)
- [<span data-ttu-id="afcbb-123">Ekran düzeni ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-123">Set up a screen layout</span></span>](pos-screen-layouts.md)
- [<span data-ttu-id="afcbb-124">Donanım istasyonu ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-124">Set up a hardware station</span></span>](retail-hardware-station-configuration-installation.md)

## <a name="call-center-channel-prerequisites"></a><span data-ttu-id="afcbb-125">Çağrı Merkezi kanalı önkoşulları</span><span class="sxs-lookup"><span data-stu-id="afcbb-125">Call Center channel prerequisites</span></span>

- <span data-ttu-id="afcbb-126">Çağrı merkezi parametreleri</span><span class="sxs-lookup"><span data-stu-id="afcbb-126">Call center parameters</span></span>
- [<span data-ttu-id="afcbb-127">Çağrı merkezi sipariş ve iade ödeme yöntemleri</span><span class="sxs-lookup"><span data-stu-id="afcbb-127">Call center order and refund payment methods</span></span>](work-with-payments.md)
- [<span data-ttu-id="afcbb-128">Çağrı merkezi teslimat ve ücret modları</span><span class="sxs-lookup"><span data-stu-id="afcbb-128">Call center modes of delivery and charges</span></span>](configure-call-center-delivery.md)

## <a name="online-channel-prerequisites"></a><span data-ttu-id="afcbb-129">Çevrimiçi kanal önkoşulları</span><span class="sxs-lookup"><span data-stu-id="afcbb-129">Online channel prerequisites</span></span>

- [<span data-ttu-id="afcbb-130">Çevrimiçi işlevsellik profili oluşturma</span><span class="sxs-lookup"><span data-stu-id="afcbb-130">Create an online functionality profile</span></span>](online-functionality-profile.md)

## <a name="additional-resources"></a><span data-ttu-id="afcbb-131">Ek kaynaklar</span><span class="sxs-lookup"><span data-stu-id="afcbb-131">Additional resources</span></span>

[<span data-ttu-id="afcbb-132">Kanallara genel bakış</span><span class="sxs-lookup"><span data-stu-id="afcbb-132">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="afcbb-133">Kuruluşlar ve kuruluş hiyerarşilerine genel bakış</span><span class="sxs-lookup"><span data-stu-id="afcbb-133">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="afcbb-134">Kuruluş hiyerarşilerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-134">Set up organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="afcbb-135">Tüzel kişilik oluşturma</span><span class="sxs-lookup"><span data-stu-id="afcbb-135">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="afcbb-136">Perakende kanalını ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-136">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="afcbb-137">Çevrimiçi kanal ayarlama</span><span class="sxs-lookup"><span data-stu-id="afcbb-137">Set up an online channel</span></span>](channel-setup-online.md)
