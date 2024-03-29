---
title: Denemenin durumunu inceleme
description: Bu makale, bir denemenin Dynamics 365 Commerce'teki deneme yaşam döngüsündeki hangi duruma sahip olduğunu açıklamaktadır.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 818435a7c901d2a6b876b9c9db27faffc8b322fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877261"
---
# <a name="review-the-status-of-an-experiment"></a>Denemenin durumunu inceleme
Dynamics 365 Commerce'ta bir deneme ayarlama ve çalıştırmayla ilgili birçok adım bulunmaktadır. Deneme yalan döngüsü hakkında daha fazla bilgi için bkz. [Dynamics 365 Commerce'ta deneme](experimentation-overview.md).

Bir denemenin yaşam döngüsü içinde nerede olduğunu öğrenmek için Commerce site oluşurucunun sol gezinme bölümündeki **Denemeler**'i seçin. Deneme oluşturmayı etkinleştirmek, varyasyonlar atamak ve verileri analiz etmek için kullanılan üçüncü taraf hizmetindeki ve Commerce'taki her bir denemenin durumunu içeren bir denemeler listesi görüntülenir.

**Commerce durumu** sütununda, aşağıdaki değerler görüntülenebilir. 
- **Taslak** - Deneme Commerce içindeki bir sayfaya veya parçaya bağlı ve düzenleniyor.
- **Yayımlandı** - Deneme varyasyonları web sitenizde görüntülenmeye hazır. Deneme üçüncü taraf hizmetinde çalışıyorsa, web sitesi kullanıcıları sayfa veya parçanın üçüncü taraf hizmet tarafından seçilen bir varyasyonunu görür.
- **Yayımdan kaldırıldı** - Deneme artık web sitenizde yok. Deneme üçüncü taraf hizmetinde çalışıyorsa, web sitesi kullanıcıları sayfa veya parçanın üçüncü taraf hizmet tarafından seçilen bir varyasyonunu görür.
- **Tamamlandı** - Deneme çalışmasını tamamladı ve bir varyasyon tüm web sitesi kullanıcıları için canlı siteye yükseltildi.

Benzer şekilde, **üçüncü taraf durumu** sütununda, denemelerin üçüncü taraf hizmette bulunduğu durumu göstermek için aşağıdaki değerler görüntülenebilir.
- **Taslak** - Deneme üçüncü taraf hizmetinde ayarlandı ancak başlatılmadı.
- **Çalışıyor** - Deneme üçüncü taraf hizmetinde başlatıldı ve veri topluyor.
- **Duraklatıldı** - Deneme duraklatıldı, veri toplamıyor. Yeniden veri toplaması için denemeyi sürdürmeniz gerekir.
- **Arşivlendi** - Deneme çalışmasını tamamladı ve sonraki başvurular için üçüncü taraf hizmette kataloğa alındı.

Aşağıdaki diyagramda her iki durum kümesi ve bunların birbirleriyle ilişkileri gösterilmektedir.

[ ![Deneme durumları.](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)


[!INCLUDE[footer-include](../includes/footer-banner.md)]