---
title: Toplu işlerden giden sevkiyatları onayla
description: Bu konuda, kullanıma hazır yüklemeler için giden transfer emri sevkiyatlarını otomatik olarak doğrulayan bir toplu işin nasıl ayarlanacağı açıklanmaktadır.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 69e61e1c04dd72efbe1d2f028c078100e07176f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838454"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Toplu işlerden giden sevkiyatları onayla

[!include [banner](../includes/banner.md)]

Bu konuda, kullanıma hazır yüklemeler için giden transfer emri sevkiyatlarını otomatik olarak doğrulayan bir toplu işin nasıl ayarlanacağı açıklanmaktadır. Burada açıklanan toplu iş, satış siparişlerine değil, yalnızca transfer emri sevkıyatları için geçerlidir.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Toplu işlerden giden sevkiyatları onaylama özelliğini etkinleştirme

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve gerekirse etkinleştirmek için [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sayfasını kullanabilir. Özellik şu şekilde listelenmiştir:

- **Modül**  - *Ambar yönetimi*
- **Özellik adı** - *Toplu işlerden giden sevkiyatları onaylama*

## <a name="process-outbound-shipments"></a>Giden sevkiyatları işle

Sevk edilmeye hazır olan yüklemeler için giden sevkiyat onayını çalıştırmak üzere planlanan bir toplu iş ayarlamak için:

1. **Ambar yönetimi \> Periyodik görevler\> Giden sevkiyatları işle**'ye gidin.
1. **Sevkiyatı Onayla** iletişim kutusu açılır. **Eklenecek kayıtlar** hızlı sekmesinde **Filtrele**'yi seçin.
1. Sorgu düzenleyicisi iletişim kutusu açılır. **Aralık** sekmesinde, aşağıdaki değerlere sahip bir satır ekleyin:
    - **Tablo** - *Yükler*
    - **Türetilmiş tablo** - *Yükler*
    - **Alan** - *Yük durumu*
    - **Kriter** - *Yüklü*
1. **Sevkiyatı Onayla** iletişim kutusuna dönmek için **Tamam**'ı seçin.
1. **Arka planda çalıştır** hızlı sekmesinde, **Toplu işleme** öğesini **Evet** olarak ayarlayın.
1. **Arka planda çalıştır** sekmesinde **Tekrar**'ı seçin.
1. **Yinelemeyi tanımlayın** iletişim kutusu açılır. İşletmeniz için gereken çalışma zamanlamasını ayarlayın.
1. **Sevkiyatı Onayla** iletişim kutusuna dönmek için **Tamam**'ı seçin.
1. Toplu işi toplu iş kuyruğuna eklemek için **Sevkiyatı onayla** iletişim kutusunda **Tamam**'ı seçin.

Daha fazla bilgi için bkz. [Toplu işlemeye genel bakış](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]