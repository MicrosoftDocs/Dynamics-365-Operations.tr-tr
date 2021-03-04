---
title: Planlanan iş emirlerinde kapasite yükünü hesaplama
description: Bu konu, Varlık Yönetiminde, planlanan iş emirleriyle ilgili kapasite yükünün nasıl hesaplanacağını açıklamaktadır.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b817909ac0950b773cba775be2502b5796c6d8d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4439436"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Planlanan iş emirlerinde kapasite yükünü hesaplama

[!include [banner](../../includes/banner.md)]

 

Belirli bir dönem için kaynakların iş yükünün genel görünümünü almak için planlanan iş emirlerindeki kapasite yükünü hesaplayabilirsiniz. Hesaplamalar aşağıdaki kaynaklar için yapılabilir: Bakım görevlileri, çalışan grupları, araçlar ve varlıklar.

1. **Varlık yönetimi** > **Sorgular** > **Plan** > **Kapasite yükü**'ne tıklayın.

2. **Kapasite yükünü hesapla** iletişim kutusu > **Göster** alanında hesaplamak istediğiniz yük türünü seçin: **Kapasite**, **Ayrılmış** veya **Kalan**.

3. Sıfır içeren sonuçları göstermek istemiyorsanız, **Sıfırı atla** düğmesi üzerinde **Evet** seçeneğini belirleyin.

4. İlgili kaydırma düğmesinde **Evet**'i seçerek kapasite yükünü hesaplamak istediğiniz kaynak türlerini seçin: **Çalışan**, **Bakım görevlisi grubu**, **Araç** ve **Varlık**.

5. **Başlangıç tarihi** alanında otomatik hesaplama için başlangıç tarihini seçin.

6. **Aralık türü** alanında, hesaplama aralığını seçin: **Gün**, **Hafta**, **Ay** veya **Üç aylık dönem**.

7. **Dönem sıklığı** alanında, hesaplamak istediğiniz aralık sayısını ekleyin. Örneğin, aralık türü olarak **Gün** seçtiyseniz ve bu alana "5" sayısını eklerseniz, başlangıç tarihinden itibaren beş gün için bir hesaplama yapılır.

8. Hesaplamayı başlatmak için **Tamam**'a tıklayın.

Aşağıdaki şekil, **Ayrılmış** yük türü için üç haftayı kapsayan bir hesaplamanın sonucunu gösterir.

![Şekil 1](media/08-work-order-scheduling.png)

[!NOTE]
Hesaplamalarınız için **Kapasite** veya **Kalan** yük türlerini seçerseniz, seçili dönemde kaynaklar için rezervasyon yoksa aynı sonuç görüntülenir.

Bakım zamanlaması satırlarındaki ve zamanlanmamış iş emirlerindeki kapasite yükünün nasıl hesaplanacağı hakkında bilgi için bkz. [Kapasite yükünü hesaplama](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]