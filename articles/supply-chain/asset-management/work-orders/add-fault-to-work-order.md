---
title: İş emrine hata ekle
description: Bu makale, Varlık Yönetiminde iş emirlerine arıza kayıtlarının nasıl ekleneceğini açıklamaktadır.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 210db3259a6c64a508119b30598a34dbda2d2dd2
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015012"
---
# <a name="add-fault-to-work-order"></a>İş emrine hata ekle

[!include [banner](../../includes/banner.md)]



Arıza tasarımcısında tasarlanmış arızaları bir iş emrine ekleyebilirsiniz. İş emrinde seçilen varlık için kullanılan varlık türlerine bir veya daha fazla arıza kaydı bağlanmalıdır. Kurulum hakkında daha fazla bilgi için bkz. [Arıza yönetimi](../setup-for-work-orders/fault-management.md)

1. **Varlık yönetimi** > **İş emirleri** > **Tüm iş emirleri** veya **Etkin iş emirleri**'ni seçin.

2. Arıza kaydı yapmak için iş emrini seçin ve sonra Eylem bölmesinde, **İş emri** sekmesinde, **Varlık** grubunda, **Varlık arızası**'nı seçin.

3. **Belirtiler** hızlı sekmesinde **Satır ekle**'yi seçin. **Arıza** alanına otomatik olarak sıralı bir arıza numarası girilir.

4. **Arıza belirtisi** alanında ilgili belirtiyi seçin.

5. **Arıza alanı** ve **Arıza türü** alanlarında uygun değerleri seçin.

6. **Arıza tarihi** alanına geçerli tarih otomatik olarak eklenir. Gereksinim duyduğunuz şekilde farklı bir tarih seçebilirsiniz.

7. **Seçilen belirtinin nedenleri** hızlı sekmesine, sorunun nedenini açıklayan bir satır ekleyin.

8. **Seçilen belirtinin çözümleri** hızlı sekmesine, sorunun olası çözümünü açıklayan bir satır ekleyin.

9. **Kaydet**'i seçin.

Aşağıdaki şekilde bir arıza merkezi kaydı örneği gösterilmiştir.

![Şekil 1.](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Varlık arızalarını görüntüleme

**Varlık arızaları** listesinde, varlıklara kaydedilen tüm arızalara genel bakış bulabilirsiniz.

**Varlık arızaları** liste sayfasında, varlıklara kaydedilmiş olan tüm arızalara genel bakış bulabilirsiniz. Sayfayı açmak için **Varlık yönetimi** > **Sorgular** > **Varlık arızası** > **Varlık arızaları**'nı seçin.


## <a name="print-asset-fault-report"></a>Varlık arızası raporunu yazdırma

**Tüm varlıklar** liste sayfasından, tüm arıza kayıtlarını görüntüleyen bir varlık arıza raporu yazdırabilir ve arıza istatistiklerine ilişkin bir grafik özet alabilirsiniz.

1. **Varlık yönetimi** > **Varlıklar** > **Tüm varlıklar**'ı seçin.

2. Arıza raporu yazdırılacak olan varlığı seçin.

3. Eylem Bölmesinde, **Genel** sekmesindeki **Raporlar** gurubunda **Varlık arızası**'nı seçin.

4. Belirli bir dönem girin veya bir arıza türü seçin.

5. Raporu yazdırmak için **Tamam**'ı seçin.

>[!NOTE]
>Çeşitli varlıklar veya varlık türleri için bir arıza raporu yazdırmak üzere **Varlık yönetimi** > **Raporlar** > **Varlıklar** > **Varlık arızası**'nı seçin.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]