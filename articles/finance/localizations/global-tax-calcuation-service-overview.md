---
title: Vergi Hesaplama (Önizleme)
description: Bu konu, Vergi Hesaplama özelliğinin tüm kapsamını ve özelliklerini açıklar.
author: wangchen
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e01247cddad4201760fd56e00e05a8373a1ca6ef7c26ae5e1f5cca63bd8a456
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775106"
---
# <a name="tax-calculation-preview"></a>Vergi Hesaplama (Önizleme)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Vergi Hesaplama, Global Tax Engine'in vergi belirleme ve hesaplama sürecini otomatikleştirmesini ve basitleştirmesini sağlayan, aşırı ölçeklenebilir çok kiracılı bir servistir. Tax Engine tam olarak konfigüre edilebilir. Konfigüre edilebilecek öğeler vergilendirilebilir veri modeli, vergi kodu, vergi uygulanabilirlik matrisi ve vergi hesaplama formülü ile sınırlı değildir. Tax Engine Microsoft Azure çekirdek hizmetler platformunda çalışır ve modern teknoloji ve artan ölçeklenebilirlik sunar.

Vergi Hesaplama hizmeti Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile tümleşir. Sonuç olarak, Dynamics 365 Project Operations, Dynamics 365 Commerce ve diğer birinci taraf ile üçüncü taraf uygulamaları ile de bütünleşir.

> [!IMPORTANT]
> Vergi Hesaplama hizmetini etkinleştirdiğinizde, ilgili veriler üzerinde bazı işlemler servis verilerinizi barındıran veri merkezinden farklı bir veri merkezinde gerçekleştirilebilir. Vergi Hesaplama servisini etkinleştirmeden önce [Hükümler ve Koşullar](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md)'ı gözden geçirin. Gizliliğiniz bizim için önemlidir. Daha fazla bilgi için [Gizlilik Bildirimimizi](https://go.microsoft.com/fwlink/?LinkId=521839) okuyun.

Vergi Hesaplama, artan ölçeklenebilirlik sağlayan mikro hizmet tabanlı bir vergi altyapısıdır. Aşağıdaki görevleri yerine getirmenize yardımcı olur:

- Vergi Hesaplama'yı Regulatory Configuration Service (RCS) aracılığıyla yapılandırın. RCS, elektronik raporlama (ER) tasarımcısının gelişmiş bir sürümüdür ve bağımsız bir hizmet olarak edinilebilir.
- Vergi kodlarının ve oranlarının otomatik olarak belirlenmesi için vergi matrisini yapılandırma.
- Vergi kayıt numarasının otomatik olarak belirlenmesi için vergi matrisini yapılandırma.
- Formül ve koşulları tanımlamak için vergi hesaplama tasarımcısını yapılandırma.
- Vergi belirleme ve hesaplama çözümünü tüzel kişilerle paylaşma.

Vergi hesaplama hizmetini kullanmak için, Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden vergi hesaplama servisi eklentisini yükleyin. Sonra, RCS'deki kurulumu tamamlayın ve Finance ve Supply Chain Management vergi hesaplama hizmetini etkinleştirin. Daha fazla bilgi için bkz. [Vergi hizmetini kullanmaya başlama](./global-get-started-with-tax-calculation-service.md).

## <a name="availability"></a>Kullanılabilirlik

Vergi Hesaplama, yalnızca korumalı alan ortamlarında ve seçili müşteriler için bir genel önizleme programı aracılığıyla kullanılabilir. Sonuç olarak, tüm müşteriler ve üretim ortamlarında genellikle kullanılabilir olacaktır.

Yeni özellikler sunulmaya devam edilmektedir. Bu nedenle, desteklenen özelliklerin kapsam bilgilerini öğrenmek için en güncel belgeleri kontrol edin.

Vergi Hesaplama aşağıdaki Azure bölgelerinde dağıtılır. Ayrıca, müşteri gereksinimlerine göre daha fazla Azure bölgesinde kullanılacak şekilde dağıtılacaktır.

- Amerika Birleşik Devletleri
- Avrupa

> [!NOTE]
> Vergi Hesaplama, Dynamics 365 şirket içi dağıtımlarını desteklemez. Ayrıca Dynamics AX 2012 gibi önceki sürümleri de desteklemez.

## <a name="feature-highlights"></a>Özellikle ilgili önemli noktalar

- Vergiyi otomatik olarak belirlemek ve hesaplamak için yapılandırılabilir vergi matrisi
- Çoklu vergisi kayıt numarası desteği
- Vergi belirleme ve hesaplama için transfer emri desteği
- Çoklu vergi kayıt numaralarının belirlenmesi için transfer emri desteği

## <a name="supported-transactions"></a>Desteklenen işlemler

Vergi Hesaplama tüzel kişilik ve işlem tarafından etkinleştirilebilir. Aşağıdaki işlemler desteklenir:

- Satış işlemi

    - Satış teklifi
    - Satış siparişi
    - Onay
    - Malzeme çekme listesi
    - Sevk irsaliyesi
    - Satış faturası
    - Alacak dekontu
    - Sipariş iadesi
    - Başlık sair masrafları
    - Satır sair masrafları

- Satın alma işlemi

    - Satın alma siparişi
    - Onay
    - Giriş listesi
    - Ürün girişi
    - Satınalma faturası
    - Başlık sair masrafları
    - Satır sair masrafları
    - Alacak dekontu
    - Sipariş iadesi
    - Satınalma talebi
    - Satın alma talebi satır sair masrafı
    - Teklif talebi
    - Teklif talebi başlık sair masrafı
    - Teklif talebi satır sair masrafı

- Stok işlemi

    - Transfer emri - sevk
    - Transfer emri - al

## <a name="related-resources"></a>İlgili kaynaklar

[Vergi hizmetini kullanmaya başlama](./global-get-started-with-tax-calculation-service.md)

[Çoklu KDV kayıt numarası](./emea-multiple-vat-registration-numbers.md)

[Transfer emri için vergi özelliği desteği](./tasks/tax-feature-support-for-transfer-order.md)

[Vergi hizmetinde uzantı oluşturma](./tax-service-add-data-fields-tax-integration-by-extension.md)
