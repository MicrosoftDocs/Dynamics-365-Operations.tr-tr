---
title: Çevrimiçi işlevsellik profili oluştur
description: Bu konuda, Microsoft Dynamics 365 Commerce'ta bir çevrimiçi işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.
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
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4416548"
---
# <a name="create-an-online-functionality-profile"></a>Çevrimiçi işlevsellik profili oluştur


[!include [banner](includes/banner.md)]

Bu konu, Microsoft Dynamics 365 Commerce için bir çevrimiçi işlevsellik profili kurma işleminin genel görünümünü sunmaktadır.

## <a name="overview"></a>Genel Bakış

Çevrimiçi işlevsellik profili, çevrimiçi kanallarda çeşitli ayarlar sağlar. Her bir çevrimiçi kanalın bir çevrimiçi işlevsellik profili belirtmesi gerekir.

## <a name="create-an-online-functionality-profile"></a>Çevrimiçi işlevsellik profili oluştur

Aşağıdaki yordamda, Commerce Headquarters uygulaması içinden bir çevrimiçi işlevsellik profilinin nasıl oluşturulacağı açıklanmaktadır.

1. Gezinti bölmesinde **modüller \> Kanal kurulumu \> çevrimiçi mağaza kurulumu \> işlevsellik profillerine** gidin.
1. Eylem bölmesinde **Yeni**'yi seçin.
1. **Profil** alanına profil için bir kod girin.
1. **Açıklama** alanına, aşağıdaki örnek görüntüye bir değer ("Adventure Works profili") girin.
1. **İşlevler** bölümünde, **alışveriş sepetini**, **perakende müşterileri** veya **kullanıma alma** ayarlarını gerektiği gibi değiştirin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

Aşağıdaki resimde örnek bir çevrimiçi işlevsellik profili gösterilmektedir.
  
![Çevrimiçi işlev profili örneği](media/online-functionality-profile.png)

## <a name="functions"></a>İşlevler

- **Toplu ürünler**: etkinleştirildiğinde, bu işlev sepetin aynı madde birden çok kez eklendiğinde miktarın güncelleştirilmesini sağlar.
- **Ödemeyle kullanıma alma işlemine izin ver**: etkinleştirildiğinde, alışveriş sepetine eklenen maddelerin fiyat $0,00 olduğunda bu işlev senaryoyu işler.
- **Müşteriyi zaman uyumsuz modda oluştur**: Bu üçüncü taraf e-ticaret kanallarına uygulanabilen eski bir ayardır ve Dynamics 365 e-ticaret sitesine uygulanamaz.

## <a name="additional-resources"></a>Ek kaynaklar

[Kanallara genel bakış](channels-overview.md)

[Kanal ayarlama önkoşulları](channels-prerequisites.md)

[Çevrimiçi kanal ayarlama](channel-setup-online.md)

[Perakende kanalını ayarlama](channel-setup-retail.md)

[Çağrı merkezi kanalını ayarlama](channel-setup-callcenter.md)
