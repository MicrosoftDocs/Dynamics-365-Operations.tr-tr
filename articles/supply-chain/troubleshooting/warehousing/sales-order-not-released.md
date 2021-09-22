---
title: Satış siparişi, giden ambar işlemleri ile serbest bırakılamadı
description: Satış siparişinin serbest bırakılamadığına dair bir hata iletisi alabilmenizin birkaç nedeni vardır. Bu sayfada sorunun nedeni ve nasıl giderileceği açıklanmaktadır.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fca5ee1bc97545ea4de56d940fdedd320a6cfe84
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477863"
---
# <a name="sales-order-could-not-be-released-with-outbound-warehouse-operations"></a>Satış siparişi, giden ambar işlemleri ile serbest bırakılamadı

## <a name="symptoms"></a>Belirtiler

Giden ambar işlemleriyle çalışırken aşağıdaki hata iletisini alabilirsiniz:

> Satış siparişi serbest bırakılamadı.

## <a name="cause"></a>Nedeni

Bu sorun birkaç nedenle oluşabilir. Örneğin, sipariş alacak yönetiminde tutuluyor durumundadır ve bir siparişle ilişkili tüm satış satırları için geçerli bir posta adresi girilene kadar hiçbir sevkiyat oluşturulamaz. Alternatif olarak, siparişin ambara serbest bırakılabilmesi için önce ele alınması gereken bir sipariş tutma işlemi vardır. Bu tutma işlemi, siparişe özgü olabilir veya müşteri hesabı üzerinde olabilir.

## <a name="resolution"></a>Çözüm

Satış siparişi ve sipariş satırlarına adres ekleyin veya adresi güncelleştirin, ardından siparişi ambara serbest bırakın. Siparişler yalnızca geçerli teslimat adresi varsa (**Kuruluş yönetimi** modülünde ayarlanan adres biçimi kurulumu için) ambara serbest bırakılabilir.

Sipariş tutmayı araştırın ve sorunları giderin. Ardından sipariş veya müşteriden tutma işlemini kaldırın ve siparişi ambara serbest bırakın.
