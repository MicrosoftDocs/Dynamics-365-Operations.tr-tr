--- 
title: "Borç hesaplarından kıymetler oluşturma ve alma"
description: "Bu görev kılavuzu size satınalma işlemiyle sabit kıymet oluşturma ve alımını gösterecek."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9149378047fc22efbd401b7af86df07c1403e4f5
ms.openlocfilehash: cfe920b2ef493ab3ae36a9557001086ed99c3e4e
ms.contentlocale: tr-tr
ms.lasthandoff: 10/05/2017

---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Borç hesaplarından kıymetler oluşturma ve alma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzu size satınalma işlemiyle sabit kıymet oluşturma ve alımını gösterecek. Kılavuzda Muhasebeci, Borç hesabı memurları ve demo USMF şirketi kullanılmaktadır.


## <a name="set-fixed-assets-parameters"></a>Sabit kıymet parametrelerini ayarlayın
1. Sabit kıymetler > Kurulum > Sabit kıymet parametreleri'ne gidin.
2. Satınalma siparişleri bölümünü genişletin veya daraltın.
3. Satınalmadan kıymet alımına izin ver onay kutusunu işaretleyin.
4. Ürün girişi veya fatura deftere nakil işlemi sırasında kıymet oluştur onay kutusunu işaretleyin.

## <a name="create-a-new-vendor-invoice"></a>Yeni bir satıcı faturası oluşturun.
1. Borç hesapları > Çalışma alanları > Satıcı faturası girişi'ne gidin.
2. Yeni satıcı faturası'na tıklayın.
3. Fatura hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. Numara alanına bir değer girin.
6. Deftere nakil tarihi alanına bir tarih girin.
7. Satır ekle'ye tıklayın.
8. Madde numarası alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Sabit kıymet alımı için ya stoğu olmayan maddeler veya tedarik kategorileri kullanılabilir.  
9. Listede, seçili satırdaki bağlantıya tıklayın.
10. Miktar alanına bir sayı girin.
    * Bir fatura satırı, miktarı ne olursa olsun tek bir sabit kıymet oluşturur.  Fatura miktarı alanı değeri, sabit kıymet miktarına aktarılır.  
11. Birim fiyatı alanına bir sayı girin.
12. Satır ayrıntıları bölümünü genişletin veya daraltın.
13. Sabit kıymetler sekmesine tıklayın.
14. Yeni bir sabit kıymet oluştur onay kutusunu işaretleyin.
15. Sabit kıymet grubu alanında, açılır menü düğmesine tıklayarak aramayı açın.
16. Listede, yeni sabit kıymet oluşturulurken kullanılacak sabit kıymet grubunu seçin.
17. Listede, seçili satırdaki bağlantıya tıklayın.
18. Deftere Naklet öğesine tıklayın.
    * Sabit kıymet oluşturulur ve fatura deftere nakledildiğinde alınır.  


