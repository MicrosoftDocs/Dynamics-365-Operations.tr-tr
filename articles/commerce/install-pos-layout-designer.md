---
title: POS Düzeni tasarımcısını yükleme
description: Tek işlemli tasarımcıyı mağazalar, kayıtlar, kasiyerler ve yöneticiler için Yatay modda veya Dikey Modda farklı Modern POS (MPOS) ve Bulut POS düzenleri tasarlamak için kullanabilirsiniz.
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f9882ae895de926e0da3579ab65a988f2b97f7be
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024394"
---
# <a name="install-the-pos-layout-designer"></a>POS Düzeni tasarımcısını yükleme

[!include [banner](includes/banner.md)]

Tek işlemli tasarımcıyı mağazalar, kayıtlar, kasiyerler ve yöneticiler için Yatay modda veya Dikey Modda farklı Modern POS (MPOS) ve Bulut POS düzenleri tasarlamak için kullanabilirsiniz.

MPOS veya Bulut POS için grafik tasarım arabirimi kasa düzeni tarafından kontrol edilir. Düzen, çeşitli nesnelerin konumunu kontrol eder. Toplam düzen, madde grubu düzeni, müşteri düzeni, ödeme düzeni ve çeşitli menü düğmeleri düzeni örnek olarak verilebilir. Düzenler ayrıca çalışanlara sunulan satış arabiriminin genel görünümünü de içerir.

## <a name="install-the-one-click-designer"></a>Tek işlemli tasarımcıyı yükleme

1. Commerce bölümünde **Retail ve Commerce** &gt; **Kanal ayarı** &gt; **POS ayarı** &gt; **POS** &gt; **Ekran düzenleri**'ne gitmek için sol üst kısımdaki menüyü kullanın.
2. **Windows için Modern POS** veya **Bulut POS** uygulama türü olan herhangi bir düzeni seçin **Düzen tasarımcısı**'na tıklayın.
3. Internet Explorer penceresinin altında beliren bildirim çubuğunda, tek işlemli tasarımcıyı yüklemeye başlamak için **Aç** öğesine tıklayın. (Bildirim çubuğu diğer tarayıcılarda farklı bir yerde görünebilir.)
4. Beliren **Uygulama Çalıştırma - Güvenlik Uyarısı** iletişim kutusunda Perakende tasarımcısı ana bilgisayarını yüklemek için **Çalıştır** öğesine tıklayın. İlerleme göstergesi, yüklemenin ilerleyişini gösterir.
5. Kurulum tamamlandıktan sonra tasarımcıyı başlatmak için **Oturum açma** sayfasında Commerce kullanıcı adınızı ve parolanızı girdikten sonra **Oturum aç**'a tıklayın.
6. Bilgileriniz doğrulandıktan ve tasarımcı başlatıldıktan sonra, kendi düzeninizi tasarlayabilir veya mevcut bir düzeni değiştirebilirsiniz.

    [![Tek işlemli tasarımcıda düzen](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Düzen tasarımcının yüklenmesi ile ilgili sorunları giderme

- **Tasarımcı**'ya tıkladığınızda yükleyiciyi indirme (veya çalıştırma) komut istemi belirmez veya geçerli güvenlik ayarlarınız dosyayı indirmenize izin vermez. 

    **Çözümler:**

    - Internet Explorer'da bu site için açılır pencere engelleyicisinin devre dışı bırakıldığından emin olun. **Ayarlar** &gt; **Seçenekler** &gt; **Gizlilik** &gt; **Açılır Pencere Engelleyicisini Bul**'a tıklayın ve değişiklik gerekiyorsa ayarı değiştirin.
    - Internet Explorer'da Commerce URL'sini güvenilir sitelerinize ekleyin. **Ayarlar** &gt; **Seçenekler** &gt; **Güvenlik** &gt; **Güvenilen siteler** &gt; **Siteler** &gt; **Ekle**'yi tıklayın.

- Program başlamıyor ve satıcıyla iletişim kurmanız talimatı verildi.

    **Çözüm:** Internet Explorer'da Commerce URL'sini güvenilir sitelerinize ekleyin. **Ayarlar** &gt; **Seçenekler** &gt; **Güvenlik** &gt; **Güvenilen siteler** &gt; **Siteler** &gt; **Ekle**'yi tıklatın.

**Bilinen sorun:** Tasarımcı Google Chrome ve Mozilla Firefox tarayıcılarında düzgün çalışmıyor. Bu sorunu düzeltmek için çalışıyoruz.

## <a name="additional-resources"></a>Ek kaynaklar

[Retail Modern POS (MPOS) yapılandırın, yükleyin ve etkinleştirin](retail-modern-pos-device-activation.md)
