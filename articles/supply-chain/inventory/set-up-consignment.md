---
title: Konsinyeyi ayarlama
description: Bu konu gelen konsinye stok operasyonlarının nasıl yapılandırılacağını açıklar.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 00102f5c7a043c5ca22458a53b1445c57c61957c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209575"
---
# <a name="set-up-consignment"></a>Konsinyeyi ayarlama

[!include [banner](../includes/banner.md)]

Bu konu gelen konsinye stok operasyonlarının nasıl yapılandırılacağını açıklar.

Konsinye stok, satıcıya ait olan ancak tesisinizde depolanan stoktur. Stoğu tüketmeye veya kullanmaya hazır olduğunuzda stoğun sahipliği size geçer. Bu konu, konsinye işlemlerini etkinleştirmek için gerekli ayarları açıklar. Konsinye işlemleri hakkında daha fazla bilgi için bkz. [Konsinye ayarlama](consignment.md).

## <a name="inventory-owners"></a>Stok sahipleri
Fiziksel gelen konsinye stoğu kaydetmek için bir satıcı sahibi tanımlamanız gerekir. Bu **Stok sahibi** sayfasında yapılır. **Satıcı hesabı**'nı seçtiğinizde bu **Ad** ve **Sahip** alanları için varsayılan değerleri oluşturur. **Sahip** alanındaki değer satıcıya görünür olacaktır, bu nedenle satıcı hesabı adlarınız şirket dışı insanların tanımaları için kolay değilse değiştirmek isteyebilirsiniz. **Sahip** alanını yalnızca **Stok sahibi** kaydını kaydettiğiniz zamana kadar düzenlemek mümkündür. **Ad** alanı satıcı hesabının ilişkilendirildiği tarafın adıyla doldurulur ve değiştirilemez.

[![stok-sahipleri](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>İzleme boyut grubu
Konsinye işlemlerinde kullanılacak maddeler **Sahip** boyutunun **Etkin** olarak ayarlandığı bir **İzleme boyut grubu** ile ilişkilendirilmelidir. Sahip boyutunda her zaman **Fiziksel stok** ve **Mali stok** seçenekleri seçili olmalıdır. **Boyuta göre tedarik planı** kesinlikle seçilmemelidir.

[![izleme-boyut-grubu](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Stok sahipliği değişiklik günlüğü
Konsinye stoğun sahipliğinin satıcıdan konsinye stoğu tüketecek tüzel kişiliğe transferini kaydetmek için **Stok sahipliği değişiklik** günlüğü kullanılır. Diğer stok günlükleri gibi bir stok günlüğü adı ile tanımlanmalıdır. Bu adlar **Stok günlüklerinin adları** sayfasında oluşturulur ve **Günlük türü**, **Sahiplik değişikliği** olarak ayarlanmalıdır.

[![stok-sahiplik-değiştirme-günlüğü](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Konsinye işlemlerdeki satıcı iş birliği
Satıcılar, satıcı iş birliği arabirimini kullanıyorsa bunu, tesisinizdeki stoğun tüketimini izlemek için kullanabilirler. Satıcı iş birliğini kullanmak için satıcıların ayarlanması hakkında daha fazla bilgi için bkz. [Satıcı portalı kullanıcı güvenliği](../procurement/configure-security-vendor-portal-users.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]