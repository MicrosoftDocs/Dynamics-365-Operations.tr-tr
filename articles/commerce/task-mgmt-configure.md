---
title: Görev yönetimini yapılandırma
description: Bu konuda, Microsoft Dynamics 365 Commerce'te görev yönetimi özelliklerinin nasıl yapılandırılacağı açıklanmaktadır.
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 80cbb7d22267aa6a0ae0568d0063fb95556958a5
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036867"
---
# <a name="configure-task-management"></a>Görev yönetimini yapılandırma

[!include [banner](includes/banner.md)]

Bu konuda, Microsoft Dynamics 365 Commerce'te görev yönetimi özelliklerinin nasıl yapılandırılacağı açıklanmaktadır.

## <a name="overview"></a>Genel Bakış

Yöneticiler ve çalışanlar ticari olarak görev yönetimi özelliklerini kullanabilmeniz için, görev yönetimi Dynamics 365 Commerce'in konfigüre edilmelidir. Yapılandırma adımları, yöneticilere ve çalışanlara izinler verilmesinde, bir satış noktasına (POS) sahip müşterilere dağıtım, POS bildirimleri kurma ve bir POS uygulamasının giriş sayfasında **görevler** döşemesini konfigüre eder.

## <a name="configure-permissions-for-store-managers"></a>Mağaza yöneticileri izinlerini konfigüre et

Belirli bir depodaki her çalışan, o mağazaya atanan tüm görevleri görüntüleyebilir. Kendilerine atanan görevlerin durumunu da güncelleştirebilirler. Ancak, depolama yöneticileri gibi kişiler, mağazaya atanan görevleri yönetmek ve tek amaçlı görevler oluşturmak için görev yönetimi izinleri bulunmalıdır.

Mağaza yöneticilerinin görev yönetimi izinlerini konfigüre etmek için aşağıdaki adımları izleyin.

1. **Perakende ve ticaret \> Çalışanlar \> Tüm çalışanlara** gidin.
1. Belirli bir izin grubu (örneğin, **yönetici**) seçin ve **Düzenle** seçin.
1. **İzinler** hızlı sekmesinde, **görev yönetimine izin ver** seçeneğini **Evet** olarak ayarlayın.
1. **Bildirimler** hızlı sekmesinde, **görev yönetimi** işlemini ekleyin ve **görüntüleme sırası** alanına bir değer girin. Örneğin, **sipariş karşılama** operasyonunu zaten **1** olan bir **görüntüleme emri** değerine sahip ise **2** değerini girin.
    
> [!NOTE]
> Bir yönetici olmayan kişinin POS'ta görev yönetimi izinleri olması gerekiyorsa, kişiye izin verebilirsiniz. Alternatif olarak, yönetici olmayanlar için yeni bir izin grubu oluşturabilir ve **görev yönetimine izin ver** seçeneğini **Evet** olarak ayarlayabilirsiniz.

Aşağıdaki çizim, mağaza yöneticilerinin görev yönetimi izinlerini konfigüre etmesini gösterir.

![Mağaza yöneticilerinin görev yönetimi izinlerini konfigüre etmesi](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>Çalışanlar için izinleri konfigüre et

Çalışanların görev listeleri oluşturmak, atama ölçütlerini yönetmek ve herhangi bir görev listesinin tekrarlarını konfigüre etmek için izinleri olmalıdır. Bu izinleri konfigüre etmek için, çalışanları **perakende Görev Yöneticisi** rolüne atarsınız.

Bir çalışan için izinleri yapılandırmak üzere bu adımları izleyin.

1. **Perakende ve Ticaret \> Personel \> Kullanıcılar**'a gidin.
1. Bir çalışan seçin.
1. **Kullanıcının rolleri** hızlı sekmesinde, **Rol ata**'ya tıklayın.
1. **Kullanıcıya rol ata** iletişim kutusunda, **perakende görev Yöneticisi** rolünü seçin ve **Tamam**'ı seçin.

## <a name="distribute-permissions-to-pos-clients"></a>POS istemcilerine ilişkin izinleri dağıt

Çalışanların POS istemcilerini kullanabilmesi için, izinlerin o istemcilerle dağıtılması ve eşitlenmelerini sağlamak gerekir.

POS istemcilerine izin dağıtmak için, aşağıdaki adımları izleyin.

1. **Retail and Commerce \> Retail and Commerce IT \> Dağıtım planı**'na gidin.
1. **1060** (**personel**) dağıtım zamanlamasını seçin ve **şimdi Çalıştır**'ı seçin.
1. **1070** (**Kanal yapılandırması**) dağıtım zamanlamasını seçin ve **şimdi Çalıştır**'ı seçin.

## <a name="configure-pos-notifications-for-tasks"></a>Görevler için POS bildirimlerini konfigüre et

Bu bildirim POS uygulamasında kullanılabilir olacak şekilde görev yönetimi konfigüre edilmelidir.

Görevler için POS bildirimleri yapılandırmak üzere bu adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS \> Operasyonlar** öğelerini seçin.
1. **1400** (**Görev yönetimi**) işlemini bulun ve bunun için **bildirimleri etkinleştir** onay kutusunu seçin.

Aşağıdaki şekil, **POS işlemleri** sayfasındaki **görev yönetimi** işlemini göstermektedir.

![POS işlemleri sayfasında görev yönetimi işlemi](media/HQ-POS-Tasks-Notifications.png)

POS bildirimlerinin nasıl yapılandırılacağı hakkında daha fazla bilgi için bkz. [satış noktasında (POS) sipariş bildirimleri göster](notifications-pos.md).

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>POS uygulaması giriş sayfasında görevler kutucuğunu konfigüre edin

Bir POS uygulamasının giriş sayfasında **Görevler** döşemesini konfigüre etmeden önce, bir POS ekran düzenine nasıl yapılandırılacağı ve yeni düğmeler ekleneceği hakkında bilgi için [satış noktası (POS) ile ilgili ekran düzenlerine](pos-screen-layouts.md) bakın.

POS uygulaması giriş sayfasında **görevler** kutucuğunu konfigüre etmek için aşağıdaki adımları izleyin.

1. **Retail ve Commerce \> Kanal kurulumu \> POS kurulumu \> POS \> Ekran düzenleri** öğelerini seçin.
1. Bir ekran düzeni seçin, bir düzen boyutu seçin ve bir düğme grubu seçin.
1. **Düğme grupları** hızlı sekmesinde, seçili düğme grubunu düzenlemek için **Tasarımcı**'yı seçin.
1. Giriş sayfasının uygun bölümüne **görevler** kutucuğu ekleyin.

Aşağıdaki çizimde POS giriş sayfasındaki **Görevler** kutucuğunun bir örneği gösterilmektedir.

![Bir POS giriş sayfasındaki görevler bölmesi](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>Ek kaynaklar

[Görev yönetimine genel bakış](task-mgmt-overview.md)

[Görev listeleri oluşturma ve görev ekleme](task-mgmt-create-lists.md)

[Mağazalara veya personele görev listeleri atama](task-mgmt-assign-lists.md)

[POS'ta görev yönetimi](task-mgmt-POS.md)
