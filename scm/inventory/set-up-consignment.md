---
title: Konsinyeyi ayarlama
description: "Bu konu gelen konsinye stok operasyonlarının nasıl yapılandırılacağını açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7268b59e0cd550178367e08284b2c3a417b33498
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-consignment"></a>Konsinyeyi ayarlama

[!include[banner](../includes/banner.md)]


Bu konu gelen konsinye stok operasyonlarının nasıl yapılandırılacağını açıklar. 

Konsinye stok, satıcıya ait olan ancak tesisinizde depolanan stoktur. Stoğu tüketmeye veya kullanmaya hazır olduğunuzda stoğun sahipliği size geçer. Bu konu, konsinye işlemlerini etkinleştirmek için gerekli ayarları açıklar. Konsinye işlemleri hakkında daha fazla bilgi için bkz. [Konsinye](consignment.md).

## <a name="inventory-owners"></a>Stok sahipleri
Fiziksel gelen konsinye stoğu kaydetmek için bir satıcı sahibi tanımlamanız gerekir. Bu **Stok sahibi** sayfasında yapılır. **Satıcı hesabı**'nı seçtiğinizde bu **Ad** ve **Sahip** alanları için varsayılan değerleri oluşturur. **Sahip** alanındaki değer satıcıya görünür olacaktır, bu nedenle satıcı hesabı adlarınız şirket dışı insanların tanımaları için kolay değilse değiştirmek isteyebilirsiniz. **Sahip** alanını yalnızca **Stok sahibi** kaydını kaydettiğiniz zamana kadar düzenlemek mümkündür. **Ad** alanı satıcı hesabının ilişkilendirildiği tarafın adıyla doldurulur ve değiştirilemez. 

[![stok-sahipleri](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>İzleme boyut grubu
Konsinye işlemlerinde kullanılacak maddeler **Sahip** boyutunun **Etkin** olarak ayarlandığı bir **İzleme boyut grubu** ile ilişkilendirilmelidir. Sahip boyutunda her zaman **Fiziksel stok** ve **Mali stok** seçenekleri seçili olmalıdır. **Boyuta göre tedarik planı** kesinlikle seçilmemelidir. 

[![izleme-boyut-grubu](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Stok sahipliği değişiklik günlüğü
Konsinye stoğun sahipliğinin satıcıdan konsinye stoğu tüketecek tüzel kişiliğe transferini kaydetmek için **Stok sahipliği değişiklik**günlüğü kullanılır. Diğer stok günlükleri gibi bir stok günlüğü adı ile tanımlanmalıdır. Bu adlar **Stok günlüklerinin adları** sayfasında oluşturulur ve **Günlük türü**, **Sahiplik değişikliği** olarak ayarlanmalıdır. 

[![stok-sahiplik-değiştirme-günlüğü](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Konsinye işlemlerdeki satıcı iş birliği
Satıcılar, satıcı iş birliği arabirimini kullanıyorsa bunu, tesisinizdeki stoğun tüketimini izlemek için kullanabilirler. Satıcı iş birliğini kullanmak için satıcıların yapılandırması hakkında daha fazla bilgi için bkz. [Satıcı iş birliği kullanıcıları için güvenlik yapılandırması](../procurement/configure-security-vendor-portal-users.md).



