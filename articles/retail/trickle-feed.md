---
title: Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma
description: Bu konuda, Microsoft Dynamics 365 Retail'deki perakende mağazası hareketleri için akış tabanlı sipariş oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: deb8399aa401af16b6fe123a433eb21864e178c6
ms.sourcegitcommit: 92322167f57b66d2accc134aaf862e6b9931ec94
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/31/2019
ms.locfileid: "2693101"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma (Genel önizleme)

[!include [banner](includes/banner.md)]

[!include [banner](includes/preview-banner.md)]

Dynamics 365 Retail 10.0.4 ve önceki sürümlerinde, perakende ekstresi deftere nakli gün sonunda gerçekleştirilen bir işlemdir ve tüm hareketler günün sonunda defterlere nakledilir. Büyük hareketler sınırlı bir zaman aralığında işlenmek zorunda olduğundan zaman zaman yük ve kilitlenmelere ve ekstre deftere nakil hatalarına yol açar. Ayrıca perakendeciler, gün içinde kendi defterlerinde gelir ve ödemeleri göremez.

Retail sürüm 10.0.5'te genel önizlemesi sunulan akış tabanlı sipariş oluşturma özelliğiyle hareketler gün içinde işlenir. Yalnızca ödemelerle ilgili mali mutabakat ve diğer nakit yönetimi hareketleri günün sonunda işlenir. Bu işlev satış siparişleri, faturalar ve ödemeler oluşturma yükünü gün içine dağıtarak daha iyi performans sağlar ve gelir ve ödemeleri defterlerde neredeyse gerçek zamanlı olarak görme olanağı tanır. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Akış tabanlı deftere nakil özelliğini kullanma
  
1. Perakende hareketlerin deftere akış tabanlı olarak nakledilmesi özelliğini etkinleştirmek için **Sistem yönetimi > Kurulum > Lisans yapılandırması**'na gidin ve **Perakende ekstreleri** anahtarını devre dışı bırakın.

2. Aynı sayfada **Perakende ekstreleri (akış) – Önizleme** lisans anahtarını etkinleştirin. Bu anahtarı etkinleştirdiğinizde, deftere nakledilmeyi bekleyen bir ekstre bulunmadığından emin olun. 

> [!Important]
> **Perakende ekstreleri (akış) - Önizleme** lisansı anahtarını etkinleştirmeden önce, deftere nakledilmeyi bekleyen ekstreler bulunmadığından emin olun.

3. Geçerli ekstre belgesi iki farklı türe bölünür: hareket ekstresi ve mali tablo.

      - Hareket ekstresi deftere nakledilmemiş ve doğrulanmış tüm perakende hareketlerini alır ve sizin yapılandırdığınız hızda satış siparişleri, satış faturaları, ödeme ve iskonto günlükleri ve gelir-gider hareketleri oluşturur. Bu işlemi, perakende hareketleri P işi aracılığıyla Retail Headquarters'a yüklenirken belgelerin oluşturulmasını sağlamak için yüksek sıklıkta çalışmak üzere yapılandırmanız gerekir. Satış siparişlerini ve satış faturalarını zaten oluşturan hareket ekstresi sayesinde **Stoğu deftere naklet** toplu işini yapılandırmanıza gerek yoktur. Ancak, bu yapılandırmayı özel iş gereksinimlerinizi karşılamak amacıyla kullanabilirsiniz.  
      
     - Mali tablo gün sonunda oluşturulacak şekilde tasarlanmıştır ve yalnızca **Vardiya** kapatma yöntemini destekler. Bu tablo mali mutabakatla sınırlandırılır ve yalnızca farklı ödemeler için sayılan tutar ile hareket tutarı arasındaki tutar farklarına yönelik günlükleri ve diğer nakit yönetimi hareketlerine ilişkin günlükleri oluşturur.   

4. Hareket ekstresini hesaplamak için **Perakende > Perakende BT > POS Deftere nakil > Hareket ekstrelerini toplu işte hesapla**'ya tıklayın. Hareket ekstrelerini toplu işle deftere nakletmek için **Perakende > Perakende BT > POS Deftere nakil > Hareket ekstrelerini toplu işle deftere naklet**'e tıklayın.

5. Mali tabloyu hesaplamak için **Perakende > Perakende BT > POS Deftere nakil > Mali tabloları toplu işte hesapla**'ya tıklayın. Mali tabloları toplu işle deftere nakletmek için **Perakende > Perakende BT > POS Deftere nakil > Mali tabloları toplu işle deftere naklet**'e tıklayın.

> [!NOTE]
> **Perakende > Perakende BT > POS Deftere nakil > Ekstreleri toplu işle hesapla** ve **Perakende > Perakende BT > POS Deftere nakil > Ekstreleri toplu işle deftere naklet** menü öğeleri bu yeni özellikle birlikte kaldırıldı.

Alternatif olarak, hareket ve mali tablo türlerini el ile oluşturabilirsiniz. **Perakende > Kanallar > Perakende mağazaları**'na gidin ve **Perakende ekstreleri**'ne tıklayın. **Yeni**'ye tıklayın ve oluşturmak istediğiniz ekstre türünü seçin. **Perakende ekstreleri** sayfasındaki alanlar ve sayfanın **Ekstre grubu** altındaki eylemler, seçilen ekstre türüne göre ilgili verileri ve eylemleri gösterir.
