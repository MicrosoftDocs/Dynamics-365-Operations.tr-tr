---
title: Varlıkları satınalma siparişlerine göre oluşturma
description: Bu konu, Varlık Yönetiminde bakım işleri için varlıklar oluşturmak üzere temel olarak kullanılabilecek bir varlık maddeleri listesini nasıl oluşturabileceğinizi açıklar.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83419fa5c6b6aee0b321c526565c3518deaf4bd0
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016996"
---
# <a name="create-assets-based-on-purchase-orders"></a>Varlıkları satınalma siparişlerine göre oluşturma

[!include [banner](../../includes/banner.md)]

 

Bu konu, Varlık Yönetiminde bakım işleri için varlıklar oluşturmak üzere temel olarak kullanılabilecek bir varlık maddeleri listesini nasıl oluşturabileceğinizi açıklar. Varlık maddelerine göre, bu maddelerde oluşturulan satınalma siparişi satırlarının listesini görüntüleyebilirsiniz. Bu işlevin amacı, Varlık Yönetiminde bir satınalma siparişini temel alarak kolayca bir varlık oluşturmaktır.

İlk olarak, **Varlık maddeleri**'ndeki bir satınalma siparişinden varlıklar oluşturmak için kullanılacak maddeler ayarlayın. Bir satınalma siparişi satırı oluşturduktan sonra, **Bekleyen varlıklar**'da varlıklar oluşturun. Varlığın satınalma siparişinin hangi aşamasında oluşturulması gerektiğine karar vermek mümkündür.


## <a name="select-asset-items"></a>Varlık maddelerini seçin

1. **Varlık yönetimi** > **Kurulum** > **Varlıklar** > **Maddeler**'e tıklayın.
2. Yeni bir varlık maddesi oluşturmak için **Yeni**'ye tıklayın.
3. **Madde numarası** alanında bir maddeyi seçin. Bu alandan çıktığınızda, madde adı otomatik olarak **Ürün adı** alanına eklenir.
4. **Genel** hızlı sekmesinde, madde için bir varlık türü seçin.
5. Madde için varlık üreticisi ve modeli seçin.
6. Maddeyi kaydedin.


## <a name="create-assets-from-pending-assets"></a>Bekleyen varlıklardan varlıklar oluşturma

1. **Varlık yönetimi** > **Genel** > **Varlıklar** > **Bekleyen Varlıklar**'a tıklayın.
2. **Varlık maddeleri**'nde seçilen maddelere göre satınalma siparişlerinin güncelleştirilmiş bir listesini görürsünüz.
3. Varlığın oluşturulması gereken yaşam döngüsü durumunu seçmek için satınalma siparişlerinin durumunu filtreleyebilirsiniz. Örneğin, yalnızca bir satınalma siparişinde bir ürün girişi deftere nakledildiğinde varlıklar oluşturmak isteyebilirsiniz.
4. Maddeyle ilgili ayrıntılı bilgileri görüntülemek için satınalma siparişi satırındaki **Referans numarası** bağlantısını seçin.
5. **Stok boyutları** hızlı sekmesinde hangi boyutların görüntüleneceğini düzenlemek istiyorsanız, **Boyutları Görüntüle** düğmesine tıklayın ve seçimlerinizi yapın.
6. Bir satınalma siparişi satırına dayalı bir varlık oluşturmak istiyorsanız, liste sayfasında bu satır için **İşaretle** sütunundaki onay kutusunu seçin ve **Varlıklar oluştur**'a tıklayın. Varlık kodunu size bildiren bir ileti görüntülenir.
7. **Tüm varlıklar** listesinde varlığı seçin ve varlığa daha fazla bilgi eklemek için **Düzenle** düğmesine tıklayın.
8. **Bekleyen varlıklar**'da, bir varlık oluşturmak istemediğiniz için bir satırı silmek istiyorsanız, ilgili satırın **İşaretle** sütunundaki onay kutusunu seçin ve **Bekleyen varlıkları at**'a tıklayın. Varlık kodunu size bildiren bir ileti görüntülenir. Satınalma siparişini veya satış siparişini silmezsiniz. Yalnızca **Varlık Yönetimi**'nde varlık oluşturabildiğiniz kaydı silersiniz.

>[!NOTE]
>Tüm ürün boyutları (boyut, renk, yapılandırma, vb.) otomatik olarak varlık özniteliklerine aktarılır. İzleme boyutları (seri numarası), varlık oluşturulduğunda doğrudan varlığa depolanır.


## <a name="find-pending-assets"></a>Bekleyen varlıkları bulma

Bekleyen varlıkları denetlemek için **Bekleyen varlık sayımı** çalıştırabilirsiniz. Örneğin, bu işlev bekleyen bir varlık, varlık olarak oluşturulmaya hazır olduğunda bir bildirim almak için kullanılabilir.

1. **Varlık yönetimi** > **Periyodik** > **Varlıklar** > **Bekleyen varlık sayısı**'na tıklayın.
2. İşi çalıştırmak için **Tamam**'a tıklayın ve **Bekleyen varlıklar**'daki listeyi güncelleştirin.
3. Bu işi, örneğin her gün bir toplu iş olarak çalışacak şekilde ayarlayabilirsiniz.

**Dikkat:** Bir satınalma siparişinde ilgili maddeyi temel alarak bir varlık oluşturduktan *sonra* veri dğiştirilirse, bu değişiklikler varlığa yansıtılmaz.
