---
title: Gelen ve giden varlıklar
description: Bu konuda Varlık Yönetimi'nde gelen ve giden varlıkları kaydetme açıklanmaktadır.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetOutboundObjectsListPage, EntAssetOutboundObjectsDeliver, EntAssetInboundObjectsListPage, EntAssetInboundObjectsRecieve
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6dfadf6824c6a3df7be9b3b6f3d9f5dd2749e34
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018083"
---
# <a name="inbound-and-outbound-assets"></a>Gelen ve giden varlıklar

[!include [banner](../../includes/banner.md)]

 

Şirketiniz başka yerlerden veya müşterilerden alınan varlıklar üzerinde onarım işleri veya bakım işleri yapıyorsa, Varlık Yönetimi hem şirketinize giden gelen varlıkları hem de iade edilen varlıkları izleyebilir.

> [!NOTE]
> Gelen ve giden varlıkları yönetmek için gelen ve giden yaşam döngüsü durumlarını kullanmak istiyorsanız bu eylemleri desteklemek için bakım talebi yaşam döngüsü durumlarını ve yaşam döngüsü modellerini ayarlamanız gerekir. Daha fazla bilgi için bkz. [Bakım istekleri](../setup-for-maintenance-requests/requests.md).

Varlık Yönetimi kurulumu, gelen ve giden varlıklarla çalışabilir olup olmadığını belirler.

## <a name="register-assets-as-inbound"></a>Varlıkları gelen olarak kaydetme

1. **Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Etkin bakım talepleri**'ni seçin.
2. Bakım talebini seçin.
3. **Bakım talebi durumunu güncelleştir**'i seçin.
4. **Gelen**'i (veya gelen varlıklar için oluşturduğunuz başka bir yaşam döngüsü durumu) seçin ve **Tamam**'ı seçin.

![Varlıkları gelen olarak kaydetme](media/07-manage-maintenance-requests.png)

## <a name="register-inbound-assets-as-received"></a>Gelen varlıkları alındı olarak kaydetme

1. **Varlık yönetimi** \> **Ortak** \> **Gelen/Giden** \> **Gelen varlıklar**'ı seçin.
2. Varlık veya bakım talebini seçin.
3. **Varlıkları al**'ı seçin.
4. **Alındı** alanında tarihi ve saati girin. Daha sonra **Tamam**'ı seçin. Kayıt, **Gelen varlıklar** listesi sayfasından kaldırılır.

![Gelen varlıkları alındı olarak kaydetme](media/08-manage-maintenance-requests.png)

## <a name="register-assets-as-outbound"></a>Varlıkları giden olarak kaydetme

Bakım veya onarım işini tamamladığınızda, varlığı iade edildiği gibi kaydedebilirsiniz.

1. **Varlık yönetimi** \> **Ortak** \> **Bakım talepleri** \> **Etkin bakım talepleri**'ni seçin.
2. Bakım talebini seçin.
3. **Bakım talebi durumunu güncelleştir**'i seçin.
4. **Giden**'i (veya giden varlıklar için oluşturduğunuz başka bir yaşam döngüsü durumu) seçin ve **Tamam**'ı seçin.

## <a name="register-outbound-assets-as-delivered"></a>Giden varlıkları teslim edildi olarak kaydetme

1. **Varlık yönetimi** \> **Ortak** \> **Gelen/Giden** \> **Giden varlıklar**'ı seçin.
2. Varlık veya bakım talebini seçin.
3. Varlıkları **Teslim et**'i seçin.
4. **Teslim edildi** alanında tarihi ve saati girin. Daha sonra **Tamam**'ı seçin. Kayıt, **Giden varlıklar** listesi sayfasından kaldırılır.
