---
title: Ana ürün oluşturma
description: Önceden tanımlanmış çeşitler için ana ürün oluşturun.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdb30b46a0e5a6d4fac997588dd47148f2664c03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439296"
---
# <a name="create-a-product-master"></a>Ana ürün oluşturma

[!include [banner](../../includes/banner.md)]

Önceden tanımlanmış çeşitler için ana ürün oluşturun. Bu yöntemi oluşturmak için kullanılan demo veri şirketi USMF'dir. Bu yordam, ürün tasarımcılarına yöneliktir.


## <a name="create-a-new-product-master"></a>Yeni bir ana ürün oluşturma
1. **Gezinti bölmesi > Modüller > Ürün bilgileri yönetimi > Ürünler > Ana ürünler**'e gidin.
2. **Yeni**'ye tıklayın.
3. **Ürün numarası** alanında bir değer girin. Numaranın benzersiz olması gerekir. **Ürün numarası** alanı için bir numara serisi ayarlanabilir. Bu durumda, kullanıcı bir değer girmesi gerekmez.
4. **Ürün adı** alanına bir değer yazın. Açıklayıcı bir ürün adı girin. Değer için arama adı varsayılan olarak, ancak bu kullanıcı tarafından değiştirilebilir.
5. **Ürün boyutu grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın. Ürün boyut grubu, ürün çeşitleri oluşturmak için 4 ürün boyutundan hangisinin kullanılabileceğini belirler. Bu örnek, renk ve boyut boyutları olan bir grup kullanır.
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın. Varsayılan **Yapılandırma teknolojisi** 'Önceden tanımlanmış çeşit'tir. Bu örnek için kullanılacaktır.
8. **Tamam**'a tıklayın.

## <a name="select-product-dimension-groups"></a>Ürün boyut gruplarını seçin
1. **Renk grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
2. Listede, istenen kaydı bulun ve seçin.
3. Listede, seçili satırdaki bağlantıya tıklayın.
4. **Ebat grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın.
5. Listede, istenen kaydı bulun ve seçin.
6. Listede, seçili satırdaki bağlantıya tıklayın.

## <a name="add-dimension-groups"></a>Boyut grupları ekleme
1. **Eylem Bölmesi**'nde, **Ürün**'e tıklayın.
2. İletişim kutusunu açmak için **Boyut grupları**'ına tıklayın.
3. **Depolama boyutu grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın. Depolama stok boyutları maddelerin nasıl depolandığını ve stoktan alındığını kontrol etmenize yardım eder. Örneğin, bir depolama boyutuna tesis ve ambar dahil olabilir.
4. Listede, istenen kaydı bulun ve seçin.
5. Listede, seçili satırdaki bağlantıya tıklayın.
6. **İzleme boyutu grubu** alanında, aramayı açmak için açılır menü düğmesine tıklayın. İzleme boyutu grubu hangi izleme boyutlarını bir ürüne atayabileceğinizi belirler. Örneğin, toplu iş numarası ve seri numarası, stok maddelerini izlemek için kullanılır.
7. Listede, istenen kaydı bulun ve seçin.
8. Listede, seçili satırdaki bağlantıya tıklayın.
9. **Tamam**'a tıklayın.
10. **Kaydet**'e tıklayın.
11. Sayfayı kapatın.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]