---
title: Toplu işlerden giden sevkiyatları onayla
description: Bu makalede, kullanıma hazır yüklemeler için giden transfer emri sevkiyatlarını otomatik olarak doğrulayan bir toplu işin nasıl ayarlanacağı açıklanmaktadır.
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
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875115"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Toplu işlerden giden sevkiyatları onayla

[!include [banner](../includes/banner.md)]

Bu makalede, kullanıma hazır yüklemeler için giden transfer emri sevkiyatlarını otomatik olarak doğrulayan bir toplu işin nasıl ayarlanacağı açıklanmaktadır. Burada açıklanan toplu iş, satış siparişlerine değil, yalnızca transfer emri sevkıyatları için geçerlidir.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>Toplu işlerden giden sevkiyatları onaylama özelliğini açma veya kapatma

Bu makalede açıklanan işlevi kullanmak için *Toplu işlerden giden sevkiyatları onayla* özelliğinin sisteminizde etkinleştirilmiş olması gerekir. Supply Chain Management sürüm 10.0.21 itibariyle, bu özellik varsayılan olarak açıktır. Supply Chain Management 10.0.25 itibarıyla, bu özellik zorunludur ve kapatılamaz. 10.0.25 sürümünden daha eski bir sürümü çalıştırıyorsanız, yöneticiler [Özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) çalışma alanında *Toplu işlerden giden sevkiyatları onayla* özelliğini aratarak bu işlevi açabilir veya kapatabilir.

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