---
title: PowerApps uygulamalarını Dynamics 365 - Core HR içine katıştırma
description: Bu konu, PowerApps menü öğesinin Sistem yönetim modülünden kaybolduğu sorunu ortadan kaldırmayı açıklamaktadır.
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
ms.openlocfilehash: 4fbc24c5ceb73389b84b125eb942ac31757928aa
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008442"
---
# <a name="embed-powerapps-apps-in-core-hr"></a>PowerApps uygulamalarını Core HR içine katıştırma

[!include [banner](includes/banner.md)]

**Çıkış**

**PowerApps** menü öğesi, **Sistem yönetimi** modülünden kayboldu.

**Nedeni**

Kullanıcı arabirimi (UI) tasarımı değiştirildi ve Microsoft PowerApps, şimdi standart kişiselleştirme modeline dahildir.

**Çözünürlük**

PowerApps uygulamalarının katıştırılma şekli değiştirildi. Artık PowerApps uygulamaları kişiselleştirme modeli aracılığıyla eklenir. PowerApps uygulamalarını Microsoft Dynamics 365 Talent içindeki neredeyse her sayfaya ekleyebilirsiniz.

Talent içerisinde PowerApps uygulamalarının nasıl katıştırılacağı hakkında bilgi için bkz: [PowerApps uygulamalarını katıştırma](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Değişimden önce uygulamalarını katıştırmış olan her PowerApps kullanıcısının yeni modele yükseltilmiş olması gerekir.

**PowerApps** düğmesi, Talent içindeki neredeyse her sayfanın sağ üst kösesindedir. Bir PowerApps uygulaması eklemek için bu düğmeyi kullanın.

Aşağıda bir örnek verilmiştir.

1. **Personel yönetimi \> Bağlantılar \> Çalışanlar \> Personel**.
2. **PowerApps** düğmesini seçin ve sonra **Bir PowerApp ekle**'yi seçin.

    ![PowerApps düğmesi](media/png.png)

3. **Bir PowerApp ekleyin** iletişim kutusundaki alanları tamamlayın.

    ![Bir PowerApp iletişim kutusu girin](media/insert-powerapp.png)

Alternatif olarak bu adımları izleyin.

1. Sayfanın Eylem Panosunda, **Seçenekler** sekmesinde, **Kişiselleştir** grubunda, **Bu formu kişiselleştirin**'i seçin.

    ![Seçenekler sekmesinde Kişiselleştir grubu](media/options.png)

    Kişiselleştirme araç çubuğu görüntülenir.

2. Araç çubuğunda **Ekle \> PowerApp**'i seçin.

    ![Kişiselleştirme araç çubuğunu kullanarak bir PowerApps uygulaması ekleme](media/powerapp-bar.png)
