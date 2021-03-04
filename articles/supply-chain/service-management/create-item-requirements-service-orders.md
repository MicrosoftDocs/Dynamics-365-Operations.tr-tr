---
title: Servis siparişleri için madde gereksinimleri oluşturma
description: Bir servis siparişi için belirli maddeleri rezerve etmeniz gerekiyorsa, bunun için stok madde gereksinimleri oluşturabilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18484b637723cef43cad288c08ddfe53cddf9e03
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439422"
---
# <a name="create-item-requirements-for-service-orders"></a>Servis siparişleri için madde gereksinimleri oluşturma 

[!include [banner](../includes/banner.md)]


Müşterilerinize sağladığınız hizmetleri yönetmek ve izlemek için servis siparişi oluşturabilirsiniz. Bir servis siparişi için belirli maddeleri rezerve etmeniz gerekiyorsa, bunun için stok madde gereksinimleri oluşturabilirsiniz. Bir madde gereksinimi hemen stoktan tüketilebilir ya da madde için üretim emri başlatabilirsiniz.

Madde hareketi yerine madde gereksinimi kullanarak, madde gerçekten kullanılmadan hemen önce teslimat planı yapabilir, bir satın alma siparişi oluşturabilir, maddeyi ticari anlaşma çerçevesine dahil edebilir ve madde gereksinimini üretim planlamasına dahil edebilirsiniz.

Servis siparişleri için madde gereksinimleri bir proje aracılığıyla işlenir. Bir servis siparişinde madde gereksinimi oluşturmak için, servis siparişinin bir projeye atanmış olması gerekir. Servis siparişi için madde gereksinimi oluşturduktan sonra madde gereksinimini seçilen projenin **Projeler** formundan görüntüleyebilirsiniz.

## <a name="create-an-item-requirement-for-a-service-order"></a>Servis siparişi için madde gereksinimi oluşturma

1.  **Servis yönetimi** \> **Ortak** \> **Servis siparişleri** \> **Servis siparişleri**'ne tıklayın.

2.  Madde gereksinimi oluşturmak istediğiniz servis siparişini seçin.

3.  **Eylem Bölmesinde**, **Gönder** sekmesinde **Madde gereksinimi**'ne tıklayın.

4.  **Madde gereksinimleri** formunda, gereken madde için bilgileri girin. Belirli alanlar hakkında daha fazla bilgi için bkz. [Madde gereksinimleri (form)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Servis sözleşmesi için madde gereksinimi oluşturma

1.  **Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın.

2.  Madde gereksinimi oluşturmak istediğiniz servis sözleşmesini açın.

3.  **Satırlar** hızlı sekmesinde yeni bir satır oluşturmak için **Ekle**'ye tıklayın.

4.  **Hareket türü** alanında **Madde**'yi seçin.

5.  **Madde kurulumu** alanında **Madde gereksinimi**'ni seçin.

6.  **Madde numarası** alanında, servis sözleşmesi için gereken maddeyi seçin.

7.  **Satır ayrıntıları** hızlı sekmesinde, **Ürün boyutları** sekmesindeki **Tesis** alanında, madde için stok tesisi seçin.

8.  Bir sözleşme satırından servis siparişi oluşturmak için **Satırlar** hızlı sekmesinde **Servis siparişleri oluştur**'a tıklayın ve **Servis siparişleri oluştur** formuna ilgili bilgileri girin. 


## <a name="see-also"></a>Ayrıca bkz.

[Servis siparişlerini otomatik olarak oluşturma](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]