---
title: Ürün yaşam döngüsü durumunu serbest bırakılan bir ana ürüne atama
description: Bu yordam, serbest bırakılan bir ana ürüne ve onun ürün çeşitlerine nasıl ürün yaşam döngüsü durumu atanacağını açıklar.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9f8f519c54ffe4f1a2a44da51ac5d97c56182a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992232"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a>Ürün yaşam döngüsü durumunu serbest bırakılan bir ana ürüne atama

[!include [banner](../../includes/banner.md)]

Bu yordam, serbest bırakılan bir ana ürüne ve onun ürün çeşitlerine nasıl ürün yaşam döngüsü durumu atanacağını açıklar. Önkoşul: Bu görev kılavuzunu oynatabilmek için önce "Yeni ürün yaşam döngüsü durumu oluşturma" görev kılavuzunu oynatarak en az bir ürün yaşam döngüsü durumu oluşturmuş olduğunuzdan emin olmanız gerekir.


## <a name="find-a-released-product-master"></a>Serbest bırakılan bir ana ürünü bulma
1. Product information management > Products > Released products (Ürün bilgi yönetimi > Ürünler > Piyasaya sürülmüş ürünler) menüsüne gidin.
2. Listede, istenen kaydı bulun ve seçin.

> [!NOTE]
> Bir ana üründe Ürün alt türü Ana ürün bulunuyor.  

## <a name="update-the-lifecycle-state"></a>Yaşam döngüsü durumunu güncelleştirme
1. Düzenle öğesine tıklayın.
2. Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.
3. Kaydet'e tıklayın.
4. Evet'i tıklatın.

> [!NOTE]
> Evet seçilirse, serbest bırakılan ana ürünle aynı orijinal duruma sahip serbest bırakılmış tüm ilgili ürün çeşitleri de yeni ürün yaşam döngüsü durumuna güncelleştirilir. Hayır seçilirse tüm ürün çeşitlerinin geçerli durumları korunur. Serbest bırakılan ana üründen farklı ürün yaşam döngüsü durumuna sahip ürün çeşitleri güncelleştirilmez.  

## <a name="verify-the-lifecycle-state-of-the-variants"></a>Ürün çeşitlerinin yaşam döngüsü durumunu doğrulama
1. Serbest bırakılan ürün çeşitleri'ne tıklayın

> [!NOTE]
> Tüm ürün çeşitlerinin seçilen yaşam döngüsü durumunu serbest bırakılan ana üründen devraldığını unutmayın.  

2. Listede, seçili satırı işaretleyin.
3. Ürün yaşam döngüsü durumu alanına bir değer girin veya buradan bir değer seçin.

