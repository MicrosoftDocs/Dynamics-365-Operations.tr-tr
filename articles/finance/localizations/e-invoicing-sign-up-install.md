---
title: Elektronik Faturalama hizmetine kaydolup yükleyin
description: Bu makalede, Elektronik Faturalama hizmetine kaydolma ve hizmeti kurmayla ilgili bilgiler yer almaktadır.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283972"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Elektronik Faturalama hizmetine kaydolup yükleyin

[!include [banner](../includes/banner.md)]

Bu makalede, Elektronik Faturalama hizmetine kaydolma ve hizmeti kurmayla ilgili bilgiler yer almaktadır. Bu işlem için dört adım vardır. 1 ile 3 arasındaki adımlar gereklidir ve adım 4 isteğe bağlıdır.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>Adım 1: Regulatory Configuration Service'e kaydolun

Regulatory Configuration Service (RCS), Elektronik faturalamayı yapılandırmak için kullanılan yapılandırma ve tasarım deneyimini sağlar. Ortamlar ve elektronik faturalama özellikleri gibi kaynaklar RCS'de oluşturulur, sürdürülür ve yönetilir. Kaynaklar hazır olduğunda, Elektronik Faturalama hizmetine yayınlanırlar.

RCS hakkında daha fazla bilgi için bkz. [Regulatory Configuration Services (RCS) - Globalleştirme özellikleri](rcs-globalization-feature.md).

RCS'ye kaydolmak için [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/) sayfasına gidin.

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Adım 2: Microsoft Dynamics Lifecycle Services'te mikro hizmetler eklentisini yükleme

Elektronik Faturalama hizmeti, Microsoft veri merkezlerinde barındırılan bir mikro hizmetler kümesidir. Varsayılan olarak, Dynamics 365 Finance ve Dynamics 365 Supply Chain Management müşterilerinin Elektronik Faturalama hizmetine erişimi yoktur. Bunu, Microsoft Dynamics Lifecycle Services'a (LCS) eklenti olarak kurmanız gerekir. Eklentiyi yüklediğinizde, Finance veya Supply Chain Management ortamınız Elektronik faturalama hizmetine bağlanmasına izin verilen uygulamaların kaydına kaydedilir.

Bu adımı tamamlamak için bkz. [Lifecycle Services'te mikro hizmetler eklentisini yükleme](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>Adım 3: RCS 'yi kurun

RCS ve Elektronik Faturalama hizmeti arasındaki tümleştirmeyi kurmanız gerekir. Ana bileşenleri de ayarlamanız gerekir.

Bu adımı tamamlamak için, bkz. [Regulatory Configuration Service'i (RCS) kurma](e-invoicing-set-up-rcs.md).

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Adım 4: Microsoft Power Platform eklentisi yönetici referansı

Bazı senaryolar, Microsoft Power Platform kapsamında Dataverse tümleştirmesi gerektirir.

Endonezya elektronik faturalama senaryoları için Elektronik faturalama çözümleri kullanıyorsanız, bu ayar zorunludur. Ancak, Suudi Arabistan elektronik faturalama senaryoları için isteğe bağlıdır. Daha fazla bilgi için, [Ülke veya bölgeye göre Elektronik faturalama özelliklerinin kullanılabilirliği](e-invoicing-country-specific-availability.md) konusuna bakın.

Bu adımı tamamlamak için, bkz. [Microsoft Power Platform eklentisi yönetici referansı](e-invoicing-power-platform-plug-in.md).
