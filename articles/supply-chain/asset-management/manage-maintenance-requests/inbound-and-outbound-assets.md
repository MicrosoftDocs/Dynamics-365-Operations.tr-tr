---
title: Gelen ve giden kıymetler
description: Bu makalede Varlık Yönetimi'nde gelen ve giden varlıkları kaydetme açıklanmaktadır.
author: johanhoffmann
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd7482cfe943347840e9fb070151d66fbe5ef9ca
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016550"
---
# <a name="inbound-and-outbound-assets"></a>Gelen ve giden varlıklar

[!include [banner](../../includes/banner.md)]

 

Şirketiniz başka yerlerden veya müşterilerden alınan varlıklar üzerinde onarım işleri veya bakım işleri yapıyorsa, Varlık Yönetimi hem şirketinize giden gelen varlıkları hem de iade edilen varlıkları izleyebilir.

> [!NOTE]
> Gelen ve giden varlıkları yönetmek için gelen ve giden yaşam döngüsü durumlarını kullanmak istiyorsanız bu eylemleri desteklemek için bakım talebi yaşam döngüsü durumlarını ve yaşam döngüsü modellerini ayarlamanız gerekir. Daha fazla bilgi için bkz. [Bakım istekleri](/d365F-O/supply-chain/asset-management/manage-maintenance-requests/../manage-maintenance-requests/maintenance-request-overview).

Varlık Yönetimi kurulumu, gelen ve giden varlıklarla çalışabilir olup olmadığını belirler.

## <a name="register-assets-as-inbound"></a>Varlıkları gelen olarak kaydetme

1. **Varlık yönetimi** \> **Bakım talepleri** \> **Etkin bakım talepleri**'ni seçin.
2. Bakım talebini seçin.
3. **Bakım talebi durumunu güncelleştir**'i seçin.
4. **Gelen**'i (veya gelen varlıklar için oluşturduğunuz başka bir yaşam döngüsü durumu) seçin ve **Tamam**'ı seçin.

![Varlıkları gelen olarak kaydetme.](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Gelen varlıkları alındı olarak kaydetme

1. **Varlık yönetimi** \> **Gelen/Giden** \> **Gelen varlıklar**'ı seçin.
2. Varlık veya bakım talebini seçin.
3. **Varlıkları al**'ı seçin.
4. **Alındı** alanında tarihi ve saati girin. Daha sonra **Tamam**'ı seçin. Kayıt, **Gelen varlıklar** listesi sayfasından kaldırılır.

![Gelen varlıkları alındı olarak kaydetme.](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Varlıkları giden olarak kaydetme

Bakım veya onarım işini tamamladığınızda, varlığı iade edildiği gibi kaydedebilirsiniz.

1. **Varlık yönetimi** \> **Bakım talepleri** \> **Etkin bakım talepleri**'ni seçin.
2. Bakım talebini seçin.
3. **Bakım talebi durumunu güncelleştir**'i seçin.
4. **Giden**'i (veya giden varlıklar için oluşturduğunuz başka bir yaşam döngüsü durumu) seçin ve **Tamam**'ı seçin.

## <a name="register-outbound-assets-as-delivered"></a>Giden varlıkları teslim edildi olarak kaydetme

1. **Varlık yönetimi** \> **Gelen/Giden** \> **Giden varlıklar**'ı seçin.
2. Varlık veya bakım talebini seçin.
3. Varlıkları **Teslim et**'i seçin.
4. **Teslim edildi** alanında tarihi ve saati girin. Daha sonra **Tamam**'ı seçin. Kayıt, **Giden varlıklar** listesi sayfasından kaldırılır.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]