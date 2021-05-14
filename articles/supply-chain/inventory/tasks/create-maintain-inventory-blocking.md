---
title: Stok durdurma oluştur ve sürdür
description: Bu konu, stok durdurmanın eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemek üzere nasıl kullanılacağını gösterir.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956170"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>Stok durdurma oluştur ve sürdür

[!include [banner](../../includes/banner.md)]

Bu konu, stok durdurmanın eldeki fiziksel stokun başka çıkış kaynak belgeleri tarafından rezerve edilmesini önlemek üzere nasıl kullanılacağını gösterir. Bu konudaki prosedürlere başlamadan önce, fiziksel eldeki stoğun kullanılabilir olduğu bir öğenizin olması gerekir.

## <a name="block-inventory"></a>Stoku engelle

Stoğun durdurabilmesi için stok durdurma kaydı oluşturmak üzere aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Stok durdurma**'ya gidin.
1. Eylem Bölmesinde, **Yeni**'yi seçin.
1. Yeni durdurma kaydının başlığında, **Öğe numarası** alanını durdurmak istediğiniz öğeye ayarlayıp bir açıklama girin.
1. **Genel** hızlı sekmesinde, **Miktar** alanına durdurulacak öğe sayısını girin.
1. **Stok boyutları** hızlı sekmesinde, durdurmak istediğiniz öğelerin bulunduğu tesisi ve ambarı belirtin.
1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="update-the-conditions-of-the-inventory-blocking"></a>Stok durdurma koşullarını güncelleştirin

Stok durdurma kaydını güncelleştirmek için aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Stok durdurma**'ya gidin.
1. Liste bölmesinde, ilgili durdurma kaydını seçin.
1. Kaydı, gerektiği şekilde düzenleyin. Örneğin, durdurulan stoğun rezervasyon için ne zaman kullanılabilir hale geleceğini belirtmek için **Beklenen tarih** alanının değerini değiştirebilirsiniz. **Beklenen girişler** seçeneği seçilmişse tarih, beklenen harekette görüntülenir. (Manuel olarak bir durdurma kaydı oluşturduğunuzda, **Beklenen girişler** seçeneği varsayılan olarak seçilir.)
1. Eylem bölmesinde, **Kaydet**'i seçin.

## <a name="unblock-inventory"></a>Stok durdurmayı kaldırma

Stoğun durdurmasını kaldırmak için stok durdurma kaydını kaldırmak üzere aşağıdaki adımları izleyin.

1. **Stok yönetimi \> Periyodik görevler \> Stok durdurma**'ya gidin.
1. Liste bölmesinde, ilgili durdurma kaydını seçin.
1. Eylem Bölmesi'nde **Sil**'i seçin.
1. İşlemi onaylamanız istenir. Devam etmek için **Eve**'i seçin.
1. Sayfayı kapatın.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
