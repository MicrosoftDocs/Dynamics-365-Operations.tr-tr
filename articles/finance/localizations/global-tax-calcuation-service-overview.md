---
title: Vergi hesaplama hizmeti (Önizleme)
description: Bu konu, vergi hesaplama servisinin tüm kapsamını ve özelliklerini açıklar.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818236"
---
# <a name="tax-calculation-service-preview"></a>Vergi hesaplama hizmeti (Önizleme)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Vergi hesaplama Servisi, Global Tax Engine'in vergi belirleme ve hesaplama sürecini otomatikleştirmesini ve basitleştirmesini sağlayan, aşırı ölçeklenebilir çok kiracılı bir servistir. Tax Engine tam olarak konfigüre edilebilir. Konfigüre edilebilecek öğeler vergilendirilebilir veri modeli, vergi kodu, vergi uygulanabilirlik matrisi ve vergi hesaplama formülü ile sınırlı değildir. Tax Engine Microsoft Azure çekirdek hizmetler platformunda çalışır ve modern teknoloji ve artan ölçeklenebilirlik sunar.

Vergi hesaplama servisi Dynamics 365 Finance ve Dynamics 365 Supply Chain Management ile birleşir. Sonuç olarak, Dynamics 365 Project Operations, Dynamics 365 Commerce ve diğer birinci taraf ile üçüncü taraf uygulamaları ile de bütünleşir.

Vergi hesaplama Servisi, artan ölçeklenebilirlik sağlayan Microsoft tabanlı bir vergi altyapısıdır. Aşağıdaki görevleri yerine getirmenize yardımcı olur:

- Vergi hesaplama hizmetini Regulatory Configuration Service (RCS) aracılığıyla yapılandırma. RCS, elektronik raporlama (ER) tasarımcısının gelişmiş bir sürümüdür ve bağımsız bir hizmet olarak edinilebilir.
- Vergi kodlarının ve oranlarının otomatik olarak belirlenmesi için vergi matrisini yapılandırma.
- Vergi kayıt numarasının otomatik olarak belirlenmesi için vergi matrisini yapılandırma.
- Formül ve koşulları tanımlamak için vergi hesaplama tasarımcısını yapılandırma.
- Vergi belirleme ve hesaplama çözümünü tüzel kişilerle paylaşma.

Vergi hesaplama hizmetini kullanmak için, Microsoft Dynamics Lifecycle Services (LCS) içindeki projenizden vergi hesaplama servisi eklentisini yükleyin. Sonra, RCS'deki kurulumu tamamlayın ve Finance ve Supply Chain Management vergi hesaplama hizmetini etkinleştirin. Daha fazla bilgi için bkz. [Vergi hizmetini kullanmaya başlama](https://go.microsoft.com/fwlink/?linkid=2138482).

## <a name="availability"></a>Kullanılabilirlik

Vergi hesaplama hizmeti yalnızca, korumalı alan ortamlarında ve seçili müşteriler için ortak bir önizleme programı aracılığıyla kullanılabilir. Sonuç olarak, tüm müşteriler ve üretim ortamlarında genellikle kullanılabilir olacaktır.

Yeni özellikler vergi hesaplama hizmetinde sunulmaya devam edecek. Bu nedenle, desteklenen özelliklerin kapsam bilgilerini öğrenmek için en güncel belgeleri kontrol edin.

Vergi hesaplama hizmeti aşağıdaki Azure bölgelerinde dağıtılır. Ayrıca, müşteri gereksinimlerine göre daha fazla Azure bölgesinde kullanılacak şekilde dağıtılacaktır.

- Amerika Birleşik Devletleri
- Avrupa
- Fransa
- Birleşik Krallık

> [!NOTE]
> Vergi hesaplama Servisi, Dynamics 365 şirket içi dağıtımlarını desteklemez. Ayrıca Dynamics AX 2012 gibi önceki sürümleri de desteklemez.

## <a name="feature-highlights"></a>Özellikle ilgili önemli noktalar

- Vergiyi otomatik olarak belirlemek ve hesaplamak için yapılandırılabilir vergi matrisi
- Çoklu katma değer vergisi (KDV) kayıt numaraları desteği
- Vergi belirleme ve hesaplama için transfer emri desteği
- Çoklu KDV kayıt numaralarının belirlenmesi için transfer emri desteği

## <a name="supported-transactions"></a>Desteklenen işlemler

Vergi hesaplama servisi tüzel kişilik ve işlem tarafından etkinleştirilebilir. Aşağıdaki işlemler desteklenir:

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

[Vergi hizmetini kullanmaya başlama](https://go.microsoft.com/fwlink/?linkid=2138482)

[Çoklu KDV kayıt numarası](https://go.microsoft.com/fwlink/?linkid=2153387)

[Transfer emri için vergi özelliği desteği](https://go.microsoft.com/fwlink/?linkid=2153388)

[Vergi hizmetinde uzantı oluşturma](https://go.microsoft.com/fwlink/?linkid=2138483)
