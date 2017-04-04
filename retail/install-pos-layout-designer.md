---
title: "Perakende POS düzeni tasarımcısını yükleme"
description: "Tek işlemli tasarımcıyı mağazalar, kayıtlar, kasiyerler ve yöneticiler için Yatay modda veya Dikey Modda farklı Perakende Modern POS (MPOS) ve Bulut POS düzenleri tasarlamak için kullanabilirsiniz."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b33cbf67c00b6baea4393e82d19300085781af29
ms.lasthandoff: 03/31/2017


---

# <a name="install-the-retail-pos-layout-designer"></a>Perakende POS düzeni tasarımcısını yükleme

Tek işlemli tasarımcıyı mağazalar, kayıtlar, kasiyerler ve yöneticiler için Yatay modda veya Dikey Modda farklı Perakende Modern POS (MPOS) ve Bulut POS düzenleri tasarlamak için kullanabilirsiniz.

MPOS veya Bulut POS için grafik tasarım arabirimi kasa düzeni tarafından kontrol edilir. Düzen, çeşitli nesnelerin konumunu kontrol eder. Toplam düzen, madde grubu düzeni, müşteri düzeni, ödeme düzeni ve çeşitli menü düğmeleri düzeni örnek olarak verilebilir. Düzenler ayrıca çalışanlara sunulan satış arabiriminin genel görünümünü de içerir.

## <a name="install-the-oneclick-designer"></a>Oneclick Tasarımcısı'nı yükleme
1.  Gitmek için sol üst köşedeki işlemleri için Microsoft Dynamics 365 içinde menüsünü kullanın **perakende****ve ticaret**&gt;**kanal Kurulumu**&gt;**POS Kurulumu**&gt;**POS**&gt;**ekran düzenleri**.
2.  **Windows için Modern POS** veya **Bulut POS** uygulama türü olan herhangi bir düzeni seçin **Düzen tasarımcısı**'na tıklayın.
3.  Internet Explorer penceresinin altında beliren bildirim çubuğunda, tek işlemli tasarımcıyı yüklemeye başlamak için **Aç** öğesine tıklayın. (Bildirim çubuğu diğer tarayıcılarda farklı bir yerde görünebilir.)
4.  Beliren **Uygulama Çalıştırma - Güvenlik Uyarısı** iletişim kutusunda Perakende tasarımcısı ana bilgisayarını yüklemek için**Çalıştır **öğesine tıklayın. İlerleme göstergesi, yüklemenin ilerleyişini gösterir.
5.  Yükleme tamamlandıktan sonra, tasarımcıyı başlatmak için **Oturum aç** sayfasında Microsoft Dynamics 365 for Operations kullanıcı adınızı ve parolanızı girin ve ardından **Oturum aç** tuşuna tıklayın.
6.  Bilgileriniz doğrulandıktan ve tasarımcı başlatıldıktan sonra, kendi düzeninizi tasarlayabilir veya mevcut bir düzeni değiştirebilirsiniz. [![Tek tıklatmayla Tasarımcısı düzeni](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Düzen tasarımcının yüklenmesi ile ilgili sorunları giderme
-   **Tasarımcı**'ya tıkladığınızda yükleyiciyi indirme (veya çalıştırma) komut istemi belirmez veya geçerli güvenlik ayarlarınız dosyayı indirmenize izin vermez. **Çözümler:**
    -   Internet Explorer'da bu site için açılır pencere engelleyicisinin devre dışı bırakıldığından emin olun. ' I **ayarları**&gt;**seçenekleri**&gt;**gizlilik**&gt;**açılır pencere engelleyicisi bulmak**ve bir değişiklik olursa ayarını değiştirin.
    -   Internet Explorer'da, Dynamics 365 for Operations URL'sini güvenilen siteler listenize ekleyin. ' I **ayarları**&gt;**seçenekleri**&gt;**güvenlik**&gt;**Güvenilen siteler**&gt;**siteleri**&gt;**Ekle**.
-   Program başlamıyor ve satıcıyla iletişim kurmanız talimatı verildi. **Çözüm:** Internet Explorer'da, Dynamics 365 for Operations URL'sini güvenilen siteler listenize ekleyin. ' I **ayarı**&gt;**seçenekleri**&gt;**güvenlik**&gt;**Güvenilen siteler**&gt;**siteleri**&gt;**Ekle**.

**Bilinen sorun:** Tasarımcı Google Chrome ve Mozilla Firefox tarayıcılarında düzgün çalışmıyor. Bu sorunu düzeltmek için çalışıyoruz.

<a name="see-also"></a>Ayrıca bkz.
--------

[Perakende Modern POS'u yapılandırma, indirme, yükleme ve etkinleştirme](retail-modern-pos-device-activation.md)


