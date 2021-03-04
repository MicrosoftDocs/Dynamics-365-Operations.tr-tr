---
title: Tercih edilen teklifi ayarlama
description: Servis anlaşması veya servis siparişi için bir tercih edilen teknisyen olarak herhangi bir çalışan seçebilirsiniz.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 850d91372fb1a918840ebc316a4479f4a70bdc24
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4438976"
---
# <a name="set-up-a-preferred-technician"></a>Tercih edilen teklifi ayarlama 

[!include [banner](../includes/banner.md)]


Servis anlaşması veya servis siparişi için bir tercih edilen teknisyen olarak herhangi bir çalışan seçebilirsiniz. Bununla birlikte, çalışanı uygun gönderme takımına dahil etmek iyi bir fikirdir; böylece çalışan **Gönderme panosu**'na dahil edilir.

## <a name="assign-employee-to-a-dispatch-team"></a>Çalışanı bir gönderilen ekibe atama

1.  **İnsan kaynakları** \> **Ortak** \> **Çalışanlar** \> **Çalışanlar**'a tıklayın. Çalışan ayrıntıları sayfasını açmak için çalışana çift tıklayın. **Eylem Bölmesi**'nde **Kurulum** \> **Gönderme takımı**'na tıklayarak **Gönderme çalışanları** formunu açın.

2.  **Gönderme takımı** alanında, çalışanın atanacağı takımı seçin.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Tercih edilen teknisyeni bir servis anlaşmasına atama

1.  **Servis yönetimi** \> **Ortak** \> **Servis sözleşmeleri** \> **Servis sözleşmeleri**'ne tıklayın. Ayrıntılar formunu açmak için bir servis sözleşmesine çift tıklayın.

2.  Uygun gönderme takımının bir üyesini servis anlaşması için tercih edilen teknisyen olarak atamak üzere **Genel** sekmesindeki **Tercih edilen teknisyen** listesini kullanın.

## <a name="assign-a-preferred-technician-to-a-service-order"></a>Tercih edilen teknisyeni bir servis siparişine atama

1.  **Servis yönetimi** \> **Periyodik** \> **Gönderme panosu**'na tıklayın.
    

    > [!NOTE]
    > <P><STRONG>Gönderme panosu</STRONG> formunda, görüntülemek istediğiniz gönderme faaliyetleri için bir tarih aralığı belirtin. Ayrıca, kapatılmış faaliyetlerin görüntülenip görüntülenmeyeceğini ve gönderme faaliyet listesini üyesi olduğunuz veya denetleme yetkisine sahip olduğunuz ekiplerle sınırlandırıp sınırlandırmayacağınızı da belirtin. <STRONG>Gönderme panosu</STRONG> formunu açmak için <STRONG>Tamam</STRONG>'ı tıklatın.</P>



2.  Değiştirilecek servis faaliyetinin satırını seçin.

3.  Uygun gönderme takımının bir üyesini servis çağrısı için tercih edilen teknisyen olarak atamak üzere **İlgili** sekmesindeki **Çalışan** listesini kullanın.

## <a name="see-also"></a>Ayrıca bkz.

[Servis sözleşmeleri geliştirme ve oluşturmaya genel bakış](service-agreements.md)

[Servis siparişlerini el ile oluşturma](create-service-orders-manually.md)

[Servis anlaşmaları (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]