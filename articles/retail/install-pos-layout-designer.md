---
title: "Retail satış noktası (POS) düzeni tasarımcısını yükleme"
description: "Tek işlemli tasarımcıyı mağazalar, kayıtlar, kasiyerler ve yöneticiler için Yatay modda veya Dikey Modda farklı Perakende Modern POS (MPOS) ve Bulut POS düzenleri tasarlamak için kullanabilirsiniz."
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 4c647f49101dcbbe7dd1feac2dd9aad5c6dd5bcc
ms.contentlocale: tr-tr
ms.lasthandoff: 08/09/2018

---

# <a name="install-the-retail-point-of-sale-pos-layout-designer"></a>Retail satış noktası (POS) düzeni tasarımcısını yükleme

[!include [banner](includes/banner.md)]

Tek işlemli tasarımcıyı mağazalar, kayıtlar, kasiyerler ve yöneticiler için Yatay modda veya Dikey Modda farklı Perakende Modern POS (MPOS) ve Bulut POS düzenleri tasarlamak için kullanabilirsiniz.

MPOS veya Bulut POS için grafik tasarım arabirimi kasa düzeni tarafından kontrol edilir. Düzen, çeşitli nesnelerin konumunu kontrol eder. Toplam düzen, madde grubu düzeni, müşteri düzeni, ödeme düzeni ve çeşitli menü düğmeleri düzeni örnek olarak verilebilir. Düzenler ayrıca çalışanlara sunulan satış arabiriminin genel görünümünü de içerir.

## <a name="install-the-one-click-designer"></a>Tek işlemli tasarımcıyı yükleme
1.  Microsoft Dynamics 365 for Retail'da **Perakende** **ve ticaret** &gt; **Kanal kurulumu** &gt; **POS kurulumu** &gt; **POS** &gt; **Ekran düzenleri**'ne gitmek için sol üstteki menüyü kullan.
2.  **Windows için Modern POS** veya **Bulut POS** uygulama türü olan herhangi bir düzeni seçin **Düzen tasarımcısı**'na tıklayın.
3.  Internet Explorer penceresinin altında beliren bildirim çubuğunda, tek işlemli tasarımcıyı yüklemeye başlamak için **Aç** öğesine tıklayın. (Bildirim çubuğu diğer tarayıcılarda farklı bir yerde görünebilir.)
4.  Beliren **Uygulama Çalıştırma - Güvenlik Uyarısı** iletişim kutusunda Perakende tasarımcısı ana bilgisayarını yüklemek için **Çalıştır** öğesine tıklayın. İlerleme göstergesi, yüklemenin ilerleyişini gösterir.
5.  Yükleme tamamlandıktan sonra, tasarımcıyı başlatmak için **Oturum aç** sayfasında Microsoft Dynamics 365 for Retail kullanıcı adınızı ve parolanızı girin ve ardından **Oturum aç** tuşuna tıklayın.
6.  Bilgileriniz doğrulandıktan ve tasarımcı başlatıldıktan sonra, kendi düzeninizi tasarlayabilir veya mevcut bir düzeni değiştirebilirsiniz. [![Tek işlemli tasarımcıda düzen](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Düzen tasarımcının yüklenmesi ile ilgili sorunları giderme
-   **Tasarımcı**'ya tıkladığınızda yükleyiciyi indirme (veya çalıştırma) komut istemi belirmez veya geçerli güvenlik ayarlarınız dosyayı indirmenize izin vermez. **Çözümler:**
    -   Internet Explorer'da bu site için açılır pencere engelleyicisinin devre dışı bırakıldığından emin olun. **Ayarlar** &gt; **Seçenekler** &gt; **Gizlilik** &gt; **Açılır Pencere Engelleyicisini Bul**'a tıklayın ve değişiklik gerekiyorsa ayarı değiştirin.
    -   Internet Explorer'da, Dynamics 365 for Retail URL'sini güvenilen siteler listenize ekleyin. **Ayarlar** &gt; **Seçenekler** &gt; **Güvenlik** &gt; **Güvenilen siteler** &gt; **Siteler** &gt; **Ekle**'yi tıklayın.
-   Program başlamıyor ve satıcıyla iletişim kurmanız talimatı verildi. **Çözüm:** Internet Explorer'da, Dynamics 365 for Retail URL'sini güvenilen siteler listenize ekleyin. **Ayarlar** &gt; **Seçenekler** &gt; **Güvenlik** &gt; **Güvenilen siteler** &gt; **Siteler** &gt; **Ekle**'yi tıklatın.

**Bilinen sorun:** Tasarımcı Google Chrome ve Mozilla Firefox tarayıcılarında düzgün çalışmıyor. Bu sorunu düzeltmek için çalışıyoruz.

<a name="additional-resources"></a>Ek kaynaklar
--------

[Perakende Modern POS'u yapılandırma, indirme, yükleme ve etkinleştirme](retail-modern-pos-device-activation.md)




