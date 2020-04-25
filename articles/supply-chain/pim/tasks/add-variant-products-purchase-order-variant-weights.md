---
title: Varyant ağırlıkları kullanarak satınalma siparişlerine çeşitli ürünler ekleme
description: Bu yordam, her ürün varyantı için satınalma siparişi satırlarını otomatik olarak doldurmak üzere varyant ağırlıklarının kullanılmasıyla ilgili açıklamalar içerir.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0199f4b05c23eec5c03c770c37111a6ee6d13efe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208398"
---
# <a name="add-variant-products-to-purchase-orders-using-variant-weights"></a>Varyant ağırlıkları kullanarak satınalma siparişlerine çeşitli ürünler ekleme

[!include [banner](../../includes/banner.md)]

Bu yordam, her ürün varyantı için satınalma siparişi satırlarını otomatik olarak doldurmak üzere varyant ağırlıklarının kullanılmasıyla ilgili açıklamalar içerir. Satın almak istediğiniz ürün miktarını seçtiğinizde, satınalma siparişi satırları ürün varyantlarında yapılandırılan ağırlıklar teme alınarak tüm ürün varyantları için önerilen miktarlarla oluşturulur. Bu yordam, ürün boyutları ve ürün çeşitlerinde ağırlık değerleri yapılandırma adımlarını içermez. Bu yordam USRT demo veri şirketini kullanır.

1. Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Genel bölümünün genişletilmiş görünümüne geçin.
6. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
9. Listede, istenen kaydı bulun ve seçin.
10. Listede, seçili satırdaki bağlantıya tıklayın.
11. Tamam'ı tıklatın.
12. Satır ayrıntıları bölümünün genişletilmiş görünümüne geçin.
13. Varyantlar sekmesine tıklayın.
14. Satır ekle'ye tıklayın.
15. Listede, seçili satırı işaretleyin.
16. Madde numarası alanına '0140' yazın.
17. Miktarı '1000' olarak ayarlayın.
18. Kaydet'e tıklayın.

