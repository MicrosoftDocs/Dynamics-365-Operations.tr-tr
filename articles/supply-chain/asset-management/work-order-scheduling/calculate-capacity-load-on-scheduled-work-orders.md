---
title: Planlanan iş emirlerinde kapasite yükünü hesaplama
description: Bu konu, Varlık Yönetiminde, planlanan iş emirleriyle ilgili kapasite yükünün nasıl hesaplanacağını açıklamaktadır.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ff244e51151a1cc0485cae25873566fa97253171516d48449fed75f070146431
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766230"
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

![Şekil 1.](media/08-work-order-scheduling.png)

[!NOTE]
Hesaplamalarınız için **Kapasite** veya **Kalan** yük türlerini seçerseniz, seçili dönemde kaynaklar için rezervasyon yoksa aynı sonuç görüntülenir.

Bakım zamanlaması satırlarındaki ve zamanlanmamış iş emirlerindeki kapasite yükünün nasıl hesaplanacağı hakkında bilgi için bkz. [Kapasite yükünü hesaplama](../capacity-planning/calculate-capacity-load.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]