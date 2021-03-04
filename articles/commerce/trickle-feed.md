---
title: Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma
description: Bu konuda, Microsoft Dynamics 365 Commerce'taki mağaza hareketleri için akış tabanlı sipariş oluşturma işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1f864fd6e3aa62cabd039922ed55ad5f7714f0ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991374"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Perakende mağaza hareketleri için akış tabanlı sipariş oluşturma

[!include [banner](includes/banner.md)]

Dynamics 365 Retail 10.0.4 ve önceki sürümlerinde, ekstre deftere nakli gün sonunda gerçekleştirilen bir işlemdir ve tüm hareketler günün sonunda defterlere nakledilir. Büyük hareketler sınırlı bir zaman aralığında işlenmek zorunda olduğundan zaman zaman yük ve kilitlenmelere ve ekstre deftere nakil hatalarına yol açar. Ayrıca perakendeciler, gün içinde kendi defterlerinde gelir ve ödemeleri göremez.

Retail sürüm 10.0.5'te sunulan akış tabanlı sipariş oluşturma özelliğiyle hareketler gün içinde işlenir. Yalnızca ödemelerle ilgili mali mutabakat ve diğer nakit yönetimi hareketleri günün sonunda işlenir. Bu işlev satış siparişleri, faturalar ve ödemeler oluşturma yükünü gün içine dağıtarak daha iyi performans sağlar ve gelir ve ödemeleri defterlerde neredeyse gerçek zamanlı olarak görme olanağı tanır. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Akış tabanlı deftere nakil özelliğini kullanma
  
1. Perakende hareketlerinin akışa tabanlı olarak deftere naklini sağlamak için, Özellik yönetimini kullanarak **Perakende ekstreleri - Akış** adlı özelliği etkinleştirin.

    > [!IMPORTANT]
    > Özelliği etkinleştirmeden önce, deftere nakledilmeyi bekleyen ekstre bulunmadığından emin olun.

2. Geçerli ekstre belgesi iki türe bölünür: hareket ekstresi ve mali tablo.

      - Hareket ekstresi, deftere nakledilmemiş ve doğrulanmış tüm hareketleri alır ve yapılandırdığınız hızda satış siparişleri, satış faturaları, ödeme ve iskonto günlükleri ve gelir-gider hareketleri oluşturur. Bu işlemi, hareketleri P işi aracılığıyla Genel Merkez'e yüklenirken belgelerin oluşturulmasını sağlamak için yüksek sıklıkta çalışmak üzere yapılandırmanız gerekir. Satış siparişlerini ve satış faturalarını zaten oluşturan hareket ekstresi sayesinde **Stoğu deftere naklet** toplu işini yapılandırmanıza gerek yoktur. Ancak, bu yapılandırmayı özel iş gereksinimlerinizi karşılamak amacıyla kullanabilirsiniz.  
      
     - Mali tablo gün sonunda oluşturulacak şekilde tasarlanmıştır ve yalnızca **Vardiya** kapatma yöntemini destekler. Bu tablo, mali mutabakatla sınırlandırılır ve yalnızca farklı ödemeler için sayılan tutar ile hareket tutarı arasındaki tutar farklarına yönelik günlükleri ve diğer nakit yönetimi hareketlerine ilişkin günlükleri oluşturur.   

3. Hareket ekstresini hesaplamak için **Retail ve Commerce > Retail ve Commerce BT > POS Deftere Nakli > Hareket ekstrelerini toplu olarak hesapla**'ya gidin. Hareket ekstrelerini toplu işle deftere nakletmek için **Retail ve Commerce > Retail ve Commerce BT > POS Deftere Nakli > Hareket ekstrelerini toplu olarak deftere naklet**'e gidin.

4. Mali tabloyu hesaplamak için **Retail ve Commerce > Retail ve Commerce BT > POS Deftere Nakli > Mali tabloları toplu olarak hesapla**'ya gidin. Mali tabloları toplu işle deftere nakletmek için **Retail ve Commerce > Retail ve Commerce BT > POS Deftere Nakli > Mali tabloları toplu işle deftere naklet**'e gidin.

> [!NOTE]
> **Retail ve Commerce > Retail ve Commerce BT > POS deftere nakli > Ekstreleri toplu işle hesapla** ve **Retail ve Commerce > Retail ve Commerce BT > POS deftere nakli > Ekstreleri toplu işle deftere naklet** menü öğeleri bu yeni özellikle birlikte kaldırıldı.

Alternatif olarak, hareket ve mali tablo türlerini el ile oluşturabilirsiniz. **Retail ve Commerce > Kanallar > Mağazalar**'a gidin ve **Ekstreler**'e tıklayın. **Yeni**'ye tıklayın ve oluşturmak istediğiniz ekstre türünü seçin. **Ekstreler** sayfasındaki alanlar ve sayfanın **Ekstre grubu** altındaki eylemler, seçilen ekstre türüne göre ilgili verileri ve eylemleri gösterir.


[!INCLUDE[footer-include](../includes/footer-banner.md)]