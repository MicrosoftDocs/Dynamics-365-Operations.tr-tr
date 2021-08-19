---
title: Satıcı talep konfigürasyonları
description: Bu konu, yeni bir satıcı talebinde doldurulması gerekli olan alanları açıklar.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 98b759e5c5c918f14ca36bec93908d2f5eeb35044de77e3f450d79ead0993c16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6725710"
---
# <a name="vendor-request-configurations"></a>Satıcı talep konfigürasyonları
[!include [banner](../includes/banner.md)]

Bir satıcı talebini tamamlamak için satıcı ilgili kişisinin aday satıcı kayıt sihirbazını tamamlaması gerekir.

**Satıcı talebi yapılandırmaları** formunda, aday satıcı kayıt sihirbazında gerekli alanları ve görülebilir alanları belirten profiller oluşturabilirsiniz.

Satıcı kayıt sihirbazı, aday satısı kullanıcısına satıcının hangi ülkede/bölgede iş yaptığını sorarak başlar. Bu bilgi uygulanacak yapılandırmayı belirler. Ülke/bölge için özel bir yapılandırma tanımlanmamışsa, varsayılan yapılandırma kullanılır.

### <a name="set-up-a-vendor-request-configuration"></a>Satıcı talebi yapılandırması ayarlama

Varsayılan olarak, Satıcı talebi yapılandırmaları formunda bir satıcı yapılandırması bulunur.

Varsayılan yapılandırma için ülke/bölge seçilemez, bu nedenle **Ülke/bölge** bölümü değiştirilemez.

1. **Tedarik ve kaynak atama** > **Kurulum** > **Satıcılar**'a ve ardından **Satıcı talebi yapılandırmaları**'na tıklayın.
2. Listelenen alanların durumunu ayarlamak için **Alanlar** sekmesine tıklayın.
3. Gizli (Görünmez)
4. Görüntülenen (Görünür, ancak zorunlu değildir)
5. Gerekli (Görünür ve zorunlu)
6. Metnin sihirbazda görünüp görünmeyeceğini ve aday satıcı kullanıcısının sihirbazda sonraki adıma geçmek için kabul etmesi gereken bir onay olup olmayacağını belirlemek için **İçerik** sekmesine tıklayın. Onay, kullanıcının devam etmek için kabul etmesi gereken tüm hüküm ve koşullar için istenecektir.

Ayrıca, sihirbaz tamamlandığı zaman gösterilecek bir onay iletisi girebilir ve bir veya daha fazla soru formu ekleyebilirsiniz.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>Belirli bir ülke/bölge için satıcı yapılandırması oluşturma
1.  **Tedarik ve kaynak atama** > **Kurulum** > **Satıcılar**'a ve ardından **Satıcı talebi yapılandırmaları**'na tıklayın.
2.  Yeni bir yapılandırma oluşturmak için **Yeni**'ye tıklayın ve yapılandırma için bir ad girin.
3.  **Kaydet**'e tıklayın.
4.  Yapılandırmanın kullanılacağı ülkeyi/bölgeyi seçmek için **Ülke/bölgeler** sekmesini açın.
5.  Varsayılan yapılandırma talimatlarını izleyerek yapılandırmayı tamamlayın.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]