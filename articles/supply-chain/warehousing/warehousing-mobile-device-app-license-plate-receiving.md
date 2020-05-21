---
title: Ambarlama uygulaması aracılığıyla plaka teslim alma
description: Bu konu, fiziksel stoğu almak için bir plaka teslim alma işlemi kullanmayı desteklemek üzere ambarlama uygulamasının nasıl ayarlanacağını açıklamaktadır.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346388"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>Ambarlama uygulaması aracılığıyla plaka teslim alma

Bu konu, fiziksel stoğu almak için bir plaka teslim alma işlemi kullanmayı destekleyecek şekilde ambarlama uygulasımanın nasıl ayarlanacağını açıklamaktadır.

Bu işlevi, bir ön sevkiyat bildirimi (ÖSB) ile ilgili gelen stoğun girişini hızlı bir şekilde kaydetmek için kullanabilirsiniz. Ambar yönetim işlemleri transfer emri sevk etmek için kullanıldığında, sistem otomatik olarak bir ÖSB oluşturur. Satınalma siparişi işlemi için, ÖSB el ile kaydedilebilir veya bir gelen ÖSB veri varlığı işlemi kullanılarak otomatik olarak içe aktarılabilir.

ÖSB verileri, paletlerin (ana plakalar) kutular içerebildiği (iç içe geçmiş plakalar) *paketleme yapıları* aracılığıyla yüklere ve sevkiyatlara bağlıdır.

> [!NOTE]
> İç içe geçmiş plakalara sahip paketleme yapıları kullanıldığında, stok hareketlerinin sayısını azaltmak için sistem ana plakadaki fiziksel eldeki stoku kaydeder. Fiziksel eldeki stoğun hareketinin ana plakadan iç içe geçmiş plakalara taşınmasını tetiklemek için, paketleme yapısı verilerine göre, mobil cihazın *İçe içe geçmiş plakalara paketle* işi oluşturma işlemini temel alan bir menü öğesi sağlaması gerekir.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Teslim alma özet sayfasını gösterme veya atlama

*Mobil cihazlarda teslim alma özet sayfası görüntülenip görüntülenmeyeceğni denetle* özelliğini, plaka teslim alma işleminin bir parçası olarak ek bir ayrıntılı ambarlama uygulaması akışından yararlanmak üzere kullanabilirsiniz.

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Mobil cihazlarda bir teslim alma özet sayfasının görüntülenip görüntülenmeyeceğini denetler*

Bu özellik etkinleştirildiğinde, plaka teslim alma veya plaka teslim alma ve yerine koyma için mobil cihaz menüsü öğeleri bir **Teslim alma özeti sayfası görüntüle** ayarı sağlar. Bu ayar aşağıdaki seçeneklere sahiptir:

- **Ayrıntılı özet görüntüle** - Plaka teslim alma sırasında çalışanlar tam ÖSB bilgilerini gösteren ek bir sayfa görürler.
- **Özeti atla** – Çalışanlar tüm ÖSB bilgilerini göremez. Ambar çalışanları da bir değerlendirme kodu ayarlayamaz veya teslim alma işlemi sırasında özel durumlar ekleyemez.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelleme

Bir ÖSB zaten varolan plaka kimliği içeriyorsa ve plaka kaydının oluştuğu ambar yerleşimden başka bir ambar yerleşimindeki eldeki fiziksel stok verilerine sahipse, plaka teslim alma işlemi kullanılamaz.

Transit ambarının plakaları izlemediği (ve bu nedenle her plaka için fiziksel eldeki stoğu izlemediği) transfer emri senaryoları için, transitteki plakaların fiziksel eldeki stoklarının güncelleştirilmesini önlemek için *Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelle* özelliğini kullanabilirsiniz.

Bu özelliği kullanabilmeniz için sisteminizde etkinleştirmeniz gerekir. Yöneticiler özellik durumunu denetlemek ve etkinleştirmek için [özellik yönetimi](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ayarlarını kullanabilir. **Özellik yönetimi** çalışma alanındabu özellik aşağıdaki şekilde listelenir:

- **Modül:** *Ambar yönetimi*
- **Özellik adı:** *Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelleme*

Bu özellik kullanılabilir olduğunda işlevselliği yönetmek için, aşağıdaki adımları izleyin.

1. **Ambar yönetimi \> Kurulum \> Ambar yönetim parametreleri**'ne gidin.
1. **Genel** sekmesinde **Plakalar** hızlı sekmesinde, **Transit ambarı plaka ilkesi** alanını aşağıdaki değerlerden birine ayarlayın:

    - **İzlenemeyen plakanın yeniden kullanılmasına izin ver** – Sistem, *Transfer emriyle sevkedilen plakaların hedef ambar dışındaki ambarlarda kullanılmasını engelleme* özelliğinin kullanılabilir olmadığı durumlardaki gibi çalışır. Bu değer, özelliği ilk etkinleştirdiğinizde varsayılan ayardır.
    - **İzlenmeyen plakanın yeniden kullanılmasını engelle** – Transfer emri alınana kadar hedef ambarda, yalnızca sevk edilen plakayla ilgili olan eldeki stok güncelleştirmelerine izin verilir.

## <a name="more-information"></a>Daha fazla bilgi

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Mobil cihaz menü öğeleri hakkında daha fazla bilgi için bkz. [Ambar işi için mobil cihazları ayarlama](configure-mobile-devices-warehouse.md).
