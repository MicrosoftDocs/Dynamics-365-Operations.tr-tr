--- 
title: " Satınalma siparişleri için ürün paketleri oluşturma"
description: "Bu yordam, bir ürün paketi oluşturma ve bunu bir satınalma siparişinde kullanmayla ilgili süreci açıklamaktadır."
author: josaw1
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 8bbdbf882f6f73d03be0a036cb975109396e4a0d
ms.openlocfilehash: 9d3ea8702c79d8aa6bb7cf7caa922277697610fa
ms.contentlocale: tr-tr
ms.lasthandoff: 11/14/2017

---
# <a name="create-product-packages-for-purchase-orders"></a> Satınalma siparişleri için ürün paketleri oluşturma

[!include[task guide banner](../includes/task-guide-banner.md)]

Bu yordam, bir ürün paketi oluşturma ve bunu bir satınalma siparişinde kullanmayla ilgili süreci açıklamaktadır. Satınalma siparişi, önceden tanımlanmış bir ürün kümesi için sipariş oluşturmak amacıyla kullanılır. Bu yordam, USRT demo veri şirketini kullanır.


## <a name="create-a-product-package"></a>Ürün paketi oluşturma
1. Retail and commerce > Inventory management > Replenishment > Product packages (Perakende ve ticaret > Stok yönetimi > Stok yenileme > Ürün paketleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Paket numarası alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
6. Listede, seçili satırdaki bağlantıya tıklayın.
7. Ekle öğesini tıklatın.
8. Madde numarası alanına '0160' yazın.
9. Boyut alanında, aramayı açmak için açılır menü düğmesine tıklayın.
10. Listede, seçili satırdaki bağlantıya tıklayın.
11. Miktar alanına bir sayı girin.
12. Ekle öğesini tıklatın.
13. Madde numarası alanına '0160' yazın.
14. Varyant numarası alanında, aramayı açmak için açılır menü düğmesine tıklayın.
15. Listede, seçili satırdaki bağlantıya tıklayın.
16. Miktar alanına bir sayı girin.
17. Ekle öğesini tıklatın.
18. Madde numarası alanına '0175' yazın.
19. Miktar alanına bir sayı girin.
20. Kaydet'e tıklayın.
21. Sayfayı kapatın.

## <a name="add-package-to-purchase-order"></a>Paketi satınalma siparişine ekleme
1. Accounts payable > Purchase orders > All purchase orders (Borç hesapları > Satınalma siparişleri > Tüm satınalma siparişleri) menüsüne gidin.
2. Yeni'ye tıklayın.
3. Satıcı hesabı alanında, açılır menü düğmesine tıklayarak aramayı açın.
4. Ürün paketi oluşturulurken bir satıcı seçildiyse, listeden aynı satıcıyı seçin.
5. Genel bölümünün genişletilmiş görünümüne geçin.
6. Tesis alanında, aramayı açmak için açılır menü düğmesine tıklayın.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Ambar alanında, açılır menü düğmesine tıklayarak aramayı açın.
9. Listede, seçili satırdaki bağlantıya tıklayın.
10. Tamam'ı tıklatın.
11. Satır ayrıntıları bölümünün genişletilmiş görünümüne geçin.
12. Ürün paketleri sekmesine tıklayın.
13. Satınalma siparişi satırına tıklayın.
14. Paketten satırlar oluştur'a tıklayın.
15. Listede, önceki adımda oluşturduğunuz ürün paketi bulun ve seçin.
16. Miktar alanına bir sayı girin.
17. Oluştur'a tıklayın.
18. Kaydet'e tıklayın.


