---
title: Servis nesnelerine genel bakış
description: Servis nesneleri, üzerinde servis gerçekleştirebileceğiniz müşteri kıymetleri ve ürünleridir.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ac26083609a337a8d78929dd6f736e1a7c26767
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215160"
---
# <a name="service-objects-overview"></a>Servis nesnelerine genel bakış

[!include [banner](../includes/banner.md)]

Servis nesneleri, üzerinde servis gerçekleştirebileceğiniz müşteri kıymetleri ve ürünleridir. Sağladığınız servis tipine bağlı olarak, parçalar maddi veya maddi olmayan parçalar olabilir:

-  Maddi parçalar, üzerlerinde fiziksel bir servis görevi gerçekleştirebileceğiniz, makine veya bina gibi şeylerdir.

    Fiziki servis nesnesi, Serbest bırakılan ürün ayrıntıları formunda oluşturduğunuz bir stok maddesi de olabilir. Maddeye iliştirdiğiniz stok boyut grubuna bağlı olarak servis nesnesini madde seri numarası ayrıntı düzeyine kadar oluşturabilirsiniz. Bu, servis nesnesinin temsil ettiği tam maddeyi izlemeniz gerektiğinde yararlı olur.

    Ancak, fiziki servis nesnesi aynı zamanda bir şirketin doğrudan üretim veya tedarik zinciriyle ilişkili bir madde de olmayabilir. Örneğin, servis siparişindeki onarımlar için kullanılan bir araç seti stoka dahil edilmeyen bir servis nesnesi olabilir. Bu durumda, bunu bir stok maddesi olarak kaydetmezsiniz.

-  Maddi olmayan nesneler, üzerlerinde servis görevleri gerçekleştirebileceğiniz, hesap kümesi veya yasal bir belge gibi fiziki olmayan öğelerdir.

## <a name="example-of-an-intangible-service-object"></a>Maddi olmayan servis nesnesi örneği

Şirket A, birkaç küçük şirketin mali kayıtlarını tutuyor. Şirket A'nın müşterilerinden biri, yerel bir futbol takımı. Şirket A kulübün hesapları için haftalık olarak defter tutmaktan ve yıllık denetimden sorumlu. Kulübün hesapları Servis nesneleri formunda ayarlanıyor ve servis sözleşmesinde nesne olarak belirtiliyor. Nesne için iki servis sözleşmesi satırı bulunuyor. Satır 1, satıra atanan haftalık aralıklı haftalık defter tutma ve satır 2, kendisine atanan yıllık aralıklı yıllık denetimdir.

## <a name="related-topics"></a>İlgili konular

[Servis nesneleri oluşturma](create-service-objects.md)

