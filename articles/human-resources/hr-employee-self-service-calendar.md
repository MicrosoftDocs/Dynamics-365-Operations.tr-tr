---
title: Takım takvimi oluşturma
description: Dynamics 365 Human Resources'De ekip takvimleri görüntüle ve oluştur.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0679a69b4d607f9d466474026d5dd0ceef0dad6f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692212"
---
# <a name="view-team-and-company-calendars"></a>Takım ve şirket takvimlerini görüntüleme

>[!Important]
>Bu konuda belirtilen işlevler şu anda bağımsız Dynamics 365 Human Resources uygulamasını kullanan müşteriler için kullanıma sunulmaktadır. İşlevlerin bazıları veya tümü, Finance 10.0.26 sürümünden sonra Finance altyapısında ileride yayınlanacak bir sürümünün parçası olarak kullanılabilir.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources'ta ekip ve şirket takvimlerini görüntüleyebilirsiniz. Takım takvimleri yalnızca, satır hiyerarşisinde tanımlandığı şekilde, doğrudan rapor görüntüler.

## <a name="view-your-team-calendar-as-an-employee"></a>Personel olarak takım takviminizi görüntüleme

- **Çalışan self servisi** çalışma alanında, **Özet** altında **Takım devamsızlık takvimi**'ni seçin.

## <a name="view-your-team-calendar-as-a-manager"></a>Yönetici olarak takım takviminizi görüntüleme

1. **Personel self servisi** çalışma alanını **Ekibim**'i seçin.

2. **İzin ve devamsızlık**'ı seçin ve sonra **Yönetici devamsızlığını görüntüle**'yi seçin.

Yöneticiler takım takvimine **Takımımdaki bekleyen izin istekleri**, **Onaylanan izin** ve **İzin istekleri** alanından da erişebilirler. 

## <a name="view-your-absence-manager-calendar-as-the-absence-manager"></a>Devamsızlık yöneticisi takviminizi devamsızlık yöneticisi olarak görüntüleme

> [!NOTE]
> Devamsızlık yöneticisi takvimini görüntülemek için Özellik yönetiminde önce **(Önizleme) İzin özelliğini yönetecek devamsızlık yöneticisi** özelliğini açmanız gerekir. Önizleme özelliklerini açma hakkında daha fazla bilgi için bkz. [Özellikleri yönetme](hr-admin-manage-features.md).

Devamsızlık yöneticisi rolündeki kullanıcılar izin taleplerini takvimlerinde görüntüleyebilir. İzin takvimine erişmek için aşağıdaki adımları izleyin.

1. **Personel self servisi** çalışma alanında, **İzin yönetimi**'ni ve ardından **Devamsızlık yöneticisi takvimi**'ni seçin.

2. **Tarih** alanına istediğiniz tarihleri girin.

3. Görünüm seçeneklerini gerektiği gibi güncelleştirin.

Devamsızlık yöneticisi takvimi, İzin hiyerarşisinde devamsızlık yöneticisine rapor veren çalışanların tüm kayıtlarını gösterir.

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

**İzin ve devamsızlık parametreleri** sayfasındaki takvim yapılandırması kullanılabilir görünüm seçeneklerini belirler.

Ayrıca, yöneticiye veya departmana göre takvimlere filtre uygulayabilirsiniz. Birincil pozisyon ataması, bu filtreler ayarlandığında görüntülenen çalışanları belirler. 

> [!IMPORTANT]
> Özellik yönetiminde **Şirket geneli görünümü** özelliğini açabilirsiniz. Daha sonra, tüzel kişilik filtresini takvimlerde göstermek için **İnsan kaynakları paylaşılan parametreleri** sayfasında özelliği etkinleştirmeniz gerekir. Daha fazla bilgi için bkz. [İzin ve devamsızlık parametreleri yapılandırma](hr-leave-and-absence-parameters.md).
> 
> Geçerli varlığa göre takvime filtre uygulayabilirsiniz. Tüzel kişiliğe bakılmaksızın tüm çalışanları görüntülemek için filtre alanını temizleyin ve **Giriş**'i seçin. 

Takvim ayarları hakkında bilgi için bkz. [Takvim parametrelerini yapılandırma](hr-leave-and-absence-parameters.md?configure-calendar-parameters).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
