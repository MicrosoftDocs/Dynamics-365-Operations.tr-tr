---
title: Konteyner etkinlikleri varlığı
description: Bu konuda, sevkiyat konteynerlerinin ilerleme durumunu izlemek için kullanılan konteyner etkinlikleri hakkında bilgi sağlanmaktadır.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 7bb2b97e8885e3b1265f0c93585873c8a64f1dfb
ms.sourcegitcommit: 611202adaa080250636efabb3b3b32b850d92d04
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2022
ms.locfileid: "8813093"
---
# <a name="container-activities-entity"></a>Konteyner etkinlikleri varlığı

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Konteyner etkinlikleri, sevkiyat konteynerlerinin ilerleme durumunu izlemek için kullanılır. Sevkiyat konteyneri oluşturma sırasında seçilen yolculuk şablonuna atanan her bir durak için bir kayıt oluşturulur. Veri varlığı aracılığıyla sevkiyat konteyneri oluşturulduğunda da kayıtlar oluşturulur.

Taşıma durumundaki sevkiyat konteynerinin ilerleme durumuyla ilgili bilgiler genellikle harici bir kaynaktan alınır. Konteyner etkinlikleri varlığı, nakliye aracısı gibi bir harici kaynağın kaydı doğrudan güncelleştirebilmesine olanak tanır. Bu nedenle, verilerin el ile güncelleştirilmesi gerekmez.

## <a name="container-activities-itmcontaineractivityentity"></a>Konteyner etkinlikleri (ITMContainerActivityEntity)

Ek etkinlik kayıtları oluşturmak için konteyner etkinlikleri varlığını (`ITMContainerActivityEntity`) kullanın. Alternatif olarak, nakliye aracısı onaylı **Fiili bitiş tarihi** değeri için güncelleştirmeleri aktarabilir.

| Adı | Eşleme | Veri türü | Anahtar | Zorunlu |
|---|---|---|---|---|
| Fiili bitiş tarihi | ITMContainerActivityTable.ActualEndDate | Datetime | No. | No. |
| Teslimat şekli | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | No. | No. |
| Tahmini bitiş tarihi | ITMContainerActivityTable.EsimatedDate | Datetime | No. | No. |
| Satır numarası | ITMContainerActivityTable.LineNum | Numeric(32, 16) | **Evet** | No. |
| Notlar | ITMContainerActivityTable.Notes | nvarchar(MAX) | No. | No. |
| Faaliyet | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | No. | **Evet** |
| Sevkiyat konteyneri | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **Evet** | **Evet** |
| Seyahat | ITMContainerActivityTable.ShipId | Nvarchar(20) | **Evet** | **Evet** |
| Durak | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | No. | **Evet** |
| Hizmet sağlayıcı | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | No. | No. |
| Sıcaklık | ITMContainerActivityTable.ShipTemperature | Numeric(32, 6) | No. | No. |
| Tekne | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | No. | No. |
| Başlangıç tarihi | ITMContainerActivityTable.StartDate | Datetime | No. | No. |

## <a name="tracking-control"></a>İzleme denetimi

İzleme denetim merkezi, belirtilen bir kaynak alanını güncelleştirmenin belirtilen bir hedef alanın güncelleştirmesi tarafından tetiklenmesini sağlar. Hem kaynak alanın değeri hem de hedef alanın değeri konteyner etkinlikleri varlığı kullanılarak güncelleştiriliyorsa, hedef alan varlık değerini gösterir. Bu davranış, *Sağlama süresi* değerine sahip bir **Oluşturma türü** olan izleme deneyimi kayıtlarıyla ilişkilidir.

**Oluşturma türü** değeri *Durum güncelleştirmesi* veya *Boş* (kullanıcı tanımlı bir değerdir) olan maliyet alanları için sistem, izleme denetimi yapılandırmasına göre seyahat durumunu veya hedef alanı güncelleştirir.

## <a name="calculated-fields"></a>Hesaplanan alanlar

Bir konteyner etkinliği kaydında aşağıdaki alanların değerleri, diğer alanların değerlerine göre hesaplanır. Bu hesaplanan alanlar veri varlığına dahil edilmese de hesaplamaların temel aldığı alanlar sağlanmışsa bu alanlar ayarlanır.

- **Tahmini gün** = **Tahmini bitiş tarihi** – **Başlangıç tarihi**
- **Gerçek gün sayısı** = **Fiili bitiş tarihi** – **Başlangıç tarihi**
