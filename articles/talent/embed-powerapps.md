---
title: Power Apps uygulamalarını Dynamics 365 - Core HR içine katıştırma
description: Bu konu, Microsoft Power Apps menü öğesinin Sistem yönetim modülünden kaybolduğu sorunu ortadan kaldırmayı açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b1dd1756be349d85af8e6d7159623a2a95e75526
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898724"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>Power Apps uygulamalarını Dynamics 365 - Core HR içine katıştırma

**Çıkış**

**Power Apps** menü öğesi, **Sistem yönetimi** modülünden kayboldu.

**Nedeni**

Kullanıcı arabirimi (UI) tasarımı değiştirildi ve Microsoft Power Apps, şimdi standart kişiselleştirme modeline dahildir.

**Çözünürlük**

Power Apps'ın katıştırılma şekli değiştirildi. Artık Power Apps kişiselleştirme modeli aracılığıyla eklenir. Power Apps'i Microsoft Dynamics 365 Talent içinde neredeyse her sayfaya ekleyebilirsiniz.

Talent içerisinde Power Apps'in nasıl katıştırılacağı hakkında bilgi için bkz. [Microsoft Power Apps'i katıştırma](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Değişimden önce uygulamalarını katıştırmış olan her Power Apps kullanıcısının yeni modele yükseltilmiş olması gerekir.

**Power Apps** düğmesi, Talent içindeki neredeyse her sayfanın sağ üst kösesindedir. Power Apps'i eklemek için bu düğmeyi kullanın.

Aşağıda bir örnek verilmiştir.

1. **Personel yönetimi \> Bağlantılar \> Çalışanlar \> Personel**.
2. **Power Apps** düğmesini seçin ve sonra **Bir PowerApp ekle**'yi seçin.

    ![Power Apps düğmesi](media/png.png)

3. **Bir PowerApp ekleyin** iletişim kutusundaki alanları tamamlayın.

    ![Bir PowerApp iletişim kutusu girin](media/insert-powerapp.png)

Alternatif olarak bu adımları izleyin.

1. Sayfanın Eylem Panosunda, **Seçenekler** sekmesinde, **Kişiselleştir** grubunda, **Bu formu kişiselleştirin**'i seçin.

    ![Seçenekler sekmesinde Kişiselleştir grubu](media/options.png)

    Kişiselleştirme araç çubuğu görüntülenir.

2. Araç çubuğunda **Ekle \> PowerApp**'i seçin.

    ![Kişiselleştirme araç çubuğunu kullanarak bir Power Apps uygulaması ekleme](media/powerapp-bar.png)
