---
title: İşlem yapılacak yerleşimler ve varlıklar
description: Bu konuda Varlık Yönetimi'ndeki işlem yapılacak yerleşimler ve varlıklar açıklanmaktadır. Varlık Yönetimi, Dynamics 365 Supply Chain Management'da varlıkların ve bakım işlerinin yönetilmesine yönelik gelişmiş bir modüldür.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe3e82f425421acdae81a02032ac6252765e1c05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439585"
---
# <a name="functional-locations-and-assets"></a>İşlem yapılacak yerleşimler ve varlıklar

[!include [banner](../../includes/banner.md)]

 

Bu konuda Varlık Yönetimi'ndeki işlem yapılacak yerleşimler ve varlıklar açıklanmaktadır. Varlık Yönetimi, Dynamics 365 Supply Chain Management'da varlıkların ve bakım işlerinin yönetilmesine yönelik gelişmiş bir modüldür.

## <a name="overview"></a>Genel bakış

Varlık Yönetimi, diğer Finance and Operations uygulamalarındaki çeşitli modüller ile sorunsuz şekilde tümleştirilir. Aşağıdaki örnekte diğer modüllerle olan arabirimler gösterilmektedir.

![Varlık Yönetiminin diğer modüllerle olan arabirimlerini gösteren diyagram](media/01-overview-image.png)

Varlık Yönetimi, şirketinizdeki birçok donanım türünün yönetimi ve bakımı ile ilgili tüm görevleri etkili bir şekilde yönetmenize ve gerçekleştirmenize olanak sağlar. Bu donanıma makineler, üretim ekipmanı ve taşıtlar dahildir. Varlık Yönetimi birçok sektördeki çözümleri de destekler.

Aşağıdaki şekilde, Varlık Yönetimi kapsamında olan ana işlevlerin genel görünümü gösterilmektedir.

![Varlık Yönetiminde ana işlevleri gösteren diyagram](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a>İşlem yapılacak yerleşimler ve varlıklar

İşlem yapılacak yerleşimler yerleşimlerdeki varlıkları yönetmek için kullanılır. Bu yönetim, İşlem yapılacak yerleşimlerdeki varlık maliyetlerinin izlenmesini içerir. İşlem yapılacak yerleşimler hiyerarşik olarak yapılandırılır ve yerleşimlerin alt yerleşimleri olabilir. İşlem yapılacak yerleşimlerin yapısı statiktir. Başka bir deyişle, yerleşimlerin yerinde değişiklik yapılamaz. Varlıklar işlem yapılacak yerleşimlere yüklenebilir ve gerekirse daha sonra başka İşlem yapılacak yerleşimlere yüklenebilir.

Varlık maliyetleri her zaman varlığın yerleşimini izler. Başka bir deyişle, bir varlığı yeni bir İşlem yapılacak yerleşime yüklerseniz, varlık otomatik olarak yeni İşlem yapılacak yerleşimle ilgili mali boyutları kullanır. Bu nedenle, varlık maliyetleri her zaman varlığın halizahırda yüklü olduğu işlem yapılacak yerleşim ile ilişkilidir. Mali boyutların bu şekilde otomatik olarak işlenmesi, şirketiniz işlem yapılacak yerleşimlerde kontrol ve raporlama yaparken maliyetlerin tam olarak izlenmesini garanti eder.

İşlem yapılacak yerleşimler hiyerarşinizi oluşturma şekliniz, şirketinizin dahili ekipmanların korunması veya müşteri ekipmanlarına bakım hizmeti yapılması gereksinimlerine bağlıdır. Aşağıdaki şekil, coğrafi konumları temel alan işlem yapılacak yerleşimler örneğini gösterir.

![Coğrafi konumlara dayalı işlem yapılacak yerleşimleri gösteren diyagram](media/03-overview-image.png)

Aşağıdaki şekil, müşterileri temel alan işlem yapılacak yerleşimler örneğini gösterir.

![Müşterilere dayalı işlem yapılacak yerleşimleri gösteren diyagram](media/04-overview-image.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]