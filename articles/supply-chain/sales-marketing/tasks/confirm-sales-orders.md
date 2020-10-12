---
title: Satış siparişlerini onaylama
description: Bu yordam, satış siparişlerinin nasıl onaylanacağını göstermektedir.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup, SalesUnconfirmedOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7dcb60b524d375cbb533e88ea456eaa2c7ca6316
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830440"
---
# <a name="confirm-sales-orders"></a>Satış siparişlerini onaylama

[!include [banner](../../includes/banner.md)]

Bu yordam, satış siparişlerinin nasıl onaylanacağını göstermektedir. Tek bir siparişin ve aynı anda birden fazla siparişin nasıl onaylanacağı size gösterilecektir. Bu görevler genellikler satış siparişi işlemcisi tarafından yerine getirilir. Bu yordamı, demo verileri şirketi USMF'de veya kendi verilerinizde kullanabilirsiniz. Başlamadan önce aynı müşteri için birkaç açık satış siparişleri bulunduğundan emin olun. USMF kullanıyorsanız, US-027 müşterisini kullanabilirsiniz.


## <a name="confirm-a-single-sales-order"></a>Tek bir satış siparişini onaylayın
1. **Gezinti bölmesi > Modüller > Satış ve pazarlama > Satış siperişler > Tüm satış siparişleri**'ne gidin.
2. Listede, onaylamak istediğiniz siparişi bulun ve seçin.
3. Seçili siparişi açmak için satış siparişi numarasındaki bağlantıyı tıklatın.
4. **Eylem bölmesi**'nde, **Satış**'a tıklayın.
5. **Satış siparişini onayla**'ya tıklayın.
6. **Parametreler** bölümünü genişletin. **Deftere nakil** seçeneğinin 'Evet' olarak ayarlanmış olduğundan emin olun.  
7. **Onayı yazdır seçeneğini** 'Evet' olarak ayarlayın. **Kredi limitini denetle** alanı, bir müşterinin kalan kredisini hesaplamak için kullanılan yöntemi belirtir. Varsayılan olarak alacak hesapları parametreleri sayfasından kopyalanır. Kredi limiti denetimini belirli bir satış siparişini onaylarken atlamak istiyorsanız, **kredi limitini denetle**'yi 'Yok' olarak ayarlayın. Fakat, bu alan 'Yok' olarak bile ayarlanmış olsa, ana müşteri verilerinde **Zorunlu kredi limiti** seçeneği seçili ise, kredi limiti denetlemesinin yine de gerçekleşecek olacağını gözden kaçırmayın. 
8. **Tamam**'a tıklayın.
9. **Evet** seçeneğini tıklatın.
10. Sayfayı kapatın.
11. **Eylem Bölmesinde**, **Seçenekler**'e tıklayın.
12. **Görünümü değiştir** öğesine tıklayın.
13. **Başlık görünümü** öğesine tıklayın. Bir siparişi teyit edildiğinde, **Belge durumu**, 'Onay' olarak ayarlanır. 
14. **Eylem bölmesi**'nde, **Satış**'a tıklayın.
15. **Satış siparişi onayı**'na tıklayın.
16. Sayfayı kapatın.

## <a name="confirm-multiple-sales-orders-at-once"></a>Aynı anda birden fazla satış siparişi onayla
1. **Satış ve pazarlama > Satış siparişleri > Sipariş teyidi > Satış siparişini onayla** seçeneğine gidin.
2. **Seç**'e tıklayın.
3. **Aralık** sekmesindeki listede, **Müşteri hesabı** alanına başvuran kaydı bulun ve seçin.
4. **Ölçütler** alanında, açılır menü düğmesine tıklayarak aramayı açın.
5. Listede, bulmak ve toplu onaylamak istediğiniz birden fazla siparişi olan müşteri hesabını seçin. USMF kullanıyorsanız, hesap US-027'yi seçebilirsiniz.  
6. **Tamam**'a tıklayın.
    - **Genel** sekmesi, sorgu ölçütleriyle eşleşen siparişlerin bir listesini görüntüler. Bunlar onaya dahil edilir.  
    - **Parametreler** bölümünün **Özet güncelleştirmesi** alanı birden çok sipariş onayı bir tek onay belgesine özetlenirken kullanılacak parametreyi belirtir. Bu seçenek varsayılan olarak, **Alacak hesapları parametreleri** sayfasındaki **Özet güncelleştirme ayarının varsayılan değerlerinden** kopyalanır.  
7. **Özet güncelleştirme** alanında 'Sipariş'i seçin. Özet güncelleştirmeleri oluşturmak için gereken minimum parametreler **Fatura hesabı** ve **Para birimi**'dir. Başka bir deyişle, farklı fatura hesapları ve farklı para birimlerine sahip Özet güncelleştirmeleri verilmez. Ek parametreler, **Alacak hesapları parametreleri** sayfasından erişilebilen **Özet güncelleştirme parametreleri** sayfasında ayarlanabilir. 
8. **Satış siparişi** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
9. Listede, özet siparişe karşılık gelmesini istediğiniz bir sipariş numarası seçin.
10. **Düzenle**'ye tıklatın.
11. **Tamam**'a tıklayın.
12. **Tamam**'a tıklayın.

