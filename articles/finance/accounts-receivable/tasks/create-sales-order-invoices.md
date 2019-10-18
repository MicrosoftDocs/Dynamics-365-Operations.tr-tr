---
title: Satış siparişi faturaları oluşturma
description: Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a41524c773284812aa6eebddcd832c78bd29166
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180383"
---
# <a name="create-sales-order-invoices"></a>Satış siparişi faturaları oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu görev kılavuzunda fatura birleştirme ve toplu işlem dahil bir satış siparişini faturalama açıklanmaktadır. Bu yordam, USMF demo şirketini kullanır.


## <a name="create-an-invoice-from-a-sales-order"></a>Satış siparişinden fatura oluşturma
1. **Gezinti bölmesi > Modüller > Alacak hesapları > Siparişler > Sevk edilen ancak faturalanmayan satış siparişleri**'ne gidin.
2. Listeden bir satış siparişi seçin. 
3. **Eylem Bölmesinde**, **Fatura > Oluştur > Fatura** öğesine tıklayın. Bu satış siparişiyle ilişkilendirilmiş birden fazla sevk irsaliyesi bulunmaktadır. Sevk irsaliyesi numarası yerine <multiple> sözcüğü görüntülenecektir.  
4. **Parametreler** bölümünü genişletin.
    - Faturanın deftere nakledilebilmesi için Nakil öğesinin Evet olarak ayarlanması gerekir. Deftere nakli devre dışı bırakıp yalnızca faturayı yazdırmayı da seçebilirsiniz. Ancak, fatura yerine bir proforma fatura hazırlayarak da aynı sonucu elde edebilirsiniz.  
    - Bu seçenek, toplu işler için kullanılır. Toplu iş çalıştırıldığında, sorgu çalıştırılır.
5. **Yazdırma** alanında 'Sonra'yı seçin.
6. **Fatura yazdır** için **Evet**'i seçin. Yazdırma yönetimi, faturanın birden çok kopyasını yazdırabilir ve aynı zamanda faturayı bir PDF dosyası olarak e-posta yoluyla gönderebilir.  
7. **Masrafları yazdır** alanında 'Özetle'yi seçin.
8. **Kredi limitini denetle** alanında 'Bakiye'yi seçin.
9. **İptal**'e tıklayın

## <a name="combine-orders-into-a-single-invoice"></a>Siparişleri tek bir faturada birleştirme
1. **Gezinti bölmesi > Modüller > Alacak hesapları > Siparişler > Tüm satış siparişleri**'ne gidin.
2. Birden fazla açık faturası olan bir müşteri bulun.
3. Aynı müşterideki birden çok açık satış siparişini seçin.
4. **Eylem Bölmesinde**, **Fatura > Oluştur > Fatura** öğesine tıklayın.
5. **Parametreler** bölümünü genişletin.
6. **Miktar** alanında "Tümü"nü seçin. Genel bakış sekmesinde iki fatura bulunmaktadır. Şimdi bunları tek bir faturada birleştirin.  
7. **Özet güncelleştirme kapsamı** alanında 'Fatura hesabı'nı seçin.
8. Satış siparişlerini tek bir faturada birleştirmek için **Düzenle**'ye tıklayın. İki satış siparişi artık tek bir fatura birleştirilmiştir.   
9. **İptal**'e tıklayın
10. **Evet** seçeneğini tıklatın.

## <a name="post-invoices-in-a-batch"></a>Faturaları toplu işte deftere nakletme
1. **Gezinti bölmesi > Modüller > Alacak hesapları > Faturalar > Toplu faturalama**'ya gidin.
2. **Seç**'e tıklayın.
3. **Tamam**'a tıklayın.
4. **Toplu iş** öğesine tıklayın.
5. **Toplu işlem** için **Evet**'i seçin.
6. **Yineleme**'ye tıklayın.
7. **Günler**'i seçin
8. **Tamam**'a tıklayın.
9. **Tamam**'a tıklayın.
10. **İptal**'e tıklayın
11. **Evet** seçeneğini tıklatın.
