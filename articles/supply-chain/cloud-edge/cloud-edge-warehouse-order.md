---
title: Bulut ve uç ölçek birimleri için ambar siparişleri
description: Bu konuda, ambar ölçek birimi iş yükünün parçası olarak kullanılan ambar siparişi özelliği hakkında bilgi sağlanmaktadır.
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105734"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Bulut ve uç ölçek birimleri için ambar siparişleri

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> Ölçek birimi iş yükleri kullanıldığında, genel önizlemedeki iş işlevlerin tümü tam olarak desteklenmez. Ölçek birimlerini kullanıyorsanız yalnızca desteklendiği bu konuda açıkça tanımlanan işlemleri kullandığınızdan emin olun.

## <a name="what-are-warehouse-orders"></a>Ambar siparişleri nelerdir?

*Ambar siparişleri*, merkez ve ölçek birimi ambar dağıtımlarını desteklemek için oluşturulan bir sipariş türüdür. Bunlar, bir ölçek biriminde ambar iş yükü çalıştırırken stok almanızı sağlar. Şu anda yalnızca satınalma siparişleriyle birlikte kullanılabilirler.

Ambar siparişleri, bir gelen satınalma siparişinin işlenmesi sırasında fiziksel eldeki stoku kaydetmek için kullanıldığı durumlarda olduğu gibi, ambar yönetimi işleminin bir parçası olarak kullanılır. Ambar siparişleri, ambar yönetim işlemlerini kullanmak üzere etkinleştirilen ölçek birimi ambarının ve ürünlerinin belirtildiği satınalma siparişleri için kullanılabilen bir *Ambara serbest bırak* işleminin parçası olarak oluşturulur.

> [!IMPORTANT]
> Ambar siparişleri yalnızca [bulut ve uç ölçek birimleri için ambar yönetimi iş yüklerini](cloud-edge-workload-warehousing.md) kullanan dağıtımlarda kullanılabilir.

## <a name="create-a-warehouse-order"></a>Ambar siparişi oluşturma

Ambar siparişi oluşturmak için şu adımları izleyin.

1. Merkezde çalışan Microsoft Dynamics 365 Supply Chain Management kurulumunda oturum açın. (Merkezde oturumunuz açıkken *Ambara serbest bırak* işlemini başlatmanız gerekir.)
1. **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin.
1. Eylem Bölmesinde, **Ambar** sekmesindeki **Eylemler** grubunda, **Ambara serbest bırak**'ı seçin.
1. İlgili ambar siparişi satırlarını görüntülemek için ilgili satınalma siparişini açın, **Satınalma siparişi satırları** bölümünde bir satır seçin ve ardından araç çubuğunda **Ambar \> Ambar siparişi satırları**'nı seçin. Tüm satırları görüntülemek için **Ambar yönetimi \> Sorgular ve raporlar \> Ambar siparişi satırları**'na gidin.

## <a name="cancel-a-warehouse-order"></a>Ambar siparişini iptal etme

*Ambara serbest bırak* işlemi kapsamında, satınalma siparişi stok hareketleri ambar siparişlerine bağlıdır ve merkez tarafından güncellenemezler. Yanlışlıkla ambara serbest bırakırsanız veya başka bir nedenle ambar siparişi satırlarının oluşturulması işlemini tersine çevirmeniz gerekirse ambar siparişi satırlarını iptal etme isteği gönderebilirsiniz.

Ambar siparişi satırlarını iptal etmek için şu adımları izleyin.

1. Merkezde çalışan Supply Chain Management kurulumunda oturum açın.
1. **Ambar yönetimi \> Sorgular ve raporlar \> Ambar siparişi satırları**'na gidin.
1. İlgili satırı seçin.
1. Eylem Bölmesinde **Ambar siparişi satırlarını iptal et**'i seçin.

> [!NOTE]
> Bekleyen iptal işlemi olan veya iş yükünü ölçek biriminde çalıştıran bir ambarda etkin olarak işlenmekte olan satırlar için satırları iptal etme isteği reddedilir.

## <a name="monitor-a-warehouse-order"></a>Ambar siparişini izleme

**Ambar siparişi satırları** görünümünde, **Alınacak miktar** sütunundaki değerleri inceleyerek gelen alım işlemlerinin ilerleme durumunu izleyebilirsiniz. Ambar uygulaması kullanılarak yapılan çalışmalara ilişkin ayrıntıları görüntülemek için aşağıdaki adımlardan birini izleyin.

- **Ambar yönetimi \> Sorgular ve raporlar \> Ambar satırı siparişleri**'ne gidin ve aradığınız satırları bulmak için filtreyi kullanın.
- **Tedarik ve kaynak atama \> Satınalma siparişleri \> Tüm satınalma siparişleri**'ne gidin ve ilgili satınalma siparişini açın. **Satınalma siparişi satırları** bölümünde, bir veya daha fazla satır seçin ve araç çubuğunda **Ambar \> Ambar makbuz girişleri**'ni seçin.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]