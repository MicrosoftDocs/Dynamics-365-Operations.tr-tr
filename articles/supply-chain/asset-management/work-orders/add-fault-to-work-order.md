---
title: İş emrine arıza ekleme
description: Bu konu, Varlık Yönetiminde iş emirlerine arıza kayıtlarının nasıl ekleneceğini açıklamaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875950"
---
# <a name="add-fault-to-work-order"></a>İş emrine arıza ekleme

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Arıza tasarımcısında bir iş emrine arızalar kurulumu ekleyebilirsiniz. İş emrinde seçilen varlık, kendisine bağlanmış bir veya daha fazla arıza kaydı olan varlık türleri içermelidir. [Arıza yönetimi](../setup-for-work-orders/fault-management.md) bölümünden kurulum hakkında daha fazla bilgi edinin.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. Listede, arıza kaydı yapmak istediğiniz iş emrini seçin ve **Varlık arızası**'na tıklayın.

3. **Belirtiler** hızlı sekmesinde **Satır ekle**'ye tıklayın. **Arıza** alanına otomatik olarak sıralı bir arıza numarası eklenir.

4. **Arıza belirtisi** alanında ilgili belirtiyi seçin.

5. **Arıza alanı** ve **Arıza türü**'nü seçin.

6. **Arıza tarihi** alanına geçerli tarih otomatik olarak eklenir. Gerekirse başka bir tarih seçebilirsiniz.

7. **Seçilen belirtinin nedenleri** hızlı sekmesine, sorunun nedenini açıklayan bir satır ekleyin.

8. **Seçilen belirtinin çözümleri** hızlı sekmesine, sorunun olası çözümünü açıklayan bir satır ekleyin.

9. **Kaydet**'e tıklayın.

![Şekil 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Varlık arızalarını görüntüleme

**Varlık arızaları** listesinde, varlıklara kaydedilen tüm arızalara genel bakış bulabilirsiniz.

Listeyi açmak için **Varlık yönetimi** > **Sorgular** > **Varlık arızası** > **Varlık arızaları**'na tıklayın.


## <a name="print-asset-fault-report"></a>Varlık arızası raporunu yazdırma

**Tüm varlıklar** listesi sayfasından, tüm arıza kayıtlarını görüntüleyen bir kıymet hata raporu yazdırabilir ve hata istatistiklerine ilişkin bir grafik özet alabilirsiniz.

1. **Varlık yönetimi** > **Ortak** > **Varlıklar** > **Tüm varlıklar** öğesini seçin.

2. **Varlıklar** listesinde, bir arıza raporu yazdırmak istediğiniz varlığı seçin.

3. **Genel** sekmesinde > **Raporlar** bölümünde **Varlık arızası**'na tıklayın.

4. Belirli bir dönem ekleyin veya bir hata türü seçin.

5. Raporu yazdırmak için **Tamam**'a tıklayın.

>[!NOTE]
>Ayrıca **Varlık yönetimi** > **Raporlar** > **Varlıklar** > **Varlık arızası**'na tıklayarak çeşitli varlıklar veya varlık türleri için bir arıza raporu yazdırabilirsiniz.

