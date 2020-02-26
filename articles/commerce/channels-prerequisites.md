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
# <a name="channel-setup-prerequisites"></a>Kanal kurulum önkoşulları


[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce'te kanal kurulum önkoşulları hakkında genel bilgi vermektedir.

## <a name="overview"></a>Genel Bakış

Bir Dynamics 365 Commerce kanalı oluşturulmadan önce, önkoşul olan bazı görevlerin tamamlanması gerekir. Aşağıdaki önkoşul görevleri listeleri kanal türüne göre düzenlenmiştir.

> [!NOTE]
> Bazı belgeler hala yazılıyor ve yeni içerik yayımlandıkça bağlantılar güncelleştirilecek.

## <a name="initialization"></a>Başlatma

- [Çekirdek verileri başlatma](../retail/enable-configure-retail-functionality.md)

## <a name="global-prerequisities-required-for-all-channel-types"></a>Tüm kanal türleri için gereken global önkoşullar

- [Tüzel kişilik yapınızı tanımlama ve yapılandırma](channels-legal-entities.md) 
- [Organizasyon hiyerarşinizi yapılandırma](channels-org-hierarchies.md)
- [Ambar ayarlama](channels-setup-warehouse.md)
- [Satış vergisini yapılandırma](https://docs.microsoft.com/en-us/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json)
- [E-posta bildirimi profili ayarlama](email-notification-profiles.md)
- [Numara serileri ayarlama](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview?toc=/dynamics365/commerce/toc.json)
- [Varsayılan müşteriyi ve adres defterini ayarlama](default-customer.md)
<!--
- [Configure commerce parameters](commerce-parameters.md)
-->

## <a name="retail-channel-prerequisites"></a>Perakende kanalı önkoşulları

- [Bilgi kodları ve bilgi kodu grupları](https://docs.microsoft.com/en-us/dynamics365/retail/info-codes-retail?toc=/dynamics365/commerce/toc.json)
- [Perakende işlevselliği profili ayarlama](retail-functionality-profile.md)
- [Çalışan adres defteri ayarlama](new-address-book.md)
- [Ekran düzeni ayarlama](https://docs.microsoft.com/en-us/dynamics365/retail/pos-screen-layouts?toc=/dynamics365/commerce/toc.json)
- [Donanım istasyonu ayarlama](https://docs.microsoft.com/en-us/dynamics365/retail/retail-hardware-station-configuration-installation?toc=/dynamics365/commerce/toc.json)

## <a name="call-center-channel-prerequisites"></a>Çağrı Merkezi kanalı önkoşulları

- Çağrı merkezi parametreleri
- Çağrı merkezi para iadesi yöntemleri
- Kiralama türleri
- Ödeme hizmetleri
- Sipariş tutma kodları

## <a name="online-channel-prerequisites"></a>Çevrimiçi kanal önkoşulları

- [Çevrimiçi işlevsellik profili oluşturma](online-functionality-profile.md)

## <a name="additional-resources"></a>Ek kaynaklar

[Kanallara genel bakış](channels-overview.md)

[Kuruluşlar ve kuruluş hiyerarşilerine genel bakış](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Kuruluş hiyerarşilerini ayarlama](channels-org-hierarchies.md)

[Tüzel kişilik oluşturma](channels-legal-entities.md)

[Perakende kanalını ayarlama](channel-setup-retail.md)
    
[Çevrimiçi kanal ayarlama](channel-setup-online.md)
