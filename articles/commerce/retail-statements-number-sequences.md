---
title: Perakende beyannamaleri için numara serilerini ayarla
description: Bu konuda, Microsoft Dynamics 365 Commerce'deki perakende beyannameleri için gerekli numara serilerinin nasıl konfigüre edildiği açıklanmıştır.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: db47ca4ee8bac0d55b9a9c732183d2734bce660f
ms.sourcegitcommit: 9e1129d30fc4491b82942a3243e6d580f3af0a29
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/27/2022
ms.locfileid: "8649220"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Perakende beyannamaleri için numara serilerini ayarla

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'deki perakende beyannameleri için gerekli numara serilerinin nasıl konfigüre edildiği açıklanmıştır.

Dynamics 365 Commerce'te iki tür perakende beyannameleri kullanılır: 

- **Hareketsel beyannameler**, yüksek frekansta oluşturulup nakledilmeleri amaçlanmıştır. Bunlar, mağazadaki mali olmayan tüm hareketleri Dynamics 365 Commerce genel merkezine nakletmek üzere kullanılır. 
- **Mali beyannameler**, iş günü başına bir kez oluşturulup deftere nakledilme amaçlıdır. Bunlar yalnızca, p işi aracılığıyla Commerce genel merkeze yüklenmiş olan perakende mağazalarından gelen kapalı vardiyalardan içerirler.

## <a name="configure-a-number-sequence-for-statement-posting"></a>Beyanname deftere nakli için numara serisi yapılandırma

Bir perakende mağaza kurulumunu tamamladıktan sonra, Commerce genel merkezde, ekstre oluşturma işlemi sırasında ekstrelerle kullanılacak benzersiz bir numara serisi konfigüre etmelisiniz.

Commerce genel merkezde ekstre deftere nakli için numara serisi yapılandırmak üzere aşağıdaki adımları izleyin.

1. **Kuruluş yönetim \> Numara serileri \> Numara serileri**'ne tıklayın.
1. Yeni bir kayıt oluşturmak için **Yeni \> Numara serisi**'ni seçin.
1. **Kimlik** hızlı sekmesinin **Numara serisi kodu** alanında bir numara serisi kodu girin.
1. **Numara serisi adı** alanına bir ad girin.
1. **Kapsam parametreleri** hızlı sekmesindeki **Kapsam** alanında, **Çalışan birim** seçeneğini belirleyin.
1. **İşletme birimi** alanında, numara serisinin kullanılacağı mağazayı seçin.
1. **Segmentler** hızlı sekmesinde, segmentleri tanımlayın.
1. **Referanslar** hızlı sekmesinde, **Alan** alanını **Perakende mağaza** olarak ayarlayın.
1. **Referans** alanını **Ekstre numarası** olarak ayarlayın ve **Tamam**'ı seçin.

    ![Numara serileri sayfasındaki tanımlama, kapsam parametreleri, segmentler ve başvurular hızlı sekmesi.](media/retail-statements-num-seq-setup-01.png)

1. **Genel** hızlı sekmesinde, **Numara tahsisatı** bölümünde, **En küçük** ve **En büyük** alanlarını, **Segmentler** hızlı sekmesinde tanımladığınız **Alfasayısal** kesimin uzunluğuyla eşleşecek şekilde güncelleştirin.
1. **Performans** hızlı sekmesinde, **Ön tahsis** seçeneğini **Evet** olarak, **Numara miktarı** alanını da **25** olarak ayarlamanız önerilir.

    ![Numara serileri sayfasında genel ve performans hızlı sekmeleri.](media/retail-statements-num-seq-setup-02.png)

1. Eylem bölmesinde, değişikliklerini kaydedip sayfayı kapatmak için **Kaydet**'i seçin.
