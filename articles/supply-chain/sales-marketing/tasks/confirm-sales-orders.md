---
title: Satış siparişlerini onaylama
description: Bu yordam, satış siparişlerinin nasıl onaylanacağını göstermektedir.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c01c5e070954b3791df3cb67ba7c4f4ec79e3003
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833990"
---
# <a name="confirm-sales-orders"></a>Satış siparişlerini onaylama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, satış siparişlerinin nasıl onaylanacağını göstermektedir. Tek bir siparişin ve aynı anda birden fazla siparişin nasıl onaylanacağı size gösterilecektir. Bu görevler genellikler satış siparişi işlemcisi tarafından yerine getirilir. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Başlamadan önce aynı müşteri için birkaç açık satış siparişleri bulunduğundan emin olun. USMF kullanıyorsanız, US-027 müşterisini kullanabilirsiniz.


## <a name="confirm-a-single-sales-order"></a>Tek bir satış siparişini onaylayın
1. Sales and marketing > Sales orders > All sales orders (Satış ve pazarlama > Satış siparişleri > Tüm satış siparişleri) menüsüne gidin.
2. Listede, onaylamak istediğiniz siparişi bulun ve seçin.
3. Seçili siparişi açmak için satış siparişi numarasındaki bağlantıyı tıklatın.
4. Eylem Bölmesinde, Satış'a tıklayın.
5. Satış siparişini onayla'ya tıklayın.
6. Parametreler bölümünü genişletin veya daraltın.
    * Deftere naklet evet alanının etkin olduğundan emin olun.  
7. Onayı yazdır seçeneğini Evet olarak ayarlayın.
    * Kredi limitini denetle alanı, bir müşterinin kalan kredisini hesaplamak için kullanılan yöntemi belirtir. Varsayılan olarak alacak hesapları parametreleri sayfasından kopyalanır. Kredi limiti denetimini belirli bir satış siparişini onaylarken atlamak istiyorsanız, kredi limitini denetle'yi Yok olarak ayarlayın. Fakat, bu alan Yok olarak bile ayarlanmış olsa, ana müşteri verilerinde Zorunlu kredi limiti seçeneği seçili ise, kredi limiti denetlemesinin yine de gerçekleşecek olacağını gözden kaçırmayın.  
8. Tamam'a tıklayın.
9. Evet'i tıklatın.
10. Sayfayı kapatın.
11. Eylem Bölmesinde, Seçenekler'e tıklayın.
12. Görünümü değiştir'e tıklayın.
13. Başlık görünümü'ne tıklayın.
    * Bir siparişi teyit edildiğinde, Belge durumu, Onay olarak ayarlanır.  
14. Eylem Bölmesinde, Satış'a tıklayın.
15. Satış siparişi onayını görüntüle'ye tıklayın.
16. Sayfayı kapatın.

## <a name="confirm-multiple-sales-orders-at-once"></a>Aynı anda birden fazla satış siparişi onayla
1. Satış ve pazarlama > Satış siparişleri > Sipariş teyidi > Satış siparişi onayla seçeneğine gidin.
2. Seç'e tıklayın.
3. Aralık sekmesindeki listede, müşteri hesabı alanına ilişkin kaydı bulun ve seçin.
4. Ölçütler alanında, açılır menü düğmesine tıklayarak aramayı açın.
5. Listede, bulmak ve toplu onaylamak istediğiniz birden fazla siparişi olan müşteri hesabını seçin.
    * USMF kullanıyorsanız, hesap US-027'yi seçebilirsiniz.  
6. Tamam'a tıklayın.
    * Genel sekmesi, sorgu ölçütleriyle eşleşen siparişlerin bir listesini görüntüler. Bunlar onaya dahil edilir.  
    * Alana ilişkin Özet güncelleştirme,birden çok sipariş onayının bir tek onay belgesine özetlenirken kullanılacak parametreyi belirtir. Bu seçenek varsayılan olarak, Alacak hesapları parametreleri sayfasındaki Özet güncelleştirme seçeneğinin varsayılan değerlerinden kopyalanır.  
7. Alana ilişkin Özet güncelleştirmede 'Sırala' seçin.
    * Özet güncelleştirmeleri oluşturmak için gereken minimum parametreler Fatura hesabı ve Para birimidir. Başka bir deyişle, farklı fatura hesapları ve farklı para birimlerine sahip Özet güncelleştirmeleri verilmez. Ek parametreler, alacak hesapları parametreleri sayfasından erişilebilen Özet güncelleştirme parametreleri sayfasında ayarlanabilir.  
8. Satış siparişi alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, özet siparişe karşılık gelmesini istediğiniz bir sipariş numarası seçin.
10. Yerleştir'i tıklatın.
11. Tamam'a tıklayın.
12. Tamam'a tıklayın.

