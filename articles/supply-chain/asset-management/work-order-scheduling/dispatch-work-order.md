---
title: İş emri gönderme
description: Bu konuda Varlık Yönetimi'nde iş emri gönderme işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 026b34934d6527416a4632d8e1aee76a8836dcb0
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652023"
---
# <a name="dispatch-work-order"></a>İş emri gönderme

[!include [banner](../../includes/banner.md)]

 

**Gönder** işlevini kullanarak bir iş emri veya iş emri işlerini bir çalışana zamanlayabilirsiniz.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. Listeden iş emrini seçin. 

3. **Genel** sekmesinde, **Gönder** seçeneğine tıklayın.

4. **İş emrini zamanla** iletişim kutusunda **Çalışan** alanından çalışanı seçin.

5. **Saatleri zamanla** alanında, beklenen çalışma saatlerinin tahmin saatlerinden farklı olması durumunda beklenen çalışma saatleri ekleyebilirsiniz.

6. **Planlanan başlangıç** alanında, gerekirse başlangıç tarihi ve saatini düzenleyebilirsiniz.

7. Planlama işlemi başka işlerde zaten zamanlanmış olan kaynaklarla ilgili kapasite sınırlamalarını gözlemlemek zorundaysa **Varlık**, **Araç** ve **Çalışan** düğmelerinin **Evet** olarak ayarlandığından emin olun. Planlama işlemiyle ilgili ayrıntılı bilgi görmek istiyorsanız, **Ayrıntılı** düğmesinde **Evet** seçeneğini seçin. Bu, iş emrindeki hesaplanan puanlar hakkında ayrıntılı bilginin Bilgi günlüğünde gösterildiği anlamına gelir.

8. Takvimdeki kapatılmış günleri yok saymak için **Zamanlamayı yoksay** düğmesini **Evet** olarak ayarlayın (varlık, çalışan ve araçlara uygulanır). Planlamayla ilgili iş emrinde seçilmiş olabilecek sınırlamaları yok saymak için **Planlı yürütmeyi yoksay** düğmesini **Evet** olarak ayarlayın. 

    Zamanlanmış yürütme kurulumu hakkında bilgi için bkz. [Zamanlanmış yürütme](../setup-for-work-orders/scheduled-execution.md) bölümü.

9. **Tamam**'a tıklayın. İş emri yaşam döngüsü durumu otomatik olarak belirtilen **Zamanlandı** yaşam döngüsü durumuna güncelleştirilir **Varlık yönetimi** > **Kurulum** > **İş emirleri** > **Yaşam döngüsü modelleri**.

Aşağıdaki şekilde, **İş emrini zamanla** iletişim kutusundaki gönderme seçimlerinin bir örneği gösterilmektedir.

![Şekil 1](media/04-work-order-scheduling.png)

[!NOTE]
Bir iş emrindeki zamanlamayı silmek istiyorsanız, **Genel** sekmesinde **Tüm iş emirleri**'nden iş emrini seçip **Zamanlamayı sil**'e tıklayın. Zamanlamayı silerseniz iş emri yaşam döngüsü durumunu el ile güncelleştirmeyi unutmayın.

