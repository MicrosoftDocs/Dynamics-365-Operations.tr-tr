---
title: Varsayılan ürün yaşam döngüsü durumu oluşturma
description: Bu yordam, nasıl varsayılan ürün yaşam döngüsü durumu oluşturulacağını ve varsayılan durumu serbest bırakılan ürünlerle nasıl ilişkilendirileceğini açıklar.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b62d47f52da7f9e18bce401578a5e2a629ac5eb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818145"
---
# <a name="create-a-default-product-lifecycle-state"></a>Varsayılan ürün yaşam döngüsü durumu oluşturma

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]