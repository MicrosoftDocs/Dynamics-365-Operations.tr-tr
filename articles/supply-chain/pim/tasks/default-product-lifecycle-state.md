---
title: Varsayılan ürün yaşam döngüsü durumu oluşturma
description: Bu yordam, nasıl varsayılan ürün yaşam döngüsü durumu oluşturulacağını ve varsayılan durumu serbest bırakılan ürünlerle nasıl ilişkilendirileceğini açıklar.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a628ed2b609f48c22076f409889c212e4d9463ac
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578212"
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