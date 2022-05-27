---
title: Borç hesaplarından kıymetler oluşturup alın
description: Bu yordam, satınalma işlemiyle bir sabit kıymet oluşturmayı ve alımını açıklar.
author: moaamer
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters, VendInvoiceWorkspace, VendEditInvoice, VendTableLookup, InventItemIdLookupSimple, AssetTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4290ced6bcf4432583cffc9122a4bba86266a559
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713627"
---
# <a name="create-and-acquire-assets-from-accounts-payable"></a>Borç hesaplarından kıymetler oluşturup alın

[!include [banner](../../includes/banner.md)]

Bu yordam, satınalma işlemiyle bir sabit kıymet oluşturmayı ve alımını açıklar.  Kılavuzda Muhasebeci, Borç hesabı memurları ve demo USMF şirketi kullanılmaktadır.


## <a name="set-fixed-assets-parameters"></a>Sabit kıymet parametrelerini ayarlayın
1. **Gezinti bölmesinde** **Modüller > Sabit kıymetler > Kurulum > Sabit kıymet parametreleri**'ne gidin.
2. **Satınalma siparişleri** hızlı sekmesini genişletin.
3. **Satınalmadan varlık alımına izin ver** onay kutusunu işaretleyin.
4. **Ürün girişi veya fatura deftere nakil işlemi sırasında varlık oluştur** onay kutusunu işaretleyin.

## <a name="create-a-new-vendor-invoice"></a>Yeni bir satıcı faturası oluşturun.
1. **Gezinti bölmesinde** **Modüller > Borç hesapları > Çalışma alanları > Satıcı faturası girişi**'ne gidin.
2. **Yeni satıcı faturası**'na tıklayın.
3. **Fatura hesabı** alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Listede, seçili satırdaki bağlantıya tıklayın.
5. **Numara** alanına bir değer girin.
6. **Deftere nakil tarihi** alanına bir tarih girin.
7. **Satır ekle**'ye tıklayın.
8. **Madde numarası** alanında, açılır menü düğmesine tıklayarak aramayı açın. Sabit kıymet alımı için ya stoğu olmayan maddeler veya tedarik kategorileri kullanılabilir.  
9. Listede, seçili satırdaki bağlantıya tıklayın.
10. **Miktar** alanına bir sayı girin. Bir fatura satırı, miktarı ne olursa olsun tek bir sabit kıymet oluşturur. Fatura miktarı alanı değeri, sabit kıymet miktarına aktarılır.  
11. **Birim fiyatı** alanına bir sayı girin.
12. **Satır ayrıntıları** hızlı sekmesini genişletin.
13. **Sabit kıymetler** sekmesine tıklayın.
14. **Yeni bir sabit kıymet oluştur** onay kutusunu işaretleyin.
15. **Sabit kıymet grubu** alanında, açılır menü düğmesine tıklayarak aramayı açın.
16. Listede, yeni sabit kıymet oluşturulurken kullanılacak sabit kıymet grubunu seçin.
17. Listede, seçili satırdaki bağlantıya tıklayın.
18. **Naklet**'e tıklayın. Sabit kıymet oluşturulur ve fatura deftere nakledildiğinde alınır.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
