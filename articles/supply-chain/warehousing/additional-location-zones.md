---
title: Ek yerleşim bölgeleri
description: Bu konu, Microsoft Dynamics 365 Supply Chain Management'a eklenen yeni bölge bölgelerinin genel görünümünü sağlar .
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocationBuild, WHSZone
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 4801077ac498699972244f3f86216790b517b47247fc7fb288614ec143c3c5cb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6762782"
---
# <a name="additional-location-zones"></a>Ek yerleşim bölgeleri

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management'ta üç yeni bölge alanı vardır. Ambar yöneticileri bunları ek ambar kuruluşları veya mizanpajları tanımlamak için kullanabilirler. Yeni bölge alanları el ile veya **konum kurulum** Sihirbazı kullanılarak ayarlanabilir. Bunlar, konumlar tablosunu kullanan herhangi bir sorgu veya filtre uygulama içinde kullanılabilirler.

Bölge alanlarını kullanmak için ek bir kurulum gerekmez.

## <a name="turn-on-the-additional-location-zone-feature"></a>Ek konum dilimi özelliğini aç

*İlave konum bölgesi* özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Ek konum bölgesi aç*

## <a name="use-location-zones"></a>Yerleşim bölgelerini kullan

1. **Ambar yönetimi \> Kurulum \> Ambar \> Konum kurulum sihirbazı**'na gidin.
2. Aşağıdaki değerleri ayarlayın:

    - **Ambar** alanında _62_'i seçin.
    - **Bölge kodu** alanında _ZEMİN_'i seçin.
    - **İlave Bölge 1** alanında _PICKZONE1_'i seçin.
    - **İlave Bölge 2** alanında _WEBSHOP1_'i seçin.
    - **Konum profil kimliği** alanında _ZEMİN_'i seçin.

3. **Zemin** satırını seçin.
4. **Gönderen numarası** alanına _1_ girin. **Kime numarası** alanına _3_ girin.
5. **Koridor** satırını seçin.
6. **Gönderen numarası** alanına _1_ girin. **Kime numarası** alanına _5_ girin.
7. **Oluştur**'u seçin.
8. Yeni konumların eklendiğini bildiren iletiler alırsınız. İletileri görüntülemek için **iletileri göster** düğmesini seçin.
9. **Ambar yönetimi \> Kurulum \> Ambar \> Konumlar** öğesine gidin. Yeni konumlar listede görünür ve tüm bölge alanları (yani, varolan bölge alanı ve yeni ek bölge alanları) kullanılabilir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]