--- 
title: "Varsayılan ürün yaşam döngüsü durumu oluşturma"
description: "Bu yordam, nasıl varsayılan ürün yaşam döngüsü durumu oluşturulacağını ve varsayılan durumu serbest bırakılan ürünlerle nasıl ilişkilendirileceğini açıklar."
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d445ea2f2362f146a1e3e7bcf747898dc2cc89ba
ms.openlocfilehash: 06a6c7c8fa767edf6fdf50c3c971b6d767f8755f
ms.contentlocale: tr-tr
ms.lasthandoff: 02/08/2018

---
# <a name="create-a-default-product-lifecycle-state"></a>Varsayılan ürün yaşam döngüsü durumu oluşturma

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, nasıl varsayılan ürün yaşam döngüsü durumu oluşturulacağını ve varsayılan durumu serbest bırakılan ürünlerle nasıl ilişkilendirileceğini açıklar.


## <a name="create-a-default-lifecycle-state"></a>Varsayılan yaşam döngüsü durumu oluşturma
1. Ürün bilgileri yönetimi > Kurulum > Ürün yaşam döngüsü durumu seçeneğine gidin.
2. Yeni'ye tıklayın.
3. Durum alanına bir değer yazın.
4. Tüzel kişiliğe serbest bırakıldığında varsayılan alanında Evet'i seçin.
5. Açıklama alanına bir değer girin.
6. Planlama için etkin alanında Hayır'ı seçin.

> [!NOTE]
> Yeni serbest bırakılan ürünün Master planlama dışında tutulması gerekiyorsa Hayır'ı seçin. Master planlamaya dahil edilmesi gerekiyorsa denetimi varsayılan değer olan Evet'te bırakın.  

## <a name="create-a-new-released-product"></a>Yeni bir serbest bırakılan ürün oluşturma
1. Sayfayı kapatın.
2. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
3. Yeni'ye tıklayın.
4. Ürün numarası alanında bir değer girin.
5. Ürün adı alanına bir değer girin.
6. Arama adı alanına bir değer yazın.
7. Model grubu alanına bir değer girin veya bir değer seçin.
8. Ürün grubu alanında bir değer girin veya bir değer seçin.
9. Stok boyutu grubu alanına bir değer girin veya bir değer seçin.
10. İzleme boyutu grubu alanına bir değer girin veya bir değer seçin.
11. Tamam'a tıklayın.

> [!NOTE]
> Varsayılan ürün yaşam döngüsü durumu genel bir tanımdır.  

## <a name="change-the-product-to-an-active-state"></a>Ürünü etkin duruma değiştirme
1. Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.

> [!NOTE]
> Etkin bir durum ayarladığınızı varsayalım: şimdi etkin durumu ürününün Master planlama ve ürün reçetesi seviyesinde hesaplamada kullanılmasına izin vermek üzere seçebilirsiniz. Bu, yalnızca tutarlı planlama için gerekli tüm ürün ayrıntılarının belirtilmiş olması durumunda bir anlam ifade etmektedir.  


