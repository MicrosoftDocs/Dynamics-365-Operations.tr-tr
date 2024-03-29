---
title: Servis düzeyi sözleşmelerine genel bakış
description: Servis düzeyi sözleşmesinde müşteri, şirketin sorunu kayda alışından sorun giderilene kadar olan süreyi temel alan bir minimum yanıt süresini kabul eder.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServicelevelagreement
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b90618d5d283b16ac8374f3b8b2df48611ba270
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014708"
---
# <a name="service-level-agreements-overview"></a>Servis düzeyi sözleşmelerine genel bakış       

[!include [banner](../includes/banner.md)]


Servis düzeyi anlaşması (SDA) bir servis şirketi ve servis müşterisi arasındaki anlaşmadır. SLA'da müşteri, şirketin sorunu kayda alışından sorun giderilene kadar olan süreyi temel alan bir minimum yanıt süresini kabul eder.

SLA, müşterilere standart servis düzeyi sunulmasını zorunlu kılar ve ayrıca bir servis şirketi için bir servis işinin ne zaman tamamlanması gerektiğini açıklar.

Servis müşterilerine farklı düzeylerde servis sunmak için istenilen sayıda SDA oluşturulabilir.

## <a name="create-a-service-level-agreement"></a>Servis düzeyi anlaşması oluşturma

1.  **Servis yönetimi** \> **Kurulum** \> **Servis sözleşmeleri** \> **Servis düzeyi sözleşmeleri**'ne tıklayın.

2.  **Servis düzeyi sözleşmesi** alanında, yeni servis sözleşmesi için bir ad girin.

3.  Servis düzeyi sözleşmesine eklenen servis çağrılarının tamamlanması için izin vermek istediğiniz süreyi yazın. Ardından servis düzeyi anlaşmasının belirli bir takvimi temel almasını istiyorsanız bir takvim seçin.

## <a name="apply-a-service-level-agreement"></a>Servis düzeyi anlaşmasını uygulama

SDA doğrudan bir servis anlaşmasına uygulanır.

El ile oluşturduğunuz ve SLA içeren bir servis anlaşmasına iliştirdiğiniz servis siparişleri bu SLA'ya göre ölçülür.

Otomatik olarak oluşturduğunuz servis siparişleri bir SDA'ya iliştirilmez.

## <a name="apply-the-service-level-agreement-to-the-service-agreement"></a>Servis düzeyi anlaşmasını servis anlaşmasına uygulama

1.  **Servis yönetimi** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın. SLA uygulamak istediğiniz servis sözleşmesini seçin ve **Eylem Bölmesinde** **Düzenle**'ye tıklayın.

2.  **Servis düzeyi sözleşmesi** alanında, atamak istediğiniz SLA'yı seçin.

## <a name="apply-the-service-level-agreement-to-the-service-agreement-group"></a>Servis düzeyi anlaşmasını servis anlaşması grubuna uygulama

1.  **Servis yönetimi** \> **Kurulum** \> **Servis sözleşmeleri** \> **Servis sözleşmesi grupları**'na tıklayın.

2.  **Servis düzeyi sözleşmesi** alanında, atamak istediğiniz SLA'yı seçin.

## <a name="track-time-on-a-service-order-against-an-sla"></a>Servis siparişindeki zamanı SDA'ya göre izleme

Bir SLA'nın atandığı bir servis sözleşmesi için yeni bir servis siparişi oluşturduğunuzda, servisin teslim edilmesi için zaman aralığı başlatılır ve sistem teslimat süresini izlemeye başlar. Ek olarak aşağıdaki seçenekleri ayarlayabilirsiniz:

  - Servis siparişlerinde harcanan toplam zamanı kaydetmek için servis siparişindeki zaman kaydını başlatabilir ve durdurabilirsiniz.

  - Servis düzeyi anlaşmasında belirlenen zaman aralığıyla uyumluluğu izleyebilirsiniz.

  - Servis düzeyi anlaşmasının zaman aralığı aşıldığında belirlenmesi gereken neden kodlarını tanımlayabilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

[Servis düzeyi anlaşmalarıyla uyumluluğu görüntüleme](view-compliance-with-service-level-agreements.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]