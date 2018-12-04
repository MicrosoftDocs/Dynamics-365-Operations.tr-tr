---
title: "Servis siparişi aşamaları"
description: "Servis siparişi aşamalarını tanımlayarak ve bunları çalışanlara atayarak, servis kuruluşundaki çeşitli kişilerin gerçekleştirdiği görevler üzerinden servis siparişi akışını kontrol edersiniz."
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9aa90dfcfc4b30d6cb4fa7ed4e6faaf505548d41
ms.contentlocale: tr-tr
ms.lasthandoff: 05/08/2018

---

# <a name="service-order-stages"></a>Servis siparişi aşamaları   

[!include [banner](../includes/banner.md)]


Tamamlanması gereken görevleri, hangi sırayla tamamlanacaklarını ve bunları tamamlamakla sorumlu çalışanları tanımlamak servis siparişi aşamaları ayarlayabilirsiniz. Servis siparişi aşamalarını tanımlayarak ve bunları çalışanlara atayarak, servis kuruluşundaki çeşitli kişilerin gerçekleştirdiği görevler üzerinden servis siparişi akışını kontrol edebilirsiniz. Aşamaların sırası bir başlangıç aşaması içermelidir.

Ayrıca her aşama için izin verilen eylemleri tanımlayabilirsiniz. Örneğin, son aşama haricindeki tüm aşamalar için **Deftere naklet** onay kutusu seçimini kaldırırsanız, servis siparişlerinin servis siparişleri tüm aşamalarla işlenmeden önce deftere nakledilmesini önlemiş olursunuz.

## <a name="branching-in-service-order-stages"></a>Servis siparişi aşamaları içinde dallara ayırma

Bir servis aşaması ayarladığınızda, daha sonraki servis aşaması için seçebileceğiniz birden çok seçenek ya da dal ayarlayabilirsiniz. Oluşturduğunuz tüm dallar ilk aşama tamamlandıktan sonra seçilebilir. Örneğin, başlangıç aşaması olarak **Planlama**'yı ayarladınız. **İşlemde** ve **İptal** adında iki aşama oluşturdunuz ve **Planlama**'yı bunların üst öğesi olacak şekilde seçtiniz. **Planlama** aşamasını satış siparişine atadınız. Satış siparişi için planlama aşaması tamamlandığında, satış siparişi üzerinde çalışmak için hazırsa **İşlemde** aşamasını ya da satış siparişi iptal edildiyse **İptal** aşamasını seçebilirsiniz.

## <a name="see-also"></a>Ayrıca bkz.

[Servis siparişi aşamalarını ayarla](set-up-service-order-stages.md)

[Servis siparişi aşamasını değiştirme](change-service-order-stage.md)

  



