---
title: Takım takvimi oluşturma
description: Dynamics 365 Human Resources'De ekip takvimleri görüntüle ve oluştur.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cedff4031c6455b446af9c56a770a00f3b2efc80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052109"
---
# <a name="view-team-and-company-calendars"></a>Ekip ve şirket takvimlerini görüntüleme

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources'ta ekip ve şirket takvimlerini görüntüleyebilirsiniz. Takım takvimleri yalnızca, satır hiyerarşisinde tanımlandığı şekilde, doğrudan rapor görüntüler.

## <a name="view-your-team-calendar-as-an-employee"></a>Personel olarak takım takviminizi görüntüleme

1. **Çalışan self servisi** çalışma alanında, **Özet** altında **Takım devamsızlık takvimi**'ni seçin.

## <a name="view-your-team-calendar-as-a-manager"></a>Yönetici olarak takım takviminizi görüntüleme

1. **Personel self servisi** çalışma alanını **Ekibim**'i seçin.

2. **İzin ve devamsızlık**'ı seçin ve sonra **Yönetici devamsızlığını görüntüle**'yi seçin.

Yöneticiler takım takvimine **Takımımdaki bekleyen izin istekleri**, **Onaylanan izin** ve **İzin istekleri** alanından da erişebilirler. 

## <a name="view-a-company-calendar"></a>Şirket takvimini görüntüle

İnsan kaynakları rollerine sahip kişiler şirket takvimlerini görüntüleyebilir. Şirket takvimleri tüm çalışanları görüntüler. Varsayılan olarak, takvim bugünün tarihini artı 28 gün görüntüler, ancak tarih aralığını değiştirebilirsiniz. Takvimi **ada**, **personel numarasına** ve **izin türüne** göre de süzebilirsiniz.

1. **İzin ve devamsızlık** çalışma alanında, **bağlantılar**'ı seçin.

2. **İzin ve devamsızlık takvimi** seçin.

İnsan kaynakları rolleri şirket takvimine **İzin ve devamsızlık istekleri**, **Onaylanan izin** ve **İzin istekleri**'nden de erişebilir. 

Takvimler artık ek filtreler ve seçenekler içerir. Tüm takvimler için görünüm seçenekleri şunlardan oluşur:

- Onaylanan talepler
- Bekleyen istekler
- İzin talepleri olan çalışanlar
- İzin talepleri olmayan çalışanlar
- Çalışan doğum günleri
- İzin süresi istekleri 
- Devamsızlık izni istekleri

İzin ve devamsızlık parametrelerinde takvim yapılandırması kullanılabilir görünüm seçeneklerini belirler.

Ayrıca, yöneticiye veya departmana göre takvimlere filtre uygulayabilirsiniz. Birincil pozisyon ataması, bu filtreler ayarlandığında görüntülenen çalışanları belirler. 

>[!IMPORTANT]
>Şirketler arasında ayrılma ve devamsızlıkların görüntülenmesi Şu anda önizleme modunda. Bunu **korumalı alan** ortamınızda etkinleştirmeniz gerekir . Önizleme özelliklerini etkinleştirme hakkında daha fazla bilgi edinmek için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).<br><br>
>Daha sonra, **insan kaynakları paylaşılan parametrelerinin**, takvimlerdeki yasal varlık filtresini görüntülemesi için özelliği etkinleştirmelisiniz. Daha fazla bilgi için bkz. [İzin ve devamsızlık parametreleri yapılandırma](hr-leave-and-absence-parameters.md).<br><br>
>Geçerli varlığa göre takvime filtre uygulayabilirsiniz. Yasal tüzel kişiliye bakılmaksızın tüm çalışanları görmek istiyorsanız, filtre kutusunu temizleyin ve ENTER 'i seçin. 

Takvim ayarları hakkında bilgi için bkz. [Takvim parametrelerini yapılandırma](hr-leave-and-absence-parameters.md?configure-calendar-parameters).



[!INCLUDE[footer-include](../includes/footer-banner.md)]