---
title: Vergi hizmetine erişilemedi
description: Bu konuda, Vergi Hesaplama hizmetine erişim sorununu giderme açıklanmaktadır.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 48a75cd0c1d91c3b3d9c3fb2e6cab93a76756532
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388573"
---
# <a name="failed-to-access-tax-service"></a>Vergi hizmetine erişilemedi

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Bu konu, Vergi Hesaplama hizmetinin "Vergi hizmetine erişilemedi" hatasının nasıl düzeltileceğini açıklamaktadır.

## <a name="symptoms"></a>Belirtiler

Microsoft Dynamics 365 Finance'te, **Vergi** \> **Kurulum** \> **Vergi yapılandırması** \> **Vergi hizmet parametreleri**'ne gidin. **Genel** sekmesinde, **Vergi hesaplamasını etkinleştir** seçeneğini etkinleştirin. Daha sonra **Özellik kurulum adı** alanında bir değer seçmeyi denerseniz, bir hata oluşur. Hata iletisinde, "Vergi hizmetine erişilemedi" yazar.

## <a name="cause"></a>Nedeni

Bu hata, Finance'in Vergi Hesaplama hizmetine erişememesi nedeniyle oluşur.

## <a name="resolution"></a>Çözüm 

1. Microsoft Dynamics Lifecycle Services (LCS)'de oturum açın.
2. **Ortam** sayfasında, **Ortam eklentileri** sekmesinde **Vergi Hesaplaması** öğesini bulun ve durumunu inceleyin. Durum, **Yükleniyor** veya **Yüklendi** olmalıdır. Vergi Hesaplama servisi eklentisi yüklü değilse, hatayı alırsınız.

## <a name="mitigation"></a>Risk azaltma

1. LCS'deki **Finance** sayfasında, **Power Platform tümleştirmesi** bölümünde, **Yeni eklenti yükle**'yi seçin.
2. Sayfanın en altına gidin ve bunu yüklemek için **Vergi Hesaplama** eklentisini seçin.
3. Finance ortamınıza dönün ve Vergi Hesaplama servisine erişmeyi deneyin.

> [!NOTE]
> Vergi Hesaplama servisini yüklemeden önce [Vergi Hesaplama servis önkoşullarını](global-get-started-with-tax-calculation-service.md#prerequisites) gözden geçirin.
> 
> **Power Platform tümleştirmesi** bölümü kullanılamadığından eklentiyi yükleyemiyorsanız [Eklentiye genel bakış](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) konusuna bakın. Eklentiyi yükledikten sonra yine de hata yaşarsanız, sistem yöneticinize başvurun.
